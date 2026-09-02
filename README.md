# Shell Scripting + DevOps Interview Questions

This repository contains commonly asked **shell scripting** and **DevOps** interview questions with short, practical answers.

## Shell Scripting Interview Questions

1. **What is shebang in a shell script?**  
   `#!/bin/bash` tells the system which interpreter should run the script.

2. **How do you make a script executable?**  
   `chmod +x script.sh` and then run `./script.sh`.

3. **Difference between `$*` and `$@`?**  
   Both represent all positional parameters, but `"$@"` preserves each argument as a separate word.

4. **How do you read user input in Bash?**  
   Use `read`, for example: `read -p "Name: " name`.

5. **How do you check exit status of the previous command?**  
   Use `$?`. `0` means success, non-zero means failure.

6. **What is the difference between `>` and `>>`?**  
   `>` overwrites a file, `>>` appends to a file.

7. **How do you run a command only if the previous one succeeds?**  
   Use `&&`, e.g., `build && deploy`.

8. **How do you run a command regardless of previous command success/failure?**  
   Use `;` to separate commands.

9. **How do you debug a shell script?**  
   Run with `bash -x script.sh` or set `set -x` inside script.

10. **What do `set -e` and `set -u` do?**  
    `set -e` exits on command failure, `set -u` errors on unset variables.

11. **How do you iterate over files in a directory?**  
    `for f in /path/*; do echo "$f"; done`

12. **How do you schedule a script to run every day?**  
    Use `cron` with crontab, e.g., `0 2 * * * /path/backup.sh`.

## DevOps Interview Questions

1. **What is DevOps?**  
   A culture and practice that combines development and operations to deliver software faster and more reliably.

2. **What is CI/CD?**  
   CI (Continuous Integration) automatically builds/tests code changes; CD (Continuous Delivery/Deployment) automates release flow.

3. **Difference between Continuous Delivery and Continuous Deployment?**  
   Delivery requires manual approval to production; Deployment automatically pushes to production after passing checks.

4. **What is Infrastructure as Code (IaC)?**  
   Managing infrastructure using code (e.g., Terraform, CloudFormation) for repeatability and version control.

5. **What is configuration management?**  
   Maintaining system consistency using tools like Ansible, Puppet, or Chef.

6. **What is containerization and why use Docker?**  
   Packaging app + dependencies into portable containers for consistent environments.

7. **What is Kubernetes used for?**  
   Orchestrating containers: deployment, scaling, self-healing, and service discovery.

8. **What are blue-green and canary deployments?**  
   Blue-green switches traffic between two environments; canary rolls out gradually to a small user subset first.

9. **Why is monitoring important in DevOps?**  
   It helps detect failures early, maintain SLAs, and improve reliability.

10. **What is the purpose of log aggregation?**  
    Centralizing logs (e.g., ELK, Loki) for troubleshooting, auditing, and observability.

11. **What are common CI/CD tools?**  
    Jenkins, GitHub Actions, GitLab CI, CircleCI, Azure DevOps.

12. **What is rollback in deployment?**  
    Reverting to a previous stable version when a release fails.

## Scenario-Based Questions

1. **A deployment fails midway. What do you do first?**  
   Stop further rollout, check logs/alerts, rollback if needed, and communicate status.

2. **How do you handle flaky tests in a pipeline?**  
   Identify root cause, quarantine unstable tests, and fix them quickly to keep trust in CI.

3. **A script works locally but fails in CI. What can be wrong?**  
   Environment differences, missing dependencies, permissions, shell differences, or unset variables.

4. **How would you secure secrets in CI/CD?**  
   Use secret managers or CI encrypted secrets; never hardcode credentials in code.

---

If you want, this list can be expanded with advanced topics (networking, security, cloud architecture, and SRE interview rounds).
