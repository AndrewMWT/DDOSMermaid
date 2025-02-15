```mermaid
sequenceDiagram
participant Attacker
participant BotNet
participant WebServer
participant Firewall
Attacker->>BotNet: Activates botnet.
BotNet->>WebServer: Starts flooding the Webserver with phony traffic. 
WebServer->>Firewall: Notices increase of traffic through interface utilization or other monitoring systems.
Firewall->>WebServer: Blocks incoming traffic through configured ACL's or rate limiting.
BotNet->>WebServer: May attempt to bypass security measures through changing the source traffic's IP.
Firewall->>WebServer: Notices the new incoming traffic and will adapt it's security rules to block the new IP source.
```

