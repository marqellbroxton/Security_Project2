# Cyber Security Analyst Lab

1. Launched a Pfsense virtual machine in VMware and configured each interface I assigned. Each virtual machine I create will be assigned to one of these IP address ranges.

![Screenshot (130)](https://user-images.githubusercontent.com/56138615/233504742-d65e6f2a-9973-4d6d-a425-d333e892f4ac.png)

2. Installed SecurityOnion and accessed it with an external Ubuntu Desktop, simulating a Security Analyst accessing a SIEM.

![Screenshot (134)](https://user-images.githubusercontent.com/56138615/233663097-dd81ff83-26ed-42b0-99ae-a8670f8ed85c.png)

![Screenshot (148)](https://user-images.githubusercontent.com/56138615/233663179-dbfbb212-2b65-46c1-863f-3c889b4b5bac.png)

3. Created a Kali Linux machine to use as an attcker of the Domain Controller and the user machine attached to it that will be set up later. 
With this machine I accessed the Pfsense web configurator to edit the interfaces and firewall rules. 

![Screenshot (133)](https://user-images.githubusercontent.com/56138615/233679175-ccce7316-fc26-4681-a216-f2f0fd724a51.png)

![Screenshot (149)](https://user-images.githubusercontent.com/56138615/233679814-1599e02f-0e29-420b-84af-1dc701b635a8.png)

![Screenshot (150)](https://user-images.githubusercontent.com/56138615/233679836-fbc69703-d8e5-419f-b34a-347601d3062b.png)

![Screenshot (151)](https://user-images.githubusercontent.com/56138615/233679862-f0d6604c-b2cb-4df3-8ede-d374d8248ccf.png)

4. Set up an Active Directory with Windows Server 2019 as the Domain Controller as well as setting up a Windows 10 machine for a new user account I added to the domain.

![Screenshot (136)](https://user-images.githubusercontent.com/56138615/233681407-afb6a5ae-6bbe-48ed-95c0-af31ef62a30c.png)

![Screenshot (137)](https://user-images.githubusercontent.com/56138615/233681450-99135977-3173-4457-b0d9-09eb66cb0aa7.png)

![Screenshot (140)](https://user-images.githubusercontent.com/56138615/233681548-0faea159-a3a4-4daa-aee4-5e97c49625e2.png)

![Screenshot (152)](https://user-images.githubusercontent.com/56138615/233685562-a6ca1add-7d8c-4851-aab1-e9ce408379b0.png)

![Screenshot (141)](https://user-images.githubusercontent.com/56138615/233681575-3e49ec0e-f415-4915-af07-dc3697348d76.png)

5. Next I deployed another Ubuntu machine to access the Splunk server that will be used as the main SIEM. On the new Windows user account I downloaded the splunk forwarder to forward activity on the machine to splunk, then created an index to store the event logs. Here we can see a successful log on to the user's account.

![Screenshot (142)](https://user-images.githubusercontent.com/56138615/233693467-684c8683-ec8b-4a52-bc12-f9344dcaa4a0.png)

![Screenshot (143)](https://user-images.githubusercontent.com/56138615/233693054-c680021e-a7a7-4064-a4f8-4d6c831455d1.png)

![Screenshot (160)](https://user-images.githubusercontent.com/56138615/233694170-a794690d-57ab-4889-9645-79eaaa5a2845.png)

![Screenshot (161)](https://user-images.githubusercontent.com/56138615/233694205-3edf2afd-8d49-4096-994b-c9fd3910ae67.png)

![Screenshot (146)](https://user-images.githubusercontent.com/56138615/233694272-c79a3041-6c3d-4ff0-9cdb-ce55cb202ca3.png)

6. With my Kali Linux machine I performed a brute force attack on the victim machine by using text files I made with usernames and passwords. Through ssh I was able to correctly guess the login credentials and also remotley connect to the machine sense I knew the password at that point.

![Screenshot (157)](https://user-images.githubusercontent.com/56138615/233696519-5fb39f63-9028-49c7-a9ea-907ce0a4f5f9.png)

![Screenshot (158)](https://user-images.githubusercontent.com/56138615/233696551-67e8314e-edef-4a19-9497-847739eb6263.png)

![Screenshot (156)](https://user-images.githubusercontent.com/56138615/233696768-517aa12d-a492-4eb6-8cb8-7ed1fa39cbcd.png)

7. Going over to splunk there is a log event that there was a logon attempt using explicit credentials and explains the action the was taken and also the path that was targeted. 

![Screenshot (163)](https://user-images.githubusercontent.com/56138615/233697689-25986c53-3b1f-4f53-81fb-cfa585143a55.png)
