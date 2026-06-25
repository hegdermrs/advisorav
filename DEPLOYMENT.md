# Netlify Deployment Guide

Complete step-by-step instructions for deploying Advisor AV to Netlify.

## ✅ Pre-Deployment Checklist

- [ ] Update `og:url` in `lp.html` with your actual domain
- [ ] Update `canonical` link in `lp.html`
- [ ] Verify all email links point to correct address (`mailto:sarzoza@gmail.com`)
- [ ] Test locally: `python -m http.server 8000`
- [ ] Verify responsive design on mobile
- [ ] Check all links work correctly
- [ ] Review content for typos and accuracy
- [ ] Confirm all images and fonts load properly

## 📋 Option 1: Deploy via Git (Recommended)

### Step 1: Push Code to GitHub

```bash
# Initialize git if not already done
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial commit: Advisor AV landing page"

# Add remote (replace YOUR_USERNAME and REPO_NAME)
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 2: Connect to Netlify

1. Go to [Netlify](https://app.netlify.com)
2. Click **"Add new site"** → **"Import an existing project"**
3. Select **GitHub** as your Git provider
4. Authorize Netlify to access your GitHub account
5. Find and select your repository
6. Click **"Deploy site"**

**Build Settings** (should auto-fill):
- Build command: (leave empty)
- Publish directory: `.`
- Runtime: Node 14 (or latest)

### Step 3: Configure Domain

1. Go to your site in Netlify dashboard
2. Click **Site settings** → **Domain management**
3. Click **Add custom domain**
4. Enter your domain (e.g., `advisorav.com`)
5. Follow DNS configuration instructions
6. Typically takes 24-48 hours to propagate

## 🚀 Option 2: Deploy via Netlify CLI

### Step 1: Install Netlify CLI

```bash
npm install -g netlify-cli
```

### Step 2: Authenticate

```bash
netlify login
```

### Step 3: Deploy

```bash
netlify deploy --prod
```

Select the current directory as the publish folder.

## 🔧 Post-Deployment Configuration

### 1. Enable HTTPS (Automatic)
Netlify automatically provides free HTTPS with Let's Encrypt.

### 2. Set Environment Variables (if needed)
- Go to **Site settings** → **Build & deploy** → **Environment**
- Add any required variables

### 3. Configure Redirects
The `netlify.toml` file already includes:
- Catch-all redirect to `lp.html`
- Security headers
- Caching headers

### 4. Set Up Monitoring
- Go to **Analytics** for Netlify analytics
- Optional: Add Google Analytics (uncomment GA code in HTML)

### 5. Enable Deploy Notifications (Optional)
- **Site settings** → **Build & deploy** → **Deploy notifications**
- Add Slack, email, or webhook notifications

## 📊 Performance Optimization

### Already Configured:
- ✅ Caching headers for static assets (1 year for CSS/JS/images)
- ✅ HTML cache (1 hour)
- ✅ Security headers
- ✅ Gzip compression (automatic)
- ✅ CDN delivery worldwide

### Recommended Additions:
1. **Google Analytics**: Uncomment GA code in `lp.html`
2. **Google Search Console**: Verify domain and submit sitemap
3. **Netlify Analytics**: Already included, view in dashboard

## 🔐 Security Checklist

- ✅ HTTPS enabled
- ✅ Security headers configured
- ✅ No sensitive data in code
- ✅ robots.txt configured
- ✅ Permissions policy set
- ✅ XSS protection headers

### Additional Security Steps:
1. Add domain to Google Search Console
2. Monitor Netlify's security features
3. Keep dependencies updated (if using any)
4. Regularly review access logs

## 🐛 Troubleshooting

### Site not deploying?
- Check Git repository is connected
- Verify `netlify.toml` syntax is correct
- Check Netlify build logs for errors

### Domain not resolving?
- DNS changes take 24-48 hours
- Verify DNS records in domain registrar
- Check Netlify domain settings

### Content not updating?
- Clear browser cache
- Check if CI/CD build succeeded
- Verify correct branch is deployed

### 404 errors?
- The `netlify.toml` catch-all redirect handles this
- All routes redirect to `lp.html`

## 📞 Support

- **Netlify Support**: https://support.netlify.com
- **Documentation**: https://docs.netlify.com
- **Community**: https://community.netlify.com

## 🔄 Continuous Deployment

Once connected to GitHub, Netlify will:
- Automatically deploy on every push to `main`
- Build in a few seconds
- Live within 1-2 minutes
- Maintain version history for easy rollback

### To Rollback:
1. Go to **Deploys** in Netlify dashboard
2. Find previous deployment
3. Click **Publish Deploy**

## 📈 Next Steps

1. **Monitor Analytics**: Track visitor behavior
2. **Optimize Performance**: Use Netlify Analytics
3. **A/B Testing**: Consider adding variants
4. **Backup**: Keep GitHub as source of truth
5. **Updates**: Make changes and push to deploy

---

**Deployment Date**: 2026-06-25
**Site**: https://advisorav.com (update as needed)
**Contact**: sarzoza@gmail.com
