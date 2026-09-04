# Yuanqi Zhang — personal academic website

This repository builds [yuanqizhang.com](https://yuanqizhang.com/) with Hugo Blox and deploys it through GitHub Pages whenever `main` changes.

The job-market draft uses a compact two-column academic layout inspired by [Gautam Rao's website](https://gautam-rao.com/) and the MIT-licensed [Academimal Hugo theme](https://github.com/yangl1996/academimal). The implementation remains within the existing Hugo Blox project rather than copying the reference repository's older build system.

## Before publishing the job-market version

Confirm and add all of the following:

- Job-market cycle (for example, `2026–27`) and the exact wording approved by UCL.
- Current CV as `static/files/yuanqi-zhang-cv.pdf`.
- Designated Job Market Paper, **Designing Experiments for Policies Beyond the Experiment**, as `static/files/yuanqi-zhang-jmp.pdf`.
- Confirmed JMP coauthors (if any), status, a 100–150 word general-audience abstract, and links to appendix, slides, code, and data where available.
- A professional headshot with permission to publish. Aim for a portrait crop at least 1200 px high.
- Teaching experience and links to a teaching statement or evaluations, if they are part of the application package.
- References, only after confirming the preferred names, affiliations, and whether email addresses should appear publicly.
- Google Scholar, ORCID, GitHub, or other profile links that should be shown.

The current draft marks unfinished materials as forthcoming, omits unconfirmed market-cycle claims, and removes the old demo CV. The bilingual CV supplied for design reference remains outside this repository and is not copied into the public site.

## Content map

- `content/_index.md`: homepage copy and research papers.
- `content/authors/admin/_index.md`: name, affiliation, research interests, and profile links.
- `config/_default/menus.yaml`: top navigation.
- `config/_default/params.yaml`: SEO, header, footer, and repository settings.
- `assets/scss/custom.scss`: visual design and responsive styles.
- `static/files/`: final public PDFs.

## Local preview

The deployment workflow currently pins Hugo Extended `0.124.1`. With Hugo Extended and Go installed:

```sh
hugo server
```

Open the local address printed by Hugo. Use `hugo --minify` for a production build.

## Publishing

Work on a feature branch and open a pull request. Merging to `main` triggers `.github/workflows/publish.yaml`, which rebuilds and deploys the site to GitHub Pages. The custom domain and HTTPS are already configured in the repository settings.
