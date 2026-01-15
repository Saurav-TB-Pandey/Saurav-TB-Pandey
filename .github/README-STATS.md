# GitHub Stats Auto-Update

This repository uses GitHub Actions to automatically update GitHub statistics in the README file.

## How It Works

1. **GitHub Actions Workflow** (`.github/workflows/update-stats.yml`)
   - Runs daily at 00:00 UTC
   - Can be manually triggered from the Actions tab
   - Automatically commits updates to the README

2. **Update Script** (`.github/scripts/update-stats.js`)
   - Fetches real-time data from GitHub's API
   - Calculates statistics (repos, stars, forks, commits, PRs, issues)
   - Updates the README with current values

## Manual Update

To manually update the stats:

1. Go to **Actions** tab in your GitHub repository
2. Select **Update GitHub Stats** workflow
3. Click **Run workflow** button
4. Select the branch (usually `main`)
5. Click **Run workflow** again

## What Gets Updated

- Repository count
- Total stars received
- Total forks
- Total commits (approximate)
- Pull requests count
- Issues count
- Language percentages (if available)

## Requirements

- GitHub Actions enabled
- Repository must be public (or use a Personal Access Token)
- Node.js 18+ (handled automatically by GitHub Actions)

## Troubleshooting

If stats aren't updating:
1. Check the Actions tab for any errors
2. Ensure the workflow file is in `.github/workflows/`
3. Verify the script is in `.github/scripts/`
4. Check that `package.json` exists with dependencies

