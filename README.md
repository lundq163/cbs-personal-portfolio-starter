# Personal portfolio starter

Make a simple portfolio and practice version control with GitHub. This is a static website: no installation, backend, or build step is required. A small GitHub Actions workflow publishes the HTML and CSS to GitHub Pages.

## Before the workshop

Complete the short setup survey so we know what help you may need:

- Do you already have a GitHub account, and can you sign in?
- Is your school email added and verified in that existing account? Add it under **Settings > Emails** if needed, then apply for [GitHub Education](https://education.github.com/). You do not need to make your school email primary or change your GitHub no-reply email.
- GitHub Education and the [GitHub Copilot desktop app](https://github.com/apps/copilot) are strongly recommended for this series.
- Do you have Git installed? Check by running `git --version` in a terminal. If the command is missing, install Git with the command for your computer:

  ```sh
  # macOS with Homebrew
  brew install git

  # Ubuntu or Debian Linux
  sudo apt install git

  # Windows with Windows Package Manager
  winget install --id Git.Git -e
  ```

## Make your own copy

On GitHub, select **Use this template > Create a new repository** to make your own copy. Name the new repository `YOUR-USERNAME.github.io`, replacing `YOUR-USERNAME` with your GitHub username. This gives your portfolio the easy-to-find address `https://YOUR-USERNAME.github.io/`. A public repository works with GitHub Free.

### Event 1: make and publish the first version

The main path is using Git on your computer with an SSH connection to GitHub. If you have not set up SSH yet, follow GitHub's [SSH key guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh); your instructor can help. Alternatively, you can use GitHub's website to edit `index.html` and `style.css` and commit each change.

1. Clone your copy to your computer. Replace `YOUR-USERNAME` with your GitHub username:

   ```sh
   git clone git@github.com:YOUR-USERNAME/YOUR-USERNAME.github.io.git
   cd YOUR-USERNAME.github.io
   ```

2. Edit `index.html`: replace the placeholder name, introduction, project, and contact text with your own. Edit `style.css` to change the appearance.
3. Save your changes in Git. For a first commit, run:

   ```sh
   git add index.html style.css
   git commit -m "Add my portfolio"
   git push
   ```

   If you made a separate first commit when creating the repository, this will be your second commit. Otherwise, it is your first. One or two commits are enough to get started.

### Event 2: customize

Add a section, update your project details, or try a small style change. Commit and push again to see GitHub Pages publish the update.

## Publish with GitHub Pages

The included [Pages workflow](.github/workflows/pages.yml) automatically packages and deploys the repository on each push to `main`. For your copy, open **Settings > Pages** and set **Build and deployment > Source** to **GitHub Actions**. The first push to `main` starts the deployment. If your default branch is named something other than `main`, change the workflow's branch under `on.push.branches` to match.

Check the **Actions** tab for deployment progress. When it succeeds, find your published URL under **Settings > Pages**. It can take several minutes for the site to appear.

If you named your repository `YOUR-USERNAME.github.io`, your portfolio address is `https://YOUR-USERNAME.github.io/`. GitHub allows only one user site per account. If you already have a repository with that name, keep it and give this portfolio a different repository name; it will be published at `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/` instead.

Use relative links to files, such as `style.css` or `images/photo.jpg`, not `/style.css`. Relative paths work both for the account site's root and a project site's repository path.

## Preview and safety

Open `index.html` in a browser to preview it locally. GitHub Pages serves static files; it cannot run server-side code or safely hide secrets. **Everything you publish is public. Never commit passwords, API keys, tokens, or other secrets.** Share only information and files you have permission to publish.

See GitHub's [Pages quickstart](https://docs.github.com/en/pages/quickstart) and [publishing source guide](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) for details and troubleshooting.
