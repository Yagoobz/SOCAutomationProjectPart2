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
<img src="..." height="30%" width="70%" alt="Disk Sanitization Steps"/>
