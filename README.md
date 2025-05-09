# Astro Starter Kit: Modern CSS Reset + Tailwind v4

An enhanced Astro starter template with a modern, optimized CSS reset and Tailwind v4 integration. This starter provides a solid foundation for creating accessible, responsive, and visually consistent web applications.

## 🚀 Getting Started

### Option 1: Clone this repository

```sh
# Clone this repository
git clone https://github.com/yourusername/astro-starter.git my-project
cd my-project

# Install dependencies
pnpm install

# Start the development server
pnpm dev
```

### Option 2: Use as a template (if published on GitHub)

First, make sure this repository is set as a template in GitHub settings.

```sh
# Create a new project using this template
pnpm create astro@latest my-project -- --template delodg/astro-starter
```

### Option 3: Create a local copy

```sh
# Copy existing project to a new directory
cp -r path/to/astro-starter my-new-project
cd my-new-project
pnpm install
```

## ✨ Features

- **Modern CSS Reset**: Carefully optimized reset with best practices
- **Tailwind v4 Integration**: Ready for the latest Tailwind features
- **Accessibility-First**: Focus states, reduced motion, high contrast support
- **Dark Mode Support**: Built-in dark mode with CSS variables
- **Responsive Typography**: Modern CSS properties like `text-wrap: balance`
- **Performance Optimized**: Minimal, no-bloat foundation

## 📁 Project Structure

```text
/
├── public/
│   └── favicon.svg
├── src/
│   ├── layouts/
│   │   └── Layout.astro
│   ├── pages/
│   │   └── index.astro
│   ├── styles/
│   │   └── global.css  # Optimized CSS reset
│   └── components/
└── package.json
```

## 🔍 CSS Reset Features

The included CSS reset (`src/styles/global.css`) provides:

- **Minimal but Complete**: Only the essentials with no unnecessary styles
- **Modern Viewport Handling**: Using `dvh` for better mobile support
- **Enhanced Typography**: Text balancing and pretty wrapping
- **Form Element Normalization**: Consistent form elements across browsers
- **Accessibility Improvements**: Better focus states and reduced motion support
- **CSS Variables**: For colors, with RGB format for Tailwind compatibility
- **Inter & Monospace Fonts**: Ready to use

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                | Action                                           |
| :--------------------- | :----------------------------------------------- |
| `pnpm install`         | Installs dependencies                            |
| `pnpm dev`             | Starts local dev server at `localhost:4321`      |
| `pnpm build`           | Build your production site to `./dist/`          |
| `pnpm preview`         | Preview your build locally, before deploying     |
| `pnpm astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `pnpm astro -- --help` | Get help using the Astro CLI                     |

## 👀 Learn More

- [Astro Documentation](https://docs.astro.build)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
