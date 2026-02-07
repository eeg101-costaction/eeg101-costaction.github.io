# EEG101 COST Action

This repository contains the website for the EEG101 COST Action.

## About

EEG101 Fundamentals of Open & Rigorous EEG Science is a European [COST Action](https://www.cost.eu) ([CA24148](https://www.cost.eu/actions/CA24148/)) dedicated to the development of standardized protocols, harmonizing data, creating shared platforms, and providing targeted training to overcome methodological heterogeneity and establish robust, reproducible, and impactful open science.

## License

The website content is licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.en).

## Website development

### Managing the content

Please note that most website content is formatted in plain [Markdown](https://www.markdownguide.org/getting-started/) format and you don't need to know much about HTML. There are a few things for which we use some HTML, such as for the formatting of cards, or the images.

- **Edit content**: Modify the Markdown files (`index.md`, `coordination.md`, `working-groups.md`, etc.)
- **Navigation**: Update `_data/navigation.yaml`, please consider the best order of menu items
- **People**: Edit `_data/people.yaml` and add a _square_ photo to assets/images/people
- **Styling**: Edit `assets/css/style.css`

### Adding Pages

Create `.md` file with front matter, followed by Markdown formatted content:

   ```yaml
   ---
      title: Page Title
   ---
   ```

The page title is automatically added, so you should _not_ add a `# Page Title` heading at the top. Within the page you should only use sub-headings at level 2 with `##`, level 3 with `###`,  etcetera.

If you want the page to appear in the main menu, you should add a navigation link in `_data/navigation.yaml`.

### Running it locally

You can build and open the website on your own computer, prior to committing any changes to this repository on GitHub. This allows you to try things out and to check the formatting.

```bash
# Install dependencies
bundle config set --local path 'vendor/bundle'
bundle install

# Serve locally
bundle exec jekyll serve --incremental --livereload
```

Visit `http://localhost:4000` to view the site.

### Deployment

The site auto-deploys via GitHub Pages when pushing to the main branch of this repository on GitHub.

## Project structure

```console
.
├── index.md
├── coordination.md
├── working-groups.md
├── grants.md
├── join.md
├── news.md
├── contact.md
├── _data/
│   ├── navigation.yaml
│   └── people.yaml
├── _layouts/
├── _includes/
│   ├── header
│   ├── footer
│   ├── person
│   └── plausible
├── assets/
│   ├── css/
│   └── images/
└── _config.yml
```
