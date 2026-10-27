# shizhe-yu.github.io

Personal academic website of Shizhe Yu, built with the [al-folio](https://github.com/alshedivat/al-folio) Jekyll template.
The previous (academicpages) version of the site is kept on the `backup-original` branch.

## Where things live

| What                    | File                                                         |
| ----------------------- | ------------------------------------------------------------ |
| About page (bio, photo) | `_pages/about.md`, photo in `assets/img/prof_pic.png`        |
| Research page (papers)  | `_bibliography/papers.bib` (abstracts, PDF/SSRN links)       |
| CV page                 | `_data/cv.yml`                                               |
| CV PDF (download icon)  | source `cv/cv.tex` → compiled copy `assets/pdf/cv.pdf`       |
| Misc page (parks map)   | `_pages/misc.md`                                             |
| Contact icons           | `_data/socials.yml`                                          |
| Site-wide settings      | `_config.yml`                                                |

## Updating the CV PDF

Compile `cv/cv.tex` with `pdflatex` (or upload it to Overleaf), then replace `assets/pdf/cv.pdf` with the new PDF and push.

## Deployment

Every push to `master` runs the **Deploy site** GitHub Action, which builds the site and publishes it to the `gh-pages` branch.
GitHub Pages must be set to serve from that branch: _Settings → Pages → Build and deployment → Deploy from a branch → `gh-pages` / `(root)`_.

## Running locally (optional)

```bash
bundle install
bundle exec jekyll serve   # then open http://localhost:4000
```

Or with Docker: `docker compose up` and open http://localhost:8080.
