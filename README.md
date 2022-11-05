# Pen Testing Live Targets

Time spent: **4** hours spent in total

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
<br />
Using BurpSuite, capture the PHP Session ID of an authenticated User. Doing so, we change our session ID to matach theirs via PHP script. Resulting to a successful hijack, bypassing authentication.
<br />
<br />
You Got Jacked!?!
<img src="Hijack.gif">


## Green

Vulnerability #1: User Enumeration

Description:
<br />
<br />
Error messages should not hint at a possible correct answer. Noticed the difference between a non existant user versus an existing one? The error message turns bold! This is just half of the work completed for an adversery to stage an attack. 
<br />
<br />
Wait a minute Your not suppose to tell me that
<img src="UserEnum.gif">
<br />
Vulnerability #2: Cross-Site Scripting

Description:
<br />
<br />
Our Target has a feedback form. Lets try a stored XXS attack. Its like a bring trap a user need to step on it. The first trap is a simple alert indicating we were successful. Lets try something more devious like directing a user to a new URL.  
<br />
<br />
Innocent Vandalism ?
<img src="Cross-Site Scripting.gif">
<br />
Lets try something more devious 
<img src="Cross-Site Scripting Bonus 2.gif">
## Red

Vulnerability #1: __________________

Description:

<img src="IDOR.gif">


## Notes

Describe any challenges encountered while doing the work

