# Pentesting-Cheat-sheet
INFORMATION GATHERING

WHOIS Lookup: whois target.com
whois -h <HOST> -p <PORT> "domain.tld"
echo "domain.ltd" | nc -vn <HOST> <PORT>
DNS Enumeration

    Basic DNS Lookup:

    bash

nslookup target.com
DNS Zone Transfer Check:

bash

    dig axfr @ns1.target.com target.com

Subdomain Enumeration

    Sublist3r:

    bash

sublist3r -d target.com

Assetfinder:

bash

assetfinder --subs-only target.com

Amass:

bash

    amass enum -d target.com

Google Dorking

    Basic Google Dorking:

    bash

site:target.com inurl:admin

Finding Login Pages:

bash

site:target.com inurl:login

Exposed Documents:

bash

    site:target.com filetype:pdf

Email Harvesting

    theHarvester:

    bash

    theHarvester -d target.com -l 500 -b google

Network Information

    IP Range and ASN Information:

    bash

    whois -h whois.cymru.com " -v target.com"

Web Application Information

    WhatWeb:

    bash

    whatweb target.com

    Wappalyzer (Browser Extension): Use to identify technologies used by the target website.

Social Media Enumeration

    Sherlock:

    bash

    sherlock username

Metadata Extraction

    exiftool:

    bash

    exiftool file.jpg

    FOCA (Fingerprinting Organizations with Collected Archives): Use to extract metadata from public documents.

Open Ports and Services

    Nmap:

    bash

nmap -sS -p- target.com

Masscan (Fast Port Scanner):

bash

    masscan target.com -p1-65535 --rate=1000

Vulnerability Scanning

    Nmap with Vulnerability Scripts:

    bash

    nmap --script vuln target.com

OSINT Frameworks and Tools

    Maltego: Comprehensive tool for gathering and correlating information.
    SpiderFoot: Automated OSINT tool.

    bash

spiderfoot -s target.com
Recon-ng: A full-featured web reconnaissance framework.

bash

recon-ng

Shodan: Search engine for Internet-connected devices.

bash

shodan search "target.com"


