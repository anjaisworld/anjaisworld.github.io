# Anjai's World - Jekyll Migration

Welcome to the Jekyll version of Anjai's World! This site has been migrated to Jekyll, making it easy to manage content without duplicating files.

## 📁 Project Structure

```
anjaisworld/
├── _layouts/           # Base HTML templates
│   ├── default.html   # Main layout with navbar, footer
│   ├── home.html      # Home page layout
│   └── post.html      # Blog post layout
├── _includes/         # Reusable components
│   ├── navbar.html    # Navigation bar
│   ├── footer.html    # Footer
│   └── background.html # Animated background
├── _posts/            # Blog posts (create new ones here!)
│   └── YYYY-MM-DD-title.md
├── assets/            # CSS, JS, and other assets
│   ├── css/
│   │   └── styles.css
│   ├── js/
│   │   └── script.js
│   └── fonts/
├── img/               # Images
├── blog/              # Blog index page
│   └── index.md
├── index.md           # Homepage
├── _config.yml        # Jekyll configuration
├── Gemfile            # Ruby dependencies
└── README.md          # This file
```

## 🚀 Getting Started

### Prerequisites
- Ruby (2.7 or higher)
- Bundler

### Installation

1. **Install dependencies:**
   ```bash
   bundle install
   ```

2. **Run Jekyll locally:**
   ```bash
   bundle exec jekyll serve
   ```

3. **Visit your site:**
   Open `http://localhost:4000` in your browser

## 📝 Creating Blog Posts

Blog posts are stored in the `_posts` folder. To create a new post:

1. Create a new file in `_posts/` with the format: `YYYY-MM-DD-title.md`
2. Add front matter at the top:

```markdown
---
layout: post
title: "Your Post Title"
date: 2026-01-20
author: Anjai
excerpt: "A brief excerpt of your post that shows in the blog listing."
---

# Your content here

This is where you write your blog post in Markdown.
```

### Example Post:
```markdown
---
layout: post
title: "Minecraft House Tour"
date: 2026-01-17
author: Anjai
excerpt: "Check out the amazing house I built in Minecraft!"
---

## My Minecraft House

I just finished building an incredible house...

### Features
- Grand entrance hall
- Multiple bedrooms
- Garden with crops
- Secret basement
```

## 🎨 Customizing the Site

### Changing Content
- **Homepage**: Edit `index.md`
- **Navigation**: Edit `_includes/navbar.html`
- **Footer**: Edit `_includes/footer.html`
- **Styling**: Edit `assets/css/styles.css`
- **Scripts**: Edit `assets/js/script.js`

### Theme Colors
Edit the CSS variables in `assets/css/styles.css`:

```css
:root {
    --kokiri-green: #2d5016;
    --forest-green: #3d6b1f;
    --light-green: #5a8f2f;
    --lime-green: #7fb347;
    --gold: #d4af37;
    /* ... more colors */
}
```

## 🚢 Deploying to GitHub Pages

1. **Push to GitHub:**
   ```bash
   git add .
   git commit -m "Migrate to Jekyll"
   git push origin main
   ```

2. **GitHub Pages will automatically build and deploy** your Jekyll site!

3. Your site will be available at: `https://anjaisworld.github.io`

## 📚 Useful Jekyll Resources

- [Jekyll Documentation](https://jekyllrb.com/)
- [Liquid Templating](https://shopify.github.io/liquid/)
- [GitHub Pages with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll)

## 💡 Tips

### Adding Images to Blog Posts
```markdown
![Alt text]({{ site.baseurl }}/img/your-image.jpg)
```

### Using Liquid Variables
```markdown
{{ site.title }}        # Site title from _config.yml
{{ page.title }}        # Current page title
{{ site.baseurl }}      # Base URL for assets
```

### Creating Collections
You can create other content collections (like photo galleries) by creating new folders with underscore prefix (`_gallery/`) and configuring them in `_config.yml`.

## 🛠 Troubleshooting

### Site not updating?
- Rebuild with `bundle exec jekyll build`
- Clear cache: `rm -rf _site/`

### Assets not loading?
- Use `{{ site.baseurl }}` in all asset paths
- Check `_config.yml` baseurl setting

### Posts not showing?
- File name must follow: `YYYY-MM-DD-title.md`
- Check front matter is valid YAML
- Ensure layout is set to `post`

## 📖 Features

✨ **Easy Content Management**
- Write posts in Markdown
- No HTML duplication needed
- Automatic post listing on blog page

🎨 **Beautiful Design**
- Responsive layout for all devices
- Parallax scrolling effects
- Smooth animations
- Green theme inspired by Legend of Zelda

🚀 **Performance**
- Static site generation
- Fast loading times
- SEO-friendly

## Need Help?

Check the [Jekyll Documentation](https://jekyllrb.com/docs/) or explore the existing files to understand the structure better!

---

**May the forest guide your journey through Anjai's World! 🌿✨**
