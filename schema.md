SpaceCake Schema - copyright (c) 2018 - 2019 Project SpaceCake. All rights reserved. Not licensed for use by anyone or anything except the SpaceCake project.

The first 10k SIDs are reserved for future use. The beginning and end of each range are reserved for special use. SIDs 10,001 through 119,999 map to the ATT&CK categories. The 200k range is reserved for behavioral detection techniques which produce nondeterministic  detects in many different ATT&CK categories including at least Execution, Persistence, Lateral Movement, Exfiltration, and Command and Control. The 300k range is reserved for multivariate correlation and the 400k range for machine learning jobs. The 1,000,000 range is reserved for local use - for numbering local or organization-specific searches that are not incorporated into the project for whatever reason.

Each range is subdivided by data pipeline to enable selection according to data pipelines (if you have no Mac events, for example, there is no need to enable these sets of searches and spend compute resources on them.) Each child category has room for 998 events and each parent category has room for 9980 not counting reserved Space IDs for a total of 109,780 which is enough space that renumbering should never be necessary. The ranges for behavioral detection, multivariate correlation and machine learning each have their own distinct range with a very large number space of 99,980 so they have practically unlimited room to grow. These will be decorated with ATT&CK categories whenever the payload or intent is narrow and clear enough to make it feasible and reasonable to confine the search to a particular TTP.

The idea here is to ensure that every search or alert has a unique identifier that can be referenced back to a description of what the search is detecting, and so that rules, searches and alerts can be precisely identified in order to reduce ambiguity. Geographically distributed teams, teams under cognitive load, and teams lacking in common languages, are less likely to miscommunicate a numeric search ID than a complex name or phrase. Another objective is make these easy to work with under cognitive load, such as in SOC (security operations center) in a state of critical incident response, the numeric ranges are designed to enable an analyst to quickly know or recognize the type and nature of a threat classification alert and what kind of platform or data pipeline it came from. For example, an alert in the 10-120k range is specification based; the 200k range is behavioral; the 300k range is a correlation and the 400k range is a machine learning result. This is intended to enable accurate decisioning under cognitive load conditions and generally help to facilitate velocity. Hunters and analysts often know which kinds of alerts are most actionable in their environment and hopefully these ranges will help velocity by making it easier to look at actionable detects first.

