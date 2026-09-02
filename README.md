# Light Analytics website

This is a static Jekyll site for [Light Analytics](https://github.com), built to run on GitHub Pages with no server, no database, and no build step beyond what GitHub Pages provides natively.

## Before you deploy

1. Add the founder photo. Save it as `assets/img/lucy-headshot.jpeg` (that exact filename, replacing the placeholder path already referenced in the CSS).
2. Set up the contact form. Go to [formspree.io](https://formspree.io), create a free account, and create a new form. Formspree will give you a form ID. Open `contact.md` and replace `YOUR_FORM_ID` in the line `action="https://formspree.io/f/YOUR_FORM_ID"` with your real ID.
3. Fill in your contact details. Open `contact.md` and replace `[INSERT EMAIL]` and `[INSERT LINKEDIN URL]` with your actual email address and LinkedIn profile URL.

## Deploy to GitHub Pages from zero

These steps assume you have never used git or GitHub before. Follow them in order.

1. **Create a GitHub account**, if you don't already have one, at [github.com](https://github.com).

2. **Install git** on your computer, if it isn't already installed:
   - Mac: open Terminal and type `git --version`. If it isn't installed, macOS will prompt you to install it.
   - Windows: download and install [Git for Windows](https://git-scm.com/download/win), which gives you "Git Bash," a terminal you'll use for the commands below.

3. **Create a new repository on GitHub:**
   - Go to [github.com/new](https://github.com/new).
   - Name the repository `light-analytics` (or any name you like).
   - Leave it **Public**.
   - Do **not** check "Add a README file" (this project already has one).
   - Click **Create repository**.
   - Keep the page GitHub shows you open. You'll need the repository URL from it in step 5 (it looks like `https://github.com/YOUR-USERNAME/light-analytics.git`).

4. **Open a terminal** and navigate into this project folder. For example, if you extracted this project to your Downloads folder:
   ```
   cd ~/Downloads/light-analytics
   ```

5. **Initialize git and push the code**, replacing the URL below with the one from your own repository page:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/light-analytics.git
   git push -u origin main
   ```
   If this is your first time using git, it may ask you to sign in to GitHub in your browser. Follow the prompts.

6. **Enable GitHub Pages:**
   - On GitHub, go to your repository's page.
   - Click **Settings** (top menu of the repository).
   - In the left sidebar, click **Pages**.
   - Under "Build and deployment," set **Source** to **Deploy from a branch**.
   - Under "Branch," select **main** and folder **/ (root)**, then click **Save**.

7. **Wait about one to two minutes**, then refresh the Pages settings screen. GitHub will show a message like "Your site is live at `https://YOUR-USERNAME.github.io/light-analytics/`." Click that link to see your site.

That's it. The site is now live and will automatically rebuild every time you push a new commit.

## How to publish a new blog post

1. Inside the `_posts/` folder, create a new file. The filename must follow this exact pattern:
   ```
   YYYY-MM-DD-your-post-title.md
   ```
   For example, a post published on 14 March 2026 called "Insider Lending at Tier 2 Banks" would be named:
   ```
   2026-03-14-insider-lending-tier-2-banks.md
   ```
   The date in the filename is what Jekyll uses to sort and publish the post, so it must match the date you want it to appear under.

2. At the top of the file, add this front matter block, filled in with your details:
   ```
   ---
   layout: post
   title: "Your Post Title Here"
   date: 2026-03-14
   author: Lucy Wangui
   ---
   ```

3. Below the second `---` line, write your post in standard Markdown (headings with `#`, bold with `**text**`, links with `[text](url)`, and so on).

4. Save the file, then push it live from your terminal, inside the project folder:
   ```
   git add .
   git commit -m "New post: Your Post Title Here"
   git push
   ```

5. GitHub Pages will automatically rebuild the site. Your new post will appear on the Blog page and in "Latest from the Blog" on Home within a couple of minutes.

To remove the placeholder template post, delete `_posts/2026-01-01-sample-post-replace-me.md` using the same `git add . && git commit && git push` steps above.

## Local preview (optional)

If you have Ruby installed and want to preview changes on your own computer before pushing:

```
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000` in your browser. This step is optional; pushing to GitHub is enough to publish.
