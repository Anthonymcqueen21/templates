# Weak Login Function on Non-Operational Endpoint

## Overview
Weak login function on non-operational endpoint allows a malicious attacker to Man-In-The-Middle (MiTM) login requests to sniff usernames and passwords.

<!--
**Please replace text in each section below**

HTTPS not Available or HTTP by default on Login Page Vulnerability Report

Resources:

- <https://owasp.org/www-project-top-ten/2017/A3_2017-Sensitive_Data_Exposure>
-->

## Walkthrough & PoC

<!-- Provide a step-by-step walkthrough on how to access the vulnerable injection point, and how to exploit the vulnerability.
Adding a dot-pointed walkthrough with relevant screenshots will speed triage time and result in faster rewards!

Example:

1. Browse to the URL <www.inscope.com/login>
1. Attempt to sign into the website using the login button
1. Observe the page running on HTTP as default

1. Run the following command on a machine with cURL installed
```bash
curl -I www.inscope.com/login
```
1. Observe the repsonse showing a 200 OK on the HTTP response

 -->

1. Navigate to Bugcrowd.com/vulnerable-endpoint or x.x.x.x:

{{screenshot}}

1. Man-in-The-Middle (MiTM) communication using {{software}} and route traffic through your computer:

{{screenshot}}

1. Send request on Bugcrowd.com/vulnerable to see the the requests are unencrypted in transit


## Vulnerability Evidence

<!-- 
Your submission MUST include evidence of the vulnerability and not be theoretical in nature.

This can include a cURL response from the website showing that HTTP is default or HTTPS is not avalible.
 -->

The following image(s) show the full exploit:
{{screenshot}}

## Demonstrated Impact
<!--
Demonstrating increased impact results in higher rewards! 

Credentials transmitted over HTTP are transmitted in Plaintext, allowing any attacker to intercept these requests, and obtain the login credentials for that user. 
-->

A malicious attacker can MiTM communication between the user and the application on the specified IP to steal administrative credentials and login to the system using admin privileges.
