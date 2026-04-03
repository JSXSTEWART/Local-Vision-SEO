# Netlify deployment guide

This repository is a Jekyll site based on the Minimal Mistakes theme. The files added for Netlify deployment are intentionally small and explicit so the hosting setup is easy to review.

## Stack

- Jekyll site built with Bundler
- `_config.yml` for site configuration
- `netlify.toml` for Netlify build and publish settings
- `.env.example` for build-time environment documentation

## Local development

```bash
bundle install
bundle exec jekyll serve
```

By default, the site is served locally at `http://127.0.0.1:4000`.

## Netlify build settings

- Build command: `bundle exec jekyll build`
- Publish directory: `_site`
- Build-time environment variable: `JEKYLL_ENV=production`

## Recommended Netlify setup

1. Create or open the Netlify project.
2. Connect this GitHub repository to the project.
3. Confirm the build command is `bundle exec jekyll build`.
4. Confirm the publish directory is `_site`.
5. Add `JEKYLL_ENV=production` as a build environment variable.
6. Trigger a deploy from the default branch after reviewing the configuration.

## Notes

- This repo does not require runtime secrets for a standard static deployment.
- Site metadata such as title, description, and canonical URL still live in `_config.yml` and should be updated there before production launch.
- The current `README.md` is still the upstream theme README and should be replaced with project-specific documentation in a follow-up change.
