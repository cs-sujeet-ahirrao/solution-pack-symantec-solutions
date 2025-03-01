# Symantec Solutions Solution Pack

## Release Information

- Solution Pack Version: 1.0.1
- Minimum Compatible FortiSOAR™ Version: 7.2.0
- Authored By: Fortinet
- Certified: No

## Overview

### Introduction

*Symantec Solutions* is designed to provide a set of investigation playbooks to respond to phishing email reported by Symantec Email.Cloud.

Configure Symantec Email Security.Cloud Connectors and ingest email of type 'Phishing', and then triggers the response workflow.

Refer to Simulation Scenario - "Symantec Email Cloud" to experience the use case without any connector configuration.

### Usage

This Solution Pack ships with the following simulation scenarios. [Refer](https://github.com/fortinet-fortisoar/solution-pack-soc-simulator/blob/develop/docs/solution-pack-guide.md) to Simulate Scenario documentation to understand how to Simulate and Reset Scenario.

#### 1. Scenario - Symantec Email Cloud

The scenario generates a demo alert of Type 'Phishing'.

Goto generated alert and observe the following:

- Reported Email contains file information like malware name, filename, malware category, file hash etc.
- Reported Information (sender, email message) is presented for analyzing the case.

**Investigate Symantec EMail.Cloud Alert** : Launch "Investigate Symantec EMail.Cloud Alert" Playbook and observe various investigation activities such as

- Created Indicator for File MD5
- Created Indicator for URL
- Created Indicator for Email

**Investigate and Escalate Symantec Email.Cloud Phishing Alert** Launch "Investigate and Escalate Symantec Email.Cloud Phishing Alert" Playbook and observe various investigation activities such as

- Lookup for Malicious Indicator
- Escalate Alert to Incident
- Find similar Alerts
- Mark Incident as a Campaign

## Prerequisites

|**Solution Pack Name**|**Purpose**|**Doc Link**|
| :- | :- | :- |
|SOAR Framework 1.0.0|Require for Incident Response modules|[Click here](https://github.com/fortinet-fortisoar/solution-pack-soar-framework/blob/develop/README.md)|
|SOC Simulator 1.0.1|Require for Scenario Module and SOC Simulator connector| [Click here](https://github.com/fortinet-fortisoar/solution-pack-soc-simulator/blob/develop/README.md)|

## Contents

1. Record Set(s)
    - Scenario: Symantec Email Cloud
2. Connector(s)
    |**SN**|**Connector Name**|
    | :- | :- |
    |1|Symantec Email Security.cloud|

     **Warning:** After deployment, this Solution Pack installs or upgrades the stated list of connectors.
3. Playbook Collection(s)
    - 02 - Use Case - Symantec Solutions (3):

    |**SN**|**Playbook Name**|**Description**|
    | :- | :- | :- |
    |1|Investigate and Escalate Symantec Email.Cloud Phishing Alert|Investigate Phishing Alert, and Escalate to Incident if Malicious Indicators are found|
    |2|Investigate Symantec EMail.Cloud Alert|Investigate Symantec EMail.Cloud Alert|
    |3|Generate - Symantec Email.Cloud | Create single alert for Symantec Email.Cloud Phishing Alert|

     **Warning:** It is recommended to clone these Playbooks before any customizations to avoid loss of information while upgrading the Solution Pack.
