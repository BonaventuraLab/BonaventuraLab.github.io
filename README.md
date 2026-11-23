# Bonaventura Lab website (Jekyll)

This is a starter website for GitHub Pages using Jekyll. It is designed so that routine updates can be made by editing simple Markdown and YAML files.

## Before publishing

1. Confirm that the GitHub organization is `BonaventuraLab`.
2. Create a repository named **BonaventuraLab.github.io** under that organization (or use the existing Pages repository if one already exists).
3. Upload the contents of this folder to the repository's root. Do not upload the enclosing ZIP folder itself.
4. In `_config.yml`, confirm `url: "https://bonaventuralab.github.io"` and `baseurl: ""`.
5. In GitHub, open **Settings → Pages** and choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then Save.
6. Wait a few minutes and check `https://bonaventuralab.github.io`.

If the repository already contains a website, download or keep a backup before replacing files. Do not delete the old repository.

## Update content

- **People:** edit `_data/members.yml`. Add portraits under `assets/images/` and set `photo: /assets/images/your-photo.jpg`.
- **Publications:** edit `_data/publications.yml`. Use verified titles, author lists, journal details, and DOI identifiers.
- **News:** create a Markdown file in `_posts` named `YYYY-MM-DD-short-title.md`. Start it with:

  ---
  layout: post
  title: "A news headline"
  date: 2026-11-22
  category: Publication
  ---

  Write the news item below the front matter.

- **Repositories:** edit `_data/repositories.yml`.
- **Research areas:** edit `_data/research.yml`.
- **Contact details:** edit `_data/links.yml`.

## Important

The member list and publication list are intentionally only starter examples. Review and replace them before making the site public. Check all institutional names, email addresses, links, biographies, and publication metadata.

## Local preview (optional)

If you have Ruby installed, run:

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://127.0.0.1:4000`.

## Design notes

The site uses a custom responsive layout and CSS, without a third-party theme. Google Fonts are loaded remotely; if you prefer no external font requests, remove the `@import` line at the top of `assets/css/main.css`.
