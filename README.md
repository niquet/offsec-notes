# OffSec Notes

<pre>
 ________     ___    ___ ________ ________ ________  _______   ________     
|\   __  \   |\  \  /  /|\  _____\\  _____\\   ____\|\  ___ \ |\   ____\    
\ \  \|\  \  \ \  \/  / | \  \__/\ \  \__/\ \  \___|\ \   __/|\ \  \___|    
 \ \  \\\  \  \ \    / / \ \   __\\ \   __\\ \_____  \ \  \_|/_\ \  \       
  \ \  \\\  \  /     \/   \ \  \_| \ \  \_| \|____|\  \ \  \_|\ \ \  \____  
   \ \_______\/  /\   \    \ \__\   \ \__\    ____\_\  \ \_______\ \_______\
    \|_______/__/ /\ __\    \|__|    \|__|   |\_________\|_______|\|_______|
             |__|/ \|__|                     \|_________|                   
                                                                            
                                                                            
</pre>
This repository includes my personal notes on different topics related to Offensive Security. The notes are not exhaustive and only reflect my previous areas of interest.

## Table of Contents
- [Unrestricted File Download](#unrestricted-file-download)
- [SQL Injection](#sql-injection)

## Unrestricted File Download
- Internal files contained within a web application can be downloaded unrestrictedly by an adversary
- Occurs due to insufficient sanitization of dynamically fetched resources sourced by legitimate functionalities (e.g., file download mechanism)
- Depending on the scenario, the lacking security controls can be exploited in a variety of ways such as traversal of the parent directory ('dot-dot-slash' attack) to target specific files in other folders
- Preventative measures:
  - Avoid building file path strings with user input
  - Use an allow list for user input
  - Validate that permitted content is contained in the input
  - Never run network-exposed services with elevated priviliges
  - Run server components as a less-priviliged user with no access to critical system files
- OWASP ASVS: [12.3.1](https://github.com/OWASP/ASVS/releases/download/v4.0.2_release/OWASP.Application.Security.Verification.Standard.4.0.2-en.pdf)
- OWASP Testing Guide: [Testing for Local File Inclusion](https://owasp.org/www-project-web-security-testing-guide/v42/4-Web_Application_Security_Testing/07-Input_Validation_Testing/11.1-Testing_for_Local_File_Inclusion.html), [Testing Directory Traversal File Include](https://owasp.org/www-project-web-security-testing-guide/v42/4-Web_Application_Security_Testing/05-Authorization_Testing/01-Testing_Directory_Traversal_File_Include.html)
 
## SQL Injection
- 
