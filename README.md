SINCERE MALWARE - EDUCATIONAL PROOF OF CONCEPT

WARNING: FOR EDUCATIONAL AND RESEARCH PURPOSES ONLY
This is functional software. Use with extreme caution.

This repository contains a proof-of-concept malware created strictly for educational cybersecurity research. It demonstrates real malware techniques in a controlled, instructional context.

CRITICAL DISCLAIMER

This software is functional and can cause damage.
The author (@lockedlocal) does not condone, encourage, or support any illegal or unauthorized activities. This project exists solely to:
- Educate about real malware behavior and attack chains
- Help security researchers analyze and understand threats
- Serve as a controlled study tool in isolated environments

By accessing this repository, you acknowledge and agree that you will:
- Use this code ONLY in isolated, controlled environments you fully own (virtual machines, sandboxes, air-gapped systems)
- NEVER deploy it against any system without explicit, written authorization
- Accept full legal and ethical responsibility for any consequences of misuse
- Comply with all applicable laws in your jurisdiction

TECHNICAL OVERVIEW: ATTACK CHAIN

This proof-of-concept demonstrates a multi-stage attack:

1. Initial Execution & Persistence: Executes from a removable drive (simulated USB attack vector).
2. User Disruption:
   - Spams the terminal with the message: "you have been spotted".
   - Opens multiple windows to obstruct the user interface and prevent closure.
3. Psychological Impact & System Clutter:
   - Generates over 1000 .txt files with a spoofed ransom message.
4. System Degradation: Intentionally consumes resources to induce severe lag.
5. System Crash & Data Destruction:
   - Terminates the critical svchost.exe process to trigger a system crash (BSOD simulation).
   - Deploys a secondary payload scheduled to delete the Master Boot Record (MBR), rendering the system unbootable.

PAYLOAD MESSAGE
The generated .txt files contain this text:

Hello, your computer has been infected
with a dangerous virus called 'sincere'.
All your data has been transferred to the server.
The virus developer is @lockedlocal (Telegram).
Your computer will die in the next 10 minutes. Good luck!
You have been spotted.

MANDATORY SAFE TESTING ENVIRONMENT

TEST ONLY IN THE FOLLOWING ISOLATED ENVIRONMENTS:
- VirtualBox / VMware / Hyper-V (WITH NETWORKING DISABLED AND SNAPSHOTS TAKEN)
- Windows Sandbox
- Dedicated, air-gapped physical hardware meant for testing
- Docker containers with strict resource and capability limits

CRITICAL SAFETY STEPS:
1. Disable all shared folders between host and VM.
2. Use NAT or Host-Only networking, never Bridged.
3. Take a full snapshot of the clean VM state before execution.
4. Assume the testing environment will be destroyed.

EDUCATIONAL VALUE FOR DEFENDERS

Analyzing this PoC helps understand and defend against:
- Behavioral Patterns: Resource exhaustion, process spawning, file flooding.
- Persistence Mechanisms: Autostart entry modification.
- Destructive Payloads: MBR corruption and critical process termination.
- Social Engineering: Use of threatening messages to cause panic.

FOR LEGITIMATE CYBERSECURITY LEARNING

To translate this knowledge into defensive skills, explore:
- Malware Analysis: Practical courses on platforms like TryHackMe or HackTheBox.
- Incident Response: Frameworks like NIST SP 800-61.
- Digital Forensics: Tools like Autopsy, Volatility, FTK Imager.
- Ethical Hacking: Certifications like OSCP (Offensive Security).

LEGAL & ETHICAL NOTICE

UNAUTHORIZED USE OF THIS SOFTWARE IS A SERIOUS CRIME.
- It violates laws such as the Computer Fraud and Abuse Act (CFAA) in the US and similar legislation worldwide.
- Penalties include fines, imprisonment, and a permanent criminal record.
- It causes real harm and financial damage to victims.

The author (@lockedlocal) explicitly states:
- This code is published for academic study only.
- I bear no responsibility for any misuse.
- I will fully cooperate with legal authorities investigating any unauthorized use.
- No support will be provided for deployment outside of lawful, controlled research.

LICENSE

This project is licensed under a strict, custom license.

Core Conditions:
- Attribution Required: Must credit @lockedlocal (https://github.com/occuredfree).
- Non-Commercial Use Only.
- Absolutely No Malicious Use Allowed.
- No Warranty: Provided "AS IS" for study at your own risk.

CONTACT

For educational discussion only regarding this PoC:
- GitHub: https://github.com/occuredfree

Last Updated: 2025 | Status: Proof-of-Concept | Purpose: Educational Research""")
