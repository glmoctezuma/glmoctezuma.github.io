# glmoctezuma.github.io

Academic website of Gabriel López-Moctezuma, served at
[www.glmoctezuma.com](https://www.glmoctezuma.com) by GitHub Pages from the
`master` branch.

Built with Jekyll, using the SNVB theme from
[svmiller.github.io](http://svmiller.github.io).

## Running it locally

Use **Ruby 3.3.x**. The current `github-pages` gem declares a Ruby ceiling that
excludes Ruby 4.x; on 4.x bundler quietly falls back to a 2019-era release whose
`liquid` calls `Object#tainted?`, removed in Ruby 3.2, and the build fails.

```sh
brew install ruby@3.3
export PATH="$(brew --prefix ruby@3.3)/bin:$PATH"
gem install bundler

bundle install
bundle exec jekyll serve -w      # http://localhost:4000
```

## Layout

| Path | What it holds |
| --- | --- |
| `index.html` | Home page |
| `research.md`, `research/` | Publication list and one page per paper |
| `teaching.md`, `teaching/` | Course list and one page per course |
| `cv.md`, `pdfs/cv.pdf` | CV page and the PDF it serves |
| `_layouts/`, `_includes/`, `_sass/` | Theme templates and styles |
| `_data/menu.yml` | Top navigation |

Paper pages carry a plain `title` for `<title>` and SEO, plus an optional
`heading` holding the same text with a `<br>` for display. Keep colons in both
inside quotes: an unquoted colon is invalid YAML and Jekyll will silently drop
the layout, rendering the page as bare text.
