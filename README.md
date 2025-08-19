# Cyber Journey Blog (GitHub Pages Starter)

This is a minimal Jekyll blog for GitHub Pages. It uses the official **minima** theme and includes a starter post and template.

## How to publish

1. Create a new repository on GitHub named: `musa-cyber-blog` or any name you like.
2. Upload the contents of this zip to the repo root.
3. In GitHub, go to **Settings → Pages**.
4. Under **Source**, choose **Deploy from a branch**.
5. Set **Branch** to **main** and **/ (root)**, then **Save**.
6. After it builds, your site will be live at `https://<your-username>.github.io/<repo-name>/`.

### Add a new post

- Create a file under `_posts` named `YYYY-MM-DD-title.md`.
- Copy the front matter from `post-template.md` and fill it in.
- Commit and push. GitHub Pages will rebuild automatically.

### Local preview (optional)

If you want to preview locally:
- Install Ruby and Bundler.
- Run:
  ```bash
  bundle install
  bundle exec jekyll serve
  ```
- Open `http://127.0.0.1:4000`

