# 8817 - Inbound Email Containing Suspicious External Link (Microsoft Support Impersonation)

## Alert Details
![Original Alert](screenshots/Evidence-8817/Alert-Details-4.png)

<h3>🕣 Time & Date of the activity:</h2>
Time of Alert: 27/07/2026 5:46 pm

<h3>🖥️ List of affected entities:</h3>

- c.allen@thetrydaily.thm — recipient of the phishing email
- c.allen's endpoint/workstation — proxy and firewall logs showed a 
  connection attempt to the suspicious link (https://m1crosoftsupport.co/login) 
  from source IP 10.20.2.25, which is c.allen's (Charlotte Allen's) IP 
  address. This connection was allowed.



