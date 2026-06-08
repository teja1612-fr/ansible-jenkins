# Ansible + Jenkins CI/CD Pipeline

## What This Does
Automates application deployment using Jenkins for pipeline 
orchestration and Ansible for multi-server configuration management.

## Tech Stack
Jenkins · Ansible · GitHub Webhooks · Linux

## How It Works
1. Code push to GitHub triggers Jenkins pipeline via webhook
2. Jenkins executes the Ansible playbook automatically
3. Ansible connects to target servers via inventory.ini
4. Playbook configures and deploys the application across all servers

## Files
- `Jenkinsfile` — Pipeline stages definition
- `playbook.yml` — Ansible tasks for server configuration
- `inventory.ini` — Target server groups and IPs

## Key Concepts Demonstrated
- CI/CD automation with zero manual deployment steps
- Multi-server configuration management with Ansible
- Idempotent playbook design safe to re-run anytime
