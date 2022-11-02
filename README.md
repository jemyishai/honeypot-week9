# Honeypot Assignment

**Time spent:** 5 hours spent in total

**Objective:** Create a honeynet using MHN-Admin. Present your findings as if you were requested to give a brief report of the current state of Internet security. Assume that your audience is a current employer who is questioning why the company should allocate anymore resources to the IT security team.

### MHN-Admin Deployment (Required)

**Summary:** How did you deploy it? Did you use GCP, AWS, Azure, Vagrant, VirtualBox, etc.?

- I used GCP exactly as described in the instructions:
- Set up GCP and deployed the MHN to it
- Deploy anoter cloud to run dionnaea, and use the MHN admin dash to monitor it

- Here is a gif of the Google cloud dash:

![gcp](https://user-images.githubusercontent.com/12431338/199579171-59e31819-8aed-481f-89f5-2936f0c1f5b6.gif)


- Here is a gif of the Honeypot dash:
![attacks](https://user-images.githubusercontent.com/12431338/199578179-4e04cb71-6e99-4963-9c48-eab629de4cd9.gif)
<img src="mhn-admin.gif">

### Dionaea Honeypot Deployment (Required)

**Summary:** Briefly in your own words, what does dionaea do?
- Dionnaea attracts attackers by creating and monitoring vulnerabilities that nmap or another port scanner might pick up. MHN is the open source framework, and dinaea is the specific "fake server" that is publicly available. MHN helps admin view attacks, manage snort/sniffing rules, deploy scripts, connect, register, send intrusion logs. Dionaea is a specific and mangeable instance of one of these servers. A sysadmin, security researcher, network engineer (or codepath student) could set up MHN and dionaea to attract attackers and see vulnerabilities in action. Dionaea is the honeypot, and the vulonerabilties are the "honey" to attackers. 



### Database Backup (Required) 

**Summary:** What is the RDBMS that MHN-Admin uses? What information does the exported JSON file record?

- It looks like MHN uses mongo to store session information


## Notes
- This command would not work for me ```mongoexport --db mnemosyne --collection session > session.json```
- I had already used up my free credits on google cloud for another project, so I was constantly checking the dashboard to make sure I didn't run up too many costs. I could have created another email, but I was concerned that may create other complications. This is also a bit of hectic time in the semester, so I'm going to come back to this material in the future. 
