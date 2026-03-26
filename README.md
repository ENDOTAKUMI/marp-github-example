# Marp GitHub Example

Markdown-based presentation slides with GitHub Actions and GitHub Pages deployment.

## Features

- Write slides in Markdown using [Marp](https://marp.app/)
- Automatic HTML generation via GitHub Actions
- Multi-language support (Japanese & English)
- GitHub Pages deployment with language selector

## Live Demo

Visit the published slides: `https://endotakumi.github.io/marp-github-example/`

## Structure

```
.
├── slides/
│   ├── slide.ja.md    # Japanese slides
│   └── slide.en.md    # English slides
├── image/             # Images used in slides
├── .github/workflows/
│   └── slide.yml      # CI/CD workflow
└── config.json        # Configuration (optional)
```

## Usage

1. Edit slide files in `slides/` directory
2. Commit and push to main branch
3. GitHub Actions automatically builds HTML files
4. Access slides at `https://[your-username].github.io/[repo-name]/`

## Local Preview

Install [Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode) extension to preview slides locally.

## GitHub Pages Setup

1. Go to repository **Settings** → **Pages**
2. Under **Source**, select **GitHub Actions**
3. Save and wait for deployment

## License

MIT
