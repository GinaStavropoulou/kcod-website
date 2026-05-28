# Knowledge Centre Open Data — Website

Source for [kcopendata.bk.tudelft.nl](https://kcopendata.bk.tudelft.nl/), built with [Hugo](https://gohugo.io/).

---

## Local development

```bash
git clone https://github.com/tudelft3d/kcod-website.git
cd kcod-website
hugo server -e development
```

Then open [http://localhost:1313](http://localhost:1313) in your browser.

---

## Adding content

### News article

Create a new `.md` file in `content/news/`. The filename must start with the publication date in `YYYY-MM-DD` format, e.g. `2024-03-15-my-article-title.md`.

The file should start with this front matter:

```yaml
---
title: "Your article title"
date: 2024-03-15
years: ["2024"]
draft: false
---

Article content goes here.
```

> The `years` field controls which year archive page the article appears under.

### Publication (article, book chapter, etc.)

Add an entry to the appropriate YAML file in `data/publications/`. Entries follow this structure:

```yaml
- title: "Maatschappelijke kosten-batenanalyse open data"
  category: "reports"
  year: 2017
  author: "Welle Donker, F., van Loenen, B. and Korthals Altes, W."
  citation: "Welle Donker, F., van Loenen, B. and Korthals Altes, W. (2017). **Maatschappelijke kosten-batenanalyse open data**. Delft: OTB-Onderzoek voor de gebouwde omgeving. Faculteit Bouwkunde, TU Delft. 128 p."
  external_url: "https://pure.tudelft.nl/..."
```

---

## Deploying changes

Push your changes to the `main` branch and the website will be updated automatically.

```bash
git status                      # review changed files
git add <file>                  # stage changed files
git commit -m "Your message"    # commit with a descriptive message
git push                        # push to the remote repository
```

You can monitor the build status on the [Actions page](https://github.com/tudelft3d/kcod-website/actions).
