# HONEYPOT 🍯🐝
A project for creating a honeypot/ SIEM (Security Information and Event Management) in Microsoft Azure Platform.<br><br>
<b>Project Purpose:</b><br> Analyzing Attacks From all over the world, Gather intelligence about adversaries’ identity, methods, and motivations.

<h3>MAP VIEW</h3>
<img src="Screenshot 2024-07-03 085445.png"><br>

<p>SIEM is a solution that helps organizations detect, analyze, and respond to security threats before they harm business operations.</p>
<p>Honeypots are cybersecurity mechanisms intentionally designed to look like legitimate targets (e.g., software applications, servers, or network components). Honeypots resemble attractive targets (e.g., payment gateways, databases, sensitive information).</p>

<h3>Steps to set up the SIEM</h3>

<ol>
  <li><h5>CREATE VIRTUAL MACHINE</h5></li>
  <ul><li>In my case I created a Windows 10 Pro Virtual Machine</li></ul><br>
  <img src="Screenshot 2024-07-01 154019.png"><br>

  <li><h5>CREATE LOG ANALYTICS WORKSPACE</h5></li>
  <img src="Screenshot 2024-07-01 160734.png"><br>

  <li><h5>SET UP DATA COLLECTION AND DEFENDER PLANS IN AZURE SECURITY CENTER</h5></li><br>
  <ul><li>Turn off the SQL services in Defender Plans</li></ul><br>
  <img src="Screenshot 2024-07-03 074437.png"><br>

  <li><h5>THEN GO TO LOG ANALYTICS AND CONNCET THE VM</li>
  <img src="Screenshot 2024-07-03 075020.png"><br>

  <li><h5>CREATE MICROSOFT SENTINAL</li>
  <img src="Screenshot 2024-07-01 162141.png"><br>

  <li><h5>LOG IN TO THE VM USING PUBLIC IP</li>
  <img src="Screenshot 2024-07-01 162538.png"><br>

  <li><h5>ANALYZE THE EVENT VIEWER</li>
  <img src="Screenshot 2024-07-01 164501.png"><br>

  <li><h5>TURN OFF ALL FIREWALL SETTINGS TO MAKE IT VULNERABLE</li>
  <img src="Screenshot 2024-07-03 082519.png"><br>

  <li><h5>OPEN THE POWERSHELL ISE</li>
  <ul><li>Create ot get the script from <a href = "https://github.com/joshmadakor1/Sentinel-Lab/blob/main/Custom_Security_Log_Exporter.ps1">here</a> </li>
  <li>Credits for the Script : <a href="https://github.com/AnastasiaCoskuner">@joshmadakor1</a> </li>
  <li>Now run the script and check it with Windows Event Viewer that the script is working correctly</li><br>
  </ul>
  <img src="Screenshot 2024-07-03 070735.png"><br>

  <li><h5>CREATE THE LOG FILE AND UPLOAD IT</li>
    <ul>
      <li>Go to the Log Analytics and now Create Custom tables or Write a query to Display values That you need to extract from the table.</li>
      <li>After you uploaded the file wait for some time to actually load it on Azure this will take some time.</li>
    </ul><br>
  <img src="Screenshot 2024-07-03 073050.png"><br>

  <li><h5>CREATE A WORKBOOK</li>
  <img src="Screenshot 2024-07-03 073050.png"><br>
</ol>
