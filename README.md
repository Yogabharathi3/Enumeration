# Enumeration
Enumeration Techniques

# Explore Google hacking and enumeration 

# AIM:

To use Google for gathering information and perform enumeration of targets

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various Google hacking keywords and enumeration tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## Pen Test Tools Categories:  

Following Categories of pen test tools are identified:
Information Gathering.

Google Hacking:

Google hacking, also known as Google dorking, is a technique that involves using advanced operators to perform targeted searches on Google. These operators can be used to search for specific types of information, such as sensitive data that may have been inadvertently exposed on the web. Here are some advanced operators that can be used for Google hacking:

site: This operator allows you to search for pages that are within a specific website or domain. For example, "site:example.com" would search for pages that are on the example.com domain.
Following searches for all the sites that is in the domain yahoo.com
# OUTPUT:
![239592969-75019822-2a90-47e2-93cf-5c0d8ce50f3d](https://github.com/Yogabharathi3/Enumeration/assets/118899387/83f20a37-3fcc-40ee-821c-58ef091a7324)

filetype: This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files.
Following searches for pdf file in the domain yahoo.com
# OUTPUT:
![239593233-aca98252-be96-42cb-8291-95388802523f](https://github.com/Yogabharathi3/Enumeration/assets/118899387/8a3b291f-a11d-4e08-8925-6be48ddf783d)

intext: This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.
# OUTPUT:
![239594061-79c3aa8a-24c1-46dc-b2fa-5d45cf440bb5](https://github.com/Yogabharathi3/Enumeration/assets/118899387/25d75c55-e1fa-41c7-aa48-5785155f4ca3)

inurl: This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.
# OUTPUT:
![239594379-5df0d26a-9a8d-41b1-806b-39ee0b516fd5](https://github.com/Yogabharathi3/Enumeration/assets/118899387/22e2b08e-e1d8-4462-b100-042b9f5ba010)

intitle: This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag.
# OUTPUT:
![239594611-76cec9fc-3756-4e59-8ab7-62ef225e49f6](https://github.com/Yogabharathi3/Enumeration/assets/118899387/c4152236-a33f-4677-804b-c24b39badd76)

link: This operator allows you to search for pages that link to a specific URL. For example, "link:example.com" would search for pages that link to the example.com domain.
# OUTPUT:
![239594767-48385782-16fa-4b11-bb77-410f4b69d328](https://github.com/Yogabharathi3/Enumeration/assets/118899387/23258453-bf2c-4e1f-9914-438be5ca342d)

cache: This operator allows you to view the cached version of a page. For example, "cache:example.com" would show the cached version of the example.com website.

# OUTPUT:
![239594985-fed106bd-ef84-4eba-9f20-42f0578caf07](https://github.com/Yogabharathi3/Enumeration/assets/118899387/0f0374af-ae90-4661-a43a-0a1c7572e7be)

# DNS Enumeration
## DNS Recon

provides the ability to perform:
Check all NS records for zone transfers
Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
Perform common SRV Record Enumeration
Top level domain expansion
## OUTPUT:
![240358807-404a97fc-30d3-4dbf-bd44-e87e8a6a7c4d](https://github.com/Yogabharathi3/Enumeration/assets/118899387/7b15262d-c0d2-4d17-895b-5a94ba502bca)
![240358918-cccb27a8-2711-492a-bda9-5fa261c0f27c](https://github.com/Yogabharathi3/Enumeration/assets/118899387/145eecb0-df46-4a6f-b9a2-44567e0e2f2b)

## dnsenum
Dnsenum is a multithreaded perl script to enumerate DNS information of a domain and to discover non-contiguous ip blocks. The main purpose of Dnsenum is to gather as much information as possible about a domain. The program currently performs the following operations:

Get the host’s addresses (A record).
Get the namservers (threaded).
Get the MX record (threaded).
Perform axfr queries on nameservers and get BIND versions(threaded).
Get extra names and subdomains via google scraping (google query = “allinurl: -www site:domain”).
Brute force subdomains from file, can also perform recursion on subdomain that have NS records (all threaded).
Calculate C class domain network ranges and perform whois queries on them (threaded).
Perform reverse lookups on netranges (C class or/and whois netranges) (threaded).
Write to domain_ips.txt file ip-blocks.
This program is useful for pentesters, ethical hackers and forensics experts. It also can be used for security tests.
# OUTPUT:
![240359135-2c7f0da3-b169-4390-a802-e7da5842a787](https://github.com/Yogabharathi3/Enumeration/assets/118899387/075ac6b2-786f-44a4-a28a-b8264c8fb7b3)

## smtp-user-enum
Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.
![240359294-36268e62-becc-4a52-971d-0db0460b9673](https://github.com/Yogabharathi3/Enumeration/assets/118899387/2f6a8934-4552-454c-96f6-55a375fce7ab)

In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:
![240359340-2decc652-0645-4faa-a05d-aee0d3903515](https://github.com/Yogabharathi3/Enumeration/assets/118899387/eee6481d-b2e2-452f-9973-c415d8d330c2)

select any username in the first column of the above file and check the same

![240359449-213e9b42-33e5-41d4-a2bc-ec3e7c03bd72](https://github.com/Yogabharathi3/Enumeration/assets/118899387/bf7fefca-dbc8-4d19-af60-9b4b2a5014ab)

# Telnet for smtp enumeration
Telnet allows to connect to remote host based on the port no. For smtp port no is 25 telnet 25 to connect and issue appropriate commands
 ![240359680-6c49d93b-c710-4e51-87af-d6cb5a453918](https://github.com/Yogabharathi3/Enumeration/assets/118899387/03c7c073-ca46-481a-a840-54475babda08)
 
## nmap –script smtp-enum-users.nse <hostname>

The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.
![240359786-5a15bf55-ccc2-4c84-81bc-a7975acc0265](https://github.com/Yogabharathi3/Enumeration/assets/118899387/49227ce6-e4d0-4b06-8cea-1c5d11c204e3)

## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully

