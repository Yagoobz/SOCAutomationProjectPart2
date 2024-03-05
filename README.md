<h2>SOC Automation Lab Part 2 </h2>

<h3>Objectives</h3>
- Install Applications 
<br />
- Install Virtual Machines
<br />
<br />

To begin, I'll need to launch a Windows 10 instance, which I'll set up on AWS. Once the cloud machine is up and running, I proceed to install Sysmon by downloading it from a Windows webpage and configuring it using a file obtained from GitHub. 
<br />
<img src="https://github.com/Yagoobz/https-github.com-Yagoobz-SOCAutomationLabPart2/assets/145611184/292bf34a-5175-4b19-a530-6d82bfbcb8b4" height="30%" width="70%" alt="Disk Sanitization Steps"/>

I unzip all the files from the Sysmon folder, then open Windows PowerShell with administrator privileges and navigate to the appropriate directory using the "cd" command. Once there, I execute the command ".\sysmon64.exe -i .\sysmonconfig.xml" to install Sysmon. To confirm the installation, I check the services, and indeed, Sysmon is listed there. Success! 
<br />
<img src="https://github.com/Yagoobz/SOCAutomationLabPart2/assets/145611184/a8a2cd0e-6787-46d2-b916-9fd62c527dfc" height="30%" width="70%" alt="Disk Sanitization Steps"/>

Following that, I proceed to build my Wazuh server on DigitalOcean. Once the server is set up, I configure a firewall to block external scanners and restrict access solely to myself. Then, using the Apple Terminal, I SSH into the Wazuh server, successfully gaining access. (Even though I have a powerful Windows PC Desktop, I still prefer using Apple devices)
<br />
<img src="https://github.com/Yagoobz/SOCAutomationLabPart2/assets/145611184/ea3888a5-eac4-430b-9369-a50fbccc05e2" height="30%" width="70%" alt="Disk Sanitization Steps"/>

Following the update and upgrade process, I begin installing Wazuh using a curl command obtained from their website. After a brief wait, the installation completes, and I make note of the username and password provided for accessing the Wazuh dashboard. Using the public IP address of the Wazuh server, I access the webpage via HTTPS, where I input the username and password, successfully gaining entry to the dashboard.
<br />
<img src="https://github.com/Yagoobz/SOCAutomationLabPart2/assets/145611184/cbf21b1c-4b5f-4576-9a3f-71b3e1107373" height="30%" width="70%" alt="Disk Sanitization Steps"/>

Next, I proceed to install TheHive, following a similar process to installing Wazuh. Using DigitalOcean, I create the server and configure a firewall, then SSH into the server from the Apple Terminal. The installation of TheHive requires three components: Java, Cassandra, and Elasticsearch, all of which I obtained from GitHub. After installing the prerequisites, I proceed to install each component, a process that typically takes about ten minutes to complete.
<br />
<img src="https://github.com/Yagoobz/SOCAutomationLabPart2/assets/145611184/9d2177fb-fd66-436e-85b9-51fc797e54e9" height="30%" width="70%" alt="Disk Sanitization Steps"/>
