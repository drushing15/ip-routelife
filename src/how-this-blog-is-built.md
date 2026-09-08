# How This Blog Is Built

This blog follows a **documentation as code** approach.

## The stack

- Posts are written in [Markdown](https://www.markdownguide.org/basic-syntax/)
- [Git](https://github.com/git-guides) tracks every change
- [mdBook](https://rust-lang.github.io/mdBook/) turns the Markdown into a static HTML site
- **GitHub Pages** + **GitHub Actions** build and deploy the site automatically on every push
- A custom domain with a free, auto-renewing SSL certificate (via Let's Encrypt, provisioned by GitHub Pages)

## Local development

```console
mdbook serve
vscode
```

This starts a local server with live-reload at `http://localhost:3000`, rebuilding the site every time a `.md` file is saved.

## Publishing

```console
git add .
git commit -m "New post: <title>"
git push
```

Pushing to `main` triggers a GitHub Actions workflow that builds the book and deploys it to GitHub Pages — no manual upload required.
