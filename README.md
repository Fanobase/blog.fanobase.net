# Fanobase blog

The public Fanobase blog at <https://blog.fanobase.net/>, built with Hugo.
It shares the devlog's minimal layouts and styling and publishes ordinary static
HTML, with a collaborators page, RSS feeds, and a sitemap.

## Local development

Install Hugo 0.161.1 or newer, then preview the site:

```sh
hugo server
```

Build the production site into `public/`:

```sh
hugo --minify
```

The site is self-contained: no external theme or Node dependencies are needed.

## Content

- Posts live in `content/posts/`.
- The home page introduction lives in `content/_index.md`.
- Collaborators are listed in `data/collaborators.yaml`.

Create a draft post with `hugo new content posts/post-title.md`, then set
`draft = false` when it is ready to publish.

## Deployment

The [GitHub Pages workflow](.github/workflows/deploy.yml) builds and deploys
`public/` on pushes to `main` or manual dispatch, following
[Hugo's GitHub Pages deployment workflow](https://gohugo.io/host-and-deploy/deploy-to-github-pages/).

In the repository's **Settings → Pages**, select **GitHub Actions** as the build
source and configure `blog.fanobase.net` as the custom domain with the appropriate
DNS records. The production URL is set in `hugo.toml` and `static/CNAME`.
The workflow uses GitHub's built-in token and does not need a separate deploy key
or site password.
