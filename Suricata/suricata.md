
Suricata configuration notes: snippets from the suricata.yaml file.

Enable eve.json for consumption in ELK. Enable other formats as desired.

Enable http, dns and tls events if Suricata is network sensor connected
to a point of network instrumentation like a span port or tap.

Disable these if Suricata is running on a balancer or web server in AWS.

Enable stats (to measure packet drops)


# global stats configuration
stats:
  enabled: yes
  # The interval field (in seconds) controls at what interval
  # the loggers are invoked.
  interval: 10

# Configure the type of alert (and other) logging you would like.
outputs:
  
  # Extensible Event Format (nicknamed EVE) event log in JSON format
  - eve-log:
      enabled: yes
      filetype: regular #regular|syslog|unix_dgram|unix_stream|redis
      filename: eve.json

        - http:
            extended: yes     # enable this for extended logging information
            # custom allows additional http fields to be included in eve-log
            # the example below adds three additional fields when uncommented
            #custom: [Accept-Encoding, Accept-Language, Authorization]
        - dns:
            # control logging of queries and answers
            # default yes, no to disable
            query: yes     # enable logging of DNS queries
            answer: yes    # enable logging of DNS answers
            # control which RR types are logged
            # all enabled if custom not specified
            #custom: [a, aaaa, cname, mx, ns, ptr, txt]
        - tls:
            extended: yes     # enable this for extended logging information
            # output TLS transaction where the session is resumed using a
            # session id
            #session-resumption: no
            # custom allows to control which tls fields that are included
            # in eve-log
            #custom: [subject, issuer, session_resumed, serial, fingerprint, sni, version, not_before, not_after, certificate, chain]
