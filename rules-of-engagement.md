# Rules of Engagement (RoE)

**Training exercise:** EdVyro — Legal Scope and Isolated Lab  
**Target owner/operator:** Learner operating their own Windows PC  
**Target:** OWASP Juice Shop container named `juice-shop-lab`  
**Target URL:** http://127.0.0.1:3000  
**Authorised window:** Fill in the actual date and start/end time before testing.

## 1. Authorised scope
Testing is limited to the intentionally vulnerable OWASP Juice Shop instance installed and run by the learner on their own computer, reachable through the localhost port binding `127.0.0.1:3000`.

## 2. Permitted activities
- Verify the local service is running and document its configuration.
- Manually inspect the application's pages and security controls.
- Perform low-rate, non-destructive tests against the local Juice Shop instance only.
- Capture minimal evidence needed to explain a finding and its remediation.
- Stop and document unexpected behaviour.

## 3. Explicit exclusions
- EdVyro websites or infrastructure, public IP addresses, third-party services, other students' devices or accounts.
- Denial-of-service, stress testing, credential stuffing, brute force, phishing, malware, persistence, destructive payloads, or accessing real personal data.
- Any target, host, port, or activity not explicitly listed in this document.
- Publishing secrets, tokens, session cookies, or copied personal information.

## 4. Safety controls
- Keep the published port bound to `127.0.0.1`; do not expose it to the LAN or internet.
- Use only synthetic/demo data.
- Keep test rates low and avoid destructive actions.
- Do not record passwords, access tokens, session cookies, or personal records in logs or screenshots.
- Stop if the target's identity is uncertain, unexpected external systems become involved, or the application/host becomes unstable.

## 5. Evidence and reporting
For each test, record the date/time, objective, steps, observed result, minimal evidence, impact, recommended remediation, and retest result. Distinguish observed facts from assumptions. Do not claim a vulnerability without evidence.

## 6. Shutdown
When finished, stop the lab with:
```powershell
docker stop juice-shop-lab
```

## 7. Learner acknowledgement — complete before testing
I confirm that I will test only the target and activities defined above, that I own/control the local lab, and that I will stop if testing leaves the authorised scope.

**Learner name:** __________________________________  
**Signature (type or sign):** ________________________  
**Date:** __________________________________________  
**Authorised test window:** __________________________

*This is the learner's scope statement, not authorisation from EdVyro or any third party.*
