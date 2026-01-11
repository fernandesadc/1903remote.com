# 1903 Remote Script Consulting Website - Setup Guide

## 📁 Project Structure

```
1903-remote-website/
├── index.html          # Main website file (everything is in one file)
└── README.md          # This file
```

---

## 🛠️ Setting Up in VSCode

### 1. Install VSCode
If you haven't already, download from: https://code.visualstudio.com/

### 2. Create Your Project Folder
```bash
# In your terminal/command prompt:
mkdir 1903-remote-website
cd 1903-remote-website
```

### 3. Open the Project in VSCode
- Open VSCode
- Click `File` → `Open Folder`
- Select the `1903-remote-website` folder you just created
- Copy the `index.html` file into this folder

### 4. Preview the Website Locally

**Option A: Live Server Extension (Recommended)**
1. Install the "Live Server" extension by Ritwick Dey:
   - Click the Extensions icon (or press `Ctrl+Shift+X` / `Cmd+Shift+X`)
   - Search for "Live Server"
   - Click Install
2. Right-click on `index.html` → "Open with Live Server"
3. Your website will open in your browser at `http://127.0.0.1:5500`
4. Any changes you make will auto-refresh!

**Option B: Simple File Open**
- Just double-click `index.html` to open it in your browser
- Refresh the page manually after making changes

---

## ✏️ Editing the Website

The HTML file is organized with clear section markers. Here's what you can easily modify:

### Change the Title
```html
<!-- Find this section around line 52 -->
<h1>1903 remote. | Script Consulting</h1>
```

### Update the About Text
```html
<!-- Find this section around line 60 -->
<section class="about">
    <p>
        Replace this Lorem ipsum text with your actual company description...
    </p>
</section>
```

### Modify Pricing
```html
<!-- Find this section around line 78 -->
<table>
    <tr>
        <td>1-40 pages</td>
        <td>£80</td>  <!-- Change prices here -->
    </tr>
    <!-- Add more rows if needed -->
</table>
```

### Change Testimonials
```html
<!-- Find this section around line 175 -->
<div class="testimonial">
    Replace with real testimonial text...
</div>
```

### Update Colors
```css
/* Find this section around line 10 */
:root {
    --color-background: #FFF8F0;  /* Change bone white color */
    --color-text: #1a1a1a;        /* Change text color */
}
```

---

## 🌐 Deploying to GitHub Pages (FREE Hosting)

### Step 1: Create a GitHub Account
Go to https://github.com and sign up (if you don't have an account)

### Step 2: Create a New Repository
1. Click the `+` icon (top right) → "New repository"
2. Repository name: `1903-remote-website` (or any name you prefer)
3. Make it **Public**
4. Click "Create repository"

### Step 3: Upload Your Files
You can do this two ways:

**Option A: GitHub Desktop (Easier for beginners)**
1. Download GitHub Desktop: https://desktop.github.com/
2. Install and sign in
3. Click "Add" → "Add Existing Repository"
4. Select your project folder
5. Click "Publish repository"
6. In the file list, click "Commit to main"
7. Click "Push origin"

**Option B: Command Line (Git)**
```bash
# In your project folder:
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/1903-remote-website.git
git push -u origin main
```

### Step 4: Enable GitHub Pages
1. Go to your repository on GitHub
2. Click "Settings" (top menu)
3. Scroll down to "Pages" (left sidebar)
4. Under "Source", select "main" branch
5. Click "Save"
6. Your site will be live at: `https://YOUR-USERNAME.github.io/1903-remote-website/`

⏱️ **Note:** It may take 2-5 minutes for your site to go live.

---

## 🌍 Using a Custom Domain

### Option 1: Using Your Existing Domain with GitHub Pages

