# PsExec Hunt Lab
> Analyze SMB traffic in a PCAP file using Wireshark to identify PsExec lateral movement, compromised systems, user credentials, and administrative shares. 

- **Category**: Network Forensics  
- **Tactics**: Execution, Defense Evasion, Discovery, Lateral Movement  
- **Tool**: Wireshark

## Scenario
An alert from the Intrusion Detection System (IDS) flagged suspicious lateral movement activity involving PsExec. This indicates potential unauthorized access and movement across the network. As a SOC Analyst, your task is to investigate the provided PCAP file to trace the attacker’s activities. Identify their entry point, the machines targeted, the extent of the breach, and any critical indicators that reveal their tactics and objectives within the compromised environment.

## Questions 
**Q1**: To effectively trace the attacker's activities within our network, can you identify the IP address of the machine from which the attacker initially gained access?

**Explanation**: PsExec usually spawns .key file on the client connection with the pattern *PSEXEC-[Source Hostname]-[8 Unique Characters].key* so we go and hunt for that pattern. Note that it is the Source IP with a "Request" String we are looking for here.

**A**: 10.0.0.130

**Q2**: To fully understand the extent of the breach, can you determine the machine's hostname to which the attacker first pivoted?

**Explanation**: For this question, i will be truthful and say this. Since we already knew that 10.0.0.130 was the one that is infected so I have scrolled through the packets and checked when another IP was introduced (or you can filter the communication with a source of 10.0.0.130 via Statistics > Conversation). All i could see was 10.0.0.130 > 10.0.0.131 and when i first saw an IP of 10.0.0.133 i immediately went in TCP Stream and found the Answer.

**A**: Sales-PC 

**Q3**: Knowing the username of the account the attacker used for authentication will give us insights into the extent of the breach. What is the username utilized by the attacker for authentication?

**Explanation**: Upon checking the first packet that 10.0.0.130 sent as a request to 10.0.0.133 under Session Id it has an account name as ssales which is the answer for this question.

**A**: ssales

**Q4**: After figuring out how the attacker moved within our network, we need to know what they did on the target machine. What's the name of the service executable the attacker set up on the target?

**Explanation**: This doesnt need any searching, every request it has a "File:" embeded in the info which is the answer to this question.

**A**: psexesvc.exe

**Q5**: We need to know how the attacker installed the service on the compromised machine to understand the attacker's lateral movement tactics. This can help identify other affected systems. Which network share was used by PsExec to install the service on the target machine?

**Explanation**: Knowing the compromised IP address, we could just check the packet that made the request to 10.0.0.131 via SMB2. The answer is under the Tree Id.

**A**: ADMIN$

**Q6**: We must identify the network share used to communicate between the two machines. Which network share did PsExec use for communication?

**Explanation**: When psexec is executed it usually installs a service and establishes communication channels using pipe named in the format PSEXECSVC-<SourceHostname>-<PID>-stdin, -stdout, and -stderr. So upon knowing this, checking a packet with the same name format reveals the answer. You can see the answer under Tree Id.

**A**: IPC$

**Q7**: Now that we have a clearer picture of the attacker's activities on the compromised machine, it's important to identify any further lateral movement. What is the hostname of the second machine the attacker targeted to pivot within our network?

**Explanation**: So the first PC that was targeted was HR-PC which was 10.0.0.130 and upon checking the TCP Stream with the destination of 10.0.0.131 showed the answer.

**A**: Marketing-PC


