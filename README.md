# Isabelle Seepersaud - Personal Portfolio Website

This is a personal portfolio website for Isabelle Seepersaud, featuring information about hobbies, career, resume, and projects.

## How to Open/View the Website

This is a static HTML website that can be opened in several ways:

### Method 1: Open Directly in Browser (Simplest)

1. Navigate to the `misproject/media/` folder
2. Double-click on `index.html` to open it in your default web browser
3. Or right-click `index.html` → "Open with" → Choose your preferred browser (Chrome, Firefox, Safari, Edge, etc.)

**File path:** `misproject/media/index.html`

### Method 2: Use a Local Web Server (Recommended for Full Functionality)

Some features like video playback and certain styling may work better with a local web server:

#### Using Python (if installed):

```bash
# Navigate to the website directory
cd misproject/media

# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

Then open your browser and go to: `http://localhost:8000`

#### Using Node.js (if installed):

```bash
# Install http-server globally (one-time setup)
npm install -g http-server

# Navigate to the website directory
cd misproject/media

# Start the server
http-server -p 8000
```

Then open your browser and go to: `http://localhost:8000`

#### Using PHP (if installed):

```bash
# Navigate to the website directory
cd misproject/media

# Start PHP built-in server
php -S localhost:8000
```

Then open your browser and go to: `http://localhost:8000`

### Method 3: Deploy to GitHub Pages

To make the website publicly accessible:

1. Go to your GitHub repository settings
2. Navigate to "Pages" section
3. Under "Source", select the branch you want to deploy
4. Set the folder to `/misproject/media` or move the contents to root and select `/ (root)`
5. Click "Save"
6. Your website will be available at: `https://[username].github.io/[repository-name]/`

## Website Structure

```
isabelle-seepersaud/
└── misproject/
    ├── CSS/                 # Stylesheets
    ├── images/              # Image assets
    ├── js/                  # JavaScript files
    ├── files/               # Additional files
    └── media/
        ├── index.html       # Main homepage (START HERE)
        ├── hobbies.html     # Hobbies page
        ├── career.html      # Career information
        ├── resume.html      # Resume page
        ├── discover.html    # Discover UMD page
        ├── game.html        # Interactive game
        └── code.html        # Code projects
```

## Navigation

Once the website is open, you can navigate using the menu bar at the top:

- **Home** - Main landing page with introduction
- **Hobbies** - Personal interests and activities
- **Discover UMD** - Information about University of Minnesota Duluth
- **Resume** - Professional resume
- **Career** - Career goals and information
- **Game** - Interactive element
- **Contact** - Email contact button

## Browser Compatibility

The website works best with modern browsers:
- Google Chrome (recommended)
- Mozilla Firefox
- Microsoft Edge
- Safari
- Opera

## Troubleshooting

**Issue:** Images or videos don't display
- **Solution:** Make sure you're viewing from the correct directory (`misproject/media/`) or use a local web server (Method 2)

**Issue:** Styling looks broken
- **Solution:** Ensure the CSS folder is in the correct location relative to the HTML files, or use a local web server

**Issue:** Links don't work
- **Solution:** Use a local web server (Method 2) for the best experience

## Quick Start

**The fastest way to view the website:**

1. Open a terminal/command prompt
2. Navigate to the project folder:
   ```bash
   cd misproject/media
   ```
3. If you have Python installed, run:
   ```bash
   python -m http.server 8000
   ```
4. Open your browser and visit: `http://localhost:8000`

---

© 2025 Isabelle Seepersaud. All rights reserved.