1. **Purchase a domain** (if you haven't already):
   - Namecheap: https://www.namecheap.com
   - GoDaddy: https://www.godaddy.com
   - Google Domains: https://domains.google

2. **Configure DNS Settings** (in your domain provider):
   
   Add these DNS records:
   ```
   Type: A
   Name: @
   Value: 185.199.108.153
   
   Type: A
   Name: @
   Value: 185.199.109.153
   
   Type: A
   Name: @
   Value: 185.199.110.153
   
   Type: A
   Name: @
   Value: 185.199.111.153
   
   Type: CNAME
   Name: www
   Value: YOUR-USERNAME.github.io
   ```

3. **Configure GitHub Pages**:
   - Go to Settings → Pages on your GitHub repo
   - Under "Custom domain", enter: `www.yourdomain.com`
   - Check "Enforce HTTPS"
   - Click Save

⏱️ **DNS propagation can take 24-48 hours**

### Option 2: Traditional Web Hosting (With Backend Support)

If you need the contact form to actually send emails with attachments, you'll need:

**Recommended Hosting Providers:**
- **Netlify** (free tier, easy): https://www.netlify.com
- **Vercel** (free tier): https://vercel.com
- **Hostinger** (paid, $2-4/month): https://www.hostinger.com
- **SiteGround** (paid, $3-7/month): https://www.siteground.com

**Steps for traditional hosting:**
1. Purchase hosting + domain
2. Access your hosting control panel (cPanel)
3. Use File Manager or FTP to upload `index.html`
4. Point your domain to the hosting server (your host will provide instructions)

---

## 📧 Making the Contact Form Actually Work

The current form opens the user's email client. For a professional solution:

### Option 1: Formspree (Easiest)
1. Go to https://formspree.io (free tier: 50 submissions/month)
2. Sign up and create a new form
3. Replace the form code with:
```html
<form action="https://formspree.io/f/YOUR-FORM-ID" method="POST" enctype="multipart/form-data">
    <!-- Keep all the existing form fields -->
</form>
```

### Option 2: EmailJS
1. Go to https://www.emailjs.com
2. Set up email service
3. Add EmailJS JavaScript library to your site
4. Configure email templates

### Option 3: Backend Service
Create a backend with:
- **Node.js + Express** with Nodemailer
- **PHP** mail function
- **Netlify/Vercel Functions** (serverless)

---

## 🚀 Quick Start Checklist

- [ ] Copy `index.html` to your project folder
- [ ] Open in VSCode
- [ ] Install Live Server extension
- [ ] Preview locally
- [ ] Replace lorem ipsum with real content
- [ ] Update pricing and contact email
- [ ] Create GitHub account
- [ ] Push to GitHub
- [ ] Enable GitHub Pages
- [ ] (Optional) Configure custom domain
- [ ] (Optional) Set up proper form handling

---

## 🔍 SEO Optimization

Your website is now optimized for search engines with the following keywords and phrases:

**Primary Keywords:**
- Script consultant / consulting
- Screenplay coverage
- Script doctor
- Script editing
- Film manuscript
- Screenplay report
- Script analysis

**SEO Features Implemented:**
1. **Meta Tags**: Title, description, and keywords optimized for search engines
2. **Open Graph Tags**: Optimized for social media sharing (Facebook, LinkedIn)
3. **Twitter Cards**: Enhanced Twitter sharing appearance
4. **Schema.org Structured Data**: Helps search engines understand your services and pricing
5. **Semantic HTML**: Proper heading hierarchy and section structure

**Additional SEO Tips:**

### Content Optimization
When you replace the Lorem ipsum text in the About section, naturally include keywords like:
- "We provide professional script consulting and screenplay coverage..."
- "Our experienced script doctors offer detailed analysis..."
- "Expert script editing services for film and television..."

### URL Structure
If you add more pages, use keyword-rich URLs:
- `/script-consulting`
- `/screenplay-coverage`
- `/pricing`

### Page Speed
Your site is already optimized:
- Single HTML file (fast loading)
- Minimal CSS (no external stylesheets)
- No heavy images or scripts

### Local SEO (if applicable)
Add your location to the Schema.org data if you serve a specific region.

### Regular Updates
- Add a blog section for fresh content
- Include case studies or success stories
- Update testimonials regularly

### Backlinks
- Get listed in screenwriting directories
- Partner with film schools
- Guest post on screenwriting blogs

### Analytics Setup
Add Google Analytics to track:
1. Which keywords bring visitors
2. How users interact with your site
3. Conversion rates (form submissions)

```html
<!-- Add before closing </head> tag -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Google Search Console
1. Verify your website at https://search.google.com/search-console
2. Submit your sitemap
3. Monitor search performance
4. Fix any crawl errors

---

## 💡 Pro Tips

1. **Test responsiveness**: Open in browser, press `F12`, click the device toggle icon to see mobile view
2. **SEO**: Add meta description in the `<head>` section
3. **Favicon**: Add a small logo icon to appear in browser tabs
4. **Analytics**: Add Google Analytics to track visitors
5. **Performance**: The site is already optimized (single file, minimal code)

---

## ❓ Need Help?

- **VSCode Tutorial**: https://code.visualstudio.com/docs
- **Git/GitHub Tutorial**: https://docs.github.com/en/get-started
- **HTML/CSS Help**: https://developer.mozilla.org/en-US/

---

## 📝 License

This website is yours to modify and use as you wish!
