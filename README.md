<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 11</b> (21H2)

<h2>List of Prerequisites</h2> 

1. IIS (Internet Information Services) Configuration on Windows 11
Project Overview, including enabling CGI support required by web-based applications such as osTicket.
It illustrates how IIS interacts with a web browser (e.g., Microsoft Edge) and how to use it for hosting, testing, and development in a local environment.

2. Web Platform Installer -  Helpful tool to install IIS, PHP, and MySQL easily.

3. Install Microsoft Visual C++ Redistributable on Windows 11 Required, because PHP or MySQL components depend on it.


 
<img width="1793" height="928" alt="image" src="https://github.com/user-attachments/assets/86c616bb-66c2-4744-bcd6-1035a770468e" />

Here’s the diagram image showing how IIS (Internet Information Services) interacts with the web browser (Microsoft Edge) on Windows 11, followed by an illustrated step-by-step demonstration of the configuration setup.
First, I had to enable IIS in Windows with CGI — this is required as a dependency for osTicket, which runs under the World Wide Web Services (WWWS) component.
To do that:
1.Open the Windows Features dialog box by pressing Windows + R, typing optional features, and pressing Enter.
2.In the list that appears, scroll down to Internet Information Services (IIS) and check the box ✅ next to it.
3.Click the “+” sign to expand and view sub-features such as Web Management Tools and World Wide Web Services.
4.Under World Wide Web Services, click the “+” sign again to expand Application Development Features, then scroll down and check the box ✅ next to CGI.
5.Click OK, and Windows will begin installing the required files (this usually takes 1–2 minutes). When the installation is complete, click Close.
Next, open your preferred web browser (Edge, Chrome, or Firefox). Type your system’s IP address or simply type http://localhost
 in the address bar, then press Enter or refresh the page. You should now see the IIS Welcome Page, which looks like the diagram shown here.

After activation, IIS automatically creates a default web folder, and anything you place in this folder can be accessed through your browser. To do that:
1.Open Notepad and run it as Administrator.
2. Inside Notepad, click File → Open, then navigate to your Windows (C:) drive.
3. Open the inetpub folder, then the wwwroot folder.
4. At the bottom-right of the dialog box, change the file type to All Files so you can view everything in the folder.
5. Open the file named iisstart.htm — this is the default IIS web page. You can view, edit, and configure this page as needed. After making your edits, click Save.
Now, go back to your web browser (Edge, Chrome, or Firefox) and refresh the page. Your changes will appear instantly.

At this point, my Windows 11 computer has successfully activated IIS and can now:
.Host local websites or test environments (like osTicket)
.Run PHP and MySQL web applications
.Simulate real web hosting environments for learning and development
</p>
<br />

<img width="1441" height="788" alt="image" src="https://github.com/user-attachments/assets/84f6cbeb-0957-424b-b2bf-c19f15a5fba8" />


After activation, IIS (Internet Information Services) automatically creates a default web folder, allowing you to host and access files directly through your browser.
To view and modify the default IIS web page, follow these steps:
Open Notepad and run it as Administrator. Inside Notepad, click File → Open.
Navigate to the following path: C:\inetpub\wwwroot\
At the bottom-right corner of the dialog box, select All Files to display every file type. Open the file named iisstart.htm — this is the IIS web page source file.
From here, you can create, edit, or configure the content displayed on the IIS home page. After editing, click Save, 
Once completed, the IIS web page source file will appear exactly like the diagram shown, representing how the IIS web page source file looks like.



<img width="777" height="231" alt="image" src="https://github.com/user-attachments/assets/a2a1d0d3-c701-4242-9cdb-ad3e8656f433" />


How to Install Microsoft Visual C++ Redistributable on Windows 11
Step 1: Download the Redistributable
(1).Visit the Official Microsoft Download Page: Go to the Microsoft Visual C++ Redistributable Downloads page. (!!) Select the Appropriate Version: For most applications, download the x64 version for 64-bit systems or the x86 version for 32-bit systems. Click on the corresponding link to start the download.
Step 2: Run the Installer. (!) Locate the Downloaded File: Navigate to your Downloads folder and find the installer file (e.g., vc_redist.x64.exe).
(!!). Execute the Installer: Double-click the installer file to run it. (!!!). Accept the License Agreement: In the setup window, read and accept the license terms, then click Install. (!V). Wait for Installation to Complete: The installation process will take a few minutes. Once finished, click Close.
Step 3: Verify Installation. (!). Open Control Panel: Press Windows + R, type appwiz.cpl, and press Enter. (!!). Check Installed Programs: In the Programs and Features window, look for entries like: *Microsoft Visual C++ 2015–2022 Redistributable (x64), *Microsoft Visual C++ 2015–2022 Redistributable (x86)
If these are listed, the installation was successful.
Step 4: Restart Your Computer (Optional). To ensure all components are properly initialized, it's recommended to restart your computer.
By following these steps, you will have successfully installed the Microsoft Visual C++ Redistributable on your Windows 11 system, enabling applications that depend on it to run correctly.
