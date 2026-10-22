# Isolated Lab Setup Report

## 1. Objective
Set up an intentionally vulnerable web application locally for authorised ethical-hacking practice, with clearly documented scope and safe boundaries.

## 2. Environment
- Host OS: Windows (exact version not recorded in the evidence available so far).
- Container runtime: Docker Desktop, Linux/WSL2 backend.
- Image: `bkimminich/juice-shop:latest`.
- Container: `juice-shop-lab`.
- Local address: `http://127.0.0.1:3000`.

## 3. Setup evidence observed
The learner provided PowerShell output showing:
- Docker Engine information was available.
- The Juice Shop container was running.
- Port mapping was `127.0.0.1:3000->3000/tcp`.
- The learner confirmed the application opened in a browser.

Add screenshots to `evidence/` so the setup can be independently reviewed.

## 4. Test methodology and results
**Security testing status: not yet performed/documented.** The setup and browser availability were verified by the learner, but no security test results have been provided. No vulnerabilities or clean bill of health are claimed.

For each future test, use this template:

| Field | Record |
|---|---|
| Test ID / date | |
| Objective | |
| Scope confirmation | |
| Steps performed | |
| Observed result | |
| Evidence filename | |
| Impact / risk rationale | |
| Recommended remediation | |
| Retest result | |

## 5. Limitations
A localhost port binding restricts access through that published port to the local machine. It does not disable the host's internet connection or establish complete isolation of all container networking. The Docker image tag `latest` can change over time; record the image ID used if reproducibility is required.

## 6. Evidence checklist
- [ ] Screenshot of `docker ps` showing `127.0.0.1:3000->3000/tcp`.
- [ ] Screenshot of Juice Shop open at `http://127.0.0.1:3000`.
- [ ] Screenshot/output of `docker port juice-shop-lab`.
- [ ] Signed and dated Rules of Engagement.
- [ ] Test notes and evidence, only after tests are actually performed.
- [ ] Retest results or a clear statement that retesting was not performed.

## 7. Short walkthrough outline
1. State the objective and legal scope.
2. Show the Docker container and localhost port binding.
3. Open the Juice Shop browser page.
4. Show the topology and signed RoE.
5. Explain actual test results and limitations; do not claim unperformed tests.

## 8. Submission
Repository: https://github.com/habinharis369-spec/edvyro-ethical-hacking-lab
