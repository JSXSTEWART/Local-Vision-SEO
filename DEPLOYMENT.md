# Netlify deployment handoff

This repository is a static Jekyll site built with the Minimal Mistakes theme.

## Recommended Netlify settings
- Build command: `bundle exec jekyll build`
- Publish directory: `_site`
- Build environment: `JEKYLL_ENV=production`

## Continuous deploy note
The current ChatGPT-connected Netlify tool surface supports project creation and deploy inspection, but it does not expose direct GitHub repository linking. Complete the one-time GitHub linking step in Netlify, then use normal pushes and pull requests to trigger future builds.
