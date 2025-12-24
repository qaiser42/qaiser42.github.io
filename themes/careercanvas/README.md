# CareerCanvas Hugo Theme

A modern, responsive Hugo theme for personal websites and portfolios, created by Felipe Cordero. This theme is designed to showcase your professional experience, skills, and projects in a clean and elegant way, with a focus on engineering and technical portfolios.

## Features

- Responsive design with modern UI
- Dark mode support
- **Complete color customization** - Every color can be customized via config
- Portfolio showcase with image galleries
- Blog support
- Skills section with interactive cards
- Experience timeline
- Contact form
- Social media integration
- Multilingual support (English/French)
- Resume/CV integration
- Tailwind CSS for styling
- Optimized for technical and engineering portfolios

## Demo

See the theme in action at [felipecordero.com](https://felipecordero.com) - my personal website built with CareerCanvas.

![CareerCanvas Demo](https://raw.githubusercontent.com/felipecordero/felipecordero.github.io/main/static/images/personal_web_demo.png)

## Installation

### As a Git Submodule

```bash
git submodule add https://github.com/felipecordero/careercanvas.git themes/careercanvas
```

### As a Git Clone

```bash
git clone https://github.com/felipecordero/careercanvas.git themes/careercanvas
```

## Configuration

Add the following to your `config.toml`:


```toml
theme = "careercanvas"

[params]
  name = "Your Name"
  tagline = "Your Tagline"
  location = "Your Location"
  email = "your.email@example.com"
  profile_image = "/images/your-profile.jpg"
  description = "Your description"
  author = "Your Name"

  # Social Media
  linkedin_url = "https://linkedin.com/in/yourprofile"
  github_url = "https://github.com/yourusername"

  # Resume/CV
  resume_url_en = "/files/your-resume-en.pdf"  # Path to English resume
  resume_url_fr = "/files/your-resume-fr.pdf"  # Path to French resume (optional)
  resume_label = "Full Resume"

  # Social Icons
  [[params.social]]
    icon = "linkedin-in"
    url = "https://linkedin.com/in/yourprofile"

  [[params.social]]
    icon = "github"
    url = "https://github.com/yourusername"
```

## Menu Configuration

```toml
[[menu.main]]
  name = "About"
  url = "/#about"
  weight = 2

[[menu.main]]
  name = "Skills"
  url = "/#skills"
  weight = 3

[[menu.main]]
  name = "Experience"
  url = "/#experience"
  weight = 4

[[menu.main]]
  name = "Contact"
  url = "/#contact"
  weight = 5
```

## Color Customization

The CareerCanvas theme supports complete color customization through an optimized system that eliminates color repetition. The new three-tier architecture uses base colors, semantic references, and section-specific colors for maximum flexibility and maintainability.

### 🎯 **Key Improvements**
- **90% reduction** in color definitions through elimination of repetition
- **Single source of truth** for all hex values
- **Semantic color mapping** for intuitive customization
- **Backward compatible** with existing configurations

### Quick Color Customization

1. Copy the example configuration from `themes/careercanvas/example-config.toml` to your site's `config.toml`
2. Customize colors by changing either base colors or semantic references
3. Rebuild your site to see the changes

### Example: Change Primary Color to Purple

**Method A - Change Semantic References:**
```toml
[params.colors.semantic]
primary = "purple_500"        # Use existing purple
primary_dark = "purple_700"
primary_light = "purple_400"
primary_lighter = "purple_300"
```

**Method B - Change Base Colors:**
```toml
[params.colors.base]
blue_500 = "#8b5cf6"  # Replace blue-500 with purple-500
blue_700 = "#7c3aed"  # Replace blue-700 with purple-600
blue_400 = "#a78bfa"  # Replace blue-400 with purple-400
blue_300 = "#c4b5fd"  # Replace blue-300 with purple-300
```

### Color System Architecture

1. **Base Colors** (`[params.colors.base]`) - Single source of truth for all hex values
2. **Semantic Colors** (`[params.colors.semantic]`) - Meaningful references to base colors
3. **Section Colors** - Component-specific references to semantic colors

### Available Color Sections

- `[params.colors.base]` - Base color palette (blue, gray, green, purple, etc.)
- `[params.colors.semantic]` - Semantic color mapping (primary, secondary, success, etc.)
- `[params.colors.light]` - Light mode colors
- `[params.colors.dark]` - Dark mode colors
- `[params.colors.hero]` - Hero section colors
- `[params.colors.skills]` - Skills section colors
- `[params.colors.experience]` - Experience timeline colors
- `[params.colors.contact]` - Contact form colors
- `[params.colors.navigation]` - Navigation colors
- `[params.colors.content]` - Blog/content page colors
- `[params.colors.effects]` - Animation and effect colors

For detailed documentation, see [COLOR_CUSTOMIZATION.md](COLOR_CUSTOMIZATION.md).

## Image Galleries

The theme includes a gallery shortcode for showcasing your work:

```markdown
{{< gallery dir="images/your-gallery" >}}
```

## 🚀 Development

To start the development server:

```bash
npm run dev
```

This command runs `hugo server -D`, which starts a local server and includes draft content (content with `draft: true` in the front matter). This is useful for previewing unpublished or in-progress content during development.

The site will be available at `http://localhost:1313`

## 🏗️ Building

To build the site for production, you need to:

1. Build the CSS with Tailwind:
   ```bash
   npm run build:css
   ```

2. Build the site with Hugo:
   ```bash
   npm run build
   ```

Or you can do both in one command:
```bash
npm run build:css && npm run build
```

The built site will be in the `public/` directory.

Note: The CSS build step is necessary because the site uses Tailwind CSS, which needs to be processed to generate the final CSS file with only the used styles.

## 📁 Project Structure

- `assets/` - Contains source files for CSS, JavaScript, and other assets
- `content/` - Contains the content of your site
- `static/` - Contains static files like images
- `themes/careercanvas/` - Contains the CareerCanvas theme
- `config.toml` - Main configuration file
- `tailwind.config.js` - Tailwind CSS configuration

## 🛠️ Technologies Used

- [Hugo](https://gohugo.io/) - Static site generator
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS framework
- [@tailwindcss/typography](https://tailwindcss.com/docs/typography-plugin) - Typography plugin for Tailwind CSS
- [CareerCanvas](https://github.com/felipecordero/careercanvas) - Custom Hugo theme

## 👨‍💻 About the Theme

The CareerCanvas theme is my own creation, designed specifically for technical and engineering portfolios. It features:
- Modern, responsive design
- Dark mode support
- Interactive components
- Image galleries
- Multilingual support
- Optimized for technical content

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/felipecordero/careercanvas/issues).

## 📫 Contact

For any questions or suggestions, please open an issue in the GitHub repository or visit [felipecordero.com](https://felipecordero.com).

## 🚨 Important Note

The built CSS file (`static/css/main.css`) is committed to this repository so that users can use the theme without running npm or Tailwind. If you make changes to the CSS source files, please run `npm run build:css` and commit the updated `main.css` file. 