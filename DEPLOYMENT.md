# GitHub Pages Deployment Instructions

This repository is now configured to automatically deploy to GitHub Pages using GitHub Actions.

## Setup Steps

To complete the GitHub Pages setup, follow these steps:

### 1. Enable GitHub Pages in Repository Settings

1. Go to your repository on GitHub: `https://github.com/sambapos/json_extractor`
2. Click on **Settings** tab
3. In the left sidebar, click on **Pages** (under "Code and automation")
4. Under **Source**, select **GitHub Actions**
5. Save the changes

### 2. Merge this Pull Request

Once you merge this PR to the main/master branch, the GitHub Actions workflow will automatically:
- Build and deploy your site
- Make it available at `https://sambapos.github.io/json_extractor/`

### 3. Trigger the Workflow

The workflow will automatically run when:
- You push to the main or master branch
- You manually trigger it from the Actions tab (using workflow_dispatch)

### 4. Access Your Site

After the workflow completes successfully, your JSON Extractor tool will be available at:
**https://sambapos.github.io/json_extractor/**

## Workflow Details

The GitHub Actions workflow (`deploy.yml`) does the following:
- Checks out the repository code
- Configures GitHub Pages
- Uploads all files as a Pages artifact
- Deploys the artifact to GitHub Pages

## Troubleshooting

If the deployment fails:
1. Check the Actions tab in your repository for error logs
2. Ensure GitHub Pages is enabled in Settings → Pages
3. Verify that the source is set to "GitHub Actions"
4. Check that you have the necessary permissions (pages: write)

## Files Added

- `.github/workflows/deploy.yml` - GitHub Actions workflow for deployment
- `README.md` - Updated with live demo link
- `DEPLOYMENT.md` - This file with deployment instructions
