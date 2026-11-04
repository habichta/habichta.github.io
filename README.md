# habichta.github.io

Personal website, built with Jekyll using the [so-simple-theme](https://github.com/mmistakes/so-simple-theme) as a remote theme, published via GitHub Pages at <https://habichta.github.io/>.

## Structure

```
├── _config.yml          # site + theme settings (title, email, github, linkedin, ...)
├── _includes/           # header and social-icon overrides
├── _layouts/blog.html   # blog overview layout
├── index.md             # home page
├── blog/index.html      # blog overview page
├── _posts/              # blog posts (Markdown, one file per post)
└── assets/              # CV.pdf, favicon, images
```

## Editing

- Change your name, description, email, GitHub and LinkedIn in `_config.yml` (`theme_settings`).
- Edit the home page in `index.md`.
- Add a blog post by creating a new file in `_posts/` named `YYYY-MM-DD-title.md` with `layout: post` in the front matter.
- Replace `assets/CV.pdf` with your real CV — the nav bar links to it.

## Local preview

```
gem install jekyll jekyll-remote-theme
jekyll serve
```

Then open <http://localhost:4000>.
