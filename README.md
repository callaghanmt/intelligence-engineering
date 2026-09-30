# Intelligence Engineering

A Quarto starter for publishing technical notes on models that retrieve, reason and decide.

## 1. Personalise it

In `_quarto.yml`, replace every occurrence of:

- `YOUR-USERNAME` with your GitHub username;
- `Your name` with your name; and
- `2026` in the footer if appropriate.

The starter assumes the repository is named `intelligence-engineering`, giving this URL:

```text
https://YOUR-USERNAME.github.io/intelligence-engineering/
```

If you choose another repository name, update both `site-url` and `repo-url`.

## 2. Preview locally

[Install Quarto](https://quarto.org/docs/get-started/) and run:

```bash
quarto preview
```

The sample articles do not require Python or R. Computational articles can use Jupyter, Knitr, Julia or Observable as needed.

## 3. Add an article

1. Create a directory such as `posts/my-article/`.
2. Copy `templates/article-template.md` to `posts/my-article/index.qmd`.
3. Add an image called `cover.svg`, `cover.png` or `cover.jpg` beside it.
4. Edit the front matter and article body.
5. Change `draft: true` to `draft: false` (or remove the line) when ready.

Posts inherit common settings from `posts/_metadata.yml`.

Useful category families might include:

- **Format:** Technical note, Experiment, Field note, Explainer, Review
- **Topic:** RAG, GraphRAG, Fine-tuning, Small models, Sovereign AI, Evaluation, Decision models

Using a controlled set of category spellings will keep filters tidy.

## 4. Publish on GitHub Pages

Create an empty GitHub repository called `intelligence-engineering`, then from this directory run:

```bash
git init
git add .
git commit -m "Initial Intelligence Engineering site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/intelligence-engineering.git
git push -u origin main
```

The workflow in `.github/workflows/publish.yml` renders the site and creates a `gh-pages` branch.

In the repository on GitHub:

1. Open **Settings → Pages**.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Select the `gh-pages` branch and `/ (root)`, then save.

Later pushes to `main` will publish automatically. The first deployment can take a few minutes.

## Site structure

```text
.
├── _quarto.yml              # Site-wide configuration
├── index.qmd                # Landing page and latest articles
├── articles.qmd             # Searchable/filterable archive
├── about.qmd
├── posts/
│   ├── _metadata.yml        # Defaults inherited by articles
│   └── article-slug/
│       ├── index.qmd
│       └── cover.svg
├── templates/
│   └── article-template.md  # Rename copied files to .qmd
├── assets/
├── theme-light.scss
├── theme-dark.scss
└── styles.css
```

## Optional next steps

- Add a custom social-preview image to individual article front matter with `image:`.
- Add citations with a BibTeX file and `bibliography: references.bib`.
- Enable Giscus comments after activating GitHub Discussions.
- Add Python or R setup steps to the workflow if articles need to execute code in CI.
- Replace the sample articles or keep them as an editorial introduction.

## Licensing

Choose this explicitly before publishing. A common arrangement is **CC BY 4.0** for prose and figures, and **MIT** for reusable code. Add the relevant licence files and state the distinction on the About page.
