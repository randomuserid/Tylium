![Carrelon](/img/120px-BattleofCarillon.jpg?raw=true "text")
# Tylium

### Primary data pipelines for intrusion detection, security analytics and threat hunting

These files contain configuration for producing EDR (endpoint detection and response) like data using open source tooling for Linux, Windows and the MacOS in additon to standard system logs. These data sets enumerate and  / or generate the security relevant events that are required by the  threat hunting intrusion detection and security analytics techniques.

Tylium is part of the SpaceCake project for doing intrusion detection, security analytics and threat hunting using open source tools. 

### Contents:

### Linux

auditd.yaml - a set of auditd rules for generating interesting file, network and process events via the auditd susbsystem for Linux

SystemLogs.md - a matrix of Linux native operating system and web server logs

### MacOS

configuration.plist - a configuration for generating sysmon-like events using the xnumon project on the MacOS.

### Suricata

Notes on event and rule setup for Suricata in cloud vs. terrestrial envioronments

### Windows

EventLogs.md - a matrix of select Windows event log messages and their locations

sysmon-config-base.xml - a sysmon configuration file for generating file, network, registry, network, process and WMI events using Sysmon for Windows

