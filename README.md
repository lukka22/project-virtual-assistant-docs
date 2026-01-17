# Local Preview

This repo uses GitHub Pages (Jekyll). To preview locally:

## Ruby Version

Use Ruby 3.1.x for local preview because GitHub Pages (Jekyll 3.9) is not compatible with Ruby 3.2+.

```powershell
# Use Bundler 2.x with Ruby 3.1
gem install bundler -v 2.4.22

# Install deps and create binstubs
bundle _2.4.22_ install
bundle _2.4.22_ binstubs jekyll --path .\bin

# Run local server
.\bin\jekyll serve --source docs --destination _site
```

Open `http://localhost:4000/project-virtual-assistant-docs/`.

## Optional: Quick static preview (no theme)

```powershell
python -m http.server 8000
```

Open `http://localhost:8000/docs/`.
