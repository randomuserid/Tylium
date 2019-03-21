![Carrelon](/img/120px-BattleofCarillon.jpg?raw=true "text")
# Tylium

### Primary data pipelines for intrusion detection, security analytics and threat hunting

These files contain configuration for producing EDR (endpoint detection and response) data in addition to standard system logs. These configurations enable the production of these data streams using F/OSS (free and / or open source tooling.) The F/OSS tools consist of Auditd for Linux; Sysmon for Windows and Xnumon for the Mac. Also inlcuded is a set of notes for configuring Suricata events and rules.

These data sets enumerate and  / or generate the kinds of security relevant events that are required by threat hunting techniques and a wide variety of security analytics. 

Tylium is part of the SpaceCake project for doing multi-platform intrusion detection, security analytics and threat hunting using open source tools for Linux and Windows in both cloud and conventional environments. 

### Contents:

### Linux

auditd.yaml - a set of auditd rules for generating file, network and process events via the auditd susbsystem for Linux

SystemLogs.md - a matrix of Linux native operating system and web server logs

### MacOS

configuration.plist - a configuration for generating sysmon-like events using the xnumon project on the MacOS

### Suricata

Notes on event and rule setup for Suricata in cloud vs. terrestrial environments

### Windows

EventLogs.md - a matrix of select Windows event log messages and their locations

sysmon-config-base.xml - a sysmon configuration file for generating file, network, registry, network, process and WMI events using Sysmon for Windows

