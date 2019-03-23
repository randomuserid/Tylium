SpaceCake Schema - copyright (c) 2018 - 2019 Project SpaceCake. All rights reserved. Not licensed for use by anyone or anything. 

The first 10k SIDs are reserved for future use. The beginning and end of each range are reserved for special use. SIDs 11000 - 20999 map to the ATT&CK categories. The 30k range is reserved for behavioral detection techniques which produce nondeterministic  detects in many different ATT&CK categories including at least Execution, Persistence, Lateral Movement, Exfiltration, and Command and Control. The 40k range is reserved for multivariate correlation and the 50k range for machine learning (primarily using the significant terms operator to do entity-relationship anomaly detection.) 

Each range is subdivided by data pipeline to enable selection according to data pipelines (if you have no Cloud or no Mac events, for example, there is no need to enable these sets of searches and spend compute resources on them.) Each child category has room for 98 events and each parent category has room for 998 not counting reserved Space IDs for a total of 13972 which is enough space that renumbering should never be necessary. The machine learning range is last because I expect this set may grow larger than 998 searches in the future, in which case it will be extended above the 50k range (and I reserve the right to do some renumbering above the 50k range if the set of machine learning techniques grows to become really large.) Multivariate correlation and machine learning detects will be decorated with ATT&CK categories whenever possible.

The idea here is to ensure that every event, search result and thing I produce always has a unique identifier. In order to try and make these easy to work with under cognitive load, such as in SOC (security operations center) in a state of critical incident response, the numeric ranges are designed to enable an analyst to quickly know or recognize the type and nature of a threat classification alert and what kind of platform or data pipeline it came from. For example, an alert in the 10-19k range is specificatino based; the 30k range is behavioral; the 40k range is a correlation and the 50k range is a machine learning result. This is intended to enable accurate decisioning under congintive load conditions and generally help to facilitate velocity. Hunters and analysts often know which kinds of alerts are most actionable in their environment and hopefully these ranges will help velocity by making it easier to look at actionable detects first. 

