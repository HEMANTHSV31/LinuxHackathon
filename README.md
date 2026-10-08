# LinuxHackathon

## Task 1 — Nginx Server Setup

### Objective

Set up Nginx to serve the custom HTML page provided by the organizers.

### Implementation

Apache2 was using port 80, so it was stopped and disabled.

Nginx was started and configured to serve:

`/home/hemanth-sv/hackathon-nginx`

The Nginx configuration was tested successfully and the service was reloaded.

### Verification

Command:

curl -I http://localhost


Result:

HTTP/1.1 200 OK Server: nginx/1.28.3 (Ubuntu)


The custom HTML page was verified using:

curl http://localhost


The page displays the organizer-provided Linux Community / OpenHack Hackathon content.

### Evidence

- `evidence/task1/nginx-status.txt`
- `evidence/task1/http-response.txt`
- `evidence/task1/page-output.html`
- `evidence/task1/nginx-config.txt`
- `evidence/task1/nginx-test.txt`
