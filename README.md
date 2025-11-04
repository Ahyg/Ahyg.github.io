# Yuguang Hu's Personal Website

Personal academic website built with Jekyll and deployed on GitHub Pages.

**Live Site:** [yuguanghu.com](https://yuguanghu.com) | [Ahyg.github.io](https://Ahyg.github.io)

## Overview

This is a clean, academic-style personal website featuring:
- **Home** - Welcome page with overview
- **About** - Professional background and education
- **Research** - Current and past research projects
- **Publications** - Academic publications and profiles
- **Contact** - Contact information and social links
- **Blog** - Regular updates and posts

## Quick Start

### Prerequisites

- Ruby 3.0 or higher
- Bundler gem

### Local Development

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Ahyg/Ahyg.github.io.git
   cd Ahyg.github.io
   ```

2. **Install dependencies:**
   ```bash
   bundle install
   ```

3. **Run the local server:**
   ```bash
   bundle exec jekyll serve
   ```

4. **View your site:**
   Open your browser and navigate to `http://localhost:4000`

The site will automatically rebuild when you make changes to files.

## Editing Content

### Updating Pages

All main pages are Markdown files in the root directory:
- `index.md` - Home page
- `about.md` - About page
- `research.md` - Research page
- `publications.md` - Publications page
- `contact.md` - Contact page

To edit, simply open the file and modify the content. The front matter (between `---` marks) controls the page layout and metadata.

### Adding Blog Posts

1. Create a new file in the `_posts` directory
2. Name it following the pattern: `YYYY-MM-DD-title-of-post.md`
3. Add front matter at the top:
   ```yaml
   ---
   layout: post
   title: "Your Post Title"
   date: YYYY-MM-DD HH:MM:SS -0000
   categories: your-category
   ---
   ```
4. Write your content below the front matter in Markdown

### Customizing Site Settings

Edit `_config.yml` to update:
- Site title and description
- Email and social links
- Navigation menu
- Build settings

**Important:** After changing `_config.yml`, restart the Jekyll server for changes to take effect.

## Publishing Changes

### Automatic Deployment

This site uses GitHub Actions for automatic deployment:

1. **Make your changes** locally or directly on GitHub
2. **Commit and push** to the `main` or `master` branch:
   ```bash
   git add .
   git commit -m "Description of changes"
   git push origin main
   ```
3. **GitHub Actions will automatically:**
   - Build the Jekyll site
   - Deploy to GitHub Pages
   - Make it live at yuguanghu.com

You can monitor deployment progress in the "Actions" tab of your repository.

### Manual Deployment

If needed, you can trigger a manual deployment:
1. Go to the "Actions" tab in your GitHub repository
2. Select "Deploy Jekyll site to GitHub Pages"
3. Click "Run workflow"

## Custom Domain Setup

The custom domain `yuguanghu.com` is configured via the `CNAME` file. 

To change or update the domain:
1. Edit the `CNAME` file with your domain name
2. Configure DNS settings with your domain provider:
   - Add an A record pointing to GitHub Pages IPs
   - Or add a CNAME record pointing to `Ahyg.github.io`
3. Enable "Enforce HTTPS" in repository Settings > Pages

## Site Structure

```
.
├── _config.yml          # Site configuration
├── _posts/              # Blog posts
├── .github/
│   └── workflows/
│       └── jekyll.yml   # GitHub Actions workflow
├── index.md             # Home page
├── about.md             # About page
├── research.md          # Research page
├── publications.md      # Publications page
├── contact.md           # Contact page
├── CNAME                # Custom domain configuration
├── Gemfile              # Ruby dependencies
└── README.md            # This file
```

## Customization Tips

### Changing the Theme

The site uses the Minima theme. To use a different theme:
1. Choose a Jekyll theme
2. Update `theme:` in `_config.yml`
3. Add the theme to your `Gemfile`
4. Run `bundle install`

### Adding Custom CSS

1. Create `assets/css/style.scss`
2. Add custom styles while importing the theme:
   ```scss
   ---
   ---
   @import "minima";
   
   /* Your custom styles here */
   ```

### Adding Images

1. Create an `assets/images/` directory
2. Add your images there
3. Reference them in Markdown: `![Alt text](/assets/images/image.jpg)`

## Troubleshooting

### Site not building?
- Check the Actions tab for error messages
- Ensure `_config.yml` is valid YAML
- Verify all Markdown files have proper front matter

### Changes not showing up?
- Clear your browser cache
- Wait a few minutes for GitHub Pages to rebuild
- Check that changes were pushed to the correct branch

### Local server issues?
- Run `bundle update` to update dependencies
- Ensure Ruby version is compatible
- Delete `_site/` and `.jekyll-cache/` directories and rebuild

## Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/pages)
- [Markdown Guide](https://www.markdownguide.org/)
- [Minima Theme](https://github.com/jekyll/minima)

## License

This website is for personal use. Content © Yuguang Hu. All rights reserved.

## Contact

For questions or issues, please contact via the information on the [Contact page](https://yuguanghu.com/contact/).
