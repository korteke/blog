---
title: "Security.txt -file generator" 
date: 2022-11-27T15:56:53+02:00 
description: "Security.txt -file generator"
featured: true
toc: false
usePageBundles: false
codeMaxLines: 10
codeLineNumbers: false
figurePositionShow: true
categories:
  - Security
tags:
  - Security
  - Go
draft: false  
---

# Security.txt -file generator
i just created my first application with Golang. I am pretty sure that the code is ugly, but it works :)

## What is Security.txt
Quote from [Securitytxt.org](https://securitytxt.org)
> “When security risks in web services are discovered by independent security researchers who understand the severity of the risk, they often lack the channels to disclose them properly. As a result, security issues may be left unreported. security.txt defines a standard to help organizations define the process for security researchers to disclose security vulnerabilities securely.”

Security.txt is based on [RFC 9116](https://www.rfc-editor.org/rfc/rfc9116) and nowadays it has been implemented by various companies. The idea is to create a file that can be distributed on a website, from a predefined address (https://xxx.test/.well-known/security.txt). The file will explain how the organisation can be notified of any security vulnerabilities found.


```
Contact: https://g.co/vulnz
Contact: mailto:security@google.com
Encryption: https://services.google.com/corporate/publickey.txt
Acknowledgements: https://bughunters.google.com/
Policy: https://g.co/vrp
Hiring: https://g.co/SecurityPrivacyEngJobs
```
example of Google's security.txt (RFC non-compliant).

## gensectext -generator
I just created small application which generate and optionally signs security.txt -file. The Go application can be found from [Github](https://github.com/korteke/gensectext).   
This was my first "real" Go-application, and it looks like it :) 