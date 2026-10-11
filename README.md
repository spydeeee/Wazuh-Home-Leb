# Wazuh-Home-Leb

## Objective
[Brief Objective - Remove this afterwards]

uilt a home SOC lab using Oracle VirtualBox — deployed 
Wazuh SIEM on Ubuntu, enrolled a Windows 10 agent, and 
monitored live security events via the dashboard.

Covered: MITRE ATT&CK mapping, vulnerability detection 
(Critical/High CVEs), CIS benchmark compliance (SCA), 
and real agent-enrollment troubleshooting.

🛠️ Wazuh • Ubuntu Linux • Windows 10 • VirtualBox • 
MITRE ATT&CK

### Skills Learned
[Bullet Points - Remove this afterwards]

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used
[Bullet Points - Remove this afterwards]

- Security Information and Event Management (Wazuh) system for log ingestion and analysis.
- Network analysis tools (such as Wireshark) for capturing and examining network traffic.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## Steps

Step 1: Prepare the Lab Environment

Create the required virtual machines and configure their network connectivity. Verify the IP addresses and ensure the scanner can reach the intended test endpoint.



Step 2: Enroll the Wazuh Agent

Register the monitored endpoint with the Wazuh Manager. Configure the agent to communicate with the correct manager address and complete the enrollment process.



Step 3: Verify the Agent Status

Open the Wazuh Dashboard and navigate to agent management. Confirm that the endpoint is registered and active before conducting the test.



Step 4: Generate Authorized Nmap Test Traffic

From the scanner machine, run an appropriate Nmap scan against your own lab endpoint.

Example command:

nmap -A -T4 <AUTHORIZED_LAB_TARGET_IP>

Replace the placeholder with the IP address of your authorized test machine.

Record the scan output and timestamp for comparison with the security events.



Step 5: Investigate Security Events

Open the Wazuh Dashboard and search for events that correspond to the test activity.

Review the available alert fields:

Timestamp

Agent name or ID

Source and destination information, when available

Rule ID and severity

Alert description

Raw log entry

A scan being completed does not automatically prove that Wazuh detected it. Confirm the result using the actual alert evidence.



Step 6: Document the Results

Save screenshots of the agent status, scan output, and relevant security events. Explain what was detected, which evidence supports the conclusion, and any limitations encountered.

