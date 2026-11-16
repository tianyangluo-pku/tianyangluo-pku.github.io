# Tianyang Luo - academic homepage

Personal Jekyll site: https://tianyangluo-pku.github.io/
Based on https://github.com/shaoyanliu/academic-homepage. Original layouts, typography, colors, JavaScript, LICENSE and third-party notices are retained. A narrowly scoped CSS fix removes empty thumbnail space and badge overlap for papers without images.

## Maintenance
- `_config.yml`: identity, canonical URL and optional profile links. Keep `baseurl` empty for this user site.
- `index.md`: About Me, Education, Research Interests and Selected Publications.
- `_data/navigation.yml`: displayed in reverse order; About and Publications only.
- `_data/publications.yml`: full list, newest first within each year; `selected: true` features a record on the homepage. Highlight Tianyang Luo with `publication-self-author`.
- `_data/publication_topics.yml`: currently empty; add verified topic IDs only when needed.
- `_includes/publications.md`: original search, filtering and resource rendering components.
- `publications.md`: full publication list.

Removed unused demo page entry points. Shared includes remain available for future sections. Demo PDFs, BibTeX and illustrations are excluded from the generated site. Add only authentic photos, email, CV and public resource links when available.

## Publication provenance and pending metadata
ISCA title and full author order verified against https://www.iscaconf.org/isca2026_dev/program/ and IEEE Xplore https://ieeexplore.ieee.org/abstract/document/11617910 (2026-11-16). DOI: 10.1109/ISCA66397.2026.00078. Title capitalization follows the conference program.
IEDM title and acceptance supplied by the site owner; no authoritative matching public record found in this check. Full author list and paper number 24-4 were subsequently supplied by the owner from the conference program; public resource links remain pending. Status is accepted for presentation, not presented.
Supervisors, email, photograph, CV and Scholar ID were not provided and are intentionally omitted.

## Build and deployment
Use Ruby/Bundler, then `bundle install` and `bundle exec jekyll build`. Preview with `bundle exec jekyll serve`.

Verified production configuration (2026-11-16): Settings > Pages > Deploy from a branch > main > / (root). GitHub's built-in Jekyll Pages build publishes each push. Keep this single automatic deployment mechanism.

`.github/workflows/pages.yml` is retained as a manual-only alternative. Before using it, resolve the GitHub account billing lock and switch Pages Source to GitHub Actions. Never run it alongside branch publishing. Custom workflow runs 43848868533 and 43853627263 did not start because GitHub reported: "The job was not started because your account is locked due to a billing issue." This does not prevent the built-in branch Pages build.

Local environment has no Ruby/Bundler or installed WSL distribution. YAML, front matter, include-reference and diff checks passed locally. Production build validation uses GitHub Pages. Rendered browser desktop/mobile review is separate from HTTP/content checks.

Git authentication and push were completed by the owner. In this environment GitHub requires the existing Windows proxy; use `git -c http.proxy=http://127.0.0.1:7890 push origin main` if direct connections fail. This command does not alter global Git configuration.

Validation: built-in Pages build succeeded; both live pages and 16 internal page/asset URLs returned 200. Removed demo pages and sample PDFs returned 404. Browser checks at 1440px and 390px verified content, no horizontal overflow, and publication search.

## ORCID update (2026-11-16)
Public ORCID record: https://orcid.org/0009-0000-5288-6817 (public API v3.0, works and educations).
Five public works were verified by DOI against Crossref: NASiC (DAC 2026), DIAMoND (ISCA 2026), LoRA write-back (ISCAS 2026), multi-level-cell computing (EDTM 2026), and ternary transistor (SNW 2024). Titles and full author order follow publisher-deposited Crossref metadata; DIAMoND now uses the deposited capitalization MOE. The IEDM accepted paper remains, for six total entries. Homepage selections are IEDM, ISCA and EDTM. Full list is ordered by publication date, with upcoming IEDM first. No abstracts or unverified PDF links added.
Education dates and departments follow the public ORCID record: bachelor's 2021-2025, doctoral start 2025. ORCID lists a future doctoral end of 2030; website uses 2025-present to avoid implying graduation. Applied Physics degree subject is owner-confirmed. Economics dates 2022-2025 and bachelor's degree status were subsequently confirmed by the owner.
NSD official English name: National School of Development. Its English pages use both "double-degree program in economics" (https://en.nsd.pku.edu.cn/aboutus/30th/537358.htm) and "Economics Double-major Program" (https://en.nsd.pku.edu.cn/programs/doublemajor/index.htm). Use owner-confirmed Bachelor of Economics (Double Degree), without inventing a B.A./B.Sc. designation; see official Chinese degree program https://nsd.pku.edu.cn/jxxm/bks/xmjs_bks/sxwfx/530304.htm.

Owner corrections: Education now follows About Me; all three school names use plain text consistently. Economics is a bachelor's degree (double degree), 2022-2025. ISCA marks both Ling Liang and Tianyang Luo with asterisks and an equal-contribution note immediately below the authors, as confirmed by the owner. IEDM uses the owner-provided 13-author conference-program order and paper number 24-4; displays the concise status Accepted and no invented DOI/PDF. No styling changes.

Presentation refinement: education uses Ph.D. (in progress), Bachelor of Science in Applied Physics, and Bachelor of Economics (Double Degree). Selected Publications is a plain heading like adjacent sections; the existing View all publications link remains. DOI replaces the template HTML resource label. Paper number 24-4 is documented here but omitted from the public IEDM venue line.

## Final presentation update
Education uses Ph.D. Student, B.S. in Applied Physics, and B.Econ. in Economics, with no double-degree parenthesis. Both ISCA co-first authors carry asterisks; the note is simply Equal contribution. Visible publication numbers are removed while year grouping, filtering and internal abstract IDs remain intact. IEDM links to its verified official Program entry: https://iedm26.mapyourshow.com/8_0/sessions/session-details.cfm?ScheduleID=290 . The owner-provided authentic portrait is stored at assets/img/tianyang-luo.jpg and displayed using the original responsive portrait component, with the aspect ratio corrected to 3:4 to preserve the complete photo. No image generation or retouching was used.

## Single-page structure
The public site now uses About (biography and Research Interests), Experience (Education), and Publications (all six records). Navigation targets /#about, /#experience, and /#publications. The old /publications/ URL redirects to /#publications; it is not a separate publication listing. Shared publication code remains reusable, including optional search/filter controls, disabled on the homepage via hide_controls=true. No View all link or footer social icons. Email luotianyang-21@stu.pku.edu.cn is owner-authorized and appears through the existing top profile-icons include. Original typography, year grouping and publication styles are retained.

Readability update: main content and publication titles are 20px; top-level section headings retain the template 32px; Research Interests and Education subheadings 24px. Font family and colors remain unchanged. Duplicate DOI/Program buttons are omitted; publication titles retain the same verified URLs. The visible heading is Tianyang Luo (罗天阳), using the Chinese name confirmed by the owner.

ISCA equal-contribution marks use a dagger on both Ling Liang and Tianyang Luo, with the matching dagger in the contribution note. Current main-section/subsection/body sizes are 32/24/20px.

Publication contribution notes are 16px; venue badges are 18px with 1.2 line height. These overrides are scoped to the homepage publication component.

Publication titles remain 20px; author lists and venue information use 18px; equal-contribution notes remain 16px.
