# GitHub Pages Deployment Guide

## What Was Done

This repository has been configured for automatic deployment to GitHub Pages. Here's what was set up:

### 1. Project Restructuring
- Moved all HTML files from `misproject/media/` to the root directory
- Organized assets into logical directories:
  - `CSS/` - Stylesheets
  - `media/images/` - Image files
  - `media/` - Video and audio files
  - `files/` - Downloadable files (PDFs)
  - `js/` - JavaScript files

### 2. Path Updates
All file references in HTML files were updated to reflect the new structure:
- CSS: `../CSS/` → `CSS/`
- Images: `images/` → `media/images/`
- Media files: Direct references → `media/filename`
- Files: `../files/` → `files/`

### 3. GitHub Actions Workflow
Created `.github/workflows/deploy.yml` that:
- Triggers on pushes to the `main` branch
- Can also be triggered manually via workflow_dispatch
- Deploys the entire repository root to GitHub Pages

### 4. Documentation
- Added `README.md` with project overview
- Added `.gitignore` to exclude system files
- Created this deployment guide

## How to Publish

### Step 1: Enable GitHub Pages
1. Go to repository Settings
2. Navigate to "Pages" in the left sidebar
3. Under "Source", select **"GitHub Actions"**
4. Save the settings

### Step 2: Merge to Main
Once this PR is merged to the `main` branch, the workflow will automatically:
1. Check out the code
2. Configure GitHub Pages
3. Upload the site as an artifact
4. Deploy to GitHub Pages

### Step 3: Access Your Website
After successful deployment, your website will be available at:
**https://seepe003-lgtm.github.io/isabelle-seepersaud/**

## Manual Deployment

You can also trigger deployment manually:
1. Go to the "Actions" tab in your repository
2. Select "Deploy to GitHub Pages" workflow
3. Click "Run workflow"
4. Select the `main` branch
5. Click "Run workflow"

## Verifying Deployment

After deployment:
1. Check the Actions tab for workflow status
2. Visit the deployed URL
3. Test all navigation links
4. Verify images, videos, and downloads work correctly

## Troubleshooting

If the deployment fails:
1. Check the Actions tab for error messages
2. Ensure GitHub Pages is enabled with "GitHub Actions" as source
3. Verify the workflow file is in `.github/workflows/`
4. Check that all file paths are correct and case-sensitive

## Local Testing

To test the site locally before deployment:
```bash
# Using Python's built-in HTTP server
python -m http.server 8000

# Or using Node.js http-server
npx http-server
```

Then visit http://localhost:8000 in your browser.

## Files Structure

```
/
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions workflow
├── CSS/
│   ├── styles.css              # Custom styles (currently empty)
│   └── template.css            # Template styles
├── media/
│   ├── images/                 # Website images
│   ├── discover.mp4            # Discover UMD video
│   └── retro-arcade-game-music-297305.mp3  # Game audio
├── files/
│   └── final resume.pdf        # Downloadable resume
├── js/
│   ├── game.js                 # Game JavaScript
│   └── scrip.js                # Additional scripts
├── index.html                  # Home page
├── hobbies.html                # Hobbies page
├── discover.html               # Discover UMD page
├── resume.html                 # Resume page
├── career.html                 # Career page
├── game.html                   # Game page
├── README.md                   # Project documentation
└── .gitignore                  # Git ignore rules
```

## Next Steps

1. Review and merge this PR to the main branch
2. Enable GitHub Pages in repository settings (select "GitHub Actions" as source)
3. Wait for the workflow to complete
4. Visit your published website!
5. Share your website URL with others

## Notes

- The workflow only runs on the `main` branch
- Changes to other branches won't trigger deployment
- You can view deployment history in the Actions tab
- The site updates automatically when you push to main

