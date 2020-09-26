---
layout: handbook-page-toc
title: "SecuriTy Operational Risk Management (STORM) Methodology"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# Security Operational Risk Management Methodology

## Purpose

This handbook page details the specific SecuriTy Operational Risk Management (“STORM”) Methodology that is used at GitLab in order to assess Risk Appetite, Risk Tolerance, as well as scoring risks based on their likelihood, impact as well as explicit inherent vs residual risk levels.

## Annual STORM Assessment Schedule

The annual STORM assessment will be conducted in accordance with the following schedule each fiscal year:

|Timing|Activities|
|-----|-----|
|March|Risk Appetite Survey is sent out to Senior Leadership to establish GitLab's Annual Risk Appetite|
|April - May|Annual STORM interviews are kicked off for risk identification. Interviews with management across the organization will be conducted. Once these interviews are completed, risks will be reviewed with GitLab's VP of Security and Director of Security Compliance & Risk for approval/agreement of risks identified. Once these approvals are obtained, risk ownership meetings will be held with identified risk owners.|
|May|The [annual STORM reports](/handbook/engineering/security/security-assurance/security-compliance/risk-management.html#annual-storm-reports) are prepared, reviewed, and approved|
|June - July|Security Compliance works with Risk Owners on the completion of Risk Treatment Plans. Note that the risk treatment does not need to be completed by the end of July, but the actual risk treatment plan needs to be finalized by the end of July|
|August and onward|Security Compliance will track and follow-up with Risk Owners on the status of risk treatment and update GitLab's risk register accordingly for remediated/accepted risks.|


## Risk Appetite and Tolerance Scoring

GitLab’s risk appetite is determined based on the total average of responses the following risk statements:
* GitLab should seek solutions to transfer risk (risk taking vs risk transfer)
* GitLab should proactively seek to offset the potential impact of risks (organizational objectives)
* GitLab should prepare a comprehensive risk strategy (risk response approach)
* GitLab should work to address all foreseeable risks (risk response drivers)

Each risk statement is ranked based on a 1 to 4 scale of importance level where 1 denotes that the statement is less important and 4 denotes that the statement is very important. Interested in seeing our FY21 Survey? A PDF is [available here](https://drive.google.com/file/d/1UFguqi2M15ZlCuo3HGaIlUTAbDqbT5u0/view?usp=sharing). Based on the responses collected, **GitLab's Risk Appetite for FY21 is `Risk Neutral` based on the following risk appetite scale:**

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-9wq8{border-color:inherit;text-align:center;vertical-align:middle}
.tg .tg-674h{font-weight:bold;background-color:#380d75;color:#ffffff;border-color:inherit;text-align:center;vertical-align:middle}
.tg .tg-yeut{font-weight:bold;background-color:#656565;color:#ffffff;border-color:inherit;text-align:center;vertical-align:middle}
.tg .tg-747f{font-weight:bold;background-color:#6e49cb;color:#ffffff;border-color:inherit;text-align:center;vertical-align:middle}
</style>
<table class="tg">
  <tr>
    <th class="tg-674h">RISK APPETITE<br>APPROACH</th>
    <th class="tg-yeut">RISK SEEKING</th>
    <th class="tg-yeut">RISK TOLERANT</th>
    <th class="tg-yeut">RISK NEUTRAL</th>
    <th class="tg-yeut">RISK AVERSE</th>
  </tr>
  <tr>
    <td class="tg-747f">RISK TAKING vs<br>RISK TRANSFER</td>
    <td class="tg-9wq8">Aggressive risk <br>taking is justified</td>
    <td class="tg-9wq8">Seek opportunities to transfer risks <br>with pre-existing vendors as applicable<br>(e.g. don't bring in a new vendor to<br> transfer risks)</td>
    <td class="tg-9wq8">Take a balanced approach to <br>risk taking vs risk transferring</td>
    <td class="tg-9wq8">Exercise caution and accept as little <br>risk as possible by identifying risk <br>transfer solutions</td>
  </tr>
  <tr>
    <td class="tg-747f">ORGANIZATIONAL<br>OBJECTIVES</td>
    <td class="tg-9wq8">Willing to accept a large negative<br> impact to the organization to pursue <br>opportunities that align with objectives</td>
    <td class="tg-9wq8">Willing to accept some negative impact <br>(e.g. LOW risks) to pursue opportunities<br> that align with objectives</td>
    <td class="tg-9wq8">The potential for a negative impact <br>vs objectives are given equal <br>consideration when making a decision</td>
    <td class="tg-9wq8">The potential for a negative impact vs <br>objectives are given equal consideration <br>when making a decision</td>
  </tr>
  <tr>
    <td class="tg-747f">RISK RESPONSE<br>APPROACH</td>
    <td class="tg-9wq8">All risks are acceptable as long <br>as they do not impact our legal <br>and regulatory obligations</td>
    <td class="tg-9wq8">Determine risk treatment options to <br>help accept or reduce risk levels<br> through internal initiatives</td>
    <td class="tg-9wq8">No explicit preference towards <br>how risks should be approached</td>
    <td class="tg-9wq8">Risks that cannot be effectively <br>treated or transferred are avoided</td>
  </tr>
  <tr>
    <td class="tg-747f">RISK RESPONSE<br>DRIVERS</td>
    <td class="tg-9wq8">No response action required for risks</td>
    <td class="tg-9wq8">Respond to risks which make sense <br>when a case can be made for the <br>cost effectiveness of potential outcomes</td>
    <td class="tg-9wq8">Risk response actions take into <br>consideration cost effectiveness, <br>management priorities, and return <br>on investment</td>
    <td class="tg-9wq8">Risk response actions are always taken, <br>regardless of cost effectiveness, <br>management priorities, return on investment, <br>and overall organizational objectives</td>
  </tr>
</table>

_GitLab's Risk Appetite Matrix was formed through consideration of guidance set forth in NIST's [SP 800-39](https://csrc.nist.gov/publications/detail/sp/800-39/final) and [SP 800-30 Rev. 1](https://csrc.nist.gov/publications/detail/sp/800-30/rev-1/final)._

Scoring is performed by individuals operating in at least Senior Leadership capacity within GitLab and spans across multiple departments. Keeping to our value of iteration, the first STORM appetite survey will include the following departments:
* Engineering
* Finance
* Legal

As the STORM program matures, the scope of departments included in the assessment process will grow.

## Identifying Threat Sources and Events

The identification of threat sources and events in relation to operational risks includes multiple considerations. These threat sources and events have been identified based on their potential to have an impact on mission critical objectives in relation to GitLab's operations. Based on this, the following threat sources and events are included as part of the operational risk assessment process:

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-wa1i{font-weight:bold;text-align:center;vertical-align:middle}
.tg .tg-clye{background-color:#380d75;color:#ffffff;font-weight:bold;text-align:center;vertical-align:middle}
</style>
<table class="tg">
  <tr>
    <th class="tg-clye">Threat Source</th>
    <th class="tg-clye">Example Threat Events</th>
  </tr>
  <tr>
    <td class="tg-wa1i">Adversarial</td>
    <td class="tg-cly1">Fraud and theft, insider threat, malicious hacker, and malicious code</td>
  </tr>
  <tr>
    <td class="tg-wa1i">Non-Adversarial</td>
    <td class="tg-cly1">Errors and ommission, loss of physical and infrastructure support (e.g. a natural disaster), exposure of sensitive information, changes to systems used to support the business, changes to external environments supporting GitLab, changes to GitLab's business model, or even changes in leadership</td>
  </tr>
</table>

## Risk Factors and Risk Scoring

A scoring model is used to score each risk and is based on the Likelihood of the risk event occurring and the Impact to GitLab if the event occurred. Likelihood and Impact scores directly determine the overall inherent risk to GitLab.

### Determining Likelihood of initiation of a threat event

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-nc7u{background-color:#d9ead3;text-align:center;vertical-align:middle}
.tg .tg-clye{font-weight:bold;background-color:#380d75;color:#ffffff;text-align:center;vertical-align:middle}
.tg .tg-f6g8{background-color:#fce5cd;text-align:center;vertical-align:middle}
.tg .tg-nrix{text-align:center;vertical-align:middle}
.tg .tg-28x2{background-color:#ffcccc;text-align:center;vertical-align:middle}
</style>
<table class="tg">
  <tr>
    <th class="tg-clye">Qualitative <br>Score</th>
    <th class="tg-clye">Risk Level</th>
    <th class="tg-clye">Scoring Guidelines</th>
  </tr>
  <tr>
    <td class="tg-nrix">5 to 6</td>
    <td class="tg-28x2">HIGH</td>
    <td class="tg-cly1">6 = Easily initiate a threat event; no expertise required<br>5 = Minimal difficulty to initiate a threat event</td>
  </tr>
  <tr>
    <td class="tg-nrix">3 to 4</td>
    <td class="tg-f6g8">MODERATE</td>
    <td class="tg-cly1">4 = Some expertise required to initiate a threat event<br>3 = Difficult to initiate a threat event, even with expertise</td>
  </tr>
  <tr>
    <td class="tg-nrix">1 to 2</td>
    <td class="tg-nc7u">LOW</td>
    <td class="tg-cly1">2 = Requires expertise to initiate a threat event<br>1 = Theoretically impossible to initiate</td>
  </tr>
</table>

### Determining the impact of a threat event

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-lboi{border-color:inherit;text-align:left;vertical-align:middle}
.tg .tg-6c9p{background-color:#d9ead3;border-color:inherit;text-align:center;vertical-align:middle}
.tg .tg-22ff{font-weight:bold;background-color:#6e49cb;color:#ffffff;border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-1mkn{font-weight:bold;background-color:#380d75;color:#ffffff;border-color:#000000;text-align:center;vertical-align:middle}
.tg .tg-747f{font-weight:bold;background-color:#6e49cb;color:#ffffff;border-color:inherit;text-align:center;vertical-align:middle}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-oej3{background-color:#fce5cd;border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-sy71{background-color:#ffcccc;border-color:inherit;text-align:center;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-1mkn" rowspan="2">IMPACT<br>SCORE</th>
    <th class="tg-1mkn" colspan="6">IMPACT AREAS</th>
  </tr>
  <tr>
    <td class="tg-747f">Organizational Output <br>(time, quality, resources)</td>
    <td class="tg-747f">Brand<br>Reputation</td>
    <td class="tg-22ff">Business<br>Continuity</td>
    <td class="tg-22ff">Customers &amp;<br>Stakeholders</td>
    <td class="tg-22ff">Legal &amp;<br>Regulatory</td>
    <td class="tg-22ff">Financial</td>
  </tr>
  <tr>
    <td class="tg-6c9p">VERY LOW (1)</td>
    <td class="tg-lboi">Organizational output is <br>impacted by less than 20%</td>
    <td class="tg-lboi">Limited to reputational damage <br>with no more than one customer <br>within a fiscal period</td>
    <td class="tg-0pky">Outages of non-critical systems <br>that impact internal GitLabbers</td>
    <td class="tg-0pky">Impact is limited to one <br>customer and/or stakeholder</td>
    <td class="tg-0pky">Breach of company policy <br>occurring once in a fiscal <br>period</td>
    <td class="tg-0pky">Loss up to $999</td>
  </tr>
  <tr>
    <td class="tg-6c9p">LOW (2)</td>
    <td class="tg-lboi">Organizational output is <br>impacted by 30% - 40%</td>
    <td class="tg-lboi">Confined to a limited number of <br>parties (e.g. specific customers) <br>and not publicized</td>
    <td class="tg-0pky">Outages which result in the inability <br>of GitLab to continue sales and finance <br>operations longer than 72+ hours</td>
    <td class="tg-0pky">Impact is limited to 2-3 <br>customers and/or stakeholders</td>
    <td class="tg-0pky">Breach of company policy <br>twice within a fiscal period</td>
    <td class="tg-0pky">Loss between $1,000 <br>and $9,999</td>
  </tr>
  <tr>
    <td class="tg-oej3">MODERATE (3)</td>
    <td class="tg-0pky">Organizational output is <br>impacted by 40% - 50%</td>
    <td class="tg-0pky">Public domain publicity but limited <br>to industry channels and not the <br>broader public</td>
    <td class="tg-0pky">Outages that impact GitLab's <br>ability to do business across 3+ <br>departments</td>
    <td class="tg-0pky">Impact is limited to 4-5 <br>customers and/or stakeholders</td>
    <td class="tg-0pky">Breach of a regulatory and/or <br>contractual obligation</td>
    <td class="tg-0pky">Loss between $10,000 <br>and $499,999</td>
  </tr>
  <tr>
    <td class="tg-sy71">HIGH (4)</td>
    <td class="tg-0pky">Organizational output is <br>impacted by 50% - 75%</td>
    <td class="tg-0pky">Wide-spread publicity but limited <br>parties are impacted</td>
    <td class="tg-0pky">Outages that result in the loss of <br>availability of GitLab for customers <br>for less than 4 hours</td>
    <td class="tg-0pky">Major impact to many <br>customers and/or stakeholders</td>
    <td class="tg-0pky">Regulatory censure and/or action <br>taken against GitLab</td>
    <td class="tg-0pky">Loss between $500,000 <br>and $999,999</td>
  </tr>
  <tr>
    <td class="tg-sy71">VERY HIGH (5)</td>
    <td class="tg-0pky">Organizational output is <br>impacted by 75% or more</td>
    <td class="tg-0pky">Widely publicized</td>
    <td class="tg-0pky">Outages that result in the loss of <br>availability of GitLab for customers <br>for 4+ hours</td>
    <td class="tg-0pky">Major impact to all <br>customers and/or stakeholders</td>
    <td class="tg-0pky">Public regulatory fines and/or major <br>litigation against GitLab</td>
    <td class="tg-0pky">Loss of $1,000,000+</td>
  </tr>
</table>

To arrive at a final impact score, the impact score of all impact categories is averaged.

### Determining Inherent Risk vs Residual Risk

Inherent Risk is determined by the following formula:
`Inherent Risk = Likelihood x Impact`

Residual risk is determined by the following formula:
`Residual Risk = Inherent Risk - Control Effectiveness Rating as a percentage`

This calculation considers the control effectiveness rating as a percentage. As a conservative measure, the control effectiveness percentage can be derived as the average of the percentage range within each respective rating (e.g. a rating of 1 means a control is operating between 80% - 100%, so to calculate the control effectiveness rating as a percentage, the average of this range is calculated and in this case, a percentage of 90% will be used to calculate residual risk).

Based on the calculations performed in the formulas above, the risk level can be determined based on the following table:

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-nc7u{background-color:#d9ead3;text-align:center;vertical-align:middle}
.tg .tg-clye{font-weight:bold;background-color:#380d75;color:#ffffff;text-align:center;vertical-align:middle}
.tg .tg-kego{background-color:#fce5cd;text-align:center;vertical-align:top}
.tg .tg-f6g8{background-color:#fce5cd;text-align:center;vertical-align:middle}
.tg .tg-dxvi{font-weight:bold;background-color:#6e49cb;color:#ffffff;text-align:center;vertical-align:middle}
.tg .tg-28x2{background-color:#ffcccc;text-align:center;vertical-align:middle}
.tg .tg-tcv6{font-weight:bold;background-color:#6e49cb;color:#ffffff;text-align:center;vertical-align:top}
.tg .tg-phmi{background-color:#ffcccc;text-align:center;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-clye" rowspan="2">LIKELIHOOD<br>SCORE</th>
    <th class="tg-clye" colspan="5">IMPACT SCORE</th>
  </tr>
  <tr>
    <td class="tg-dxvi">1</td>
    <td class="tg-dxvi">2</td>
    <td class="tg-dxvi">3</td>
    <td class="tg-dxvi">4</td>
    <td class="tg-dxvi">5</td>
  </tr>
  <tr>
    <td class="tg-dxvi">1</td>
    <td class="tg-nc7u">LOW (1)</td>
    <td class="tg-nc7u">LOW (2)</td>
    <td class="tg-nc7u">LOW (3)</td>
    <td class="tg-nc7u">LOW (4)</td>
    <td class="tg-f6g8">MODERATE (5)</td>
  </tr>
  <tr>
    <td class="tg-dxvi">2</td>
    <td class="tg-nc7u">LOW (2)</td>
    <td class="tg-nc7u">LOW (4)</td>
    <td class="tg-f6g8">MODERATE (6)</td>
    <td class="tg-f6g8">MODERATE (8)</td>
    <td class="tg-f6g8">MODERATE (10)</td>
  </tr>
  <tr>
    <td class="tg-dxvi">3</td>
    <td class="tg-nc7u">LOW (3)</td>
    <td class="tg-f6g8">MODERATE (6)</td>
    <td class="tg-f6g8">MODERATE (9)</td>
    <td class="tg-f6g8">MODERATE (12)</td>
    <td class="tg-f6g8">MODERATE (15)</td>
  </tr>
  <tr>
    <td class="tg-dxvi">4</td>
    <td class="tg-nc7u">LOW (4)</td>
    <td class="tg-f6g8">MODERATE (8)</td>
    <td class="tg-f6g8">MODERATE (12)</td>
    <td class="tg-f6g8">MODERATE (16)</td>
    <td class="tg-28x2">HIGH (20)</td>
  </tr>
  <tr>
    <td class="tg-dxvi">5</td>
    <td class="tg-f6g8">MODERATE (5)</td>
    <td class="tg-f6g8">MODERATE (10)</td>
    <td class="tg-f6g8">MODERATE (15)</td>
    <td class="tg-28x2">HIGH (20)</td>
    <td class="tg-28x2">HIGH (25)</td>
  </tr>
  <tr>
    <td class="tg-tcv6">6</td>
    <td class="tg-kego">MODERATE (6)</td>
    <td class="tg-kego">MODERATE (12)</td>
    <td class="tg-phmi">HIGH (18)</td>
    <td class="tg-phmi">HIGH (24)</td>
    <td class="tg-phmi">HIGH (30)</td>
  </tr>
</table>

### Determining Control Effectiveness Rating (CER)

The effectiveness rating of a control is determined using a percentage that is based on the control's operating status in the environment. Additionally, when assessing the control effectiveness rating, there may be scenarios where a low effectiveness rating will lead to a control being escalated from a Tier 3 observation into a Tier 2 risk.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-j45n{font-weight:bold;background-color:#ffcccc;text-align:center;vertical-align:middle}
.tg .tg-clye{font-weight:bold;background-color:#380d75;color:#ffffff;text-align:center;vertical-align:middle}
.tg .tg-vcol{font-weight:bold;background-color:#d9ead3;text-align:center;vertical-align:middle}
.tg .tg-nrix{text-align:center;vertical-align:middle}
.tg .tg-3ig7{font-weight:bold;background-color:#fce5cd;text-align:center;vertical-align:middle}
</style>
<table class="tg">
  <tr>
    <th class="tg-clye">CONTROL<br>EFFECTIVENESS<br>RATING</th>
    <th class="tg-clye">RATING DEFINITION</th>
    <th class="tg-clye">CONSIDER TIER 2<br>UPGRADE (Y/N)?</th>
  </tr>
  <tr>
    <td class="tg-vcol">1</td>
    <td class="tg-cly1">The control has no outstanding HIGH, MODERATE, or LOW risk observations open.</td>
    <td class="tg-nrix">N</td>
  </tr>
  <tr>
    <td class="tg-vcol">2</td>
    <td class="tg-cly1">There are no outstanding HIGH or MODERATE risk observations associated with the control, but there are some LOW risk observations that are open</td>
    <td class="tg-nrix">N</td>
  </tr>
  <tr>
    <td class="tg-3ig7">3</td>
    <td class="tg-cly1">There are no outstanding HIGH risk observations associated with the control, but there are a combination of open MODERATE and LOW risk observations.</td>
    <td class="tg-nrix">N</td>
  </tr>
  <tr>
    <td class="tg-3ig7">4</td>
    <td class="tg-cly1">There are no outstanding HIGH or LOW risk observations associated with the control, but there are open MODERATE risk observations.</td>
    <td class="tg-nrix">N</td>
  </tr>
  <tr>
    <td class="tg-j45n">5</td>
    <td class="tg-cly1">There are outstanding HIGH risk observations associated with the control.</td>
    <td class="tg-nrix">Y</td>
  </tr>
</table>

#### A note on Opportunites for Improvement (OFIs)

OFIs will not impact a CER as they are meant to be areas of improvement for a control whereas an observation which impacts a control's CER is specifically tied to a failure in operating effectiveness. OFIs should never impact the operating effectiveness conclusion of a control that is tested and are considered "nice to haves."

## Risk Treatment Options

Each risk identified as part of the annual STORM assessment is required to undergo a risk treatment determination. This is an activity that will be discussed with each individual risk owner for the risks that they own. The following risk treatment options are available:

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-wa1i{font-weight:bold;text-align:center;vertical-align:middle}
.tg .tg-clye{font-weight:bold;background-color:#380d75;color:#ffffff;text-align:center;vertical-align:middle}
</style>
<table class="tg">
  <tr>
    <th class="tg-clye">TREATMENT<br>OPTION</th>
    <th class="tg-clye">DEFINITION</th>
  </tr>
  <tr>
    <td class="tg-wa1i">Monitor (do nothing)</td>
    <td class="tg-cly1">The risk level falls within our risk tolerance levels and no additional actions will be pursued at this time</td>
  </tr>
  <tr>
    <td class="tg-wa1i">Remediate the Risk</td>
    <td class="tg-cly1">Complete a risk remediation plan to remediate the risk through: Sharing the risk (identify and implement solutions to share the risk with other parties), Reducing the likelihood of occurrence, and/or Reducing the level of impact to GitLab</td>
  </tr>
  <tr>
    <td class="tg-wa1i">Accept the Risk</td>
    <td class="tg-cly1">Accept the risk because the value gained by GitLab outweigh the costs associated with pursuing other treatment options</td>
  </tr>
</table>

Once a risk treatment option is agreed upon, the Risk Owner will complete a Risk Treatment Plan. Due to the sensitivity of the information about risks documented in risk treatment plans, these plans are documented via Google Docs and access is maintained by the Security Compliance Team. This risk treatment plan will ultimately be the source of truth for the status of risk treatment. The risk treatment plan document provides options for risk remediation or risk acceptance. Specific information about risk treatment options are documented below.

### Monitor (do nothing)

In the cases where a risk owner has concluded that a risk is low enough level, no additional action is required besides ensuring that the STORM Program DRI agrees with the treatment option.

### Remediate the Risk

When choosing to remediate the risk, a specific path must be seleted:
   * Remediate by reducing the likelihood that the risk could occur
   * Remediate by reducing the impact to GitLab if the risk occurs
   * Remediate by sharing or transferring the risk with a third party
   * Remediate by fully eliminating the risk from GitLab

As part of the documentation in the risk treatment plan, these specific risk remediation paths are called out. Once a path is selected, the risk owner is required to provide a specific, detailed plan that includes milestones and due dates for working towards risk remediation. Security Compliance will leverage these risk treatment plans to track the status of risk remediation.

### Accept the Risk

In the cases where a risk owner has opted to pursue a risk acceptance, the following approvals will be required based on risk rating that was assigned to the risk undergoing a risk acceptance:

|Risk Level|Approval Level Required|
|-----|-----|
|HIGH|Risk Owner, Risk Owner's Manager, Risk Owner's VP, Director of Security Compliance & Risk, VP of Security|
|MODERATE|Risk Owner, Risk Owner's Manager, Director of Security Compliance & Risk|
|LOW|Risk Owner, STORM Program DRI
