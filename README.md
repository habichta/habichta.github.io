# habichta.github.io

Personal website, built with Jekyll. The [so-simple-theme](https://github.com/mmistakes/so-simple-theme) files are vendored locally (`_layouts/`, `_includes/`, `_sass/`), published via GitHub Pages at <https://habichta.github.io/>.

## Structure

```
├── _config.yml          # site + theme settings (title, email, github, linkedin, ...)
├── Gemfile              # gem dependencies (github-pages, webrick)
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

Gems install into your user gem directory (`~/.gems`) — no sudo needed:

```
bundle install               # once after cloning, and when the Gemfile changes
bundle exec jekyll serve
```

Then open <http://localhost:4000>.

Notes:

- `bundle install` resolves the Gemfile and writes a local `Gemfile.lock` (gitignored) that pins all versions.
- Always start Jekyll through Bundler (`bundle exec jekyll serve`). Bare `jekyll serve` activates the newest installed gems before Bundler runs and can fail with `You have already activated ...` errors (e.g. `json`, `public_suffix`).
- If a bare `gem install <gem>` ever complains about `/var/lib/gems` permissions, add `--user-install` or make sure `GEM_HOME` points at a writable directory (`export GEM_HOME="$HOME/.gems"`).
