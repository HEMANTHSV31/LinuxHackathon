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

Task 2 — Accessing the page from another computer

For this task, I used the local IP address of my Linux machine:

10.10.154.24

I checked that Nginx was running on port 80 and then accessed the page from another computer connected to the same network.

From the second computer, I opened:

http://10.10.154.24

The index.html page was successfully displayed on the second computer.

I also verified the connection from the terminal and confirmed that the page was being served by Nginx.
Result

Task 2 completed successfully. The HTML page hosted on my Linux machine was accessed from another computer on the same network.
Evidence

    evidence/task2/server-ip.txt
    evidence/task2/http-response.txt
    evidence/task2/page-output.html
    evidence/task2/nginx-port.txt



Task 3 — Modify the HTML from another computer

For this task, I connected to the Linux machine from the second computer using SSH.

I modified the index.html file and added my name and roll number as required by the organizers.

After saving the changes, I accessed the hosted page again from the second computer using:

http://10.10.154.24

The updated details were displayed on the hosted page.
Result

Task 3 completed successfully. The HTML page was modified from another computer and the changes were reflected on the Nginx-hosted page.
Evidence

    evidence/task3/modified-page.html
    evidence/task3/name-roll-verification.txt
    evidence/task3/modified-index.html



Task 4 — Run a Different HTML Page on a Separate Port

For this task, I created a different HTML page and configured Nginx to serve it on port 8080.

The original hackathon page continues to run on port 80, while the new page is available on port 8080.

I verified the new page locally using:

curl http://localhost:8080

I also accessed the page from the second computer using:

http://10.10.154.24:8080

The second computer successfully displayed the new HTML page.
Result

Task 4 completed successfully. A different HTML page was served through Nginx on a separate port while the original page continued to run on port 80.
Evidence

    evidence/task4/http-response.txt
    evidence/task4/page-output.html
    evidence/task4/nginx-port.txt
    evidence/task4/nginx-task4-config.txt
