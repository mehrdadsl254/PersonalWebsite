# Deploying to GitHub Pages

This guide will help you deploy your personal website to GitHub Pages (username.github.io).

## Step 1: Connect to GitHub

1. In Lovable, click the **GitHub** button in the top right
2. Click **Connect to GitHub** and authorize the Lovable GitHub App
3. Select your GitHub account
4. Click **Create Repository** - this will create a new repo with all your code

## Step 2: Configure GitHub Pages

1. Go to your repository on GitHub (e.g., `github.com/yourusername/your-repo-name`)
2. Click **Settings** → **Pages** (in the left sidebar)
3. Under **Source**, select **GitHub Actions**
4. That's it! The workflow will automatically deploy your site

## Step 3: Update Your Links

Before deploying, update the placeholder links in your code:

### In `src/components/Hero.tsx` and `src/components/Contact.tsx`:

Replace these placeholders:
- `your.email@example.com` → Your actual email
- `https://github.com/yourusername` → Your GitHub profile URL
- `https://linkedin.com/in/yourusername` → Your LinkedIn profile URL

## Step 4: Deploy

Once you've updated the links:
1. Make sure all changes are saved in Lovable
2. Changes automatically sync to GitHub
3. The GitHub Action will automatically build and deploy
4. Your site will be live at: `https://yourusername.github.io/repository-name/`

### For username.github.io

To deploy to `https://yourusername.github.io/` (without the repo name):
1. When creating the repository in Step 1, name it exactly: `yourusername.github.io` (replace `yourusername` with your actual GitHub username)
2. In `vite.config.ts`, change `base: './'` to `base: '/'`
3. Your site will be available at: `https://yourusername.github.io/`

## Manual Deployment Alternative

If you prefer to deploy manually without the GitHub Action:

1. Clone your repository locally:
   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   ```

2. Install dependencies and build:
   ```bash
   npm install
   npm run build
   ```

3. Deploy the `dist` folder to GitHub Pages using `gh-pages`:
   ```bash
   npm install -g gh-pages
   gh-pages -d dist
   ```

## Updating Your Site

Any changes you make in Lovable will automatically:
1. Sync to your GitHub repository
2. Trigger the GitHub Action
3. Deploy the updated site within 2-3 minutes

## Troubleshooting

- **404 errors**: Make sure you set `base: './'` in `vite.config.ts` (already configured)
- **Action fails**: Check the Actions tab in GitHub for error logs
- **Links don't work**: Verify you updated all placeholder URLs

## Custom Domain (Optional)

To use a custom domain like `mehrdadsalehi.com`:

1. Buy a domain from any registrar (Namecheap, GoDaddy, etc.)
2. In your repo settings → Pages → Custom domain, enter your domain
3. In your domain registrar's DNS settings, add:
   - Type: `A` → Name: `@` → Value: GitHub Pages IPs (see GitHub docs)
   - Type: `CNAME` → Name: `www` → Value: `yourusername.github.io`
4. Wait for DNS propagation (up to 24 hours)

---

Your personal website is now live! 🎉
