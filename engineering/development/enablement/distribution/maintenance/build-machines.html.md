---
layout: handbook-page-toc
title: "Distribution Team Infrastructure and Maintenance"
---

## On this page

{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Common links

- [Distribution Team Handbook](/handbook/engineering/development/enablement/distribution/)
- [Distribution Team Infrastructure and Maintenance](/handbook/engineering/development/enablement/distribution/maintenance/)

## Build Machines

GitLab CI runner manager is responsible for creating build machines for package
builds.  This node configuration is managed by
[cookbook-gitlab-runner](https://gitlab.com/gitlab-cookbooks/cookbook-wrapper-gitlab-runner).
Configuration values are stored in the vault named the same as the node,
[see example](https://ops.gitlab.net/gitlab-cookbooks/chef-repo/-/blob/a62742886ed1dec291d66df3508e37163431538d/roles/build-trigger-runner-manager-gitlab-org.json#L37).

Currently, the version of GitLab CI runner is locked. We aim to be close to the
current version of runner in order to get the fixes that we need without getting
into issues that could cause a failure. These failures could prevent the release
from going out so be careful with unnecessary changes on these nodes.

### Runner manager machines

Distribution team maintains 2 runner manager machines for running different
types of pipelines. Both these machines are in GCP project
`omnibus-build-runners`.

1. build-runners.gitlab.org:
1. build-trigger-runner-manager.gitlab.org

#### build-runners.gitlab.org

This runner manager manages the machines used for building and publishing
official GitLab CE and EE packages. It is locked to the [omnibus-gitlab](https://dev.gitlab.org/gitlab/omnibus-gitlab/)
and [gitlab-omnibus-builder](https://dev.gitlab.org/cookbooks/gitlab-omnibus-builder/) projects in dev.gitlab.org.

It spins up the following types of machines:

1. x86_64 machines for building packages. They are `n1-highcpu-32` machines with 60GB
   SSD disks, spawned inside GCP using `google` docker-machine driver.

1. Arm64 marchines for building packages. They are `m6g.2xlarge` machines with 50GB SSD
   disks, spawed inside AWS using `amazonec2` docker-machine driver.

1. `package-promotion` machines for uploading packages. Since they are only used
   to upload packages, they are scaled down to save costs. They are
   `n1-standard-2` machines, spawned inside GCP using `google` docker-machine
   driver.

1. ARM machines for building Raspberry Pi packages. They are `C1` machines
   spawned inside Scaleway using `scaleway` docker-machine driver.
   [See the specific documentation for ARM support information][arm].

#### build-trigger-runner-manager.gitlab.org

This runner manager manages the machines used for building packages as part of
triggered pipeline used by developers to test their changes.

It spins up the following types of machines:

1. x84_64 machines for building packages. They are `n1-highcpu-32` machines with 50GB
   SSD disks, spawned inside GCP using `google` docker-machine driver.

1. Arm64 machines for building arm64 builder images. They are `m6g.2xlarge` machines with 50GB SSD
   disks, spawed inside AWS using `amazonec2` docker-machine driver.

1. `qa-builder` machines for creating qa test images. They are `n1-standard-2` machines
   with 50GB disks, spawned inside GCP using `google` docker-machine driver.

1. ARM machines for building Raspberry Pi builder images. They are `C1` machines
   spawned inside Scaleway using `scaleway` docker-machine driver.
   [See the specific documentation for ARM support information][arm].

### Maintenance tasks

**Requirements:**

- Access to the node
- Access to merge into master on the [ops chef repo](https://ops.gitlab.net/gitlab-cookbooks/chef-repo)
- Some tasks need access to a Chef Vault admin. At minimum, contact the Engineering Manager,
  Distribution for help.

#### Changing version of GitLab CI runner

*To be performed by any team member:*

   1. Create a new merge request on the chef repo that updates the runner version

   1. Ensure the CI pass, and the MR is reviewed by another team member

   1. Merge the change into the chef repo

   1. Login to the node and run,

      ```sh
      sudo /root/runner_upgrade.sh
      ```

      to perform the upgrade. This will stop the chef-client service, stop the
      runner and cleanup the machines, run the chef-client to fetch the new
      version and finally, start gitlab runner again.

#### When builds are pending on dev.gitlab.org

The common reason for builds to be pending on dev.gitlab.org project is that the
number of failed machines is high. Failed machines prevent the runner manager
from starting up new machines and this can slow down or even block the release.
To resolve this, we need to clean those failed machines. The steps to do this
are:

  1. Login to the [build machine](#build-machines) node

  1. Enter the root session: `sudo su`. This is required because
     `docker-machine` command will list running machines for currently active
     user

  1. Run `docker-machine ls`. This will print out the list of machines that are
     either in `Running`, `Error` or have an empty state.

  1. To list only machines in `Error` state, you can use

      ```sh
      /root/machines_operations.sh list-failing
      ```

  1. To safely clean the machines with `Error` state, run

      ```sh
      /root/machines_operations.sh remove-failing
      ```

  1. If the machine has an empty state, you can always remove the machine
     manually. Running

      ```sh
      docker-machine ls | grep -v 'Running' | awk '{print $1}' | xargs docker-machine rm --force
      ```

      will remove all machines that do not have `Running` state.

[arm]: /handbook/engineering/development/enablement/distribution/maintenance/arm.html
