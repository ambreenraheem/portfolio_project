# portfolio_project

### Name: Ambreen Abdul Raheem
### Profession: Microsoft Power BI Data Analyst (Upwork Freelancer)
### Project: Making my own Portfolio Website
#### I'd like to share my coding experience in creating a portfolio website, and this GitHub repository is open-source for all.
### Date:01-06-2025

# Building a portfolio

We will use MkDocs for building a portfolio. MkDocs is a static site generator designed for project documentation. It is written in Python and uses the Jinja2 templating engine. Mkdocs is easy to use and has a lot of features that make it a good choice for a portfolio.

#### For full documentation, visit [mkdocs.org](https://www.mkdocs.org).

# Step 1: Install Mkdocs
```bash
pip install mkdocs
pip install mkdocs-git-revision-date-localized-plugin mkdocs-material mkdocs-material-extensions mkdocs-git-authors-plugin
```

# Step 2: Creating a new project
```bash
mkdocs new my_portfolio_website_project
cd my_portfolio_website_project
```

# Step 3: Run the development server
```bash
mkdocs serve
```

> This is how you can specify the port and host
mkdocs serve -a 127.0.0.1:8500


# Step 4: Build the project
```bash
mkdocs build
```
#### Note: "It will create a new folder named site containing the complete HTML code for our website. You can reuse this folder on any platform to build a new website with a different name or for a new project." 


# Step 5: mkdocs.yml and docs/
 #### Note: "For the website, we will implement all remaining changes, updates, and information additions in these two separate files."


# Step 6: Initialize Git and push your project:
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/your-username/mera_portfolio.git # replace the link to your repo
git push -u origin main
```

# Step 7: Install GitHub Deploy Tool
#### Install the deploy helper, follow the instructions given in Step 1 to install the mkdocs package.
#### And update mkdocs.yml if you need to customize anything:
```bash
theme:
  name: material          # if you want
```
# Step 8: Deploy to GitHub Pages
```bash
mkdocs gh-deploy
```
**This command will deploy your site to the gh-pages branch of your repository. If you want to deploy to a different branch, you can specify it using the --remote-branch option.**


# 🌐 Step 9: Access Your Live Site
The site is live on GitHub Pages at: https://your-username.github.io/mera_portfolio/ Replace your-username with your GitHub username and mera_portfolio with your repository name. You can also specify a custom domain by adding a CNAME file to the docs/ directory. This file should contain your custom domain name (e.g., www.yourdomain.com).

# Step 10: (mkdocs build --clean) — Why and When You Need It
# Purpose:
This command cleans the old site build before creating a new one.

⚠️ Problem Without --clean:
MkDocs by default keeps old files from previous builds in the site/ folder — even if:
- You've deleted or renamed a file (like a PDF),

- Or moved it inside docs/,

- Or changed folder structure.
