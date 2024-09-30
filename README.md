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



**1. Attacker initiates attack: The attacker sends a command to the botnet, instructing it to flood the web server with requests.**
**2. Botnet floods the WebServer: Each bot in the network sends numerous requests, overwhelming the web server.**
**3. WebServer detects abnormal traffic: The web server notices the unusual spike in traffic and alerts the firewall.**
**4. Firewall response: The firewall analyzes the traffic, blocks the malicious IPs from the botnet, and monitors further traffic from the attacker.**
**5. Botnet continues attack: The botnet persists with the attack, but the firewall escalates defenses by blocking additional traffic.**