| SpaceID (SID) Range Start | Range End                | Classification             |         |
|---------------------------|--------------------------|----------------------------|---------|
| 0                         | 10,000                   | Reserved for SpaceCake Use |         |
| 10,001                    | 19,999                   | Initial Access             |         |
| 20,001                    | 29,999                   | Execution                  |         |
| 30,001                    | 39,999                   | Persistence                |         |
| 40,001                    | 49,999                   | Privliege Escalation       |         |
| 50,001                    | 59,999                   | Defense Evasion            |         |
| 60,001                    | 69,999                   | Credential Access          |         |
| 70,001                    | 79,999                   | Discovery                  |         |
| 80,001                    | 89,999                   | Lateral Movement           |         |
| 90,001                    | 99,999                   | Collection                 |         |
| 100,001                   | 109,999                  | Exfiltration               |         |
| 110,001                   | 119,999                  | Command and Control        |         |
| 200,001                   | 299,999                  | Behavioral Detection       |         |
| 300,001                   | 399,999                  | Multivariate Correlation   |         |
| 400,001                   | 499,999                  | Machine Learning           |         |
| 1,000,001                 | 1,999,999                | Reserved for Local Use     |         |
|                           |                          |                            |         |
| Data Pipeline             | Category                 | SpaceID (SID) start        | SID end |
| Auth                      | Initial Access           | 10,001                     | 10,999  |
| Cloud                     | Initial Access           | 11,001                     | 11,999  |
| Data Layer                | Initial Access           | 12,001                     | 12,999  |
| Linux                     | Initial Access           | 13,001                     | 13,999  |
| MacOS                     | Initial Access           | 14,001                     | 14,999  |
| Mobile                    | Initial Access           | 15,001                     | 15,999  |
| Network                   | Initial Access           | 16,001                     | 16,999  |
| Other                     | Initial Access           | 17,001                     | 17,999  |
| Web                       | Initial Access           | 18,001                     | 18,999  |
| Windows                   | Initial Access           | 19,001                     | 19,999  |
|                           |                          |                            |         |
| Auth                      | Execution                | 20,001                     | 20,999  |
| Cloud                     | Execution                | 21,001                     | 21,999  |
| Data Layer                | Execution                | 22,001                     | 22,999  |
| Linux                     | Execution                | 23,001                     | 23,999  |
| MacOS                     | Execution                | 24,001                     | 24,999  |
| Mobile                    | Execution                | 25,001                     | 25,999  |
| Network                   | Execution                | 26,001                     | 26,999  |
| Other                     | Execution                | 27,001                     | 27,999  |
| Web                       | Execution                | 28,001                     | 28,999  |
| Windows                   | Execution                | 29,001                     | 29,999  |
|                           |                          |                            |         |
| Auth                      | Persistence              | 30,001                     | 30,999  |
| Cloud                     | Persistence              | 31,001                     | 31,999  |
| Data Layer                | Persistence              | 32,001                     | 32,999  |
| Linux                     | Persistence              | 33,001                     | 33,999  |
| MacOS                     | Persistence              | 34,001                     | 34,999  |
| Mobile                    | Persistence              | 35,001                     | 35,999  |
| Network                   | Persistence              | 36,001                     | 36,999  |
| Other                     | Persistence              | 37,001                     | 37,999  |
| Web                       | Persistence              | 38,001                     | 38,999  |
| Windows                   | Persistence              | 39,001                     | 39,999  |
|                           |                          |                            |         |
| Auth                      | Privliege Escalation     | 40,001                     | 40,999  |
| Cloud                     | Privliege Escalation     | 41,001                     | 41,999  |
| Data Layer                | Privliege Escalation     | 42,001                     | 42,999  |
| Linux                     | Privliege Escalation     | 43,001                     | 43,999  |
| MacOS                     | Privliege Escalation     | 44,001                     | 44,999  |
| Mobile                    | Privliege Escalation     | 45,001                     | 45,999  |
| Network                   | Privliege Escalation     | 46,001                     | 46,999  |
| Other                     | Privliege Escalation     | 47,001                     | 47,999  |
| Web                       | Privliege Escalation     | 48,001                     | 48,999  |
| Windows                   | Privliege Escalation     | 49,001                     | 49,999  |
|                           |                          |                            |         |
| Auth                      | Defense Evasion          | 50,001                     | 50,999  |
| Cloud                     | Defense Evasion          | 51,001                     | 51,999  |
| Data Layer                | Defense Evasion          | 52,001                     | 52,999  |
| Linux                     | Defense Evasion          | 53,001                     | 53,999  |
| MacOS                     | Defense Evasion          | 54,001                     | 54,999  |
| Mobile                    | Defense Evasion          | 55,001                     | 55,999  |
| Network                   | Defense Evasion          | 56,001                     | 56,999  |
| Other                     | Defense Evasion          | 57,001                     | 57,999  |
| Web                       | Defense Evasion          | 58,001                     | 58,999  |
| Windows                   | Defense Evasion          | 59,001                     | 59,999  |
|                           |                          |                            |         |
| Auth                      | Credential Access        | 60,001                     | 60,999  |
| Cloud                     | Credential Access        | 61,001                     | 61,999  |
| Data Layer                | Credential Access        | 62,001                     | 62,999  |
| Linux                     | Credential Access        | 63,001                     | 63,999  |
| MacOS                     | Credential Access        | 64,001                     | 64,999  |
| Mobile                    | Credential Access        | 65,001                     | 65,999  |
| Network                   | Credential Access        | 66,001                     | 66,999  |
| Other                     | Credential Access        | 67,001                     | 67,999  |
| Web                       | Credential Access        | 68,001                     | 68,999  |
| Windows                   | Credential Access        | 69,001                     | 69,999  |
|                           |                          |                            |         |
| Auth                      | Discovery                | 70,001                     | 70,999  |
| Cloud                     | Discovery                | 71,001                     | 71,999  |
| Data Layer                | Discovery                | 72,001                     | 72,999  |
| Linux                     | Discovery                | 73,001                     | 73,999  |
| MacOS                     | Discovery                | 74,001                     | 74,999  |
| Mobile                    | Discovery                | 75,001                     | 75,999  |
| Network                   | Discovery                | 76,001                     | 76,999  |
| Other                     | Discovery                | 77,001                     | 77,999  |
| Web                       | Discovery                | 78,001                     | 78,999  |
| Windows                   | Discovery                | 79,001                     | 79,999  |
|                           |                          |                            |         |
| Auth                      | Lateral Movement         | 81,001                     | 81,999  |
| Cloud                     | Lateral Movement         | 81,001                     | 81,999  |
| Data Layer                | Lateral Movement         | 81,001                     | 81,999  |
| Linux                     | Lateral Movement         | 81,001                     | 81,999  |
| MacOS                     | Lateral Movement         | 81,001                     | 81,999  |
| Mobile                    | Lateral Movement         | 81,001                     | 81,999  |
| Network                   | Lateral Movement         | 81,001                     | 81,999  |
| Other                     | Lateral Movement         | 81,001                     | 81,999  |
| Web                       | Lateral Movement         | 81,001                     | 81,999  |
| Windows                   | Lateral Movement         | 81,001                     | 81,999  |
|                           |                          |                            |         |
| Auth                      | Collection               | 90,001                     | 90,999  |
| Cloud                     | Collection               | 91,001                     | 91,999  |
| Data Layer                | Collection               | 92,001                     | 92,999  |
| Linux                     | Collection               | 93,001                     | 93,999  |
| MacOS                     | Collection               | 94,001                     | 94,999  |
| Mobile                    | Collection               | 95,001                     | 95,999  |
| Network                   | Collection               | 96,001                     | 96,999  |
| Other                     | Collection               | 97,001                     | 97,999  |
| Web                       | Collection               | 98,001                     | 98,999  |
| Windows                   | Collection               | 99,001                     | 99,999  |
|                           |                          |                            |         |
| Auth                      | Exfiltration             | 100,001                    | 100,999 |
| Cloud                     | Exfiltration             | 101,001                    | 101,999 |
| Data Layer                | Exfiltration             | 102,001                    | 102,999 |
| Linux                     | Exfiltration             | 103,001                    | 103,999 |
| MacOS                     | Exfiltration             | 104,001                    | 104,999 |
| Mobile                    | Exfiltration             | 105,001                    | 105,999 |
| Network                   | Exfiltration             | 106,001                    | 106,999 |
| Other                     | Exfiltration             | 107,001                    | 107,999 |
| Web                       | Exfiltration             | 108,001                    | 108,999 |
| Windows                   | Exfiltration             | 109,001                    | 109,999 |
|                           |                          |                            |         |
| Auth                      | Command and Control      | 110,001                    | 110,999 |
| Cloud                     | Command and Control      | 111,001                    | 111,999 |
| Data Layer                | Command and Control      | 112,001                    | 112,999 |
| Linux                     | Command and Control      | 113,001                    | 113,999 |
| MacOS                     | Command and Control      | 114,001                    | 114,999 |
| Mobile                    | Command and Control      | 115,001                    | 115,999 |
| Network                   | Command and Control      | 116,001                    | 116,999 |
| Other                     | Command and Control      | 117,001                    | 117,999 |
| Web                       | Command and Control      | 118,001                    | 118,999 |
| Windows                   | Command and Control      | 119,001                    | 119,999 |
|                           |                          |                            |         |
| Auth                      | Behavioral Detection     | 200,001                    | 209,999 |
| Cloud                     | Behavioral Detection     | 210,001                    | 219,999 |
| Data Layer                | Behavioral Detection     | 220,001                    | 229,999 |
| Linux                     | Behavioral Detection     | 230,001                    | 239,999 |
| MacOS                     | Behavioral Detection     | 240,001                    | 249,999 |
| Mobile                    | Behavioral Detection     | 250,001                    | 259,999 |
| Network                   | Behavioral Detection     | 260,001                    | 269,999 |
| Other                     | Behavioral Detection     | 270,001                    | 279,999 |
| Web                       | Behavioral Detection     | 280,001                    | 289,999 |
| Windows                   | Behavioral Detection     | 290,001                    | 299,999 |
|                           |                          |                            |         |
| Auth                      | Multivariate Correlation | 300,001                    | 309,999 |
| Cloud                     | Multivariate Correlation | 310,001                    | 319,999 |
| Data Layer                | Multivariate Correlation | 320,001                    | 329,999 |
| Linux                     | Multivariate Correlation | 330,001                    | 339,999 |
| MacOS                     | Multivariate Correlation | 340,001                    | 349,999 |
| Mobile                    | Multivariate Correlation | 350,001                    | 359,999 |
| Network                   | Multivariate Correlation | 360,001                    | 369,999 |
| Other                     | Multivariate Correlation | 370,001                    | 379,999 |
| Web                       | Multivariate Correlation | 380,001                    | 389,999 |
| Windows                   | Multivariate Correlation | 390,001                    | 399,999 |
|                           |                          |                            |         |
| Auth                      | Machine Learning         | 400,001                    | 409,999 |
| Cloud                     | Machine Learning         | 410,001                    | 419,999 |
| Data Layer                | Machine Learning         | 400,002                    | 410,000 |
| Linux                     | Machine Learning         | 410,002                    | 420,000 |
| MacOS                     | Machine Learning         | 400,003                    | 410,001 |
| Mobile                    | Machine Learning         | 410,003                    | 420,001 |
| Network                   | Machine Learning         | 400,004                    | 410,002 |
| Other                     | Machine Learning         | 410,004                    | 420,002 |
| Web                       | Machine Learning         | 400,005                    | 410,003 |
| Windows                   | Machine Learning         | 410,005                    | 420,003 |
