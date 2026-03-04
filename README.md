# Gallery

A beautiful, private photo gallery for sharing memories with family and friends. Built with [Hugo](https://gohugo.io/) and deployed on [GitHub Pages](https://pages.github.com/).

## Features

- 📸 **Album Organization** - Group photos into albums with titles and descriptions
- 🖼️ **Responsive Grid Layout** - Looks great on desktop, tablet, and mobile
- 🔍 **Lightbox Viewer** - Click any photo to view full-size with keyboard navigation
- ⚡ **Fast Loading** - Lazy loading images and optimized thumbnails
- 🎨 **Clean Design** - Simple, elegant interface that puts photos first
- 🚀 **GitHub Pages** - Free hosting with automatic deployments

## Demo

Visit the live gallery at: `https://railsbrain.github.io/gallery/`

## Quick Start

### Adding a New Album

1. Create a new folder in `content/albums/`:
   ```
   content/albums/my-new-album/
   ```

2. Create an `index.md` file with your photos:
   ```yaml
   ---
   title: "My New Album"
   description: "Description of this album"
   date: 2024-06-15
   cover: "https://example.com/cover.jpg"  # Optional
   photos:
     - src: "https://example.com/photo1.jpg"
       title: "First photo caption"
     - src: "https://example.com/photo2.jpg"
       title: "Second photo caption"
   ---
   ```

### Option A: Use External Image URLs

Host your images anywhere (Google Photos, Imgur, Cloudflare Images, etc.) and use the URLs directly in the `photos` list.

### Option B: Use Local Images (Recommended)

1. Add images to the album folder:
   ```
   content/albums/my-album/
   ├── index.md
   ├── photo1.jpg
   ├── photo2.jpg
   └── photo3.jpg
   ```

2. Hugo will automatically include all images. No need for the `photos` list in front matter:
   ```yaml
   ---
   title: "My Album"
   description: "Using local images"
   date: 2024-06-15
   ---
   ```

## Project Structure

```
gallery/
├── config.toml          # Site configuration
├── content/
│   ├── albums/          # All photo albums
│   │   ├── _index.md    # Albums list page
│   │   ├── vacation/    # Individual album
│   │   │   ├── index.md # Album metadata
│   │   │   └── *.jpg    # Optional local images
│   │   └── birthday/
│   └── about/           # About page
├── layouts/
│   ├── index.html       # Homepage
│   └── albums/          # Album-specific layouts
│       ├── list.html    # Albums grid
│       └── single.html  # Photo viewer
├── static/              # Static files
└── themes/              # Hugo theme
```

## Configuration

Edit `hugo.toml` to customize:

```toml
title = 'Your Gallery Name'

[params]
  description = 'Your gallery description'
  author = 'Your Name'

[params.gallery]
  enable_lightbox = true
  photos_per_row = 3
```

## Local Development

```bash
# Install Hugo (macOS)
brew install hugo

# Start local server
hugo server -D

# Open in browser
open http://localhost:1313
```

## Deployment

This site automatically deploys to GitHub Pages when you push to the `main` branch.

1. Push changes to GitHub
2. The GitHub Action workflow builds and deploys automatically
3. View your site at `https://YOUR_USERNAME.github.io/gallery/`

## Privacy Tips

To keep your gallery private:

1. **Use a private repository** (requires GitHub Pro)
2. **Use a non-obvious URL** (e.g., `my-family-photos-2024` instead of `family-photos`)
3. **Don't share the link publicly**

> ⚠️ **Note:** GitHub Pages on public repositories are publicly accessible by URL, even if not indexed by search engines.

## Customization

### Custom Colors

Edit the CSS in `layouts/index.html` and `layouts/albums/*.html` to change the color scheme.

### Custom Layouts

- Modify `layouts/index.html` for the homepage
- Modify `layouts/albums/list.html` for the albums grid
- Modify `layouts/albums/single.html` for the photo viewer

## Tech Stack

- [Hugo](https://gohugo.io/) - Static site generator
- [Ananke Theme](https://github.com/theNewDynamic/gohugo-theme-ananke) - Base theme
- [GitHub Pages](https://pages.github.com/) - Hosting
- [GitHub Actions](https://github.com/features/actions) - CI/CD

## License

Personal use only. Please respect the privacy of family members featured in photos.

---

Built with ❤️ for family and friends.