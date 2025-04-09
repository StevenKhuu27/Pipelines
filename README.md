# Security Pipelines 
Repo to store github action pipelines.
This is a compilation of all the scanning github actions tools I have used over my career. Some are from different projects so there are multiple of the same sorts of scanning, pick and choose as needed.

### For additional security:
- Enable GitHub Advanced Security (includes CodeQL and secret scanning)
- Used dependabot to monitor and auto-update insecure dependencies
```
  version: 2
updates:
  - package-ecosystem: "npm"
    directory: "/"
    schedule:
      interval: "weekly"
  - package-ecosystem: "pip"
    directory: "/"
    schedule:
      interval: "weekly"
```
- Branch protection rules

There are also SAST and DAST scanning tools that have been shared during a call with GitLab:
https://gitlab.com/bpark-customer-demos/autodevops
