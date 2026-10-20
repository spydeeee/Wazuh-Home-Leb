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
<img width="1536" height="1024" alt="KMTFUZFZ0TDEh_EDSl1vNFTCem7JoIqL0TSLmCHi1QODiC2FiT6r9OqTNDxM3xIlgN8GT1sim5OkURKxMyu7bnlihZEgFq6PPr-y4cHO_9Rf-kFcdoiynbIhayFoKwEGJjyAl6n8FD4ZVyWBRl_RMCSMBapp5-9xVjoSF3ptT9BIoEN2rfZD5O5HAb-y5iOq" src="https://github.com/user-attachments/assets/f0d593e4-fd63-4141-81a6-0b422ff94299" />



Step 2: Enroll the Wazuh Agent

Register the monitored endpoint with the Wazuh Manager. Configure the agent to communicate with the correct manager address and complete the enrollment process.
<img width="694" height="627" alt="ZhR9VWKtH8G3pqPmvWDvs9mrDpN-iU3MZm79Oj9phZ2HHkZMgJRy6eLadebOu4qowF--T7lnsuZbsie0uHKyIIEo2kjPZLQGOJT3gtUzji5jarggAmROTJtK2kCzqFr4JAIEGG7qJfC1_KMWbfSadPhpbxwvxIjOGHPH_x65OcF-Fv8KXmo0Y03H_RWpzV0k" src="https://github.com/user-attachments/assets/0ac7e867-ce01-4826-b681-3239c676a59c" />




Step 3: Verify the Agent Status

Open the Wazuh Dashboard and navigate to agent management. Confirm that the endpoint is registered and active before conducting the test.
<img width="1400" height="906" alt="c4eAAgQYxPBXnJij-4Yismd-qxVgMTBRsERliw8ftOZ8P0h0QwvZGaToEECs1h__TSmUgRkRx7tru1uQcvI9TQZ3bm3SQRS9Zea41n0kJzZ_7nI-PosAjQlTsrLd9yGUGDjnM9pANGvh_JuPCydNpjcLyhxSgUzfs1HjgzTjDSHcOHm12Vi7LpHYhmHYch3c" src="https://github.com/user-attachments/assets/33c897c2-b38c-4c81-8cf1-275fbee21856" />




Step 4: Generate Authorized Nmap Test Traffic

From the scanner machine, run an appropriate Nmap scan against your own lab endpoint.

Example command:

nmap -A -T4 <AUTHORIZED_LAB_TARGET_IP:-[192.168.70.97]>

Replace the placeholder with the IP address of your authorized test machine.

Record the scan output and timestamp for comparison with the security events.
<img width="1026" height="837" alt="mVyTR5HrNlHu5ClLyvEafN3DTTWGHM95VeusXNnH_lXNdJGMLMHoADQDruvzqT066k1MO2GwiEj5r0QDSIE1HwN9_IpdJ-qUp6PDKTes7kAvqCzXfj7F23Jf9C7x33KKjznAX6qSdM2IUY7bjTLEPd2cJ_4UCetACLnmPcD1huMTWZ5_NDv7AREy2lFowQLa" src="https://github.com/user-attachments/assets/991d17f2-3300-4fb7-b2a6-ff611233f2cc" />




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
<img width="1158" height="764" alt="EA7yvqLdsWL_BufxjK6L_c7zoMH5NIcyBiUFvop5JE6gShld0m42dzHBhcOqr7DJshbu156IMDkjOyvYqRY1WuAmQ0YOpMmXgz_MJw9-KojsWIetWNbXmrtCW6Lep03sGqa7I_8Hx6B4totAEtL_pjPy6lxZaHrwg2RTPQlMVPnADwzC5sA_DO2XTjhD9qlP" src="https://github.com/user-attachments/assets/b226e35a-92bc-4a32-a6b6-569edbdaedd1" />



Step 6: Document the Results

Save screenshots of the agent status, scan output, and relevant security events. Explain what was detected, which evidence supports the conclusion, and any limitations encountered.
<img width="621" height="400" alt="v2GUqzVzXkfywNEF-WLwCRq8sG3MCvUNYOb3MGW0z0NWBl9hCGFbtLJrzPHyDeou5_Q4EjbUudRlB25P3Y8RfRChxE0zh1nLzFr5E-2HTOBL1QmQlGQMn13el66ZceAolEu6WJo0EPt6ztCAoepSolWKBSaXHPf3dWBvojwGF34mozzUUtZBwzQsfVXHEcHQ" src="https://github.com/user-attachments/assets/9cebeb47-09e7-4cde-9794-2b13514003ab" />


