te# Enumeration
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

<img width="1817" height="912" alt="Screenshot 2026-02-03 071902" src="https://github.com/user-attachments/assets/18feb265-d512-4e95-8aa3-aa82af56c3de" />



filetype: This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files.
Following searches for pdf file in the domain yahoo.com


<img width="1876" height="910" alt="Screenshot 2026-02-03 072128" src="https://github.com/user-attachments/assets/20feee88-db90-46f3-ad74-9b6c8ca4e25a" />


intext: This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.


<img width="1326" height="899" alt="Screenshot 2026-02-03 072250" src="https://github.com/user-attachments/assets/107c0ba9-27ab-4eb6-8485-135aa0238bba" />


inurl: This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.


<img width="1150" height="899" alt="Screenshot 2026-02-03 072347" src="https://github.com/user-attachments/assets/4e9d58ab-9855-4b9c-bd2b-1ab39f64b7f0" />


intitle: This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag.


<img width="1282" height="911" alt="Screenshot 2026-02-03 072445" src="https://github.com/user-attachments/assets/9ef6b7cf-f9a1-4305-bcb2-94a9a8f3d50c" />


link: This operator allows you to search for pages that link to a specific URL. For example, "link:example.com" would search for pages that link to the example.com domain.


<img width="1201" height="872" alt="Screenshot 2026-02-03 072730" src="https://github.com/user-attachments/assets/f22735c2-125b-4ea9-a164-aa1ee7ebb898" />


<img width="1766" height="765" alt="image" src="https://github.com/user-attachments/assets/aaded0fd-c975-4677-babe-5e8964f74f83" />


cache: This operator allows you to view the cached version of a page. For example, "cache:example.com" would show the cached version of the example.com website.


<img width="1863" height="969" alt="image" src="https://github.com/user-attachments/assets/05cc9c5c-7e2c-4831-9697-9a3056eb5200" />

 
#DNS Enumeration


##DNS Recon
provides the ability to perform:
Check all NS records for zone transfers
Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
Perform common SRV Record Enumeration
Top level domain expansion
## OUTPUT:

<img width="624" height="315" alt="image" src="https://github.com/user-attachments/assets/384da70b-77f3-4625-aff0-08db01f47642" />





<img width="630" height="421" alt="image" src="https://github.com/user-attachments/assets/88dcf8f5-de8f-4be7-adbd-df45503d9a05" />




##dnsenum
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


<img width="644" height="421" alt="image" src="https://github.com/user-attachments/assets/96495291-d31b-44a7-a494-a211c6044f98" />



##smtp-user-enum
Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.

<img width="641" height="336" alt="image" src="https://github.com/user-attachments/assets/e972301f-3e5a-43eb-9f16-500d35d5fd34" />


In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:

<img width="512" height="205" alt="image" src="https://github.com/user-attachments/assets/bb50fcb4-666b-49b6-91a1-6e8a96be1646" />


select any username in the first column of the above file and check the same

<img width="630" height="326" alt="image" src="https://github.com/user-attachments/assets/25deb5ab-4b88-4aa2-90f7-746907d65a71" />


#Telnet for smtp enumeration
Telnet allows to connect to remote host based on the port no. For smtp port no is 25
telnet <host address> 25 to connect
and issue appropriate commands
  
 ## Output
  
<img width="624" height="362" alt="image" src="https://github.com/user-attachments/assets/133e5caf-27e5-4df9-bea0-5a0ce7d0471d" />



## nmap –script smtp-enum-users.nse <hostname>

The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.
## OUTPUT:

<img width="601" height="172" alt="image" src="https://github.com/user-attachments/assets/6cf714ab-6929-4d7d-85cc-f433ed7d9d0e" />


## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully

