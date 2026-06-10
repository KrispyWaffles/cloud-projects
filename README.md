# Lab 01 — Static Website Hosting on S3

## Overview
**Service(s):** Amazon S3  
**CLF-C02 Domain:** Cloud Technology & Services  
**Date Completed:** June 8, 2026  
**Status:** ✅ Complete  

---

## What I Built
Built and deployed a static website to AWS S3. Created a simple HTML page locally in VS Code, provisioned an S3 bucket, configured AWS CLI with IAM credentials, and pushed the file from my local repo to the bucket using the CLI. Enabled static website hosting and set a public bucket policy to make the site accessible via the S3 endpoint URL. Also set up a zero-spend billing alert and created a dedicated IAM user with programmatic access to keep the root account secure.

---

## Key Steps
- Created a new AWS account with zero-spend billing alert
- Created IAM user `cli-admin` with programmatic access keys
- Installed and configured AWS CLI in VS Code terminal
- Created S3 bucket `wess-cloud-lab-site`
- Disabled Block Public Access and added public read bucket policy
- Uploaded `index.html` via `aws s3 sync`
- Enabled static website hosting with `index.html` as index document

-----

## Site URL
`http://wess-cloud-lab-site.s3-website-us-east-1.amazonaws.com`

---

## Gotchas
- Access Key ID must start with `AKIA` — easy to mix up with the Secret Access Key
- Block Public Access must be disabled before the bucket policy takes effect
- `aws s3 sync` won't upload a file that doesn't exist in the current directory — always verify with `ls` first

---

## Key Concepts Reinforced
- S3 bucket policies vs Block Public Access settings
- IAM users and programmatic access keys
- AWS CLI configuration and authentication
- Static hosting vs dynamic hosting

---

## Next Steps
- [ ] Add CloudFront in front of the site (HTTPS + CDN)
- [ ] Enable S3 versioning
- [ ] Add a custom error page