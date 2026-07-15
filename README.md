# DecodeLabs — Project 2: The Server Commander

Cloud Computing Internship (AWS/Azure) — DecodeLabs, July 2026

## What this project does

Provisions a Linux virtual server on AWS EC2 from scratch, secures it, and
deploys a live web server hosting a custom static webpage — without using
any managed/serverless hosting. The goal was to practice full sysadmin-level
control over a cloud instance rather than relying on abstracted services.

## What I did

- Launched an Amazon Linux 2023 EC2 instance (t3.micro) using an IAM user
  (not root), with MFA enabled
- Created and secured an SSH key pair for authentication
- Configured a security group to allow SSH only from my own IP, and HTTP
  from anywhere
- Connected to the instance via SSH
- Installed and enabled Nginx as a system service using `dnf`
- Edited the served HTML file directly on the server via the terminal
- Styled the page with embedded CSS (flexbox) to center the heading
- Verified the page was publicly reachable over the internet
- Pulled the final file back to my local machine via `scp` and pushed it
  to this repo

## Tools used

AWS EC2, Amazon Linux 2023, Nginx, SSH, Git/GitHub

## Live verification

Confirmed the page loading correctly from an external network, separate
from the one used to provision the server.