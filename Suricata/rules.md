### Suricata rules: enable these rule feeds using this syntax:

```suricata-update -add-source oisf/trafficid
suricata-update -add-source ptresearch/attackdetection
suricata-update -add-source sslbl/ssl-fp-blacklist
suricata-update -add-source et/open
suricata-update -add-source tgreen/hunting
suricata-update -add-source  etnetera/aggressive

Name: oisf/trafficid
  Vendor: OISF
  Summary: Suricata Traffic ID ruleset
  License: MIT
Name: ptresearch/attackdetection
  Vendor: Positive Technologies
  Summary: Positive Technologies Attack Detection Team ruleset
  License: Custom
Name: sslbl/ssl-fp-blacklist
  Vendor: Abuse.ch
  Summary: Abuse.ch SSL Blacklist
  License: Non-Commercial
Name: et/open
  Vendor: Proofpoint
  Summary: Emerging Threats Open Ruleset
  License: MIT
Name: tgreen/hunting
  Vendor: tgreen
  Summary: Threat hunting rules
  License: GPLv3
Name: etnetera/aggressive
  Vendor: Etnetera a.s.
  Summary: Etnetera aggressive IP blacklist
  License: MIT```
