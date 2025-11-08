# 🚀 Deployment Guide - Hotel Food Management

This guide will help you deploy the Hotel Food Management application to GitHub Pages, Vercel, or Netlify.

## 📋 Prerequisites

- GitHub account
- Node.js installed (v16 or higher)
- Git installed

## 🌐 Option 1: GitHub Pages Deployment

### Method A: Manual Deployment

1. **Build the application:**
   ```bash
   npm install
   npm run build
   ```

2. **Push to GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Click on **Settings** tab
   - Scroll down to **Pages** section
   - Under **Source**, select **GitHub Actions**
   - The workflow will automatically deploy on every push

### Method B: Using GitHub Actions (Automatic)

The repository includes a GitHub Actions workflow (`.github/workflows/deploy.yml`) that automatically deploys your app to GitHub Pages whenever you push to the `main` branch.

**Steps:**
1. Push your code to GitHub
2. Go to repository **Settings** → **Pages**
3. Select **Source**: `GitHub Actions`
4. The workflow will run automatically on every push to `main`

**Important:** Make sure to update the `base` path in `vite.config.js` if your repository name is not the root:
```javascript
export default defineConfig({
  base: '/your-repo-name/', // Add this if deploying to subdirectory
  plugins: [react()],
  // ...
})
```

## ⚡ Option 2: Vercel Deployment

1. **Install Vercel CLI (optional):**
   ```bash
   npm i -g vercel
   ```

2. **Deploy:**
   ```bash
   vercel
   ```
   Or use the Vercel website:
   - Go to [vercel.com](https://vercel.com)
   - Click **New Project**
   - Import your GitHub repository
   - Vercel will auto-detect Vite and deploy

3. **Automatic deployments:** Vercel automatically deploys on every push to your main branch.

## 🎯 Option 3: Netlify Deployment

1. **Install Netlify CLI (optional):**
   ```bash
   npm i -g netlify-cli
   ```

2. **Deploy:**
   ```bash
   npm run build
   netlify deploy --prod --dir=dist
   ```
   Or use the Netlify website:
   - Go to [netlify.com](https://netlify.com)
   - Click **Add new site** → **Import an existing project**
   - Connect your GitHub repository
   - Build command: `npm run build`
   - Publish directory: `dist`

3. **Automatic deployments:** Netlify automatically deploys on every push.

## 📱 Local Development

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Start development server:**
   ```bash
   npm run dev
   ```

3. **Access on mobile (same network):**
   - Find your local IP address:
     - Windows: `ipconfig` (look for IPv4 Address)
     - Mac/Linux: `ifconfig` or `ip addr`
   - Access from mobile: `http://YOUR_IP_ADDRESS:3000`
   - Example: `http://192.168.1.100:3000`

## 🔧 Build Configuration

### For GitHub Pages (subdirectory)

If your repository is at `github.com/username/repo-name`, update `vite.config.js`:

```javascript
export default defineConfig({
  base: '/repo-name/', // Replace with your actual repo name
  plugins: [react()],
  // ...
})
```

### For Root Domain

If deploying to root domain (e.g., `yourdomain.com`), keep base as `/`:

```javascript
export default defineConfig({
  base: '/',
  plugins: [react()],
  // ...
})
```

## ✅ Post-Deployment Checklist

- [ ] Test all CRUD operations (Create, Read, Update, Delete)
- [ ] Verify images load correctly
- [ ] Test search and filter functionality
- [ ] Check mobile responsiveness
- [ ] Verify data persists in localStorage
- [ ] Test on different browsers

## 🐛 Troubleshooting

### Images not loading
- Ensure image URLs are from trusted sources (Unsplash, etc.)
- Check browser console for CORS errors
- Verify image URLs are accessible

### Routing issues on GitHub Pages
- Make sure `base` path in `vite.config.js` matches your repository name
- Use HashRouter instead of BrowserRouter if issues persist

### Build errors
- Clear `node_modules` and reinstall: `rm -rf node_modules && npm install`
- Check Node.js version: `node --version` (should be v16+)

## 📞 Support

If you encounter any issues:
1. Check the browser console for errors
2. Review the build logs
3. Ensure all dependencies are installed
4. Verify your Node.js version

---

Happy Deploying! 🎉

