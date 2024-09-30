# DDoS_Attack_Diagram
```mermaid
sequenceDiagram
    participant Attacker
    participant BotNet
    participant WebServer
    participant Firewall

    Attacker ->> BotNet: Initiates attack command
    loop DDoS Traffic
        BotNet ->> WebServer: Send massive requests
    end
    WebServer ->> Firewall: Detect abnormal traffic
    Firewall ->> WebServer: Activate traffic filtering
    Firewall ->> BotNet: Block IPs
    Firewall ->> Attacker: Monitor traffic for new IPs
    BotNet ->> WebServer: Continue sending requests
    WebServer ->> Firewall: Escalate defense measures
