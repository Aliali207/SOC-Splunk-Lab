# RDP Brute Force Practice

## What I did
I simulated a Brute Force attack on my Windows VM using my Kali Linux machine to see how such attacks appear in Splunk.

## What I found
- The attack was very fast (around 5 seconds).  
- I observed 12 failed login attempts (Event ID 4625) for account `workmachine_1` from IP `10.0.2.15`.  
- Immediately after the 13th attempt, the account was locked (Event ID 4740).

## Self-Correction
At first, I missed the lockout event, but after searching for Event ID 4740, I confirmed the account was automatically locked.

## My Conclusion
The account lockout policy worked as expected. Next time, I plan to configure a Splunk alert to detect account lockouts automatically.
