# MediaSort Website

Landing page, About, and Privacy Policy for mediasortapp.com

## Structure
```
index.html          → Home / waitlist (mediasortapp.com)
about/index.html    → About page   (mediasortapp.com/about)
privacy/index.html  → Privacy      (mediasortapp.com/privacy)
icon.png            → App icon
```

## Deploy to GitHub Pages (10 minutes)

### Step 1 — Create a GitHub repo
1. Go to github.com → New repository
2. Name it: `mediasort-site`  (or any name)
3. Set to **Public**
4. Do NOT add README (we have our own)
5. Click Create

### Step 2 — Push these files
Open Terminal and run:
```bash
cd /path/to/this/folder
git init
git add .
git commit -m "Initial site launch"
git branch -M main
git remote add origin git@github.com:deabonn/mediasort-site.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages
1. Go to repo Settings → Pages
2. Source: Deploy from branch → main → / (root)
3. Click Save
4. Your site will be live at: https://deabonn.github.io/mediasort-site

### Step 4 — Connect your GoDaddy domain
In GoDaddy DNS settings, add these records:

| Type  | Name | Value                  |
|-------|------|------------------------|
| A     | @    | 185.199.108.153        |
| A     | @    | 185.199.109.153        |
| A     | @    | 185.199.110.153        |
| A     | @    | 185.199.111.153        |
| CNAME | www  | deabonn.github.io      |

Then in GitHub repo Settings → Pages → Custom domain → enter: mediasortapp.com

### Step 5 — Set up Buttondown for email
1. Go to buttondown.com → Sign up free with mediasortapp@gmail.com
2. In Settings, set your newsletter name/slug to: mediasort
3. The signup forms on the site will automatically submit to your list

### Step 6 — Update App Store Connect
Once the domain is live, update these URLs in App Store Connect:
- Support URL: https://mediasortapp.com
- Privacy Policy URL: https://mediasortapp.com/privacy

## When app is approved — add App Store link
In index.html, find the comment `<!-- APP STORE BADGE GOES HERE -->` 
Replace the "Coming soon" badge with:
```html
<a href="YOUR_APP_STORE_LINK" target="_blank">
  <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg" 
       alt="Download on the App Store" height="44" />
</a>
```
