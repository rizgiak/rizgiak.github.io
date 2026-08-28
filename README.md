# Aulia Khilmi Rizgi

This repository contains the source code for [Aulia Khilmi Rizgi's personal website](https://rizgiak.github.io/). The site is built with Jekyll and hosted on GitHub Pages.

The website collects Khilmi's background, robotics work, publications, talks, teaching activities, and selected projects.

## Repository layout

- `_pages/`: main pages such as About, CV, Publications, Projects, Talks, and Teaching
- `_projects/`: project entries shown on the website
- `_publications/`: publication entries and metadata
- `_talks/`: talks and presentations
- `_teaching/`: teaching-related entries
- `_data/`: navigation, author, interface, and comment data
- `images/`: images used by the website
- `files/`: downloadable files such as CVs and project documents
- `assets/` and `_sass/`: stylesheets, JavaScript, and other frontend assets
- `markdown_generator/`: optional tools for generating publication and talk pages

## Run locally

### Requirements

- Ruby and RubyGems
- Bundler
- Node.js and npm for JavaScript asset tasks

Configure Bundler to install gems in the project directory. This avoids requiring write access to system Ruby directories:

```bash
bundle config set --local path 'vendor/bundle'
```

Install the Ruby dependencies from the repository root:

```bash
bundle install
```

Do not use `sudo bundle install`. The generated `.bundle/` configuration and `vendor/bundle/` directory are local development files and are ignored by Git.

Start the development server with the project's bundled Jekyll version:

```bash
bundle exec jekyll serve --config _config.yml,_config.dev.yml --livereload --host 127.0.0.1 --port 4000
```

Open <http://127.0.0.1:4000> in a browser. Jekyll will rebuild the site when files change, and LiveReload will refresh the page when supported by the browser.

To build the site without starting a server:

```bash
bundle exec jekyll build
```

Use `bundle exec` for Jekyll commands so the versions declared by the project's `Gemfile` are used instead of a system-wide Jekyll installation.

## Updating content

Most content can be updated by editing the corresponding Markdown file:

1. Update personal details and site-wide settings in `_config.yml`.
2. Add or edit pages in `_pages/`.
3. Add projects, publications, talks, or teaching entries in their respective collection directories.
4. Put public downloads in `files/` and reference them from Markdown.
5. Use `npm run build:js` when JavaScript source changes require rebuilding the minified asset.

## Deployment

The `master` branch is the source for the GitHub Pages site. Push changes to GitHub and let the repository's Pages workflow build and publish the site.

Before pushing, it is useful to run:

```bash
bundle exec jekyll build
```

## Credits

The site started from [Academic Pages](https://academicpages.github.io/), which is based on the [Minimal Mistakes Jekyll theme](https://mmistakes.github.io/minimal-mistakes/). The original project and theme are retained under the terms described in [LICENSE](LICENSE).
