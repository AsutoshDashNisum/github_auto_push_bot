# GitHub Daily Auto-Commit Bot

This repository contains a GitHub Actions workflow that automatically makes a daily commit to keep your contribution graph active or simply to log daily activities.

## Features
- **Automated**: Runs every day at 10:00 AM IST (04:30 UTC).
- **Manual Trigger**: Can be run manually via the "Actions" tab.
- **Simple**: Updates a single file `auto_commit_log.txt` with the current timestamp.
- **Secure**: Uses the built-in `GITHUB_TOKEN`, no personal access tokens required.

## Setup Instructions

1. **Create a Repository**: Create a new repository on GitHub (or use this one).
2. **Push the Code**: Ensure the following files are in your repository:
   - `.github/workflows/daily_commit.yml`
   - `auto_commit_log.txt`
   - `README.md`
3. **Enable Workflow Permissions**:
   - Go to your repository **Settings** > **Actions** > **General**.
   - Under **Workflow permissions**, select **Read and write permissions**.
   - Click **Save**.
4. **Sit back and relax**: The bot will run automatically at the scheduled time!

## How it works
The workflow script performs these steps:
1. Checks out your repository code.
2. Appends the current UTC timestamp to `auto_commit_log.txt`.
3. Commits the change with the message: `🤖 Daily auto-commit - YYYY-MM-DD`.
4. Pushes the commit back to your repository.

---
*Created with ❤️ using Antigravity.*
