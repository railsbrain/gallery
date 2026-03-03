---
title: "About This Gallery"
description: "A private photo gallery for family and friends"
---

## Welcome to Our Family Gallery

This is a private space for sharing photos and memories with family and friends.

### How It Works

- **Browse Albums** - Check out the [Albums](/albums/) page to see all photo collections
- **View Photos** - Click any album to browse photos, then click a photo to view it full-size
- **Navigate** - Use arrow keys or on-screen buttons to browse through photos in the lightbox

### Adding New Photos

To add photos:

1. Create a new folder in `content/albums/your-album-name/`
2. Create an `index.md` file with front matter like this:

```yaml
---
title: "My Album Name"
description: "Description of the album"
date: 2024-01-15
cover: "path/to/cover/image.jpg"
photos:
  - src: "path/to/photo1.jpg"
    title: "Photo caption"
  - src: "path/to/photo2.jpg"
    title: "Another caption"
---
```

You can also put images directly in the album folder and Hugo will automatically pick them up!

### Privacy

This gallery is hosted on GitHub Pages. To control access:
- Make the repository private (GitHub Pro required)
- Or use a less discoverable repository name

---

Made with ❤️ using [Hugo](https://gohugo.io/) and deployed on [GitHub Pages](https://pages.github.com/)