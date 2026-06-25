# Advisor AV - Landing Page

A professional landing page for Advisor AV, helping financial advisors in Southern California become recognized experts through video content creation.

## 🚀 Quick Start

### Local Development
```bash
# Start a local server
python -m http.server 8000

# Then open http://localhost:8000/lp.html
```

## 📦 Deployment on Netlify

### Prerequisites
- GitHub account with this repository
- Netlify account (sign up at netlify.com)

### Deployment Steps

1. **Connect Your Repository**
   - Go to [Netlify](https://app.netlify.com)
   - Click "Add new site" → "Import an existing project"
   - Connect your GitHub repository
   - Select the repository containing this code

2. **Configure Build Settings**
   - Build command: (leave empty)
   - Publish directory: `.`
   - The `netlify.toml` file handles all configuration

3. **Deploy**
   - Click "Deploy site"
   - Netlify will automatically deploy your site

4. **Custom Domain (Optional)**
   - Go to Site settings → Domain management
   - Add your custom domain (e.g., advisorav.com)
   - Update DNS records if necessary

### Environment Variables (if needed)
Add any environment variables in Netlify:
- Site settings → Build & deploy → Environment
- Set any required variables there

## 📁 File Structure

```
.
├── lp.html              # Main landing page
├── netlify.toml         # Netlify configuration
├── robots.txt           # SEO robots file
├── sitemap.xml          # XML sitemap for search engines
├── .gitignore           # Git ignore rules
└── README.md            # This file
```

## 🔧 Key Features

- **Responsive Design**: Mobile-first, works on all devices
- **Performance Optimized**: Fast load times, CDN delivery
- **SEO Ready**: Meta tags, sitemap, robots.txt
- **Security Headers**: CSP, X-Frame-Options, etc.
- **Accessibility**: WCAG compliant
- **Modern UI**: Tailwind CSS with custom animations

## 📊 Performance

- Minified CDN assets
- Optimized image delivery
- Efficient caching headers
- Fast DNS resolution

## 🔒 Security

- Security headers configured in netlify.toml
- HTTPS enforced (automatic with Netlify)
- Content Security Policy headers
- No sensitive data in code

## 📧 Contact Links

All contact buttons point to: `mailto:sarzoza@gmail.com`

Update this email in the HTML if needed.

## 🎨 Customization

### Colors
Update color values in the `<style>` section:
- `--navy: #0F172A` - Primary dark color
- `--gold: #C9A227` - Accent color

### Content
Edit text directly in the HTML sections:
- Hero section
- Benefits
- Testimonials
- Pricing
- FAQ

### Domain
Update the following in `lp.html`:
- `og:url` meta tag
- `canonical` link tag
- Replace `https://advisorav.com` with your actual domain

## 📞 Support

For issues or questions, contact: sarzoza@gmail.com

## 📝 License

© 2026 Advisor AV. All rights reserved.
