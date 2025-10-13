# Life and other stuff — Jekyll site

This repository contains a small Jekyll site scaffold and one converted post. It uses a minimal layout and supports comments via Utterances (GitHub Issues).

Getting started locally

1. Install Ruby and Bundler (macOS / Linux):

```bash
# install bundler if missing
gem install bundler
bundle install
```

2. Build and serve locally:

```bash
bundle exec jekyll serve --livereload
```

Open http://127.0.0.1:4000 in your browser.

Enable comments (Utterances)

This site includes the Utterances script in `_layouts/post.html`. To enable comments:

1. Create a GitHub repository to hold Utterances issues (e.g., `yourusername/utterances-comments`).
2. Go to https://utteranc.es/ and authorize the app for that repo and choose a mapping (e.g., pathname or title).
3. Replace `repo="YOUR_GITHUB_USERNAME/YOUR_UTTERANCES_REPO"` in `_layouts/post.html` with your repo name.

Example: for this site the GitHub repo is `lifeandotherstuff/Website` and the published URL is `https://lifeandotherstuff.com`.

If you use the repo `lifeandotherstuff/Website`, the script tag should look like:

```html
<script src="https://utteranc.es/client.js"
	repo="lifeandotherstuff/Website"
	issue-term="pathname"
	theme="github-light"
	crossorigin="anonymous"
	async>
</script>
```

Notes:
- Utterances creates GitHub issues for each post (depending on your chosen issue-term). Make sure the repository allows issues and that you've granted Utterances access.
- If you want comments to show immediately, open one blog post after configuring Utterances; it will create an issue if none exists.

Notes on deployment

- You can deploy to GitHub Pages by pushing this repo to GitHub and enabling Pages in the repository settings.
- If you use a custom domain, set `url` and `baseurl` in `_config.yml` and add the `CNAME` file.

Next steps (optional)

- Add pagination on the blog index.
- Improve styling and mobile responsiveness.
- Add social sharing, RSS, and additional posts.
