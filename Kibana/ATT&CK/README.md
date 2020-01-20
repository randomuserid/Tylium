
### Contents:

### attack-dashboards.ndjson

A set of dashboards for sifting the ATT&CK data from a data coverage perspective. There are more than fifty data sources required to detect the 7081 instances of the 244 numbered techniques. I'm not aware of anyone who has most or all of these 50 data sources. Usually people have cloud, endpoint or network data, but not all three. Dashboards measure observed vs. expected (by the matrix) named events. Sample configurations for instrumenting events more completely are part of this project:
-https://github.com/randomuserid/Tylium/tree/master/Windows
-https://github.com/randomuserid/Tylium/tree/master/Suricata

### Datasource matrix

This is a matrix for resolving ATT&CK data sources into specific log classes and events. These are the events and log message types measured in the dashboards. 

| Name                               | Source         | Auditbeat        | Winlogbeat               | Filebeat                              | Suricata                     |
|------------------------------------|----------------|------------------|--------------------------|---------------------------------------|------------------------------|
| Antivirus Logs                     | Winlogbeat     | .                | Windows Defender Logs    | .                                     | .                            |
| API monitoring                     | APM events     | .                | .                        | .                                     | .                            |
| Application logs                   | APM events     | .                | .                        | .                                     | system events                |
| Authentication logs                | Multiple       | System Module    | Windows Event Logs       | .                                     | .                            |
| AWS CloudTrail logs                | Filebeat       | .                | .                        | CloudTrail module                     | .                            |
| AWS OS logs                        | Multiple       | System Module    | Sysmon, Event Logs       | .                                     | .                            |
| Binary file metadata               | .              | .                |                          | .                                     | .                            |
| Data loss prevention               | Multiple       | System Module    | Sysmon, Event Logs       | .                                     | .                            |
| Digital certificate logs           | Suricata       | .                | .                        | .                                     | TLS events                   |
| DLL monitoring                     | Winlogbeat     | .                | Sysmon Event 7           | .                                     | .                            |
| DNS records                        | Multiple       | .                | Sysmon Event 22          | .                                     | DNS events                   |
| Email gateway                      | .              | .                | .                        | .                                     | -                            |
| Environment variable               | .              | .                | .                        | .                                     | .                            |
| File monitoring                    | Multiple       | FIM events       | Sysmon Events 2,11,15    | .                                     | .                            |
| Host network interface             | .              | .                | .                        | .                                     | .                            |
| Kernel drivers                     | Multiple       | Exec, FIM events | Sysmon Event 6           | .                                     | .                            |
| Loaded DLLs                        | Winlogbeat     | N/A              | Sysmon Event 7           | .                                     | -                            |
| Mail server                        | -              | -                | -                        | .                                     | .                            |
| Malware RE                         | .              | .                | .                        | .                                     | .                            |
| Malware reverse engineering        | Cuckoo sandbox | .                | .                        | .                                     | .                            |
| Netflow/Enclave netflow            | Suricata       | .                | .                        | .                                     | Flow events                  |
| Network device logs                | Multiple       | .                | .                        | Cisco, Palo Alto modules              | .                            |
| Network IDS                        | Suricata       | -                | -                        | .                                     | alerts                       |
| Network intrusion detection system | Suricata       | .                | .                        | .                                     | alerts                       |
| Network protocol analysis          | Suricata       | .                | .                        | .                                     | flows, http, tls, ssh events |
| Packet capture                     | Suricata       | .                | .                        | .                                     | optional                     |
| PowerShell logs                    | Winlogbeat     | .                | PowerShell logs          | .                                     | .                            |
| Process command-line parameters    | Multiple       | System module    | Sysmon events 1,5,8      | .                                     | .                            |
| Process monitoring                 | Multiple       | Exec events      | Sysmon events 1,5,9      | .                                     | .                            |
| Process use of network             | .              | System module    | Sysmon event 3           | .                                     | .                            |
| Sensor health and status           | Multiple       | System module    | Sysmon events 4,16       | Multiple modules                      | .                            |
| Services                           | .              | .                | Windows Event Logs       | .                                     | .                            |
| SSL/TLS inspection                 | Multiple       | .                | .                        | CEF module; Nginx module; Palo module | .                            |
| Stackdriver logs                   | .              | .                | .                        | Google Cloud module                   | .                            |
| System calls                       | Multiple       | System module    | Sysmon events            | .                                     | .                            |
| Third-party application logs       | .              | .                | .                        | CEF module                            | .                            |
| User interface                     | .              | .                | .                        | .                                     | .                            |
| Web application firewall logs      | Modsecurity    | .                | .                        | .                                     | .                            |
| Web logs                           | Multiple       | .                | .                        | Apache / IIS / Nginx modules          | .                            |
| Web proxy                          | Squid          | .                | .                        | .                                     | .                            |
| Windows Error Reporting            | Winlogbeat     | .                | Windows events 1000-1001 | .                                     | .                            |
| Windows event logs                 | Winlogbeat     | .                | Windows events           | .                                     | .                            |
| Windows Registry                   | Winlogbeat     | .                | Sysmon events 12-14      | .                                     | .                            |
| WMI Objects                        | Winlogbeat     | .                | Sysmon events 19-21      | .                                     | .                            |
