# Welcome to your Lovable project

## Project info

**URL**: https://lovable.dev/projects/a9f294f8-734b-43ef-85fd-41e5c281dd93

## How can I edit this code?

There are several ways of editing your application.

**Use Lovable**

Simply visit the [Lovable Project](https://lovable.dev/projects/a9f294f8-734b-43ef-85fd-41e5c281dd93) and start prompting.

Changes made via Lovable will be committed automatically to this repo.

**Use your preferred IDE**

If you want to work locally using your own IDE, you can clone this repo and push changes. Pushed changes will also be reflected in Lovable.

The only requirement is having Node.js & npm installed - [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating)

Follow these steps:

```sh
# Step 1: Clone the repository using the project's Git URL.
git clone <YOUR_GIT_URL>

# Step 2: Navigate to the project directory.
cd <YOUR_PROJECT_NAME>

# Step 3: Install the necessary dependencies.
npm i

# Step 4: Start the development server with auto-reloading and an instant preview.
npm run dev
```

**Edit a file directly in GitHub**

- Navigate to the desired file(s).
- Click the "Edit" button (pencil icon) at the top right of the file view.
- Make your changes and commit the changes.

**Use GitHub Codespaces**

- Navigate to the main page of your repository.
- Click on the "Code" button (green button) near the top right.
- Select the "Codespaces" tab.
- Click on "New codespace" to launch a new Codespace environment.
- Edit files directly within the Codespace and commit and push your changes once you're done.

## What technologies are used for this project?

This project is built with:

- Vite
- TypeScript
- React
- shadcn-ui
- Tailwind CSS

## How can I deploy this project?

### Deploy to GitHub Pages

This project is configured for GitHub Pages deployment with automatic CI/CD.

**Quick Setup:**

1. **Create a GitHub repository** (or use an existing one)
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   git push -u origin main
   ```

2. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Click **Settings** → **Pages** (in the left sidebar)
   - Under **Source**, select **GitHub Actions**
   - The workflow will automatically deploy your site on every push to main/master

3. **Your site will be live at:**
   - `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/` (if using a repository)
   - `https://YOUR_USERNAME.github.io/` (if repository is named `YOUR_USERNAME.github.io`)

**For username.github.io (root domain):**
- Name your repository exactly: `YOUR_USERNAME.github.io`
- In `vite.config.ts`, change `base: './'` to `base: '/'`
- Your site will be at: `https://YOUR_USERNAME.github.io/`

**Manual Build & Test:**
```bash
npm run build
npm run preview  # Test the production build locally
```

The build output will be in the `dist` folder, which is automatically deployed by GitHub Actions.

## Can I connect a custom domain to my Lovable project?

Yes, you can!

To connect a domain, navigate to Project > Settings > Domains and click Connect Domain.

Read more here: [Setting up a custom domain](https://docs.lovable.dev/features/custom-domain#custom-domain)
