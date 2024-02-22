# Deep Web and Cybersecurity

Disclaimer: This course is only worth itself as it lists tools for automating dark web threat intel

## Chapter 1 - What is Dark Web?
- Secret network of website accessible with a specialized browser
- Used to maintain privacy and anonymity online with both ethical and unethical use.
- Surface web
    - The World Wide Web, indexed on public search engines and accessible from public computers
- Deep web
    - Hidden sites, or sites behind paywalls, password protected sites, sites requiring authentication.
    - Local networks / private networks
    - But, still accessible without special services/hardware
- Dark web
    - Segregated networks requiring specialized systems to access the networks
    - Especially hidden networks requiring high
    - Systems, services and websites on segregated and hidden networks unreachable from standard browser and computers
- ToR
    - Tor Browser
    - Tor networking
    - Tor browser gives access to hidden marketplaces for buying illegal information and contraband
    - Tor browser also gives secure, anonymous access to services, such as dropbox for whistleblowers and journalits

## Chapter 2 - Importance of the dark web and how dangerous it is
- Dark Web monitoring
    - Contains unlisted information, eg. data breaches, ransomware information and zero days.
    - Listed on threat actors sites, marketplaces and forums
- Automation
    - Automating processes like threat intel and data gathering
    - Receving onion links
    - Fetch data from onion links
    - Port scan Onion sites
    - Build automation platforms
- Maintaining privacy
    - Tor allows secure connections
    - Tor allows for anonymysing the origin location of the requests
- Blocking censorships
    - Tor has a censorship byuypass, but its mainly through a bridge proxy for accessing ToR which is usually blocked.
- Dark web markets
    - There exists services providing updated view of new, and active onion sites with description of content
    - Hunchly Daily Dark Web report
        - Serves free daily darkweb onion sites
- How dangerous is the dark web
    - Visiting sites / using the TOR network can put you in the eyes of threat actors and make you susceptible to blackmail
        - Eg. state level actors or based on what you've accessed threat actors  
    - Governmental monitoring may be incurred as result of dark web use
    - Scams may occur, as there are rampant with unethical use on dark web
- Darkweb resources
    - GitHub vlall/Darksearch
        - query cached onion sites, IRC chatrooms, PDFS, game chats, blackhatforums and more using python
        - Queries old data and sites which are taken down
    - GitHub apurvsinghgautam/dark-web-osint-tools
        - Gives tools for performing OSINT on dark web content
    - GitHub fastfire/depdarkCTI
        - Collection of threat intel for dak web
        - Telegram, marketplaces and more

## Chapter 3 - Staying safe on the dark web
- One must access the Dark web securely
    - Hide your originating location, eg. access a remote host via VPN which then is used to access darkweb
    - TOR cloaks your exiting location, but the ingress host knows your originating location
- Tips
    - Be aware of scams, malware and malicious actors on the dark web
    - Disable JavaScript on sites, but this will break websites
    - Access Tor through a sandboxed application or separate VM, which can be deleted in retrospect when stuff goes awry
    - Use bridges for TOR access to bypass blockades
- Downloading files
    - Stay very vigilant and validate all files before executing or performing tasks
    - Run anti virus scans and other needed tasks
- Communicate on the dark web
    - Use fake contact information
        - Email, name, phone, location and others
    - The information will be logged by malicious entities if possible and used for later
- TAILS
    - OS for providing anonymity, which runs from a USB drive and contains tools for running anonymously and no data is stored by default
    - Stupid TAILS installation tutorial, and TOR browser access.
- Secure communications
    - ProtonMail (encrypted mail)
    - Temp mail, generates temporary and disposable email accounts for different purposes
    - Secure messaging - off-the-record messaging - encrypted and authenticated messaging on the dark web
    - Pidgin allows for multiple accounts and chat services simultaneously in one GUI client
    - Bullshit Pidgin video

## Chapter 4 - Cyber threat intelligence and dark web
- Threat intel is needed to understand what threats our organisation/clients are facing
- Figure out what trends are occurring in order to proactively thwart threats
- CTI
    - Tactical CTI - Looks at active threats and current attacks for immediate security work
    - Strategic CTI - Big picture planning and looks at future attacks
- CTI comes from various sources, eg OSINT, social media, dark web, vendors, and colleagues
- Challenges are
    - Huge datasets which requires processing, and interpretation
- Benefits
    - Improved situational awareness, better incident respons and risk management
    - Good understanding of cybersecurity landscape will result in better informed decisions
- Use-Cases
    - Types
        - Threat intelligence
        - Dark web monitoring
        - Dum sites listing
        - Vulnerability intelligence
        - APT monitoring
    - General use case
        1. Data collection - Gather data from sources, OSINT, social maeda, dark web, vendors and more
        1. Data analysis - Identify threats, risks, activities and targets.  Identify patterns and trends within the data
        1. Intelligence extraction - Identify and extract intelligence from the data regarding interesting topics. Emerging threats, stolen credentials, personal information or financial details
        1. Risk assessment - Assess the risk posed by each potential threat to determine its severity and likelihood of occurrence.
        1. Mitigation - Develop mitigative actions and controls to combat/hinder exploitation/compromise from threats
        1. Reporting - generate reports containing insights into threats, their impact on the findings to stakeholdes
    - Use Case: Banking
        - Highly attractive target and requires continuous threat intel to proactively mitigate and protect against emerging threats
    - Use Case: Developers
        - Monitoring leaked data, eg. keys, security risks, exploited APIs/libraries and compromised supply chain
    - Use Case: Social Media Influencer
        - Highly attractive target for PII, credentials an financial information
        - Selling data, taking over accounts, spreading malicious content and blackmailing
    - Use Case: Tech stack
        - Monitoring the tech stack a company utilise
        - Proactively discovering vulnerabilities, and reactively discover compromised accounts and chatter
- Threat intellicen tools
    - Recorded Future, intel147, Kaspersky, StealthMole, IntelligenceX
    - Free: AlienVault, Huncly daily summary, Feedly, URLscan.io, breachdirectory, haveibeenpwnd
- Telegram
    - Encrypted chat service
    - Contains data breach leaks, zero days, leaked credic cards, malware and hackers/apt data
    - Private groups which requires unlisted links
    - Example groups
        - X-Force - credit card leaks

## Chapter 5 - Dark web automation
1. Python script running queries against the ahmia.fi search engine on the WWW
    - Returns indexed onion URLs
1. Crawl Onion URLs using python
    - Crawls TOR using a proxy on the localhost to access the TOR (tor proxy)
1. Telegram bot - Python script  utilising the telebot library
    - Generate API key for the bot and start utilisingt he bot library

