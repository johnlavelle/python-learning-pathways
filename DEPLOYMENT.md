# GitLab Pages Deployment Guide

This guide explains how to deploy the Slidev presentation to GitLab Pages.

## Automatic Deployment Setup

The repository is now configured for automatic deployment to GitLab Pages. Here's what has been set up:

### 1. `.gitignore` File
Created to exclude build artifacts and dependencies from version control:
- `node_modules/`
- `dist/` (build output)
- Other temporary files

### 2. `.gitlab-ci.yml` Pipeline
Updated to handle the build and deployment process:
- **Build stage**: Installs dependencies and builds the presentation with the correct base path
- **Deploy stage**: Copies the built files to the `public` directory for GitLab Pages

## Manual Steps Required

### 1. Commit and Push Changes
```bash
# Add the new/modified files
git add .gitignore .gitlab-ci.yml

# Commit the changes
git commit -m "Add GitLab Pages deployment configuration"

# Push to GitLab
git push origin master
```

### 2. Enable GitLab Pages
1. Go to your GitLab project: https://gitlab.dmi.dk/jola/pathways_to_learn_python_for_scientific_software_development
2. Navigate to **Settings** → **Pages**
3. GitLab Pages should be automatically enabled once the pipeline runs

### 3. Access Your Deployed Site
After the pipeline completes successfully, your presentation will be available at:
```
https://jola.pages.dmi.dk/pathways_to_learn_python_for_scientific_software_development/
```

## Building Locally with Base Path

If you need to build the presentation locally with the correct base path for GitLab Pages:

```bash
# Install dependencies
npm install

# Build with base path
npm run build -- --base /pathways_to_learn_python_for_scientific_software_development/

# The built files will be in the dist/ directory
```

## Troubleshooting

### Pipeline Fails
- Check the CI/CD → Pipelines section in GitLab for error messages
- Ensure all dependencies are listed in `package.json`
- Verify the `site` runner tag is available in your GitLab instance

### Page Not Found (404)
- Ensure the base path in the build command matches your project path
- Check that the `public` directory is created correctly in the pipeline
- Verify GitLab Pages is enabled in project settings

### Styling Issues
- The base path must be correctly set for assets to load properly
- Check browser console for 404 errors on assets

## Alternative: Deploy Pre-built Files

If you want to deploy the existing `dist/` directory without rebuilding:

1. Remove `dist/` from `.gitignore`
2. Commit the `dist/` directory
3. The pipeline will use the existing built files

```bash
# Remove dist/ from .gitignore
sed -i '/^dist\/$/d' .gitignore

# Add and commit the dist directory
git add dist/
git commit -m "Add pre-built presentation files"
git push origin master
```

## Notes

- The pipeline runs on pushes to `master` or `main` branches
- Build artifacts are kept for 1 week
- The `site` runner tag is preserved from the original configuration
- Node.js 18 Alpine image is used for smaller size and faster builds