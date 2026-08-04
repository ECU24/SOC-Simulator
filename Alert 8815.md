# 8815 - Inbound Email Containing Suspicious External Link (Amazon Impersonation)

## Alert Details
![Original Alert](screenshots/Evidence-8815/Alert-Details-2.png)

<h3>🕣 Time & Date of the activity:</h2>
Time of Alert: 27/07/2026 5:43 pm

<h3>🖥️ List of affected entities:</h3>

- h.harris@thetrydaily.thm — recipient of the phishing email
- h.harris's endpoint/workstation — proxy and firewall logs showed a 
  connection attempt to the suspicious link (http://bit.ly/3sHkX3da12340) 
  from source IP 10.20.2.17 (Hannah Harris's workstation). The connection 
  was blocked by the firewall.

<h3>🧐 Investigation Steps Taken:</h3>

1. Reviewed the email content and headers — sender domain amazon.biz is not 
   an official Amazon domain (legitimate Amazon domains are amazon.com and 
   regional variants). The link within the email is an unencrypted HTTP 
   link (http://bit.ly/3sHkX3da12340), which is a further indicator the 
   link is unsafe.

2. Noted urgency tactics used in the email content — a "48 hour deadline" 
   and "Action Required" language — along with a shortened URL (bit.ly), 
   which obscures the true destination.

3. Searched Splunk SIEM email logs for the domain amazon.biz — only one 
   email was found sent from this domain to h.harris@thetrydaily.thm, at 
   17:43.

4. Searched proxy and firewall logs for http://bit.ly/3sHkX3da12340 — the 
   link was accessed from source IP 10.20.2.17 at 17:45, less than 2 
   minutes after the email was received. However, the connection was 
   blocked by the firewall, preventing Hannah from reaching the malicious 
   website.

<h3>🕵️‍♂️ Evidence</h3>






