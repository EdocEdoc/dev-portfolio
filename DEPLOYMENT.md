# Deployment Guide

This document outlines the steps to deploy Vince Aaron Genodipa's portfolio website to various hosting platforms.

## Prerequisites

Before deploying, ensure you have:

- The complete project files
- A GitHub account (if using GitHub Pages)
- Access credentials for your chosen hosting provider
- Domain name (optional but recommended)

## Deployment Options

### 1. GitHub Pages (Free)

GitHub Pages provides free hosting for static websites directly from a GitHub repository.

#### Steps:

1. Push your code to a GitHub repository

2. Configure GitHub Pages:

   - Go to your repository settings
   - Scroll down to "GitHub Pages" section
   - Select the branch to deploy (usually `main` or `master`)
   - Click "Save"

3. Custom domain (optional):

   - In the GitHub Pages settings, enter your custom domain
   - Configure your domain provider's DNS settings:
     - Add an A record pointing to GitHub Pages IP addresses
     - Or add a CNAME record pointing to your GitHub Pages URL

4. Your site will be available at `https://username.github.io/repository` or your custom domain

### 2. Netlify (Free tier available)

Netlify offers continuous deployment from Git, global CDN, and many other features.

#### Steps:

1. Create a Netlify account at [netlify.com](https://www.netlify.com/)

2. Deploy from Git:

   - Click "New site from Git"
   - Connect to your GitHub/GitLab/Bitbucket account
   - Select your repository
   - Configure build settings (not needed for this static site)
   - Click "Deploy site"

3. Custom domain:
   - Go to "Domain settings"
   - Click "Add custom domain"
   - Follow the instructions to verify and configure your domain

### 3. Vercel (Free tier available)

Vercel provides a similar deployment experience to Netlify with global CDN.

#### Steps:

1. Create a Vercel account at [vercel.com](https://vercel.com/)

2. Import your project:

   - Click "Import Project"
   - Connect to your Git provider
   - Select your repository
   - Configure project settings
   - Click "Deploy"

3. Custom domain:
   - Go to "Project Settings" > "Domains"
   - Add your domain and follow the verification steps

### 4. Traditional Web Hosting

You can also use traditional web hosting services like SiteGround, Bluehost, or HostGator.

#### Steps:

1. Purchase a hosting plan and domain

2. Access your hosting control panel (cPanel, Plesk, etc.)

3. Upload files:

   - Use FTP client like FileZilla
   - Or use the file manager in your hosting control panel
   - Upload all files to the public directory (often called `public_html`, `www`, or `htdocs`)

4. Verify your website is working by visiting your domain

## Post-Deployment

After deploying, make sure to:

1. Test your website on different devices and browsers
2. Check that all links and functionalities work correctly
3. Set up analytics (Google Analytics, Plausible, etc.)
4. Submit your site to search engines

## Updating Your Website

### For GitHub Pages, Netlify, or Vercel:

- Push changes to your repository
- The site will automatically rebuild and deploy

### For traditional hosting:

- Make changes locally
- Upload the modified files via FTP or your hosting's file manager

## Need Help?

If you encounter any issues during deployment, contact Vince Aaron Genodipa at vagenodipa@gmail.com.

---

Good luck with your deployment!
