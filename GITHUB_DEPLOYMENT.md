# GitHub Pages Deployment Guide

This guide explains how to deploy the Slidev presentation to GitHub Pages.

## Prerequisites

- GitHub account (username: johnlavelle)
- Node.js and npm installed locally
- Git configured with GitHub credentials

## Setup Steps

### 1. Create GitHub Repository

1. Go to https://github.com/new
2. Create a new repository (e.g., `python-learning-pathways`)
3. Don't initialize with README, .gitignore, or license

### 2. Update Git Remote

```bash
# Remove GitLab remote
git remote remove origin

# Add GitHub remote (replace with your actual repository name)
git remote add origin https://github.com/johnlavelle/python-learning-pathways.git

# Verify the change
git remote -v
```

### 3. Push to GitHub

```bash
# Push all branches and tags
git push -u origin master
```

### 4. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **Settings** tab
3. Scroll down to **Pages** section
4. Under **Source**, select **GitHub Actions**
5. Save the changes

## Automatic Deployment

The repository includes a GitHub Actions workflow (`.github/workflows/deploy.yml`) that:

1. Triggers on every push to `main` or `master` branch
2. Builds the Slidev presentation with the correct base path
3. Deploys to GitHub Pages automatically

### Build Process

- Uses Node.js 18
- Installs dependencies from `package.json`
- Builds with base path: `/<repository-name>/`
- Deploys the `dist/` directory to GitHub Pages

## Accessing Your Deployed Presentation

After the first deployment completes, your presentation will be available at:

```
https://johnlavelle.github.io/<repository-name>/
```

Replace `<repository-name>` with your actual repository name.

## Manual Deployment (Optional)

If you need to build and deploy manually:

```bash
# Install dependencies
npm install

# Build with GitHub Pages base path
npm run build -- --base /<repository-name>/

# The built files will be in the dist/ directory
```

## Monitoring Deployments

1. Go to the **Actions** tab in your GitHub repository
2. You'll see the deployment workflow running
3. Click on a workflow run to see detailed logs
4. Green checkmark = successful deployment

## Troubleshooting

### Build Fails
- Check the Actions tab for error messages
- Ensure `package.json` and `package-lock.json` are committed
- Verify all dependencies are properly listed

### 404 Error
- Wait a few minutes for GitHub Pages to propagate
- Check that GitHub Pages is enabled in Settings
- Verify the base path in the build command matches your repository name

### Assets Not Loading
- Ensure the base path is correctly set in the build command
- Check browser console for 404 errors on assets
- Verify the repository name in the URL matches the base path

## Updating Content

1. Edit `slides.md` locally
2. Test locally: `npm run dev`
3. Commit and push changes
4. GitHub Actions will automatically rebuild and deploy

## Custom Domain (Optional)

To use a custom domain:

1. Go to Settings → Pages
2. Add your custom domain
3. Create a CNAME file in the repository root
4. Configure DNS records with your domain provider