# Pen Testing Live Targets

Time spent: **X** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:

* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each color is vulnerable to only 2 of the 6 possible exploits. First discover which color has the specific vulnerability, then write a short description of how to exploit it, and finally demonstrate it using screenshots compiled into a GIF.

## Blue

Vulnerability #1: Session Hijacking

Description:
<br />
Using BurpSuite, capture the PHP Session ID of an authenticated User. Doing so, we change our session ID to matach theirs via PHP script. Resulting to a successful hijack, bypassing authentication.
<br />
You Got Jacked!?!
<img src="Hijack.gif">


## Green

Vulnerability #1: __________________

Description:

<img src="UserEnum.gif">


## Red

Vulnerability #1: __________________

Description:

<img src="IDOR.gif">


## Notes

Describe any challenges encountered while doing the work