| SpaceID (SID) Range Start | End                 | Classification           |               |
|---------------------------|---------------------|--------------------------|---------------|
| 0                         | 10000               | Reserved                 |               |
| 10001                     | 10999               | Initial Access           |               |
| 11001                     | 11999               | Execution                |               |
| 12001                     | 12999               | Persistence              |               |
| 13001                     | 13999               | Privliege Escalation     |               |
| 14001                     | 14999               | Defense Evasion          |               |
| 15001                     | 15999               | Credential Access        |               |
| 16001                     | 16999               | Discovery                |               |
| 17001                     | 17999               | Lateral Movement         |               |
| 18001                     | 18999               | Collection               |               |
| 19001                     | 19999               | Exfiltration             |               |
| 20001                     | 20999               | Command and Control      |               |
| 30001                     | 30999               | Behavioral Detection     |               |
| 40001                     | 40999               | Multivariate Correlation |               |
| 50001                     | 50999               | Machine Learning         |               |
|                           |                     |                          |               |
| Category                  | SpaceID (SID) start | SID end                  | Data Pipeline |
| Initial Access            | 10001               | 10099                    | Auth          |
| Initial Access            | 10101               | 10199                    | Cloud         |
| Initial Access            | 10201               | 10299                    | Data Layer    |
| Initial Access            | 10301               | 10399                    | Linux         |
| Initial Access            | 10401               | 10499                    | MacOS         |
| Initial Access            | 10501               | 10599                    | Mobile        |
| Initial Access            | 10601               | 10699                    | Network       |
| Initial Access            | 10701               | 10799                    | Other         |
| Initial Access            | 10801               | 10899                    | Web           |
| Initial Access            | 10901               | 10999                    | Windows       |
|                           |                     |                          |               |
| Execution                 | 11001               | 11099                    | Auth          |
| Execution                 | 11101               | 11199                    | Cloud         |
| Execution                 | 11201               | 11299                    | Data Layer    |
| Execution                 | 11301               | 11399                    | Linux         |
| Execution                 | 11401               | 11499                    | MacOS         |
| Execution                 | 11501               | 11599                    | Mobile        |
| Execution                 | 11601               | 11699                    | Network       |
| Execution                 | 11701               | 11799                    | Other         |
| Execution                 | 11801               | 11899                    | Web           |
| Execution                 | 11901               | 11999                    | Windows       |
|                           |                     |                          |               |
| Persistence               | 12001               | 12099                    | Auth          |
| Persistence               | 12101               | 12199                    | Cloud         |
| Persistence               | 12201               | 12299                    | Data Layer    |
| Persistence               | 12301               | 12399                    | Linux         |
| Persistence               | 12401               | 12499                    | MacOS         |
| Persistence               | 12501               | 12599                    | Mobile        |
| Persistence               | 12601               | 12699                    | Network       |
| Persistence               | 12701               | 12799                    | Other         |
| Persistence               | 12801               | 12899                    | Web           |
| Persistence               | 12901               | 12999                    | Windows       |
|                           |                     |                          |               |
| Privliege Escalation      | 13001               | 13099                    | Auth          |
| Privliege Escalation      | 13101               | 13199                    | Cloud         |
| Privliege Escalation      | 13201               | 13299                    | Data Layer    |
| Privliege Escalation      | 13301               | 13399                    | Linux         |
| Privliege Escalation      | 13401               | 13499                    | MacOS         |
| Privliege Escalation      | 13501               | 13599                    | Mobile        |
| Privliege Escalation      | 13601               | 13699                    | Network       |
| Privliege Escalation      | 13701               | 13799                    | Other         |
| Privliege Escalation      | 13801               | 13899                    | Web           |
| Privliege Escalation      | 13901               | 13999                    | Windows       |
|                           |                     |                          |               |
| Defense Evasion           | 14001               | 14099                    | Auth          |
| Defense Evasion           | 14101               | 14199                    | Cloud         |
| Defense Evasion           | 14201               | 14299                    | Data Layer    |
| Defense Evasion           | 14301               | 14399                    | Linux         |
| Defense Evasion           | 14401               | 14499                    | MacOS         |
| Defense Evasion           | 14501               | 14599                    | Mobile        |
| Defense Evasion           | 14601               | 14699                    | Network       |
| Defense Evasion           | 14701               | 14799                    | Other         |
| Defense Evasion           | 14801               | 14899                    | Web           |
| Defense Evasion           | 14901               | 14999                    | Windows       |
|                           |                     |                          |               |
| Credential Access         | 15001               | 15099                    | Auth          |
| Credential Access         | 15101               | 15199                    | Cloud         |
| Credential Access         | 15201               | 15299                    | Data Layer    |
| Credential Access         | 15301               | 15399                    | Linux         |
| Credential Access         | 15401               | 15499                    | MacOS         |
| Credential Access         | 15501               | 15599                    | Mobile        |
| Credential Access         | 15601               | 15699                    | Network       |
| Credential Access         | 15701               | 15799                    | Other         |
| Credential Access         | 15801               | 15899                    | Web           |
| Credential Access         | 15901               | 15999                    | Windows       |
|                           |                     |                          |               |
| Discovery                 | 16001               | 16099                    | Auth          |
| Discovery                 | 16101               | 16199                    | Cloud         |
| Discovery                 | 16201               | 16299                    | Data Layer    |
| Discovery                 | 16301               | 16399                    | Linux         |
| Discovery                 | 16401               | 16499                    | MacOS         |
| Discovery                 | 16501               | 16599                    | Mobile        |
| Discovery                 | 16601               | 16699                    | Network       |
| Discovery                 | 16701               | 16799                    | Other         |
| Discovery                 | 16801               | 16899                    | Web           |
| Discovery                 | 16901               | 16999                    | Windows       |
|                           |                     |                          |               |
| Lateral Movement          | 17001               | 17099                    | Auth          |
| Lateral Movement          | 17101               | 17199                    | Cloud         |
| Lateral Movement          | 17201               | 17299                    | Data Layer    |
| Lateral Movement          | 17301               | 17399                    | Linux         |
| Lateral Movement          | 17401               | 17499                    | MacOS         |
| Lateral Movement          | 17501               | 17599                    | Mobile        |
| Lateral Movement          | 17601               | 17699                    | Network       |
| Lateral Movement          | 17701               | 17799                    | Other         |
| Lateral Movement          | 17801               | 17899                    | Web           |
| Lateral Movement          | 17901               | 17999                    | Windows       |
|                           |                     |                          |               |
| Collection                | 18001               | 18099                    | Auth          |
| Collection                | 18101               | 18199                    | Cloud         |
| Collection                | 18201               | 18299                    | Data Layer    |
| Collection                | 18301               | 18399                    | Linux         |
| Collection                | 18401               | 18499                    | MacOS         |
| Collection                | 18501               | 18599                    | Mobile        |
| Collection                | 18601               | 18699                    | Network       |
| Collection                | 18701               | 18799                    | Other         |
| Collection                | 18801               | 18899                    | Web           |
| Collection                | 18901               | 18999                    | Windows       |
|                           |                     |                          |               |
| Exfiltration              | 19001               | 19099                    | Auth          |
| Exfiltration              | 19101               | 19199                    | Cloud         |
| Exfiltration              | 19201               | 19299                    | Data Layer    |
| Exfiltration              | 19301               | 19399                    | Linux         |
| Exfiltration              | 19401               | 19499                    | MacOS         |
| Exfiltration              | 19501               | 19599                    | Mobile        |
| Exfiltration              | 19601               | 19699                    | Network       |
| Exfiltration              | 19701               | 19799                    | Other         |
| Exfiltration              | 19801               | 19899                    | Web           |
| Exfiltration              | 19901               | 19999                    | Windows       |
|                           |                     |                          |               |
| Command and Control       | 20001               | 20099                    | Auth          |
| Command and Control       | 20101               | 20199                    | Cloud         |
| Command and Control       | 20201               | 20299                    | Data Layer    |
| Command and Control       | 20301               | 20399                    | Linux         |
| Command and Control       | 20401               | 20499                    | MacOS         |
| Command and Control       | 20501               | 20599                    | Mobile        |
| Command and Control       | 20601               | 20699                    | Network       |
| Command and Control       | 20701               | 20799                    | Other         |
| Command and Control       | 20801               | 20899                    | Web           |
| Command and Control       | 20901               | 20999                    | Windows       |
|                           |                     |                          |               |
| Behavioral Detection      | 30001               | 30099                    | Auth          |
| Behavioral Detection      | 30101               | 30199                    | Cloud         |
| Behavioral Detection      | 30201               | 30299                    | Data Layer    |
| Behavioral Detection      | 30301               | 30399                    | Linux         |
| Behavioral Detection      | 30401               | 30499                    | MacOS         |
| Behavioral Detection      | 30501               | 30599                    | Mobile        |
| Behavioral Detection      | 30601               | 30699                    | Network       |
| Behavioral Detection      | 30701               | 30799                    | Other         |
| Behavioral Detection      | 30801               | 30899                    | Web           |
| Behavioral Detection      | 30901               | 30999                    | Windows       |
|                           |                     |                          |               |
| Multivariate Correlation  | 40001               | 40099                    | Auth          |
| Multivariate Correlation  | 40101               | 40199                    | Cloud         |
| Multivariate Correlation  | 40201               | 40299                    | Data Layer    |
| Multivariate Correlation  | 40301               | 40399                    | Linux         |
| Multivariate Correlation  | 40401               | 40499                    | MacOS         |
| Multivariate Correlation  | 40501               | 40599                    | Mobile        |
| Multivariate Correlation  | 40601               | 40699                    | Network       |
| Multivariate Correlation  | 40701               | 40799                    | Other         |
| Multivariate Correlation  | 40801               | 40899                    | Web           |
| Multivariate Correlation  | 40901               | 40999                    | Windows       |
|                           |                     |                          |               |
| Machine Learning          | 50001               | 50099                    | Auth          |
| Machine Learning          | 50101               | 50199                    | Cloud         |
| Machine Learning          | 50201               | 50299                    | Data Layer    |
| Machine Learning          | 50301               | 50399                    | Linux         |
| Machine Learning          | 50401               | 50499                    | MacOS         |
| Machine Learning          | 50501               | 50599                    | Mobile        |
| Machine Learning          | 50601               | 50699                    | Network       |
| Machine Learning          | 50701               | 50799                    | Other         |
| Machine Learning          | 50801               | 50899                    | Web           |
| Machine Learning          | 50901               | 50999                    | Windows       |
