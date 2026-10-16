# MSME Profile Automations

This repository contains GitHub Actions that automatically create new public repositories every week to keep the GitHub profile active and showcase practical fintech work for Indian MSMEs.

## Setup required

1. Create a **Personal Access Token (classic)** with these scopes:
   - `repo` (full control of private repositories)
   - `public_repo` (access public repositories)

   Or use a fine-grained token with **Contents: Read and write** and **Administration: Read and write** on your user account / repositories.

2. Add the token as a repository secret:
   - Go to **Settings → Secrets and variables → Actions**
   - New repository secret
   - Name: `REPO_CREATOR_TOKEN`
   - Value: your PAT

3. The workflow runs every **Monday at 10:00 AM IST** (or you can trigger it manually from the Actions tab).

## What it creates

- A new public repo with a unique name like `msme-fintech-tool-YYYYMMDD`
- Auto-initialized with a README
- Description related to MSME cash-flow, invoicing, GST, UPI, or grants

You can later improve the workflow to add more files, better content, or different templates.

## Manual trigger

Go to **Actions → Weekly MSME Fintech Repo Creator → Run workflow**.
