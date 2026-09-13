# Songs

Source for a songbook web site built with [MkDocs](https://www.mkdocs.org/) and the [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme, published via GitHub Pages.

## Files in this repo

| Path                             | Purpose                                                                                                 |
| -------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `Songs/`                         | The site content. Each `.md` file is one song page; `Songs/index.md` is the site's home page.           |
| `mkdocs.yml`                     | MkDocs config: site name, theme, markdown extensions, and plugins used to build the site from `Songs/`. |
| `.github/workflows/gh-pages.yml` | GitHub Actions workflow that builds the site and deploys it to GitHub Pages on every push to `main`.    |

### Song's  publishing status

Each song's file (optionally) starts with a special YAML "front matter" consumed by the `pub-meta` plugin:

```yaml
---
publish: "true"   # or: draft / hidden
---
```
Value is one of:
- `"true"`(**the default if omitted**)  — page is built and shown in navigation.
- `draft` — page is excluded from the build.
- `hidden` — page is built and reachable by URL but left out of navigation (used for `index.md`).

