# Original Fuzz Hiatus Website

A single-page static website for originalfuzz.com, deployed on GitHub Pages.

## File Structure

```
/index.html          # Main page with Tailwind CSS
/assets/             # Images and favicon
  ├── logo.png       # Original Fuzz logo
  ├── signature.png  # Lee McAlilly signature  
  └── favicon.ico    # Website favicon
/CNAME              # Domain configuration
```

## Deployment Steps

### 1. GitHub Repository Setup
1. Create a public GitHub repository
2. Upload all files to the main branch
3. Go to Settings → Pages
4. Set source to "Deploy from a branch" → main (root)
5. Set custom domain to `originalfuzz.com`
6. Enable "Enforce HTTPS" once DNS resolves

### 2. Cloudflare DNS Configuration
Replace existing Shopify DNS records with:

**A Records (DNS only, grey cloud):**
```
@   A   185.199.108.153
@   A   185.199.109.153  
@   A   185.199.110.153
@   A   185.199.111.153
```

**CNAME Record (DNS only, grey cloud):**
```
www   CNAME   <your-username>.github.io
```

### 3. Required Assets
Before deploying, add these files to the `/assets/` folder:
- `logo.png` - Original Fuzz logo
- `signature.png` - Lee McAlilly signature
- `favicon.ico` - Website favicon

### 4. Domain Verification
Once DNS propagates (24-48 hours), the site will be available at:
- https://originalfuzz.com
- https://www.originalfuzz.com (redirects to apex)

## Technical Details
- Built with vanilla HTML and Tailwind CSS CDN
- No build process required
- Responsive design optimized for all devices
- Semantic HTML for accessibility