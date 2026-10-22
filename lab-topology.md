# Lab Topology

## Purpose
A local training setup for the EdVyro “Legal Scope and Isolated Lab” task.

```text
+-------------------------------------------+
| Windows PC (learner's own computer)       |
|                                           |
|  Browser                                  |
|       | http://127.0.0.1:3000             |
|       v                                   |
|  Docker Desktop (Linux / WSL2 backend)    |
|       | published port bound to loopback  |
|       v                                   |
|  Container: juice-shop-lab                |
|  Image: bkimminich/juice-shop:latest      |
|  Container port: 3000                     |
+-------------------------------------------+

No public target is in scope.
```

## Observed configuration
The learner's `docker ps` output showed a running `juice-shop-lab` container with `127.0.0.1:3000->3000/tcp`. The learner confirmed that the page opened in the browser.

## Interpretation and limitations
- `127.0.0.1` is the host's loopback address. Binding the published port to it prevents access to this published port from other machines on the LAN.
- This does not turn off the computer's internet connection and does not prove complete isolation of all container networking.
- Do not change the port binding to `0.0.0.0` or expose the target publicly.
- Only the learner's own Juice Shop container is authorised for testing.

## Evidence to attach
Add real screenshots to the repository's `evidence/` folder:
1. Docker container status and published port.
2. Browser showing the local application URL.
3. Output of `docker port juice-shop-lab`.

Redact personal data and secrets before uploading.
