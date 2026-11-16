# Tianyang Luo ? academic homepage

Personal Jekyll site: https://tianyangluo-pku.github.io/
Based on https://github.com/shaoyanliu/academic-homepage. Original CSS, layouts, JavaScript, LICENSE and third-party notices are retained.

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
GitHub Settings > Pages > Build and deployment > Source should be GitHub Actions. `.github/workflows/pages.yml` is the retained deployment workflow; do not add a competing branch deployment. Push to main triggers it.

Run 43848868533 failed before starting any build steps. Its check annotation states: "The job was not started because your account is locked due to a billing issue." Resolve the account issue in GitHub billing/support, then rerun the workflow. Workflow logs were unavailable (BlobNotFound); the check annotation establishes the cause.
Local environment has no Ruby/Bundler or installed WSL distribution. YAML and source checks can run here, but a real Jekyll build and rendered desktop/mobile review remain required after unlocking Actions.
