# Project 7 - WordPress Pen Testing

Time spent: **X** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pen Testing Report

### 1. User Enumeration (CVE-2020-7918)

- [ ] Summary:     
  - Vulnerability types: Insecure direct object reference
  - Tested version: 4.2
  - Fixed version: NOT FIXED
  - Affected source code: (http://wpdistillery.vm/wp-login.php)
  - Tools/Resources Used:
  <br /> https://www.kali.org/get-kali/#kali-virtual-machines
  <br /> https://www.kali.org/tools/wpscan
  <br /> https://wpscan.com/
  <br /> password list: rockyou.txt
  - Techniques: BruteForce, Dictionary Attack, Credential Stuffing
  - Preventative Action: Password Complexity, Multi-Factor Authentication (MFA), Password Manager, Account Lockout Policy
  - Commands used:
  <br /> sudo gunzip /usr/share/wordlists/rockyou.txt.gz (extract and move for ease of use)
  <br /> wpscan -h (Display the Help)
  <br /> wpscan --url http://wpdistillery.vm (Reconnasissance)
  <br /> wpscan --url http://wpdistillery.vm --enumerate u (Finding Usernames)
  <br /> wpscan --url http://wpdistillery.vm -U ~/Desktop/wpusers.txt -P ~/Desktop/rockyou.txt (BruteForce Attack)
  


- [ ] Walkthrough:
<br /> Where's the Beef ?!?
<img src="user_enum1.gif">
<br /> A Successful Attack against all 5 User Accounts took 2min and 11 seconds !?!
<img src="BruteForce.gif">
<br /> The Damage... We got User credentials, PII, and our very own Administrative Account !?!
<img src="damage.gif">


- [ ] Steps to recreate:
<br /> - Try common usernames in the TARGET's login page, guess common passwords. Maybe we'll get some helpful info. Lets PLAN our attack.
<br /> - Kali is a great toolbox. Lets use our handy dandy tool wpSCAN to gather information on a TARGET. Perfome RECONNAISSANCE.
<br /> - After some poking and proding with WPSCAN lets use our collected INTEL to test our might. Commense Brute Force Attack!!! 
<br /> - Have I been pwned? Lets use the compromised credentials. GAIN ACCESS!!!
<br /> - Lets cause some damage...hmmm how about we just add a way to get back in. Add our own administrator ;). MAINTAIN ACCESS
<br /> - Considerations: COVER YOUR TRACKS!!!
  
### 2. Vulnerable Plugin (CVE-2015-4133)

- [ ] Summary: 
  - Vulnerability types: Arbitrary File Upload
  - Tested in version: 3.1.3
  - Fixed in version: 3.1.4
- [ ] GIF Walkthrough: 
- [ ] Steps to recreate: 
- [ ] Affected source code:
  - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

### 3. (Required) Vulnerability Name or ID

- [ ] Summary: 
  - Vulnerability types:
  - Tested in version:
  - Fixed in version: 
- [ ] GIF Walkthrough: 
- [ ] Steps to recreate: 
- [ ] Affected source code:
  - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

### 4. (Optional) Vulnerability Name or ID

- [ ] Summary: 
  - Vulnerability types:
  - Tested in version:
  - Fixed in version: 
- [ ] GIF Walkthrough: 
- [ ] Steps to recreate: 
- [ ] Affected source code:
  - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

### 5. (Optional) Vulnerability Name or ID

- [ ] Summary: 
  - Vulnerability types:
  - Tested in version:
  - Fixed in version: 
- [ ] GIF Walkthrough: 
- [ ] Steps to recreate: 
- [ ] Affected source code:
  - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with  ...

[ScreenToGif](https://www.screentogif.com/) for Windows

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
