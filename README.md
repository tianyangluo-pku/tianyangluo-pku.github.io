# Tianyang Luo | Academic Homepage

Personal academic website of Tianyang Luo, a Ph.D. student at the School of Integrated Circuits, Peking University.

**Website:** https://tianyangluo-pku.github.io/

Built with Jekyll using [Shaoyan Liu's academic homepage template](https://github.com/shaoyanliu/academic-homepage).

## Site structure

The homepage contains About (biography and research interests), Experience (education), and Publications. Navigation links to these sections. The previous `/publications/` address redirects to the homepage publication section.

## Editing

| File | Content |
| --- | --- |
| `index.md` | Biography, research interests, and education |
| `_config.yml` | Site details, profile links, email, and portrait path |
| `_data/navigation.yml` | Navigation links |
| `_data/publications.yml` | Publication titles, authors, venues, and resource links |
| `_includes/publications.md` | Shared publication display component |
| `assets/css/about.css` | Homepage layout and typography adjustments |
| `assets/img/tianyang-luo.jpg` | Profile photograph |

The homepage displays all publication records, grouped by year. Add new entries to `_data/publications.yml` using the existing format and verified metadata. Publication titles link to their public resources when available. Search and filtering remain available in the shared component but are hidden on the homepage.

Keep `url` set to `https://tianyangluo-pku.github.io` and `baseurl` empty for this GitHub Pages user site.

## Local preview

With Ruby and Bundler installed:

```sh
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000 to preview. Run `bundle exec jekyll build` to generate the site in `_site/`.

## Publishing

Commit changes and push to `main`. GitHub Pages builds and publishes the site automatically using **Settings > Pages > Deploy from a branch > main > / (root)**. Check the **pages build and deployment** run in the Actions tab, then verify the live site.

The workflow in `.github/workflows/pages.yml` is a manual alternative; it is not used for the current branch-based deployment.

## Credits and licensing

The original template license is preserved in [LICENSE](LICENSE). See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for template attribution and third-party component licenses.
