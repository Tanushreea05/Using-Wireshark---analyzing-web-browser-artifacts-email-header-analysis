# Using-Wireshark---analyzing-web-browser-artifacts-email-header-analysis
## AIM:
To use Wireshark to analyze web browser activities and inspect email headers from captured network traffic.

## DESIGN STEPS:
### Step 1:
Launch Wireshark and start capturing traffic on the appropriate network interface.

### Step 2:
Use filters like http, dns, or tcp.port == 80 to monitor web browser artifacts such as visited URLs, cookies, and user-agent strings.

### Step 3:
Apply filters like smtp, pop, or imap to locate and analyze email header details (e.g., sender, receiver, subject) from email communications.

## PROGRAM:
Wireshark Web and Email Traffic Filtering Steps

## OUTPUT:
**A. Capturing Traffic in Wireshark**

1. Open Wireshark and start capturing on the active interface (Wi-
Fi/Ethernet).

2. Perform activities like opening a website or sending an email through a
client (e.g., Gmail via browser or Thunderbird).
3. Stop the capture once done.

<img width="1917" height="1079" alt="image" src="https://github.com/user-attachments/assets/bd3b0d05-0ca7-4d76-a858-33e075572e7d" />

**Analyze DNS Queries:**
o Filter: dns

o Reveal domains the browser tried to resolve.

<img width="1916" height="1076" alt="image" src="https://github.com/user-attachments/assets/1780ce3e-fdac-42a3-a47a-89a9d9ccfe7d" />


**Email Header Analysis**

1. Apply relevant filters:
2. 
o For POP3: tcp.port == 110

o For SMTP: tcp.port == 25 or 587

o For IMAP: tcp.port == 143 or 993

4. Locate email data:
5. 
o Look for SMTP packets to see sender/receiver email addresses.

o Use "Follow TCP Stream" to view the full email headers and body if unencrypted.

**Extract Email Header Fields:**

o Analyze From, To, Subject, Date, Message-ID, and relay servers used in sending the email.

<img width="1906" height="1077" alt="image" src="https://github.com/user-attachments/assets/f908dc05-120a-42a3-a13c-bcfaf7c8a237" />


<img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/06ecdb66-73e3-4a6c-a865-3a5a72b7e0ed" />

<img width="1863" height="693" alt="image" src="https://github.com/user-attachments/assets/a72ce999-630e-479e-a3a9-945175d9baa2" />

<img width="1919" height="1073" alt="image" src="https://github.com/user-attachments/assets/06a36a90-521b-47da-8ce5-e8b93f0768d2" />

## RESULT:
Web browser artifacts and email headers were successfully analyzed using Wireshark
