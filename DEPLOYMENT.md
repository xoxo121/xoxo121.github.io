# How to Deploy Your Portfolio Website

## Option 1: GitHub Pages (Recommended - Free)

### Step 1: Create a GitHub Repository

1. Go to [GitHub.com](https://github.com) and sign in
2. Click the "+" icon in the top right → "New repository"
3. Repository name options:
   - **Option A**: `yourusername.github.io` (e.g., `rahulvimalkanth.github.io`) - This will make your site available at `https://yourusername.github.io`
   - **Option B**: Any name (e.g., `portfolio`) - Your site will be at `https://yourusername.github.io/portfolio`
4. Make it **Public** (required for free GitHub Pages)
5. **Don't** initialize with README, .gitignore, or license (we already have files)
6. Click "Create repository"

### Step 2: Push Your Code to GitHub

Open terminal in this directory and run:

```bash
cd /Users/rahulvimalkanth/Documents/Coding/Site/jonbarron.github.io

# Remove the old git remote (if it exists)
git remote remove origin

# Add your new repository as origin
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git

# Stage all changes
git add .

# Commit your changes
git commit -m "Initial commit: Personal portfolio website"

# Push to GitHub
git push -u origin master
```

**Note**: Replace `YOUR_USERNAME` and `YOUR_REPO_NAME` with your actual GitHub username and repository name.

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top menu)
3. Scroll down to **Pages** (left sidebar)
4. Under **Source**, select:
   - **Branch**: `master` (or `main` if that's your default)
   - **Folder**: `/ (root)`
5. Click **Save**

### Step 4: Access Your Website

- If repository is `yourusername.github.io`: Your site will be at `https://yourusername.github.io`
- If repository has another name: Your site will be at `https://yourusername.github.io/repository-name`

**Note**: It may take a few minutes (up to 10) for the site to go live after enabling Pages.

---

## Option 2: Custom Domain (Optional)

If you have your own domain (e.g., `rahulvimalkanth.com`):

1. Create a file named `CNAME` in the root directory with just your domain name:
   ```
   rahulvimalkanth.com
   ```

2. In your domain registrar's DNS settings, add:
   - **Type**: CNAME
   - **Name**: @ (or www)
   - **Value**: `yourusername.github.io`

3. Push the CNAME file to GitHub:
   ```bash
   git add CNAME
   git commit -m "Add custom domain"
   git push
   ```

4. In GitHub repository Settings → Pages, you'll see your custom domain option.

---

## Option 3: Other Hosting Services

- **Netlify**: Drag and drop your folder at [netlify.com](https://netlify.com)
- **Vercel**: Connect your GitHub repo at [vercel.com](https://vercel.com)
- **Cloudflare Pages**: Free hosting with GitHub integration

---

## Troubleshooting

- **Site not loading?** Wait 5-10 minutes after enabling Pages
- **Images not showing?** Make sure all image paths are relative (starting with `images/`)
- **Styling broken?** Check that `stylesheet.css` is in the root directory
- **Need to update?** Just push new changes to GitHub - Pages auto-updates

