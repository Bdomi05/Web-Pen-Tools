# Web-Pen-Tools
#A set of tools that will be used for one bigger pen-test scan

##List of Tools with Description:
-------------------------------
#XXStrike - https://github.com/s0md3v/XSStrike -Python<br>
Command: “python3 xsstrike.py -u "https://mysmartsa.com/" --crawl”<br>
Info: This git-hub is used to detect Cross-Site Scripting, It’s pretty smart as it will analyze the responses and craft a payloads for that type of response. It can also crawl a website.<br>
Results: When I ran the scan, it found jquery v3.6.0  and bootstrap v5.2.0-beta1 but found zero vulnerabilities within those.<br>


#yoiThon - https://github.com/gyoisamurai/GyoiThon - Python<br>
Command: “python3 gyoithon.py” Must add url into host.txt<br>
Info: GyoiThon is a gathering tool for a web server, it will gather product operated on a server, like CMS, etc. It does a web crawl, gathering HTTP responses, get identification of product/version, uses CVE’s to identifies any, looks for unnecessary HTML/JavaScript comments and debug messages, and examines login pages. Uses the Python library Scrapy to web crawl.<br>
Results: It web crawled found all links on website, made a lot of logs from what I could understand, nothing was found.<br>


#Vulscan - https://github.com/scipag/vulscan<br>
Command: “nmap -sV –script=vulscan/vulscan.nse www.mysmartsa.com”<br>
A vulnerability scanner that uses Nmap. This scanner adds a script to nmap and searches of different exploit cves from a preinstalled database of different ones from different websites like exploitdb.csv<br>
Results: It found a ton of info for Google applications on the website.<br>


#OWASP - https://github.com/OWASP/Nettacker – Python<br>
Command: “”<br>
Used for info gathering and vulnerability scanning with it utilizing TCP SYN, Ack, and ICMP.<br>
Seems to be a very powerful tool to scan for vulnerabilities it has a lot of modules that can do a lot of different things. Has different built in modules to find exploits, like admin directory finder, subdomains, strict transport security vuln,etc. <br>
Results: Finds port 80 and 443 from the scans I ran like STS it found nothing, the subdomain scan worked, while the admin scan did not find the admin page.<br> 


#Snallyhaster - https://github.com/hannob/snallygaster - Python<br>
Command: “snallygaster mysmartsa.com”<br>
Info: A tool used to find files on a website that shouldn’t be public<br>
Results: After running it on mysmartsa.com, it came back with nothing, which means it didn’t find any exposed files. I did test it on a website that did and it seemed to work.<br>


#Dirsearch - https://github.com/maurosoria/dirsearch – Python<br>
Command: “python3 dirsearch.py -u https://mysmartsa.com”<br>
Info: A tool used for recursive scanning, it identifies hidden directories and will crawl to find more. Its build with a ton of features for different purposes.<br>
Results: Went through a whole word-list, finding , /admin/, /cgi-bin, /map, /users, from there it was trying different sub-directories in each of the found directory's. It was unsuccessful at finding anything exposed as for example when it tried to do anything in /admin it would be redirected to the admin login page.<br>


#Breacher - https://github.com/s0md3v/Breacher – Python<br>
Command: “python3 breacher.py -u mysmartsa.com”<br>
Info: Is a info gathering tool that is used to find admin login pages and EAR vulnerabilities, also checking for robots.txt.<br> 
Results: The website didn’t have a EAR vul or a robots.txt. It was successful at finding the admin login page on the website. <br>


#Photon - https://github.com/s0md3v/Photon - Python<br>
Command: ”python3 photon.py -u mysmartsa.com”<br>
Info: Is a fast web crawler<br>
Results: From what I saw it didn’t find anything juicy but it found all the directories and outside links like professor info.<br>


#Scanless - https://github.com/vesche/scanless – Python<br>
Command: “scanless -t mysmartsa.com -s spiderip”<br>
Info: Is a simple little port scanner<br>
Results: Found ports 80 and 443<br>
