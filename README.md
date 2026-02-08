# NFT Marketplace Landing Page

A modern, responsive NFT marketplace landing page built with vanilla HTML and CSS. This project recreates a professional NFT marketplace design with clean structure and styling.

---

## Table of Contents

- [Getting Started](#getting-started)
- [Git Workflow Guide](#git-workflow-guide)
- [Project Structure](#project-structure)
- [CSS Implementation Pseudo Code](#css-implementation-pseudo-code)
- [Design Specifications](#design-specifications)
- [Resources](#resources)

---

## Getting Started

### Prerequisitesgit@github.com:BeneDefi/nft-marketplace.git

- Git installed on your computer ([Download Git](https://git-scm.com/downloads))
- A text editor (VS Code, Sublime Text, etc.)
- A GitHub account ([Sign up here](https://github.com/join))
- Basic understanding of HTML and CSS

### Initial Setup

1. **Create a GitHub Account** (if you don't have one)
   - Go to https://github.com/join
   - Follow the registration steps
   - Verify your email address

2. **Install Git**
   - Download from https://git-scm.com/downloads
   - Follow installation instructions for your OS
   - Verify installation: Open terminal and type `git --version`

---

## Git Workflow Guide

### Step 1: Clone the Repository

```bash
# Navigate to where you want to store the project
cd ~/Documents/Projects

# Clone the repository (replace YOUR-USERNAME with your GitHub username)
git clone https://github.com/YOUR-USERNAME/nft-marketplace.git

# Navigate into the project folder
cd nft-marketplace
```

**What this does:**
- `git clone` creates a copy of the repository on your local machine
- You now have all project files in a folder called `nft-marketplace`

---

### Step 2: Create a New Branch

```bash
# Check which branch you're on (should be 'main' or 'master')
git branch

# Create a new branch for your work
git checkout -b feature/implement-css-styling

# Verify you're on the new branch
git branch
```

**What this does:**
- `git checkout -b` creates a new branch AND switches to it
- Branch naming convention: `feature/description-of-work`
- Working on a separate branch keeps your main code safe

**Why use branches?**
- Keep your main branch clean and stable
- Work on features independently
- Easy to undo changes if something goes wrong
- Multiple people can work on different features simultaneously

---

### Step 3: Make Your Changes

1. Open the project in your text editor
2. Create your CSS file: `styles.css`
3. Implement the styling (see Pseudo Code section below)
4. Test your changes in a browser

---

### Step 4: Stage Your Changes

```bash
# Check what files have changed
git status

# Add specific files to staging area
git add nft-styles.css
git add nft-marketplace.html

# OR add all changed files at once
git add .

# Verify files are staged
git status
```

**What this does:**
- `git status` shows which files have been modified
- `git add` prepares files to be committed
- Staged files appear in green when you run `git status`

**Best Practice:**
- Review your changes before staging: `git diff filename`
- Stage related changes together for cleaner commits

---

### Step 5: Commit Your Changes

```bash
# Commit with a descriptive message
git commit -m "Implement CSS styling for NFT marketplace landing page"

# For longer commit messages
git commit -m "Implement CSS styling for NFT marketplace
- Added navigation bar styling with dark theme
- Implemented hero section with responsive layout
- Styled auction and NFT cards with hover effects
- Added responsive grid layouts for all sections
- Implemented footer with newsletter form styling"
```

**What this does:**
- `git commit` saves your staged changes with a message
- Creates a snapshot of your project at this point

**Commit Message Best Practices:**
- Use present tense ("Add feature" not "Added feature")
- Be descriptive but concise
- First line should be 50 characters or less
- Add details in subsequent lines if needed

---

### Step 6: Push to GitHub

```bash
# Push your branch to GitHub for the first time
git push -u origin feature/implement-css-styling

# For subsequent pushes (after first time)
git push
```

**What this does:**
- `git push` uploads your commits to GitHub
- `-u origin feature/implement-css-styling` sets up tracking for your branch
- After the first push, you can simply use `git push`

**Troubleshooting:**
- If push fails, you may need to set up authentication
- For HTTPS: Use a personal access token instead of password
- For SSH: Set up SSH keys in GitHub settings

---

### Step 7: Create a Pull Request (PR)

1. Go to your repository on GitHub
2. You'll see a banner suggesting to create a pull request
3. Click "Compare & pull request"
4. Add a title and description for your PR
5. Click "Create pull request"

**What this does:**
- Opens your changes for review
- Allows others to see what you changed
- Starts a discussion about your code
- Prepares your work to be merged into main branch

**PR Best Practices:**
- Include screenshots of the final result
- List all major changes
- Mention any issues or limitations
- Tag relevant people for review

---

### Step 8: Merge Your Changes

Once your PR is approved:

1. Click "Merge pull request" on GitHub
2. Confirm the merge
3. Delete the branch (GitHub will suggest this)

Then update your local repository:

```bash
# Switch back to main branch
git checkout main

# Pull the latest changes (including your merged work)
git pull origin main

# Delete your local feature branch (optional)
git branch -d feature/implement-css-styling
```

---

## Common Git Commands Reference

### Checking Status
```bash
git status              # See current changes
git log                 # View commit history
git log --oneline       # Compact commit history
git diff                # See unstaged changes
git diff --staged       # See staged changes
```

### Branch Management
```bash
git branch              # List all branches
git branch -a           # List all branches (including remote)
git checkout main       # Switch to main branch
git checkout -b new-branch  # Create and switch to new branch
git branch -d branch-name   # Delete a branch
```

### Undoing Changes
```bash
git restore filename    # Discard changes in working directory
git restore --staged filename  # Unstage a file
git reset HEAD~1        # Undo last commit (keep changes)
git reset --hard HEAD~1 # Undo last commit (discard changes)
```

### Remote Operations
```bash
git remote -v           # View remote repositories
git fetch               # Download changes without merging
git pull                # Fetch and merge changes
git push                # Upload local commits
```

---

## Project Structure

```
nft-marketplace/
│
├── index.html    # Main HTML file with structure
├── styles.css          # CSS file for styling (to be created)
├── README.md               # This file
│
└── assets/                 # (Optional) Folder for images and icons
    ├── images/
    └── icons/
```

---

## CSS Implementation Pseudo Code

Below is a comprehensive guide to implementing the CSS styling to match the reference design.

### 1. GLOBAL RESET & VARIABLES

```
PSEUDOCODE:

RESET all default browser styles:
  - Remove margin and padding from all elements
  - Set box-sizing to border-box for consistent sizing
  - Set default font smoothing

DEFINE CSS VARIABLES for:
  - Primary color (orange): #FF6B35 or similar
  - Dark background: #0F0F1A or similar
  - Card background: #1A1A2E or similar
  - Text color primary: #FFFFFF
  - Text color secondary: #888888
  - Border radius: 8px, 12px, 16px
  - Container max-width: 1200px
  - Spacing scale: 8px, 16px, 24px, 32px, 48px, 64px

SET body styles:
  - Background color: dark background color
  - Font family: sans-serif (Inter, system fonts)
  - Font size: 16px
  - Line height: 1.6
  - Color: white
```

---

### 2. TYPOGRAPHY

```
PSEUDOCODE:

DEFINE heading styles (h1, h2, h3):
  - h1: font-size 48px, font-weight 700, line-height 1.2
  - h2: font-size 32px, font-weight 700, line-height 1.3
  - h3: font-size 20px, font-weight 600, line-height 1.4

DEFINE text utilities:
  - .section-label: small text, uppercase, orange color, font-size 14px
  - .section-title: large heading style, white color
  - Description text: font-size 16px, gray color, line-height 1.6

SPECIAL STYLING:
  - .hero-title-highlight: orange outline text effect using:
    - color: transparent
    - -webkit-text-stroke: 1px orange
```

---

### 3. CONTAINER & LAYOUT

```
PSEUDOCODE:

CREATE .container class:
  - max-width: 1200px
  - margin: 0 auto (center horizontally)
  - padding: 0 24px (breathing room on sides)

CREATE GRID SYSTEMS:
  - .wallets-grid: 6 columns, gap 24px
  - .auction-cards-grid: 4 columns, gap 24px
  - .nft-cards-grid: 4 columns, gap 24px
  - .steps-grid: 4 columns, gap 32px
  - .creators-grid: 4 columns (2 rows), gap 24px
  - .collections-grid: 3 columns, gap 24px

RESPONSIVE BREAKPOINTS:
  - Desktop: default (1200px+)
  - Tablet: 768px - 1199px (adjust grids to 2-3 columns)
  - Mobile: below 768px (single column or 2 columns)
```

---

### 4. HEADER / NAVIGATION

```
PSEUDOCODE:

STYLE .header:
  - position: fixed (stays at top when scrolling)
  - top: 0, left: 0, right: 0
  - background: semi-transparent dark with blur effect
  - backdrop-filter: blur(10px)
  - padding: 16px 0
  - z-index: 1000 (appears above other content)

STYLE .navbar:
  - display: flex
  - justify-content: space-between
  - align-items: center

STYLE .logo:
  - font-size: 32px
  - font-weight: bold
  - color: orange
  - text-decoration: none

STYLE .nav-menu:
  - display: flex
  - list-style: none
  - gap: 32px

STYLE .nav-link:
  - color: white
  - text-decoration: none
  - font-size: 14px
  - transition: color 0.3s
  - HOVER: color changes to orange

STYLE .btn-primary (Connect Wallet):
  - background: orange gradient
  - color: white
  - padding: 12px 24px
  - border: none
  - border-radius: 8px
  - cursor: pointer
  - transition: transform 0.3s
  - HOVER: scale up slightly (transform: scale(1.05))
```

---

### 5. HERO SECTION

```
PSEUDOCODE:

STYLE .hero-section:
  - padding-top: 120px (account for fixed header)
  - padding-bottom: 80px
  - min-height: 100vh

STYLE .hero-content:
  - display: grid
  - grid-template-columns: 1fr 1fr (two equal columns)
  - gap: 64px
  - align-items: center

STYLE .hero-text:
  - text-align: left

STYLE .hero-title:
  - font-size: 56px
  - line-height: 1.1
  - margin-bottom: 16px

STYLE .hero-title-highlight:
  - color: transparent
  - -webkit-text-stroke: 1px orange
  - text-stroke: 1px orange

STYLE .hero-description:
  - font-size: 18px
  - color: light gray
  - margin-bottom: 32px

STYLE .hero-buttons:
  - display: flex
  - gap: 16px

STYLE .btn-secondary:
  - background: transparent
  - border: 1px solid white
  - color: white
  - padding: 12px 24px
  - border-radius: 8px
  - HOVER: background becomes slightly white

STYLE .hero-character-placeholder:
  - width: 400px
  - height: 400px
  - background: gradient or placeholder color
  - border-radius: 50%
  - position: relative
  - ANIMATION: floating effect (subtle up and down movement)
```

---

### 6. WALLETS SECTION

```
PSEUDOCODE:

STYLE .wallets-section:
  - padding: 80px 0
  - background: slightly lighter dark color

STYLE .section-header:
  - text-align: center
  - margin-bottom: 48px

STYLE .wallets-grid:
  - display: grid
  - grid-template-columns: repeat(6, 1fr)
  - gap: 24px

STYLE .wallet-card:
  - background: card background color
  - border: 1px solid dark border color
  - border-radius: 12px
  - padding: 24px
  - text-align: center
  - transition: all 0.3s
  - HOVER:
    - transform: translateY(-8px)
    - border-color: orange
    - box-shadow: 0 8px 24px rgba(255, 107, 53, 0.2)

STYLE .wallet-icon:
  - width: 64px
  - height: 64px
  - margin: 0 auto 16px
  - background: placeholder color
  - border-radius: 12px
  - (Each wallet should have different color/icon)

STYLE .wallet-name:
  - font-size: 14px
  - color: white
```

---

### 7. AUCTION CARDS SECTION

```
PSEUDOCODE:

STYLE .trending-auctions-section:
  - padding: 80px 0

STYLE .section-header-with-nav:
  - display: flex
  - justify-content: space-between
  - align-items: center
  - margin-bottom: 48px

STYLE .navigation-arrows:
  - display: flex
  - gap: 12px

STYLE .arrow-btn:
  - width: 40px
  - height: 40px
  - background: card background
  - border: 1px solid border color
  - border-radius: 8px
  - cursor: pointer
  - HOVER: border-color becomes orange

STYLE .auction-cards-grid:
  - display: grid
  - grid-template-columns: repeat(4, 1fr)
  - gap: 24px

STYLE .auction-card:
  - background: card background color
  - border: 1px solid border color
  - border-radius: 12px
  - overflow: hidden
  - transition: transform 0.3s
  - HOVER: transform: translateY(-8px)

STYLE .auction-card-image:
  - position: relative
  - height: 240px
  - overflow: hidden

STYLE .auction-image-placeholder:
  - width: 100%
  - height: 100%
  - background: gradient or image placeholder
  - (Each should have different gradient/color)

STYLE .bookmark-btn:
  - position: absolute
  - top: 16px
  - right: 16px
  - width: 32px
  - height: 32px
  - background: semi-transparent black
  - border: none
  - border-radius: 50%
  - cursor: pointer
  - HOVER: background becomes more opaque

STYLE .auction-card-content:
  - padding: 20px

STYLE .auction-header:
  - display: flex
  - justify-content: space-between
  - margin-bottom: 16px

STYLE .auction-title:
  - font-size: 18px
  - font-weight: 600

STYLE .auction-timer:
  - background: orange
  - padding: 4px 12px
  - border-radius: 16px
  - font-size: 12px

STYLE .auction-details:
  - display: grid
  - grid-template-columns: 1fr 1fr
  - gap: 16px
  - margin-bottom: 16px

STYLE .auction-label:
  - font-size: 12px
  - color: gray
  - display: block

STYLE .auction-price:
  - font-size: 14px
  - font-weight: 600
  - color: white

STYLE .btn-small:
  - width: 100%
  - padding: 10px
  - font-size: 14px
```

---

### 8. TRENDING NFTS SECTION

```
PSEUDOCODE:

STYLE .trending-nfts-section:
  - padding: 80px 0
  - background: slightly different dark shade

STYLE .section-header-with-filters:
  - margin-bottom: 48px

STYLE .filter-tabs:
  - display: flex
  - gap: 16px
  - list-style: none
  - justify-content: center
  - margin-top: 24px

STYLE .filter-tab:
  - padding: 8px 20px
  - background: transparent
  - border: 1px solid border color
  - border-radius: 20px
  - font-size: 14px
  - cursor: pointer
  - transition: all 0.3s
  - HOVER: border-color orange, color orange

STYLE .filter-tab-active:
  - background: orange
  - border-color: orange
  - color: white

STYLE .nft-cards-grid:
  - display: grid
  - grid-template-columns: repeat(4, 1fr)
  - gap: 24px

STYLE .nft-card:
  - background: card background
  - border: 1px solid border color
  - border-radius: 12px
  - overflow: hidden
  - transition: all 0.3s
  - HOVER: transform translateY(-8px), box-shadow

STYLE .nft-card-header:
  - padding: 16px
  - border-bottom: 1px solid border color

STYLE .nft-creator:
  - display: flex
  - align-items: center
  - gap: 12px

STYLE .creator-avatar:
  - width: 40px
  - height: 40px
  - border-radius: 50%
  - background: placeholder gradient

STYLE .creator-badge:
  - background: badge color
  - padding: 2px 8px
  - border-radius: 8px
  - font-size: 10px

STYLE .nft-card-content:
  - padding: 16px

STYLE .nft-info:
  - display: flex
  - justify-content: space-between
  - margin-bottom: 12px

STYLE .nft-price-info:
  - display: flex
  - justify-content: space-between
  - margin-bottom: 16px

STYLE .btn-full:
  - width: 100%
```

---

### 9. STEPS SECTION

```
PSEUDOCODE:

STYLE .steps-section:
  - padding: 80px 0

STYLE .section-header-center:
  - text-align: center
  - max-width: 600px
  - margin: 0 auto 64px

STYLE .steps-grid:
  - display: grid
  - grid-template-columns: repeat(4, 1fr)
  - gap: 32px

STYLE .step-card:
  - text-align: center
  - padding: 32px 24px

STYLE .step-icon:
  - width: 80px
  - height: 80px
  - margin: 0 auto 24px
  - background: gradient or icon placeholder
  - border-radius: 16px
  - (Each step has different icon/color)

STYLE .step-title:
  - font-size: 20px
  - margin-bottom: 16px

STYLE .step-description:
  - font-size: 14px
  - color: gray
  - line-height: 1.6
```

---

### 10. CREATORS SECTION

```
PSEUDOCODE:

STYLE .trending-creators-section:
  - padding: 80px 0
  - background: slightly different dark

STYLE .section-header-with-dropdown:
  - display: flex
  - justify-content: space-between
  - align-items: center
  - margin-bottom: 48px

STYLE .dropdown-button:
  - padding: 10px 20px
  - background: card background
  - border: 1px solid border color
  - border-radius: 8px
  - color: white
  - cursor: pointer
  - display: flex
  - align-items: center
  - gap: 12px

STYLE .creators-grid:
  - display: grid
  - grid-template-columns: repeat(4, 1fr)
  - gap: 24px

STYLE .creator-card:
  - background: card background
  - border: 1px solid border color
  - border-radius: 12px
  - padding: 24px
  - text-align: center
  - transition: all 0.3s
  - HOVER: transform translateY(-8px), border-color orange

STYLE .creator-avatar-large:
  - width: 80px
  - height: 80px
  - border-radius: 50%
  - margin: 0 auto 16px
  - background: gradient placeholder
  - border: 3px solid orange

STYLE .creator-card-name:
  - font-size: 16px
  - margin-bottom: 8px

STYLE .creator-card-badge:
  - background: badge background
  - padding: 4px 12px
  - border-radius: 8px
  - font-size: 11px
  - display: inline-block

STYLE .creator-card-price:
  - font-size: 18px
  - font-weight: 600
  - color: orange
  - margin-top: 12px
  - display: block
```

---

### 11. COLLECTIONS SECTION

```
PSEUDOCODE:

STYLE .popular-collection-section:
  - padding: 80px 0

STYLE .collections-grid:
  - display: grid
  - grid-template-columns: repeat(3, 1fr)
  - gap: 24px

STYLE .collection-card:
  - background: card background
  - border: 1px solid border color
  - border-radius: 12px
  - padding: 20px
  - transition: all 0.3s
  - HOVER: transform translateY(-8px)

STYLE .collection-header:
  - display: flex
  - justify-content: space-between
  - align-items: center
  - margin-bottom: 16px

STYLE .collection-creator:
  - display: flex
  - align-items: center
  - gap: 12px

STYLE .creator-avatar-small:
  - width: 48px
  - height: 48px
  - border-radius: 50%
  - background: gradient

STYLE .collection-label:
  - font-size: 16px
  - font-weight: 600
  - display: block

STYLE .collection-count:
  - font-size: 12px
  - color: gray

STYLE .collection-images:
  - display: grid
  - gap: 12px

STYLE .collection-main-image:
  - height: 200px
  - border-radius: 8px
  - overflow: hidden

STYLE .collection-thumbnail-grid:
  - display: grid
  - grid-template-columns: repeat(3, 1fr)
  - gap: 12px

STYLE .collection-image-placeholder:
  - height: 100px
  - background: gradient placeholder
  - border-radius: 8px
```

---

### 12. FOOTER

```
PSEUDOCODE:

STYLE .footer:
  - background: darkest background color
  - padding: 64px 0 24px
  - border-top: 1px solid border color

STYLE .footer-content:
  - display: grid
  - grid-template-columns: repeat(5, 1fr)
  - gap: 32px
  - margin-bottom: 48px

STYLE .footer-heading:
  - font-size: 18px
  - margin-bottom: 20px

STYLE .footer-links:
  - list-style: none

STYLE .footer-link:
  - color: gray
  - text-decoration: none
  - font-size: 14px
  - line-height: 2
  - transition: color 0.3s
  - HOVER: color becomes white

STYLE .newsletter-form:
  - display: flex
  - gap: 8px

STYLE .newsletter-input:
  - flex: 1
  - padding: 12px 16px
  - background: card background
  - border: 1px solid border color
  - border-radius: 8px
  - color: white
  - font-size: 14px

STYLE .footer-bottom:
  - text-align: center
  - padding-top: 24px
  - border-top: 1px solid border color

STYLE .footer-copyright:
  - font-size: 14px
  - color: gray
```

---

### 13. RESPONSIVE DESIGN

```
PSEUDOCODE:

TABLET BREAKPOINT (max-width: 1024px):
  - .hero-content: grid-template-columns 1fr
  - .auction-cards-grid: 3 columns
  - .nft-cards-grid: 3 columns
  - .steps-grid: 2 columns
  - .creators-grid: 3 columns
  - .collections-grid: 2 columns
  - .footer-content: 3 columns

TABLET BREAKPOINT (max-width: 768px):
  - .navbar: flex-direction column
  - .nav-menu: flex-direction column
  - .wallets-grid: 3 columns
  - .auction-cards-grid: 2 columns
  - .nft-cards-grid: 2 columns
  - .steps-grid: 2 columns
  - .creators-grid: 2 columns
  - .filter-tabs: wrap, smaller gap
  - .footer-content: 2 columns

MOBILE BREAKPOINT (max-width: 480px):
  - .container: padding 16px
  - .hero-title: font-size 36px
  - .wallets-grid: 2 columns
  - .auction-cards-grid: 1 column
  - .nft-cards-grid: 1 column
  - .steps-grid: 1 column
  - .creators-grid: 1 column
  - .collections-grid: 1 column
  - .footer-content: 1 column
  - .newsletter-form: flex-direction column
```

---

### 14. ANIMATIONS & TRANSITIONS

```
PSEUDOCODE:

ADD smooth transitions to interactive elements:
  - Cards: transform and box-shadow on hover (0.3s ease)
  - Buttons: scale and background on hover (0.3s ease)
  - Links: color on hover (0.3s ease)
  - Images: scale on hover (0.3s ease)

ADD subtle animations:
  - Hero character: floating animation (up and down)
  - Cards: fade in on scroll (optional)
  - Buttons: ripple effect on click (optional)

KEYFRAME for floating animation:
  - 0%: transform translateY(0)
  - 50%: transform translateY(-20px)
  - 100%: transform translateY(0)
  - Duration: 3s, infinite, ease-in-out
```

---

### 15. UTILITIES & HELPER CLASSES

```
PSEUDOCODE:

CREATE utility classes:
  - .text-center: text-align center
  - .text-left: text-align left
  - .text-right: text-align right
  - .mt-1, .mt-2, .mt-3: margin-top (8px, 16px, 24px)
  - .mb-1, .mb-2, .mb-3: margin-bottom
  - .pt-1, .pt-2, .pt-3: padding-top
  - .pb-1, .pb-2, .pb-3: padding-bottom

CREATE display utilities:
  - .flex: display flex
  - .grid: display grid
  - .hidden: display none
  - .block: display block

CREATE color utilities:
  - .text-primary: orange color
  - .text-secondary: gray color
  - .text-white: white color
  - .bg-dark: dark background
```

---

## Design Specifications

### Color Palette
```
Primary Orange: #FF6B35 or #FF8C42
Dark Background: #0F0F1A
Card Background: #1A1A2E
Border Color: #2A2A3E
Text Primary: #FFFFFF
Text Secondary: #888888
Accent: #646CFF (for some icons)
```

### Typography
```
Font Family: Inter, system-ui, sans-serif
Font Sizes:
  - Hero Title: 56px
  - Section Title: 32px
  - Card Title: 18px
  - Body: 16px
  - Small: 14px
  - Extra Small: 12px

Font Weights:
  - Regular: 400
  - Medium: 500
  - Semi-bold: 600
  - Bold: 700
```

### Spacing Scale
```
xs: 8px
sm: 16px
md: 24px
lg: 32px
xl: 48px
2xl: 64px
3xl: 80px
```

### Border Radius
```
Small: 8px
Medium: 12px
Large: 16px
Circle: 50%
```

---

## Resources

### Learning Resources
- [HTML Documentation](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [CSS Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)

### Design Tools
- [CSS Grid Generator](https://cssgrid-generator.netlify.app/)
- [Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Color Palette Generator](https://coolors.co/)
- [Google Fonts](https://fonts.google.com/)

### Testing
- Test responsiveness using browser DevTools
- Check different screen sizes (mobile, tablet, desktop)
- Validate HTML: [W3C Validator](https://validator.w3.org/)
- Validate CSS: [W3C CSS Validator](https://jigsaw.w3.org/css-validator/)

---

## Troubleshooting

### Common Issues

**Problem: Changes not appearing in browser**
- Solution: Hard refresh (Ctrl+Shift+R or Cmd+Shift+R)
- Clear browser cache

**Problem: Git push rejected**
- Solution: Pull latest changes first: `git pull origin main`
- Then push again: `git push`

**Problem: CSS not loading**
- Check file path in HTML is correct
- Make sure CSS file is in same directory as HTML
- Check browser console for errors (F12)

**Problem: Layout breaking on mobile**
- Use responsive breakpoints in CSS
- Test with browser DevTools device mode
- Use relative units (%, rem, em) instead of fixed px

---

## Next Steps

1. Start by creating the CSS file: `nft-styles.css`
2. Implement global styles and variables first
3. Work section by section from top to bottom
4. Test responsiveness at each major section
5. Add animations and hover effects last
6. Test across different browsers
7. Commit frequently with descriptive messages
8. Create a pull request when complete

---

## Contributing

If you find issues or want to improve this project:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

---

## License

This project is for educational purposes.

---

