# Kreativa landing page

Static site, no build step. `index.html` is self-contained: the sample work images, the K·A logo and the word-embedding data for the word map are embedded in the file, and fonts load from Google Fonts.

- The "What are you planning?" question at the top is a Netlify Form named `project-question`. Turn on form detection in Netlify (Project configuration → Forms) to receive submissions; each one includes a `sentiment` field with the word-map score.
- The word map at the bottom uses GloVe word vectors (word2vec-style) computed in the visitor's browser.
- `assets/logo/` holds the logo file. The older files in `assets/` are no longer used by the page.

Netlify: publish directory is the repo root (set in `netlify.toml`). To preview locally: `python3 -m http.server` and open http://localhost:8000.
