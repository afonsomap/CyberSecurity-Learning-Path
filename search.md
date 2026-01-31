# Searching Techniques

## Evaluate the information (Basic)

- **Source**: Identify the author or organization publishing the information. Consider whether they are reputable and authoritative on the subject matter.
- **Evidence and reasoning**: Check whether the claims are backed by credible evidence and logical reasoning.
- **Objectivity and bias**: Evaluate whether the information is presented impartially and rationally, reflecting multiple perspectives. 
- **Corroboration and consistency**: Validate the presented information by corroboration from multiple independent sources. Check whether multiple reliable and reputable sources agree on the central claims.

## Search Operators

- **"exact phrase"** : Double quotes indicate that you are looking for pages with the exact word or phrase. For example, one might search for `"passive reconnaissance"` to get pages with this exact phrase.
- **site:** : This operator lets you specify the domain name to which you want to limit your search. For example, we can search for success stories on TryHackMe using `site:tryhackme.com` success stories.
- **-** : The minus sign allows you to omit search results that contain a particular word or phrase. For example, you might be interested in learning about the pyramids, but you don’t want to view tourism websites; one approach is to search for `pyramids -tourism` or `-tourism pyramids`.
- **filetype:** : This search operator is indispensable for finding files instead of web pages. Some of the file types you can search for using Google are Portable Document Format (PDF), Microsoft Word Document (DOC), Microsoft Excel Spreadsheet (XLS), and Microsoft PowerPoint Presentation (PPT). For example, to find cyber security presentations, try searching for `filetype:ppt cyber security`.

## Specialized Search Engines

### Shodan

It allows you to search for **specific types and versions of servers, networking equipment, industrial control systems, and IoT devices**.

You may want to see how many servers are still running Apache 2.4.1 and the distribution across countries. To find the answer, we can search for apache 2.4.1, which will return the list of servers with the string “apache 2.4.1” in their headers.

![shodanExample](/images/shodan.png)

### Censys

At first glance, Censys appears similar to Shodan. However, Shodan focuses on Internet-connected devices and systems, such as servers, routers, webcams, and IoT devices. Censys, on the other hand, focuses on **Internet-connected hosts, websites, certificates, and other Internet assets**.

Some of its use cases include enumerating domains in use, auditing open ports and services, and discovering rogue assets within a network. You might want to check Censys Introductory Use Cases.

![censysExample](/images/censys.png)

### VirusTotal

VirusTotal is an online website that **provides a virus-scanning service for files using multiple antivirus engines**. It allows users to upload files or provide URLs to scan them against numerous antivirus engines and website scanners in a single operation.

They can even input file hashes to check the results of previously uploaded files.

The screenshot below shows the result of checking the submitted file against 67 antivirus engines. Furthermore, one can check the community's comments for more insights. 

Occasionally, a file might be flagged as a virus or a Trojan; however, this might not be accurate for various reasons, and that's when community members can provide a more in-depth explanation.

![virusTotalExample](/images/virusTotal.png)

### Have I Been Pwned

Have I Been Pwned (HIBP) **tells you if an email address has appeared in a leaked data breach**. Finding one’s email within leaked data indicates leaked private information and, more importantly, passwords. 

Many users use the same password across multiple platforms, if one platform is breached, their password on other platforms is also exposed. Indeed, passwords are usually stored in encrypted format; however, many passwords are not that complex and can be recovered using a variety of attacks.

![haveIBeenPwnedExample](/images/pwned.png)

## Vulnerabilities & Exploits

### CVE (Common Vulnerabilities and Exposures)

CVE, which stands for Common Vulnerabilities and Exposures, **is a publicly available list of standardized identifiers for cybersecurity vulnerabilities in software and hardware**. Think of it as a unique "ID card" for a specific security flaw, such as `CVE-2021-44228`. By assigning a unique ID to each vulnerability, the system allows security professionals, researchers, and vendors to *speak the same language*, ensuring that everyone is tracking and discussing the exact same threat across different security tools and databases.

Managed by the **MITRE Corporation** in collaboration with various CVE Numbering Authorities (CNAs)—such as Microsoft, Google, and Red Hat—the system provides a clear description and reference links for every recorded flaw. It is important to distinguish a CVE from its CVSS score; while the CVE identifies what the vulnerability is, the **CVSS provides a numerical score (0.0 to 10.0) to indicate how severe it is**. This standardized approach helps organizations worldwide prioritize their patching efforts and defend against cyberattacks more effectively.