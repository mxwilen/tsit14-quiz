<a name="top"></a> <!-- Top anchor -->

- [Module 1 - Intro to DFIR](#module-1---intro-to-dfir)
- [Module 2 - Preparation](#module-2---preparation)
- [Module 3 - Filesystem Forensics](#module-3---filesystem-forensics)
- [Module 4 - Network Forensics](#module-4---network-forensics)
- [Module 5 - Logs and Timeline](#module-5---logs-and-timeline)
- [Module 6 - Local Systems Forensics](#module-6---local-systems-forensics)

# Module 1 - Intro to DFIR
1. **Q**: What is digital forensics?
    
    - **A**: Digital forensics is the process of identifying, preserving, analyzing, and presenting digital evidence for investigations.
2. **Q**: What is incident response?
    
    - **A**: Incident response is a systematic approach to identifying, managing, and resolving security incidents to minimize damage and prevent recurrence.
3. **Q**: What is DFIR?
    
    - **A**: DFIR stands for Digital Forensics and Incident Response, combining forensic analysis with real-time incident handling to address security breaches effectively.

---

4. **Q**: What is the difference between conventional digital forensics and digital forensics in incident response?
    
    - **A**: Conventional digital forensics is detailed and methodical for legal contexts, while digital forensics in incident response prioritizes rapid data analysis for threat containment.
5. **Q**: Why might conventional digital forensic methods be unsuitable for incident response?
    
    - **A**: They are often too time-consuming, lacking the immediacy required to quickly contain and remediate security incidents.

---

6. **Q**: Why is incident response performed?
    
    - **A**: It is performed to detect, contain, and remediate security incidents to protect assets, minimize damage, and prevent future incidents.
7. **Q**: Why is incident response considered a team effort?
    
    - **A**: Incident response requires collaboration across various skill sets and roles, ensuring a comprehensive and coordinated approach to handling security incidents.
8. **Q**: Name two organizations focused on improving incident response capabilities.
    
    - **A**: TF-CSIRT (Trusted Introducer CSIRT network) and FIRST (Forum of Incident Response and Security Teams).

---

9. **Q**: Name three sources of incident response models.
    
    - **A**: NIST (National Institute of Standards and Technology), ISO 27035, and SANS.
10. **Q**: Why is it beneficial to use a framework for establishing incident response capacity?
    
    - **A**: Frameworks provide structured guidelines, making it easier to implement consistent, effective incident response practices across organizations.

---

11. **Q**: What does NIST do, and where do they operate?
    
    - **A**: NIST, based in the United States, develops standards, guidelines, and frameworks to improve information security and cybersecurity practices.
12. **Q**: Which categories of the NIST Cybersecurity Framework (CSF) does their incident response framework cover?
    
    - **A**: NIST's incident response framework covers categories such as Identification, Protection, Detection, Response, and Recovery.

---

13. **Q**: List the four phases of incident response according to the NIST framework.
    
    - **A**: The four phases are Preparation, Detection and Analysis, Containment and Eradication, and Post-Incident Recovery.
14. **Q**: Briefly explain each phase in the NIST incident response framework.
    
    - **A**:
        - **Preparation**: Establish policies, plans, and resources for effective incident handling.
        - **Detection and Analysis**: Identify and investigate potential security events.
        - **Containment and Eradication**: Stop the threat's spread, remove malicious components, and ensure a secure environment.
        - **Post-Incident Recovery**: Return to normal operations, review response, and improve policies if necessary.

---

15. **Q**: What does the ISO 27000 family of standards focus on?
    
    - **A**: ISO 27000 standards focus on information security management, providing guidelines for securing information assets.
16. **Q**: What is ISO 27035 specifically about?
    
    - **A**: ISO 27035 is a standard dedicated to incident management, providing a framework for effectively managing security incidents.

---

17. **Q**: What are the five phases of the ISO 27035 model?
    
    - **A**: The five phases are:
        - **Preparation**: Setting up the necessary tools, teams, and procedures.
        - **Detection and Reporting**: Identifying and documenting security events.
        - **Assessment and Decision**: Evaluating the severity of incidents to prioritize response.
        - **Responses**: Taking action to mitigate and resolve the incident.
        - **Lessons Learned**: Reviewing the incident and response to improve future handling.
18. **Q**: How does incident management differ from incident response?
    
    - **A**: Incident management involves the processes and frameworks to handle incidents strategically, while incident response refers to the immediate actions taken to address specific incidents.

---

19. **Q**: List the seven phases of the SANS incident response model.
    
    - **A**: The SANS model includes:
        - **Preparation**: Building and training a response team, gathering tools and resources.
        - **Identification**: Detecting and determining the nature of an incident.
        - **Containment**: Preventing the spread of the incident’s impact.
        - **Eradication**: Removing the root cause of the incident.
        - **Recovery**: Restoring affected systems and services.
        - **Lessons Learned**: Reviewing the incident for improvements.
        - **Continuous Improvement**: Updating practices based on lessons learned and new threats.
20. **Q**: How does each phase in the SANS model relate to ISO 27035 and NIST frameworks?
    
    - **A**: The phases align closely in purpose:
        - **Preparation** (all models): Establishing resources and readiness.
        - **Identification/Detection** (SANS/NIST): Identifying the incident.
        - **Containment and Eradication/Response** (SANS/ISO): Addressing and neutralizing threats.
        - **Recovery** (SANS/NIST): Returning to operational stability.
        - **Lessons Learned/Improvement** (all models): Improving future response.
---
[Back to Top](#top)

# Module 2 - Preparation
1. **Q**: What is an incident response policy?
    
    - **A**: An incident response policy defines an organization's overarching approach and guidelines for managing security incidents.
2. **Q**: What are some key elements of an incident response policy?
    
    - **A**: Key elements include scope, objectives, roles and responsibilities, incident classification, and communication plans.
3. **Q**: How is the incident response policy related to the incident response plan?
    
    - **A**: The policy provides high-level guidance, while the plan details the specific actions and steps to be followed during incidents.

---

4. **Q**: What is an incident response plan?
    
    - **A**: An incident response plan outlines detailed procedures for detecting, responding to, and recovering from security incidents.
5. **Q**: What are some key elements of an incident response plan?
    
    - **A**: Key elements include incident detection methods, escalation procedures, response steps, communication protocols, and recovery steps.
6. **Q**: How does the incident response plan relate to the incident response policy?
    
    - **A**: The plan operationalizes the policy, providing actionable steps based on the guidelines set by the policy.

---

7. **Q**: What is an incident response playbook?
    
    - **A**: A playbook is a predefined set of steps for responding to specific types of incidents, ensuring consistency and efficiency.
8. **Q**: What are the benefits of using incident response playbooks over ad-hoc responses?
    
    - **A**: Playbooks provide structure, reduce response time, minimize errors, and ensure alignment with best practices.
9. **Q**: Define a playbook for a task.
    
    - **A**: A playbook might include steps for handling a phishing attempt, such as identifying affected accounts, isolating them, and notifying affected users.
10. **Q**: What is the difference between a playbook and a procedure?
    
    - **A**: A playbook outlines responses for specific scenarios, while a procedure is a broader, step-by-step process applicable to various tasks.

---

11. **Q**: What is an incident response procedure?
    
    - **A**: A procedure is a sequence of steps designed to perform a specific task within incident response.
12. **Q**: What are the benefits of using incident response procedures over ad-hoc responses?
    
    - **A**: Procedures ensure accuracy, consistency, and repeatability, leading to more reliable incident handling.

---

13. **Q**: What is the CSIRT services framework, and what is its purpose?
    
    - **A**: The CSIRT framework provides a structured approach to cybersecurity incident response services, such as alert handling and incident analysis.
14. **Q**: Name and describe a few services in the CSIRT framework.
    
    - **A**: Services include alert handling (receiving and analyzing alerts), vulnerability assessment (evaluating vulnerabilities), and incident management (coordinating response efforts).
15. **Q**: What is RFC 2350, and what is its goal?
    
    - **A**: RFC 2350 provides a template for CSIRT descriptions to promote transparency and standardization in cybersecurity response capabilities.
16. **Q**: Name a few key parts of the CSIRT description in RFC 2350.
    
    - **A**: Key parts include contact information, service scope, response methods, and operating hours.

---

17. **Q**: Why are training and exercises important for CSIRT teams?
    
    - **A**: Training and exercises help teams build and retain skills, enhancing readiness and performance during actual incidents.
18. **Q**: What is the difference between training and exercises?
    
    - **A**: Training builds individual knowledge and skills, while exercises simulate real incidents to test team coordination and readiness.
19. **Q**: Describe a few formats for exercises.
    
    - **A**: Formats include tabletop exercises, simulations, and full-scale drills.
20. **Q**: Identify a few sources or activities for training.
    
    - **A**: Sources include online courses, certifications, workshops, and cybersecurity conferences.

---

21. **Q**: What is a vulnerability scanner, and how does it contribute to incident prevention?
    
    - **A**: A vulnerability scanner identifies security weaknesses in systems, helping prevent incidents by enabling timely remediation.
22. **Q**: What is an EDR tool, and how might it be superior to signature-based antimalware?
    
    - **A**: EDR (Endpoint Detection and Response) provides continuous monitoring and response capabilities, making it more effective against advanced threats than traditional signature-based solutions.
23. **Q**: Explain why evading signature-based antimalware software is easy.
    
    - **A**: Signature-based tools rely on known threat patterns, making them ineffective against new or modified malware.

---

24. **Q**: Name several types of incident detection tools.
    
    - **A**: Examples include EDR tools, SIEM (Security Information and Event Management) systems, and IDS (Intrusion Detection Systems).
25. **Q**: What is a SIEM, and how is it used in incident response?
    
    - **A**: A SIEM collects and analyzes security data in real-time, helping identify, investigate, and respond to incidents.
26. **Q**: What is an IDS, and how does it differ from an IPS?
    
    - **A**: An IDS detects suspicious activities and generates alerts, while an IPS actively blocks malicious traffic.

---

27. **Q**: Describe several kinds of incident resolution tools.
    
    - **A**: Tools include timelining tools for incident reconstruction, forensic tools for data analysis, and remediation tools for system recovery.
28. **Q**: Why is documentation important in incident response?
    
    - **A**: Documentation provides a record of actions and decisions, which is crucial for analysis, reporting, and legal accountability.

---

29. **Q**: What is threat intelligence, and what role does it play in incident response?
    
    - **A**: Threat intelligence provides information on emerging threats, helping teams anticipate, prevent, and respond to security incidents.
30. **Q**: What are IOCs, and how are they used in incident response?
    
    - **A**: Indicators of Compromise (IOCs) are signs of malicious activity, such as IP addresses or file hashes, used to detect and analyze incidents.
31. **Q**: Name and briefly describe one APT group listed in MITRE ATT&CK.
    
    - **A**: APT29, associated with state-sponsored espionage, is known for advanced malware and spear-phishing tactics.

---

32. **Q**: What is the CISA Known Exploited Vulnerabilities Catalog?
    
    - **A**: This catalog lists known vulnerabilities actively exploited in cyber-attacks, guiding organizations in prioritizing patch management.
33. **Q**: Describe the role of information sharing in incident response.
    
    - **A**: Information sharing enables collaborative threat intelligence, helping organizations prepare for and respond to threats more effectively.
34. **Q**: What is an ISAC, and name one example.
    
    - **A**: An Information Sharing and Analysis Center (ISAC) facilitates information sharing within a specific sector, such as the Financial Services ISAC (FS-ISAC).

---

35. **Q**: What is the Traffic Light Protocol (TLP), and what do the levels mean?
    
    - **A**: The TLP is a framework for sharing sensitive information, with levels indicating sharing restrictions (e.g., TLP for restricted, TLP for unrestricted).
36. **Q**: What is the Permissible Actions Protocol, and what do the levels indicate?
    
    - **A**: The protocol indicates acceptable actions for shared information, with levels guiding whether information can be disclosed or acted upon.
37. **Q**: What is the Chatham House Rule, and how is it applied?
    
    - **A**: The Chatham House Rule allows participants to use shared information without attributing it to specific speakers, promoting open discussions.
---
[Back to Top](#top)

# Module 3 - Filesystem Forensics
1. **Q**: What is filesystem forensics, and what can it be used for?
    
    - **A**: Filesystem forensics involves analyzing digital storage structures to recover, analyze, and interpret files, which can be used to uncover evidence of data access, modification, and deletion.
2. **Q**: Briefly describe a model of the forensic process.
    
    - **A**: A common model is the "Identify, Preserve, Analyze, Present" process, which includes identifying relevant data, preserving it without alteration, analyzing it for evidence, and presenting findings.
3. **Q**: What are some trade-offs in incident response versus criminal investigations?
    
    - **A**: Incident response often prioritizes speed over detailed analysis to mitigate active threats, whereas criminal investigations require comprehensive evidence collection, which can be slower.

---

4. **Q**: What are some types of storage relevant to filesystem forensics?
    
    - **A**: Types include hard disk drives (HDDs), solid-state drives (SSDs), memory cards, and embedded storage, each with unique challenges for data acquisition.
5. **Q**: What are the properties and forensic challenges with HDDs, SSDs, memory cards, and embedded storage?
    
    - **A**:
        - **HDDs**: Mechanical, slower, but easier for traditional forensic methods.
        - **SSDs**: Faster, with complex wear leveling, making data recovery challenging.
        - **Memory Cards**: Compact, prone to data loss and corruption.
        - **Embedded Storage**: Limited access and often encrypted.

---

6. **Q**: What is the difference between live and dead acquisition?
    
    - **A**: Live acquisition captures data from a running system, whereas dead acquisition involves acquiring data from a powered-off system, typically ensuring data integrity.
7. **Q**: What is a hardware write blocker, and why is it used?
    
    - **A**: A hardware write blocker prevents modifications to data during acquisition, preserving evidence integrity.
8. **Q**: What is an imager, and what is its purpose?
    
    - **A**: An imager creates a bit-for-bit copy of a storage medium, used to preserve and analyze data without altering the original.
9. **Q**: Why are validated tools valuable in forensic acquisition?
    
    - **A**: Validated tools ensure reliability and accuracy, while unvalidated tools may risk evidence contamination or data corruption.

---

10. **Q**: Define the terms cylinder, head, and sector in CHS addressing.
    
    - **A**:
        - **Cylinder**: A vertical alignment of tracks across multiple platters.
        - **Head**: The read/write part for each platter surface.
        - **Sector**: The smallest data storage unit on a disk.
11. **Q**: What is Logical Block Addressing (LBA)?
    
    - **A**: LBA is a method of specifying the location of blocks of data on storage devices without using CHS values.
12. **Q**: What are the most common sector sizes?
    
    - **A**: Common sector sizes are 512 bytes and 4096 bytes.

---

13. **Q**: What is a partition, and why are partitions used?
    
    - **A**: A partition is a logically divided section of storage, used to separate and manage data efficiently on a storage device.
14. **Q**: What is a partition table, and what information does it contain?
    
    - **A**: A partition table records the locations, sizes, and types of partitions on a disk.
15. **Q**: Name the two most common partition table formats.
    
    - **A**: The most common formats are MBR (Master Boot Record) and GPT (GUID Partition Table).
16. **Q**: What are the main limitations of MBR that GPT overcomes?
    
    - **A**: MBR is limited to four primary partitions and 2 TB of addressable storage, whereas GPT supports larger disks and more partitions.

---

17. **Q**: What are HPA and DCO, and why are they important in forensic acquisition?
    
    - **A**: HPA (Host Protected Area) and DCO (Device Configuration Overlay) are hidden areas on a disk; they may contain user data or system settings, requiring specific methods to access during forensics.
18. **Q**: Name some items commonly stored in the HPA.
    
    - **A**: Often, firmware, diagnostic tools, and recovery data are stored in the HPA.

---

19. **Q**: How are long filenames implemented in certain filesystems?
    
    - **A**: Long filenames are implemented by using special directory entries before the actual directory entry.
20. **Q**: What are the limitations of deleted file recovery in FAT-like filesystems?
    
    - **A**: In FAT filesystems, deleted files are marked as free, and data blocks may be overwritten, making recovery more challenging.
21. **Q**: What is file carving, and when might it be used?
    
    - **A**: File carving reconstructs files based on data patterns, useful when directory structure is missing, but challenging without metadata.

---

22. **Q**: What is slack space, and why is it significant in forensic analysis?
    
    - **A**: Slack space is unused space in a data block, which may contain remnants of previous files, revealing valuable evidence.
23. **Q**: How can information end up in slack space?
    
    - **A**: When smaller files are stored, the remaining space in a block can retain data from previously deleted files.

---

24. **Q**: What are MFT entries, and what do they contain?
    
    - **A**: MFT (Master File Table) entries in NTFS store metadata for files, including attributes like file names, timestamps, and file size.
25. **Q**: Name several important fields in MFT attributes.
    
    - **A**: Fields include file name, timestamps, permissions, and data location.
26. **Q**: What are the four timestamps in $STANDARD_INFORMATION, and what do they represent?
    
    - **A**: Creation, modification, last access, and metadata modification times, representing various file interactions.
27. **Q**: Why can a file have a created timestamp later than its modified timestamp?
    
    - **A**: System or user operations may reset the created timestamp, making it appear newer than the modification timestamp.
28. **Q**: Why are multiple timestamps beneficial in forensic analysis?
    
    - **A**: They provide context on file access patterns and can help establish timelines and detect suspicious behavior.

---

29. **Q**: How can files be recovered in NTFS?
    
    - **A**: Deleted files may still reside in the MFT and be recoverable until overwritten by new data.
30. **Q**: What are the effects of sparse, compressed, and encrypted files on recovery?
    
    - **A**: Sparse and compressed files require special handling to restore data, while encrypted files may need decryption.

---

31. **Q**: What is a block group in ext4?
    
    - **A**: A block group is a collection of data blocks, inodes, and bitmap structures that manage ext4 storage efficiently.
32. **Q**: What is an inode in ext4, and what role does it play?
    
    - **A**: An inode is a data structure that stores metadata about a file, such as permissions, timestamps, and block locations.
33. **Q**: What are hard links in ext4, and why are they used?
    
    - **A**: Hard links create multiple references to the same file, allowing it to exist under different names without duplicating data.
34. **Q**: How are files deleted in ext4?
    
    - **A**: In ext4, file deletion marks inode references as free, but the actual data may remain until overwritten.

---

35. **Q**: How do block maps work in filesystems?
    
    - **A**: Block maps keep track of data blocks associated with a file, ensuring data continuity.
36. **Q**: How do extents work in filesystems?
    
    - **A**: Extents are contiguous data blocks recorded as a single entry, reducing fragmentation and improving efficiency.
37. **Q**: Which allocation models do NTFS, EXT3, EXT4, and XFS use?
    
    - **A**: NTFS and EXT3 use block allocation, while EXT4 and XFS use extents for efficiency.

---

38. **Q**: What timestamps are recorded in ext4?
    
    - **A**: Ext4 records access (atime), modification (mtime), change (ctime), and deletion times.
39. **Q**: What is the accuracy of the atime timestamp?
    
    - **A**: It generally records down to the day but can be updated based on system configurations.
40. **Q**: Which timestamps can be manipulated using the touch command?
    
    - **A**: Access, modification, and change timestamps can be altered with touch.

---

41. **Q**: What are the limitations of deleted file recovery on ext4?
    
    - **A**: Ext4 lacks native undelete support, making recovery difficult once metadata is overwritten.
42. **Q**: How can the filesystem journal in ext4 assist with file recovery?
    
    - **A**: The journal logs changes before they’re finalized, which can help recover recent modifications if needed.

---

43. **Q**: Describe the tools Sleuth Kit, Autopsy, and PhotoRec.
    - **A**:
        - **Sleuth Kit**: Command-line tool for analyzing file systems.
        - **Autopsy**: GUI-based tool for forensic analysis built on Sleuth Kit.
        - **PhotoRec**: A tool for recovering lost files, especially from storage with damaged filesystems.

---

44. **Q**: What are some of the technical challenges in filesystem forensics?
    - **A**: Challenges include handling encrypted storage, SSD wear-leveling effects, complex filesystem structures, and data recovery from fragmented or damaged storage media.
---
[Back to Top](#top)

# Module 4 - Network Forensics

1. **Q**: What is the role of network forensics in cybersecurity operations and incident response?
    
    - **A**: Network forensics analyzes network traffic to detect, investigate, and respond to security incidents, providing insights into threat sources and impacts.
2. **Q**: Give examples of how network forensics can be used in cybersecurity and incident response.
    
    - **A**: Examples include identifying unauthorized access, tracing data exfiltration paths, detecting malware communication, and monitoring for DDoS attacks.

---

3. **Q**: Name the four layers of the TCP/IP model and their purposes.
    
    - **A**:
        - **Link Layer**: Handles hardware and physical connections.
        - **Internet Layer**: Manages addressing and routing.
        - **Transport Layer**: Ensures data integrity and delivery.
        - **Application Layer**: Facilitates end-user communication and services.
4. **Q**: What are the main protocols at the Link, Internet, and Transport layers?
    
    - **A**:
        - **Link**: Ethernet, Wi-Fi.
        - **Internet**: IP (IPv4/IPv6).
        - **Transport**: TCP, UDP.

---

5. **Q**: Explain the concept of encapsulation in networking.
    
    - **A**: Encapsulation wraps data with necessary headers for each network layer, ensuring it can be transmitted and processed correctly across devices.
6. **Q**: Provide an example of encapsulation conceptually.
    
    - **A**: A web request’s data is wrapped in an HTTP header (Application layer), a TCP header (Transport layer), an IP header (Internet layer), and an Ethernet header (Link layer).

---

7. **Q**: What are the main components of an Ethernet frame?
    
    - **A**: Source MAC address, destination MAC address, EtherType, and data payload.
8. **Q**: What is a MAC address, and what is the OUI portion?
    
    - **A**: A MAC address is a unique identifier for a network interface, with the OUI (Organizationally Unique Identifier) identifying the manufacturer.

---

9. **Q**: Explain the purpose of the U/L and I/G bits in a MAC address.
    
    - **A**: U/L indicates whether the address is universally or locally administered, while I/G denotes if the address is individual or group-based.
10. **Q**: Why is MAC address randomization used, and how can it be recognized?
    
    - **A**: MAC randomization protects user privacy by changing the MAC address, recognized by its frequent changes or non-standard OUI values.

---

11. **Q**: What is the TTL field, and how is it used?
    
    - **A**: TTL (Time to Live) prevents packets from circulating indefinitely by decrementing with each hop and discarding the packet when it reaches zero.
12. **Q**: Describe the concept of fragmentation.
    
    - **A**: Fragmentation splits large data packets into smaller ones to fit within the MTU (Maximum Transmission Unit) of network links.

---

13. **Q**: Explain CIDR notation and the concept of a prefix.
    
    - **A**: CIDR notation represents an IP range, with the prefix indicating the number of fixed bits defining the network portion of the address.
14. **Q**: Translate an IP address between dotted quad and binary formats.
    
    - **A**: For example, `192.168.1.1` in binary is `11000000.10101000.00000001.00000001`.

---

15. **Q**: What are loopback, link-local, multicast, private, and 6to4 relay addresses?
    
    - **A**: Loopback (127.0.0.1), link-local (169.254.x.x), multicast (224.x.x.x), private (e.g., 192.168.x.x), and 6to4 relay (2002::/16) addresses are special-purpose IP addresses.
16. **Q**: Explain the ARP protocol and what gratuitous and proxy ARP are.
    
    - **A**: ARP maps IP to MAC addresses. Gratuitous ARP announces an IP change, while proxy ARP responds to ARP requests on behalf of another device.

---

17. **Q**: What is IPv6, and why has its adoption been slow?
    
    - **A**: IPv6 is a new IP addressing system designed for address space expansion. Adoption has been slow due to NAT and limited vendor support.
18. **Q**: What is IPv6 autoconfiguration, and how does it relate to DHCP?
    
    - **A**: IPv6 autoconfiguration (SLAAC) allows devices to self-assign addresses; DHCPv6 can also assign IPv6 addresses in managed networks.

---

19. **Q**: Describe the router discovery protocol and its potential abuse.
    
    - **A**: The protocol helps devices find local routers. Attackers could manipulate this to redirect traffic in man-in-the-middle attacks.
20. **Q**: What is the Neighbour Discovery Protocol (NDP), and how can it be abused?
    
    - **A**: NDP uses ICMPv6 to discover neighbors. Attackers can hijack traffic by spoofing neighbor responses, redirecting data.

---

21. **Q**: Explain the concept of ports and four-tuples.
    
    - **A**: Ports separate communication channels on devices, with four-tuples (local address, remote address, local port, remote port) uniquely identifying connections.
22. **Q**: What is the three-way handshake?
    
    - **A**: It’s a TCP connection process where SYN, SYN-ACK, and ACK messages are exchanged to establish a connection.

---

23. **Q**: Explain source and destination NAT and its challenges in DFIR.
    
    - **A**: NAT translates IPs for traffic routing, masking original IPs, which can obscure source information in forensic investigations.
24. **Q**: What is port mirroring, and when is it appropriate?
    
    - **A**: Port mirroring duplicates traffic to another port for monitoring, suitable for analyzing network activity without disrupting operations.

---

25. **Q**: What is promiscuous mode, and when is it useful in capturing packets?
    
    - **A**: Promiscuous mode allows capturing all network packets, helpful in passive monitoring but can pose security risks if misused.
26. **Q**: What is eBPF, and why is it efficient?
    
    - **A**: eBPF allows high-speed packet processing within the kernel, improving performance and flexibility in network monitoring.

---

27. **Q**: Explain a full packet capture and its main challenges.
    
    - **A**: Full packet capture records all packet data but requires significant storage and processing power, especially on high-speed networks.
28. **Q**: What is a network flow, and how does it differ from full packet capture?
    
    - **A**: Network flow records metadata like IPs and ports, reducing storage needs while allowing high-level traffic analysis.

---

29. **Q**: Describe the challenges in high-performance networks and how they can be mitigated.
    
    - **A**: High throughput may overwhelm analysis tools. Solutions include filtering, load balancing, and using specialized hardware.
30. **Q**: What is hypothesis testing and hunting in network forensics?
    
    - **A**: Hypothesis testing involves formulating and testing theories about network traffic patterns, while hunting proactively searches for threats.

---

31. **Q**: What is a SYN flood, and how can it be mitigated?
    
    - **A**: A SYN flood is a DDoS attack overloading a server with connection requests; SYN cookies can mitigate it by managing connection states.
32. **Q**: Describe a reflected DDoS attack.
    
    - **A**: A reflected DDoS uses third-party servers to amplify traffic against a target, with commonly abused services like DNS, NTP, and SSDP.

---

33. **Q**: What are some signs of ARP and DNS spoofing in network traffic?
    
    - **A**: ARP spoofing may show duplicate IPs with different MAC addresses, while DNS spoofing can reveal unexpected IP responses for known domains.
34. **Q**: List some current challenges in network forensics.
    
    - **A**: Challenges include encrypted traffic, NAT obscuring sources, high-speed traffic analysis, and identifying anomalous patterns among large datasets.
---
[Back to Top](#top)

# Module 5 - Logs and Timeline

1. **Q**: What is a log and a log record (or entry)?
    
    - **A**: A log is a recorded sequence of events or activities on a system, with each log entry capturing a specific event’s details, such as timestamp and event type.
2. **Q**: What are some uses for logs, including in DFIR?
    
    - **A**: Logs help in auditing, monitoring security, troubleshooting issues, and are essential in DFIR for reconstructing events and identifying malicious activity.
3. **Q**: Why should logs be collected at a central point, and what are the consequences if they aren’t?
    
    - **A**: Central collection enables comprehensive analysis and cross-referencing; without it, incidents may be harder to detect or reconstruct due to fragmented data.
4. **Q**: Why is time synchronization essential in logs, and what are the consequences if it’s not maintained?
    
    - **A**: Synchronization ensures consistency across logs; without it, timelines may be inaccurate, complicating incident analysis and evidence correlation.
5. **Q**: Why is log normalization important, and what happens if logs aren’t normalized?
    
    - **A**: Normalization standardizes log formats, enabling effective analysis; without it, comparing and searching logs from different sources becomes challenging.
6. **Q**: Why is log integrity crucial, and what are the consequences if it’s compromised?
    
    - **A**: Log integrity ensures the accuracy of recorded data; compromised integrity can lead to loss of evidence or incorrect conclusions in investigations.

---

7. **Q**: Name and briefly describe several types of logs.
    
    - **A**: Types include system logs (OS-level events), application logs (app-specific events), security logs (access control), and network logs (traffic activity).
8. **Q**: Where can each type of log typically be found, and what information do they provide in DFIR?
    
    - **A**: System logs are in the OS (e.g., Event Viewer in Windows); application logs are in app directories; security logs track access events, providing insights into potential breaches.

---

9. **Q**: What is the Windows Event Log?
    
    - **A**: It’s a log service in Windows that records system, security, and application events for monitoring and analysis.
10. **Q**: What are the Event ID, Computer name, and User SID fields in Windows Event Logs?
    
    - **A**:
        - **Event ID**: Unique identifier for each type of event.
        - **Computer name**: Identifies the computer where the event occurred.
        - **User SID**: Identifies the user associated with the event.
11. **Q**: Why is analyzing only main Windows logs insufficient for incident response?
    
    - **A**: Main logs may miss critical app-specific or low-level system events, leaving gaps in incident analysis.

---

12. **Q**: What are the two main Linux logging methods?
    
    - **A**: syslog and systemd journal.
13. **Q**: What are some differences between syslog and the systemd journal?
    
    - **A**: syslog is widely supported and plain text, while systemd journal includes binary data and structured entries, offering more detailed logging.
14. **Q**: How do events end up in a local log file, journal, or on a remote log server?
    
    - **A**: Events are sent by system services or applications, stored locally or forwarded to a remote server based on configuration.

---

15. **Q**: List the fields in an RFC 3164 syslog message.
    
    - **A**: Timestamp, host, facility, level, application, process ID, and message content.
16. **Q**: Explain the limitations of RFC 3164 timestamps.
    
    - **A**: RFC 3164 does not include a year or time zone, complicating correlation across different time zones or with events in other years.
17. **Q**: What does a typical RFC 3164 syslog message contain?
    
    - **A**: It contains a header (timestamp and host) and a message (event details).

---

18. **Q**: What is the systemd journal facility?
    
    - **A**: The systemd journal logs events for systemd-managed systems, providing structured and more detailed data than syslog.
19. **Q**: What additional information does the systemd journal collect?
    
    - **A**: It includes structured metadata, system state, and binary data, enhancing troubleshooting and analysis.
20. **Q**: How can systemd journald messages be forwarded to a remote collector?
    
    - **A**: Using configuration options in journald to send logs to a central syslog server or directly to another systemd journal.

---

21. **Q**: How can you extract fields such as timestamp, host, facility, and message from a syslog message?
    
    - **A**: By parsing the message structure based on RFC standards to retrieve each field's position and format.
22. **Q**: How would you interpret a sudo log message?
    
    - **A**: A sudo log shows command executions with elevated privileges, providing details on the user, command, and success or failure status.

---

23. **Q**: List several types of network logs and the information they contain.
    
    - **A**: Types include router logs (traffic data), firewall logs (blocked/allowed traffic), and DNS logs (domain queries).
24. **Q**: What information can be found in firewall logs?
    
    - **A**: Information on source and destination IPs, protocols, action taken (allow/deny), and rule names or IDs.

---

25. **Q**: What are the two types of logs typically produced by a web server?
    
    - **A**: Access logs (details of each request) and error logs (errors encountered).
26. **Q**: How do virtual hosts affect web server logging?
    
    - **A**: Logs can be separated by virtual host, allowing tracking of specific domains or sites hosted on the same server.
27. **Q**: What fields should you look for in a web server log to detect reconnaissance?
    
    - **A**: Fields like unusual user agents, excessive 404 errors, or requests to uncommon endpoints can indicate reconnaissance.

---

28. **Q**: What is the importance of clock synchronization in DFIR?
    
    - **A**: It ensures consistency across logs, crucial for accurate event correlation in investigations.
29. **Q**: What are the issues related to time zones in DFIR?
    
    - **A**: Variances in time zones can lead to misalignment in event timing, affecting the accuracy of timelines.
30. **Q**: What is the most common method for synchronizing clocks?
    
    - **A**: NTP (Network Time Protocol).

---

31. **Q**: What is a timeline in DFIR?
    
    - **A**: A sequence of events generated from log data, used to reconstruct incident activities.
32. **Q**: What questions can be answered through timeline analysis?
    
    - **A**: Questions about event timing, sequences, duration of attacks, and affected assets can be answered.

---

33. **Q**: Name several types of data collected in timelines.
    
    - **A**: File access times, network connection timestamps, system events, and application logs.
34. **Q**: What is a targeted timeline analysis approach?
    
    - **A**: It focuses on specific events or indicators, filtering out irrelevant data for a concise timeline.
35. **Q**: What is a comprehensive or “kitchen sink” timeline approach?
    
    - **A**: It includes all events to avoid missing details but may require more time and resources to analyze.

---

36. **Q**: What is the difference between automated and manual timeline creation?
    
    - **A**: Automated creation uses tools for efficiency, while manual creation allows deeper inspection, though it’s time-intensive.
37. **Q**: What is Plaso, and what is it used for?
    
    - **A**: Plaso is a tool for creating timelines by parsing and extracting data from logs, useful in forensic analysis.

---

38. **Q**: What is correlation in log analysis, and how is it used?
    
    - **A**: Correlation identifies relationships between events across logs, helping to uncover patterns or sequences of malicious activity.
39. **Q**: Provide examples of correlations used in investigations.
    
    - **A**: Examples include matching login times with network access logs or connecting process start times with file modification events.

---

40. **Q**: What are some common reasons for gaps in timelines?
    
    - **A**: Reasons include missed or deleted logs, time synchronization issues, or data from non-synchronized sources.
41. **Q**: What should an analyst do when faced with a gap in the timeline?
    
    - **A**: Investigate the missing data, correlate with other logs, and look for evidence of data tampering or loss.

---

42. **Q**: What are patterns in log analysis, and why are they useful?
    
    - **A**: Patterns identify repeated sequences or behaviors, aiding in detecting normal vs. anomalous activities.
43. **Q**: Give examples of patterns that may occur in logs.
    
    - **A**: Examples include failed logins before a successful login, repeated access to specific files, or data exfiltration patterns.

---

44. **Q**: What is Timesketch, and what is it used for?
    
    - **A**: Timesketch is a tool for visualizing and analyzing timelines, offering features like annotation, filtering, and collaboration.
45. **Q**: What is a sigma rule, and how is it used?
    
    - **A**: Sigma rules define patterns for identifying suspicious events across different log formats, commonly used for automated detection.
---
[Back to Top](#top)

# Module 6 - Local Systems Forensics

1. **Q**: What are the five high-level questions in local systems forensics?
    
    - **A**:
        1. Who was involved?
        2. What actions took place?
        3. When did they happen?
        4. Where were they done?
        5. Why did they happen?
2. **Q**: What types of evidence are relevant to answer each forensic question?
    
    - **A**: User account details, system logs, timestamps, network logs, and file metadata are often key to answering the five high-level questions.

---

3. **Q**: What is the difference between kernel and user space?
    
    - **A**: Kernel space is for core OS processes with higher privileges, while user space is for user applications with limited access to hardware.
4. **Q**: What is a security principal?
    
    - **A**: A security principal is an entity (user, group, or device) with a unique identity in a security system, like a user account or service.
5. **Q**: What is an access token?
    
    - **A**: An access token is a data structure in Windows that holds a user’s identity and permissions for accessing system resources.
6. **Q**: What are object permissions in Windows?
    
    - **A**: Object permissions control access rights to files, folders, and other system resources based on the user’s identity and privileges.
7. **Q**: What are privileges in Windows?
    
    - **A**: Privileges are special rights assigned to user accounts to perform administrative or restricted tasks on the system.

---

8. **Q**: What is the MIC mechanism in Windows, and why does it exist?
    
    - **A**: MIC (Mandatory Integrity Control) assigns integrity levels to processes and objects, helping control access and prevent privilege escalation.
9. **Q**: What role does UAC play in Windows security?
    
    - **A**: User Account Control (UAC) prompts users to approve administrative actions, reducing the risk of unauthorized system modifications.
10. **Q**: What happens if UAC is bypassed?
    
    - **A**: Bypassing UAC allows attackers to perform administrative actions without user consent, potentially compromising system security.

---

11. **Q**: What is an Active Directory Domain?
    
    - **A**: It’s a central directory of user and computer accounts for network management, mainly used in Windows environments.
12. **Q**: What are the consequences if an attacker gains control of the domain controller?
    
    - **A**: Control over the domain controller enables an attacker to manage or impersonate any user or device within the network.

---

13. **Q**: What is the Windows Registry?
    
    - **A**: The Windows Registry is a hierarchical database storing configuration settings, user preferences, and application information.
14. **Q**: What is the Windows SAM, and why might an attacker access it?
    
    - **A**: The Security Account Manager (SAM) database stores user passwords; attackers target it to retrieve credentials for system access.

---

15. **Q**: What is a SID, and what is its role in Windows security?
    
    - **A**: A Security Identifier (SID) uniquely identifies user accounts and groups, assigning permissions and access rights.
16. **Q**: What is a RID?
    
    - **A**: A Relative Identifier (RID) is part of a SID, uniquely identifying a user or group within a specific domain or system.

---

17. **Q**: What is ShimCache, and what information does it store?
    
    - **A**: ShimCache records executables that were run on a system, helping investigators trace program execution history.
18. **Q**: What is the purpose of Prefetch files in Windows?
    
    - **A**: Prefetch files speed up application launch times and store data on recent program executions, aiding in forensic analysis.
19. **Q**: Where can you find a SHA1 hash of executables in Windows?
    
    - **A**: SHA1 hashes of executables are found in the AmCache and ShimCache data, useful for identifying and verifying program integrity.
20. **Q**: What is a jump list, and what information does it contain?
    
    - **A**: A jump list stores recent files or actions for quick access in Windows, providing forensic clues on user activity.

---

21. **Q**: What information can be found in the USBSTOR and USB registry keys?
    
    - **A**: They log USB devices connected to the system, including device IDs, dates, and connection details.
22. **Q**: How can you determine if a user accessed a particular USB storage device?
    
    - **A**: By analyzing the USBSTOR keys and timestamps associated with the device in the Registry.

---

23. **Q**: Name some typical persistence mechanisms used by attackers.
    
    - **A**: Scheduled tasks, registry modifications, autorun files, and malicious services are common methods for persistence.
24. **Q**: Who is Eric Zimmerman, and what tools is he known for?
    
    - **A**: Eric Zimmerman is known for developing free, specialized forensic tools, such as Registry Explorer and Timeline Explorer.

---

25. **Q**: What is the VFS subsystem in Linux?
    
    - **A**: The Virtual File System (VFS) abstracts filesystem operations, allowing different filesystems to be accessed uniformly by applications.
26. **Q**: Explain the phrase “everything is a file” in Linux.
    
    - **A**: In Linux, most entities, including devices and processes, are treated as files, simplifying access and management.
27. **Q**: What is a process, and what is a process ID?
    
    - **A**: A process is an instance of a running program, and a process ID uniquely identifies it on the system.

---

28. **Q**: What is the significance of user ID 0 in Linux?
    
    - **A**: User ID 0 is the root user, with unrestricted access and administrative privileges.
29. **Q**: What are Linux permissions and Access Control Lists (ACLs)?
    
    - **A**: Permissions control access to files and directories, while ACLs offer more granular permissions beyond the standard user-group-other model.
30. **Q**: What is an LSM, and name a model available in Linux.
    
    - **A**: Linux Security Module (LSM) enforces security policies. SELinux is a commonly used LSM for mandatory access control.

---

31. **Q**: What is the purpose of wtmp and btmp files?
    
    - **A**: **wtmp** logs successful logins and logouts, while **btmp** logs failed login attempts, useful for tracking access.
32. **Q**: What is the significance of an empty or truncated wtmp/btmp file?
    
    - **A**: It may indicate tampering to cover up unauthorized access or an attempt to hide login activity.

---

33. **Q**: How might attackers modify users to establish persistence?
    
    - **A**: They may create backdoor accounts, elevate privileges, or modify existing accounts in system files, such as `/etc/passwd`.
34. **Q**: What is a cron job, and how can it be used for persistence?
    
    - **A**: A cron job schedules recurring tasks, which attackers can use to execute malicious scripts regularly.

---

35. **Q**: How do systemd unit files enable persistence?
    
    - **A**: Attackers can modify or create unit files to start malicious services or processes on boot.
36. **Q**: Explain how attackers could use shell init files for persistence.
    
    - **A**: Shell init files (e.g., `.bashrc`) can be modified to execute malicious commands each time a user logs in.

---

37. **Q**: What is setuid/setgid, and how can attackers exploit it?
    
    - **A**: **setuid/setgid** attributes allow programs to run with elevated privileges, which attackers exploit to gain unauthorized access.
38. **Q**: What are some other Linux persistence mechanisms?
    
    - **A**: Examples include altering `/etc/rc.local`, modifying startup scripts, or installing backdoor programs.

---

39. **Q**: What is the purpose of the `/proc` filesystem in Linux?
    
    - **A**: `/proc` is a virtual filesystem providing process and system information, useful for monitoring active processes and system status.
40. **Q**: What information can be found in `/proc` for individual processes?
    
    - **A**: Data on process IDs, memory usage, open file descriptors, and network connections are available in `/proc`.

---

41. **Q**: What is a sysctl, and where is it found?
    
    - **A**: A sysctl is a parameter for system configuration, usually located in `/proc/sys`, allowing control over kernel settings.
42. **Q**: What are loop devices, and what are they used for?
    
    - **A**: Loop devices allow files to be mounted as if they were physical disks, commonly used for disk image mounting.
43. **Q**: What are `/dev/null` and `/dev/zero` used for?
    
    - **A**: **/dev/null** discards data, while **/dev/zero** provides a stream of zero bytes, both commonly used for testing or managing I/O operations.

---

44. **Q**: Name locations for nonpersistent temporary file storage in Linux.
    
    - **A**: **/tmp** and **/var/tmp** are directories for temporary files, cleared periodically by the system.
45. **Q**: What are world-writable directories in Linux?
    
    - **A**: Common examples include **/tmp** and **/var/tmp**, allowing any user to read and write files within these directories.
