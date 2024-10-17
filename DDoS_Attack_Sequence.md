```mermaid
sequenceDiagram
    participant Attacker
    participant BotNet
    participant WebServer
    participant Firewall
    
    Attacker->>BotNet: Command to initiate attack
    BotNet->>WebServer: Sends a lot of requests
    Firewall->>WebServer: Analyze incoming traffic
    Firewall->>BotNet: Block malicious IPs
    BotNet-->>WebServer: Continues sending requests
    Firewall-->>Attacker: Report suspicious activity
    WebServer-->>Attacker: Denied service to legitimate users

```

## Documentation

The attacker sends a command to the BotNet to start the attack. The BotNet sends a lot of requests to the WebServer. The Firewall of the server anaylzes these requests. In response, the firewall blocks malicious IPs associated with the BotNet. In this process, some legitimate users will be denied service because it is flooded with requests from the attack.