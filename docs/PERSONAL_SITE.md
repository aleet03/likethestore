# Albert Lee's personal site

This site uses the al-folio template with a resume-based biography, selected work, experience, education, and profile links. Template examples remain in the repository and are excluded from publication in `_config.yml`.

## Deploy

1. In `aleet03/likethestore`, open **Settings > Pages** and set **Source** to **GitHub Actions**. Keep the repository public unless your GitHub plan supports Pages for private repositories.
2. Commit and push the site changes to `main`.
3. Open **Actions > Deploy site** and wait for the build and deploy jobs. You can also start it with **Run workflow**.
4. The expected address is <https://aleet03.github.io/likethestore/>. The deployment job reports the actual URL after it succeeds.

From PowerShell in the project directory, publish the prepared changes with:

```powershell
git add .github/workflows/deploy.yml _config.yml _data/repositories.yml _data/socials.yml _pages/about.md _pages/projects.md _pages/repositories.md _pages/experience.md docs/PERSONAL_SITE.md
git commit -m "Set up Albert Lee personal site and GitHub Pages deployment"
git push origin main
```

This follows [GitHub's custom Pages workflow documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages).

The workflow builds with Ruby 3.3.5, runs the template boundary check and upgrade audit, verifies the generated pages and local asset paths, and deploys with GitHub's official Pages actions. Pull requests build and validate without publishing. A full Jekyll build is required before deployment; YAML checks alone do not establish that the site works.

## Edit content

- `_pages/about.md`: introduction and interests.
- `_pages/projects.md`: selected research and engineering work.
- `_pages/experience.md`: roles, education, and skills.
- `_data/socials.yml`: email, GitHub, and LinkedIn.
- `_data/repositories.yml`: GitHub profile and repository cards.
- `_config.yml`: site identity, URL, feature flags, and sample-content exclusions.

The content is based on the September 2026 resume. Update ongoing roles and the expected graduation date as needed. The original resume PDF, phone number, and citizenship are not published. Add a headshot later through the about page's `profile` setting; no sample portrait is used.

## Local build

With Ruby 3.3.5, Bundler, Node, Python, and ImageMagick installed:

```sh
bundle install
npm ci
npm run lint:prettier
npm run lint:style-contract
bundle exec al-folio upgrade audit --no-fail
bundle exec jekyll serve
```

Open <http://localhost:4000/likethestore/>. Preserve `baseurl: /likethestore`; links and assets require the repository path on GitHub Pages. No gem-owned layouts or runtime files have been overridden.
