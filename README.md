# Tianyang Luo - academic homepage

Personal Jekyll site: https://tianyangluo-pku.github.io/
Based on https://github.com/shaoyanliu/academic-homepage. Original layouts, typography, colors, JavaScript, LICENSE and third-party notices are retained. A narrowly scoped CSS fix removes empty thumbnail space and badge overlap for papers without images.

## Maintenance
- `_config.yml`: identity, canonical URL and optional profile links. Keep `baseurl` empty for this user site.
- `index.md`: About Me, Research Interests, Selected Publications and Education.
- `_data/navigation.yml`: displayed in reverse order; About and Publications only.
- `_data/publications.yml`: full list, newest first within each year; `selected: true` features a record on the homepage. Highlight Tianyang Luo with `publication-self-author`.
- `_data/publication_topics.yml`: currently empty; add verified topic IDs only when needed.
- `_includes/publications.md`: original search, filtering and resource rendering components.
- `publications.md`: full publication list.

Removed unused demo page entry points. Shared includes remain available for future sections. Demo PDFs, BibTeX and illustrations are excluded from the generated site. Add only authentic photos, email, CV and public resource links when available.

## Publication provenance and pending metadata
ISCA title and full author order verified against https://www.iscaconf.org/isca2026_dev/program/ and IEEE Xplore https://ieeexplore.ieee.org/abstract/document/11617910 (2026-11-16). DOI: 10.1109/ISCA66397.2026.00078. Title capitalization follows the conference program.
IEDM title and acceptance supplied by the site owner; no authoritative matching public record found in this check. Full author list and public resources remain pending; temporary authors: Tianyang Luo et al. Status is accepted for presentation, not presented.
Education dates, supervisors, email, photograph, CV and Scholar ID were not provided and are intentionally omitted.

## Build and deployment
Use Ruby/Bundler, then `bundle install` and `bundle exec jekyll build`. Preview with `bundle exec jekyll serve`.

Verified production configuration (2026-11-16): Settings > Pages > Deploy from a branch > main > / (root). GitHub's built-in Jekyll Pages build publishes each push. Keep this single automatic deployment mechanism.

`.github/workflows/pages.yml` is retained as a manual-only alternative. Before using it, resolve the GitHub account billing lock and switch Pages Source to GitHub Actions. Never run it alongside branch publishing. Custom workflow runs 43848868533 and 43853627263 did not start because GitHub reported: "The job was not started because your account is locked due to a billing issue." This does not prevent the built-in branch Pages build.

Local environment has no Ruby/Bundler or installed WSL distribution. YAML, front matter, include-reference and diff checks passed locally. Production build validation uses GitHub Pages. Rendered browser desktop/mobile review is separate from HTTP/content checks.

Git authentication and push were completed by the owner. In this environment GitHub requires the existing Windows proxy; use `git -c http.proxy=http://127.0.0.1:7890 push origin main` if direct connections fail. This command does not alter global Git configuration.

Validation: built-in Pages build succeeded; both live pages and 16 internal page/asset URLs returned 200. Removed demo pages and sample PDFs returned 404. Browser checks at 1440px and 390px verified content, no horizontal overflow, and publication search.
