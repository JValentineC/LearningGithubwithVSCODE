GitHub Portfolio Setup Runbook
Eight steps from an empty GitHub repo to a live portfolio site: create the repo, clone it, set up your files, work on a branch, then commit, merge, and publish with GitHub Pages. Follow them in order.
Step 1 · Make the repo (on github.com)
1. Click New repository.
2. Name it portfolio.
3. Choose Public, check Add a README file, click Create repository.
Step 2 · Clone it to your computer
1. On the repo page, click the green Code button and copy the HTTPS URL.
2. Open your terminal and go to where you keep your projects, e.g. cd ~/Projects.
3. Run git clone https://github.com/USERNAME/portfolio.git.
4. Move into the new folder: cd portfolio.
✅ Checkpoint 1 — Repo cloned locally. Running ls (Windows: dir) shows a README.md file already there.
Step 3 · Set up your file structure
1. Create your main files: touch index.html style.css (Windows PowerShell: ni index.html, style.css, or just create them in your editor).
2. Open the folder in your code editor: code .
3. Add a basic HTML skeleton to index.html — doctype, <head>, and a <body> with a placeholder heading. Leave style.css empty for now.
✅ Checkpoint 2 — Files created. Your editor's file tree shows index.html, style.css, and README.md.
Step 4 · Create your working branch
Keep main clean — build on a separate branch:
git switch -c build-portfolio
This creates build-portfolio and switches to it in one step. Confirm with git branch — the current branch has a * next to it.
Step 5 · Build your portfolio
Add your content to index.html and your styling to style.css. Save often — nothing gets committed until Step 7, so there's no risk in experimenting.
Step 6 · Check your work

Before committing, see what Git has noticed:
git status
You should see index.html and style.css listed as untracked (or modified) files.
Checkpoint 3 — Ready to commit. git status shows your changed files, and git branch confirms you're still on build-portfolio.

Step 7 · Commit, push, merge
Save your files first, then run:
git add index.html style.css
git commit -m "Add portfolio structure and styling"
git push -u origin build-portfolio
Now bring your work onto main:
git switch main
git merge build-portfolio
git push
Checkpoint 4 — Pushed & merged. Refresh your repo page on GitHub — you should see index.html and style.css with your commit message.

Step 8 · Publish with GitHub Pages
On GitHub, in your repo:
1. Settings → Pages (left sidebar).
2. Source: choose Deploy from a branch.
3. Branch: main, folder / (root). Click Save.
4. Wait 1–2 minutes, then refresh the page. A green banner shows your link: https://USERNAME.github.io/portfolio/
Open it. Paste the link in the class channel.
Checkpoint 5 — Live on Pages. Your styled portfolio loads at your public URL. You shipped it. 🚀