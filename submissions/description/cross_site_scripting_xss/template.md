# Generic XSS

## Overview

<!--
Provide a 1-2 sentence description - see http://cveproject.github.io/docs/content/key-details-phrasing.pdf for tips

This format is a good guide:
[VULNTYPE] in [COMPONENT] in [APPLICATION] allows [ATTACKER] to [IMPACT] via [VECTOR]
-->

XSS in {{application}} of {{target}} allows malicious attacker to {{action}}

## Walkthrough & PoC

<!--
Provide a step-by-step walkthrough on how to access the vulnerable injection point, and how to exploit the vulnerability.
Adding a dot-pointed walkthrough with relevant screenshots will speed triage time and result in faster rewards!
-->

1. Navigate to {{url}}
1. Insert {{payload}} into {{parameter}} in {{url}}
1. Observe that the JavaScript payload was executed

## Vulnerability Evidence

<!--
Your submission MUST include evidence of the vulnerability and not be theoretical in nature.

For an XSS vulnerability, please include a simple URL or HTML payload that can be executed to easily demonstrate and reproduce the issue.
-->

The screenshot below demonstrates the injected JavaScript executing at {{url}}.

{{screenshot}}

## Demonstrated Impact

<!--
Attempt to escalate the XSS to perform additional actions (such as an account takeover or CSRF bypass to perform a sensitive action). If this is possible, provide a full proof-of-concept here.
-->

A malicious attacker could abuse this XSS further to {{action}} by using the following JavaScript payload.


```javascript
{{payload}}
```

You can find a screenshot of the full exploit taking place below:

{{screenshot}}

````
