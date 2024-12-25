<h1>Network Traffic Analysis & Decryption with Logging Tool</h1>


<h2>Description</h2>

This project consists of a set of Linux scripts designed for network traffic analysis and decryption. The utility leverages TCPDump to capture TCP traffic and provides automated tools for cyber forensic investigations. The scripts enable users to capture network packets, organize and parse the data, and decrypt the content of the captured traffic for further analysis. This project simplifies the process of extracting meaningful insights from network traffic while showcasing expertise in scripting, forensics, and decryption techniques.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Bash</b> 
- <b>TCPDump</b>
- <b>Wireshark</b>
- <b>Tshark</b>
   
<h2>Environments Used </h2>

- <b>Operating System: Kali Linux</b> (via VirtualBox on Windows 11 22H2)
- <b>Network Environment: Local traffic capture from Google searches</b>
- <b>Development/Testing Tools: Visual Studio Code, VirtualBox</b>

<h2>Program walk-through:</h2>

<p align="center">
In this step, I used the tcpdump command to capture and analyze network traffic to and from google.com. By running sudo tcpdump -c 10 -#XXtttt host google.com, I captured 10 packets, ensuring the data was displayed in both hexadecimal and ASCII formats for detailed examination. The use of high-precision timestamps and packet counters provided clear tracking of the captured traffic, offering a structured view of the interactions with google.com. : <br/>
<img src="https://imgur.com/NIIYMZw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I used tcpdump to capture traffic to and from google.com and saved it to a file named capture.cpap using the -w option. To automate logging, I created a script watchdog.sh that monitored traffic and managed sequential dump files, with each file limited to 100 bytes in size using the -C 1 flag. The script ensured efficient and organized logging of captured data. :  <br/>
<img src="https://imgur.com/xrM9S7u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I tested the functionality of watchdog.sh to ensure it effectively captured and logged network traffic as intended. This involved running the script, verifying that sequential dump files were created correctly based on the specified size limit, and confirming the captured data was accurate and complete. : <br/>
<img src="https://imgur.com/lcp5j95.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I used Wireshark to open and analyze the captured packets in greater detail, utilizing its advanced filtering and highlighting features to identify and examine any encrypted data collected by TCPdump. :  <br/>
<img src="https://imgur.com/DTF5YC3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I captured the private key used by the browser during an SSL handshake by setting the SSLKEYLOGFILE environment variable to specify the file path for storing private keys. This allowed the browser to log the keys used in SSL encryption. I then switched the host from google.com to nhs.uk to generate more traffic and encrypted data for capture, providing a richer dataset for analysis. :  <br/>
<img src="https://imgur.com/xZVSOJg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
