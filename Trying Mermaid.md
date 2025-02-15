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

Step 1: Once the attacker has a target, he activates numerous hosts. 
Step 2: These hosts start sending traffic to one destination with the goal of denying service. 
Step 3: The Web Server will notice on the increase of traffic. At first this may cause latency or denial of service. 
Step 4: The firewall will start it's defensive measures or may have aleady started through configured ACL's or rate limiting the offending users. 
Step 5: If the attack is unsuccessful, the attacker can alter the IP in which the traffic is coming from.
Step 6: This sends the firewall back into defensive mode to stop the traffic. 