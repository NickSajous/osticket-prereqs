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

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Install the OsTicket requirements
- Install OsTicket 
<h2>Installation Steps</h2>



<p>
  1. Copy and paste this link (https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD) onto your browser, and download. When finished, unzip the folders onto the desktop. The folder should be called osTicket-Installation-files.
  
  ![Screenshot 2025-04-26 181444](https://github.com/user-attachments/assets/be75b31a-03c8-4863-af3d-ca3b6592537e) ![Screenshot 2025-04-27 131339](https://github.com/user-attachments/assets/0068c85e-ad08-4101-9e2c-666a25f683f8) ![Screenshot 2025-04-27 131356](https://github.com/user-attachments/assets/44c22df5-87e8-4801-a38d-385b0f8cfa01)



</p>
<p>
</p>
<br />

<p>
2. Before we do anything, we have to enable support for CGI executables. To do that, we need to go to the control panel, open "Programs", Then click on " Turn Windows features on or off". 
  
  ![Screenshot 2025-04-26 183537](https://github.com/user-attachments/assets/fe4d9591-0cac-450a-b050-b1621a9168d0) ![Screenshot 2025-04-26 183557](https://github.com/user-attachments/assets/89f9e328-86aa-4345-8e3b-018f2c0d8ac4) ![Screenshot 2025-04-26 183616](https://github.com/user-attachments/assets/7102fe9f-e698-47fc-aad4-887b1d5d3da6)



</p>
<p>
</p> 
<br />

<p>
  3. Scroll down to Internet Information Services, and click on World Wide Web Services. Click on Application Development Features and select CGI from the drop down menu. Click ok to install. 

  ![Screenshot 2025-04-26 183637](https://github.com/user-attachments/assets/a6698adc-41fd-44a6-9f51-0edbc058c023) ![Screenshot 2025-04-26 183711](https://github.com/user-attachments/assets/3be09af4-de50-4fb2-944b-cdb4f448e3ef) ![Screenshot 2025-04-26 183722](https://github.com/user-attachments/assets/7866b2e0-3c11-4d13-95b4-83b96290a194) 

</p>
<p>
</p> 
<br />
4. Now, go back into the "osTicket installation files" folder, and double click "PHPManagerForIIS_V1.5.0.msi" to install. Click on yes and ok for every option and install. After that, we're going to install the Rewrite Module. Double click "rewrite_amd64_en-US.msi", click yes and ok for every option and install. 

![Screenshot 2025-04-27 124153](https://github.com/user-attachments/assets/d64f493b-4ab0-4d28-8d64-28c7a1d461b4) ![Screenshot 2025-04-27 124221](https://github.com/user-attachments/assets/4d6fb2a5-d29f-4baa-9116-2dc99f6088aa) ![Screenshot 2025-04-27 124253](https://github.com/user-attachments/assets/5e50319d-5f46-405c-85b5-34c2c84baf13) ![Screenshot 2025-04-27 124308](https://github.com/user-attachments/assets/195ec913-4bc5-417b-ab38-b8985d1ef37f) 




</p>
<p>
</p> 
<br />

5. Go into your file explorer and create a new file named "PHP" in the Local Disk. after that, right click on "php-7.3.8-nts-Win32-VC15-x86.zip" and click Extract All. When it asks you for a destination, select the PHP folder you made in your local disk and extract.

![Screenshot 2025-04-27 124439](https://github.com/user-attachments/assets/eb0203ff-a3e5-443e-ba2c-afd48ce51426) ![Screenshot 2025-04-27 124804](https://github.com/user-attachments/assets/e9d1dd7a-a4c1-4bb2-bd57-7c1e02af3524) ![Screenshot 2025-04-27 124826](https://github.com/user-attachments/assets/5ae7c0da-72d8-465b-9a2f-fbd51f7a92de) ![Screenshot 2025-04-27 124847](https://github.com/user-attachments/assets/84ba3b5f-0ed7-4f82-b126-9d375080352f)
 




</p>
<p>
</p> 
<br />
6. Go back to the osTicket installation folder, and double click " VC_redist.x86.exe" to install. When you're done with that, double click "mysql-5.5.62-win32.msi" to start installing. When you get to the choose setup screen, select the "typical" installation. When you get to the "complete setup wizard" screen, make sure to check the "launch the MySQL Instance Configuration Wizard" box before clicking finish.

![Screenshot 2025-04-27 125056](https://github.com/user-attachments/assets/0691a3ce-8964-448d-bd24-c55d41a6b018)  ![Screenshot 2025-04-27 125115](https://github.com/user-attachments/assets/a48137bb-0f22-425d-ad12-4a642869622e) ![Screenshot 2025-04-27 125140](https://github.com/user-attachments/assets/30111956-a29a-4908-8797-87324b9948ed) ![Screenshot 2025-04-27 125232](https://github.com/user-attachments/assets/e4054dca-cf20-48ad-9df9-03b29438c098)  






</p>
<p>
</p> 
<br />
7. A "MySQL Server Instance Configuration Wizard" should pop up. Select the "Standard Configuration" option and click next. *IMPORTANT* For the username and password, type in "root". Click Next and then click execute.

![Screenshot 2025-04-27 125258](https://github.com/user-attachments/assets/35cd37b3-5394-4a5b-a1fa-00551c9d44db) ![Screenshot 2025-04-27 125330](https://github.com/user-attachments/assets/40fdefbc-1643-45fe-b44d-b88614d24c1f) ![Screenshot 2025-04-27 125544](https://github.com/user-attachments/assets/56a77cd6-bfe3-4817-b841-2490de0f935c)





</p>
<p>
</p> 
<br />
8. Next, open IIS as an Admin. You can do this by opening the Microsoft search bar and typing in IIS. Click PHP Manager and click register new PHP version.

![Screenshot 2025-04-27 143606](https://github.com/user-attachments/assets/0eb15ff9-4af6-43a1-b951-8c12e9443442) ![Screenshot 2025-04-27 143740](https://github.com/user-attachments/assets/89ce168c-054c-4b79-a9de-a6f9f23e157f)  ![Screenshot 2025-04-27 143807](https://github.com/user-attachments/assets/fd6fee67-7871-4041-a52b-5e26ea6f663d) 





</p>
<p>
</p> 
<br />
9. When it asks you to select an executable file, select the PHP file you made prior and click "php-cgi" then click ok. When you're finished with all of that, stop and start the server in the IIS Manager.

![Screenshot 2025-04-27 143848](https://github.com/user-attachments/assets/a2bb23e4-2ac2-4c8e-a1e3-56d073ab399a) ![Screenshot 2025-04-27 143911](https://github.com/user-attachments/assets/b22a0ae8-abd4-43fc-ac61-d643600643d1) ![Screenshot 2025-04-27 143931](https://github.com/user-attachments/assets/90bac724-8bbb-4086-95f0-a3a8c04ba898) ![Screenshot 2025-04-27 144018](https://github.com/user-attachments/assets/e7e934a3-4345-47e5-b191-6dab2c3331f4)




</p>
<p>
</p> 
<br />
10. Go back to the osTicket Installation files, right click “osTicket-v1.15.8.zip”, and click extract all. You'll see a folder named “osTicket-v1.15.8” thats unzipped in the same folder when it is finished. 

![Screenshot 2025-04-27 145141](https://github.com/user-attachments/assets/e32f4b2d-204d-4e34-a060-612a7a1989e9) ![Screenshot 2025-04-27 155826](https://github.com/user-attachments/assets/9d12f8e2-1cb3-42df-b012-e2dceda9aa35) ![Screenshot 2025-04-27 160725](https://github.com/user-attachments/assets/367fd053-dead-4fa7-bfa6-11e4a433e476)



 


</p>
<p>
</p> 
<br />
11. in the Files manager, Click on windows (C:), and click on inetpub, then wwwroot, then move the "upload" folder from “osTicket-v1.15.8” into the wwwroot folder. Rename the "upload" folder to "osTicket" *IMPORTANT* make sure it is spelled exactly like "osTicket". It will not work if it is spelled any other way.

![Screenshot 2025-04-27 162712](https://github.com/user-attachments/assets/2ab5c971-9d56-4c37-80ab-af2de0d249f5) ![Screenshot 2025-04-27 145338](https://github.com/user-attachments/assets/7d186b6a-1d04-4ee0-aa5f-9162a2a0e3f2) ![Screenshot 2025-04-27 145408](https://github.com/user-attachments/assets/682b5f99-9249-4c7c-b8b0-9f512239099d) ![Screenshot 2025-04-27 145439](https://github.com/user-attachments/assets/187c4e4d-aac4-43d5-ae4e-d07c4cea2a3c) 





</p>
<p>
</p> 
<br />
12. Go to the IIS Manager and stop and start the server again. Then, click the drop down for Sites, Default Web Site, then osTicket. On the right side of the screen, click  “Browse *:80” and it should take you to a website that looks like the one below, considering you did all of the steps right so far. 

![Screenshot 2025-04-27 145843](https://github.com/user-attachments/assets/d8c1098b-44aa-42f2-9210-d76e4fcf02eb) ![Screenshot 2025-04-27 145928](https://github.com/user-attachments/assets/ae8ef438-79e8-4878-b908-8e8c85182a71) ![Screenshot 2025-04-27 150039](https://github.com/user-attachments/assets/0895f33d-ccb7-45fe-8e0d-af270f84aa14) 




</p>
<p>
</p> 
<br />
13. Go back to the IIS Manager screen and click on PHP Manager. Under PHP Extentions, click "Enable or disable an Extension". Search for "php_imap.dll", "php_intl.dll", and "php_opcache.dll" and enable all 3. Refresh the website and it should change to the one below. 

![Screenshot 2025-04-27 150456](https://github.com/user-attachments/assets/5c62ffeb-aa15-4e76-8320-f7a25c4567b8) ![Screenshot 2025-04-27 150517](https://github.com/user-attachments/assets/625c0c8d-a641-4c53-be17-09bb6b69b4d4) ![Screenshot 2025-04-27 150640](https://github.com/user-attachments/assets/8bde2447-b330-45ac-a0cd-26d384d8a2ba) ![Screenshot 2025-04-27 150759](https://github.com/user-attachments/assets/ba3f2cc0-a347-47e0-8c46-3826282ff820) 





</p>
<p>
</p> 
<br />
14. Back in the wwwroot folder, open the "osTicket" folder, then the "include" folder. Find and rename the "ost-sampleconfig.php" to "ost-config.php" *IMPORTANT* Make sure you spell "ost-config.php" correctly. It won't work if it's spelled any other way.

![Screenshot 2025-04-27 184913](https://github.com/user-attachments/assets/b258a425-490a-4703-98e1-8d7c6ec10167) ![Screenshot 2025-04-27 184943](https://github.com/user-attachments/assets/de8cc767-c45c-44da-a2ff-f51f32bb4241)  ![Screenshot 2025-04-27 185013](https://github.com/user-attachments/assets/9d143fb7-d4ce-45b5-bd3e-550dec8d3dd1) ![Screenshot 2025-04-27 185039](https://github.com/user-attachments/assets/faf3f8f2-6cce-47e8-8498-c97a67f49d9f)






</p>
<p>
</p> 
<br />
15. Right click on "ost-config.php", click on properties, and click on advanced. Disable all inheritance, click add, then select a principal. Under "Enter the object name to select" type "Everyone" then ok. Before hitting ok again, give "Full control" to "Everyone"

![Screenshot 2025-04-27 185131](https://github.com/user-attachments/assets/27f51714-2261-4b1f-927b-71c5508a5e91) ![Screenshot 2025-04-27 185147](https://github.com/user-attachments/assets/257708ad-4d36-4159-b36c-daddb047a95f) ![Screenshot 2025-04-27 185223](https://github.com/user-attachments/assets/4b9ccff9-c591-4fb1-8656-f29d75e5b66d) ![Screenshot 2025-04-27 185248](https://github.com/user-attachments/assets/f1983d0e-0fe2-46aa-99fc-b104b58f3501) ![Screenshot 2025-04-27 185600](https://github.com/user-attachments/assets/db21132d-14a1-41d1-a8cf-d9c8903a1853) ![Screenshot 2025-04-27 185626](https://github.com/user-attachments/assets/3dc590fe-c2cc-40c6-95bc-07d4a2724fd4) ![Screenshot 2025-04-27 185705](https://github.com/user-attachments/assets/eae3ee81-6719-4fd8-a54d-12cc1791c8ea)



 

</p>
<p>
</p> 
<br />
16. Go back to the osTicket website and click "Continue" on the bottom to continue with the installation process. You can name your HelpDesk whatever you want, same thing with your first and last name. Just make sure that the email you put in the "Default Email" and "Email Address" feilds are different. They dont have to be real emails. Under the "username and password" feilds, put in the one you see below.

![Screenshot 2025-04-27 190525](https://github.com/user-attachments/assets/e19b7425-92d2-4e18-ae58-879c6d4c5e02) ![Screenshot 2025-04-28 093311](https://github.com/user-attachments/assets/fb5ac2b4-3bad-490a-83eb-9c3132d8ea08) ![Screenshot 2025-04-28 093405](https://github.com/user-attachments/assets/a25224cc-e41a-485d-a756-a9b2013275da) 




</p>
<p>
</p> 
<br />
17. Back in the osTicket-installation foolder, Double click "HeidiSQL" to install. Click yes and ok for every option until the installation is complete. When finished, make sure the "Launch HeidiSQL" checkbox is checked. when the Session manager pops up on your screen, click "New" on the bottom left, type in "root" for the password, then "Open". Right click on "Unnamed", then click "Create New" then "Database". Type in "osTicket" then click ok. *IMPORTANT* Make sure "osTicket" os spelled correctly. IT will not work if its spelled wrong. You should see "osTicket" under the "Unnamed" menu. 

![Screenshot 2025-04-28 093553](https://github.com/user-attachments/assets/ee1b575f-b57f-4d7e-bb95-8b3861a60ab7) ![Screenshot 2025-04-28 093759](https://github.com/user-attachments/assets/28a20e74-bbe6-4952-a0df-2f712f005617) ![Screenshot 2025-04-28 093914](https://github.com/user-attachments/assets/79935246-baea-462f-aa74-33a83558c5bb) ![Screenshot 2025-04-28 094218](https://github.com/user-attachments/assets/633ee8f8-4c04-441e-824f-3f63f118e990) ![Screenshot 2025-04-28 094239](https://github.com/user-attachments/assets/0f01af96-c21a-44e2-ac6e-fec1ed11e3f6) ![Screenshot 2025-04-28 094259](https://github.com/user-attachments/assets/ca17033b-9e65-44a7-8aea-86cb513077f6)







</p>
<p>
</p> 
<br />
18. Go back to the webpage and type in what you see below. Make sure evrything is spelled correctly, otherwise it wont install porperly. Click install now. If everything was done correctly, you should be taken to a screen that looks like the one below. 

![Screenshot 2025-04-28 101027](https://github.com/user-attachments/assets/790cabd2-6185-4a19-89e1-e49163a78464) ![image](https://github.com/user-attachments/assets/a7bf335f-eed0-4889-8d85-f4d1c2d46bfe) 




</p>
<p>
</p> 
<br />
19. Open a new tap and type "http://localhost/osTicket/scp/login.php" into the URL. You should be taken to the page below. To login, use the osTicket Admin username and password you used in the previous steps. You should be met with a screen like the one below. To make your own tickets, open a new tab and type "http://localhost/osTicket/" in the URL.

![image](https://github.com/user-attachments/assets/a11b71cd-38a4-4c8d-88f7-9a554ac2eec8) ![image](https://github.com/user-attachments/assets/1860b73a-85fd-4e84-abde-a74efa0ae0f9) ![image](https://github.com/user-attachments/assets/5e78c175-fa36-4a21-9c18-ed2d80f2d838)




</p>
<p>
</p> 
<br />

Congrats! You've successfully installed osTicket onto your computer!

