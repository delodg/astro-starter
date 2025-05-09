# Astro Starter Kit: Modern CSS Reset + Tailwind v4

An enhanced Astro starter template with a modern, optimized CSS reset and Tailwind v4 integration. This starter provides a solid foundation for creating accessible, responsive, and visually consistent web applications.

## 📋 Table of Contents

- [Getting Started](#-getting-started)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [CSS Reset Features](#-css-reset-features)
- [Tailwind with Astro Guide](#-tailwind-with-astro-guide)
- [Best Practices](#-best-practices)
- [Commands](#-commands)
- [Updating Dependencies](#-keeping-dependencies-updated)
- [Recommended Resources](#-recommended-resources)

## 🚀 Getting Started

### Option 1: Clone this repository

```sh
# Clone this repository
git clone https://github.com/delodg/astro-starter.git my-project-name
cd my-project-name

# Install dependencies
pnpm install

# Start the development server
pnpm dev
```

### Option 2: Use as a template (if published on GitHub)

First, make sure this repository is set as a template in GitHub settings.

```sh
# Create a new project using this template
pnpm create astro@latest my-project-name -- --template delodg/astro-starter
```

### Option 3: Create a local copy

```sh
# Copy existing project to a new directory
cp -r path/to/astro-starter my-new-project-name
cd my-new-project-name
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

## 🎨 Tailwind with Astro Guide

### Getting Started with Tailwind

This starter comes with Tailwind v4 pre-configured. Here are some tips to get the most out of it:

1. **Use the Tailwind VS Code extension** for autocompletion and linting
2. **Leverage the reset CSS** - it's designed to work harmoniously with Tailwind
3. **Check the [Tailwind v4 docs](https://tailwindcss.com/docs)** for the latest features and syntax

### Dark Mode

The CSS reset includes dark mode variables. Use Tailwind's dark mode utilities to enable dark mode support:

```html
<div class="bg-white text-gray-900 dark:bg-gray-900 dark:text-white">
  <!-- Content -->
</div>
```

### Common Component Patterns

#### Responsive Card Grid

```html
<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
  <div class="bg-white dark:bg-gray-800 rounded-lg shadow-md p-6 hover:shadow-lg transition-shadow">
    <!-- Card content -->
  </div>
  <!-- More cards -->
</div>
```

#### Accessible Button

```html
<button
  class="inline-flex items-center justify-center rounded-md bg-indigo-600 px-4 py-2 text-sm font-medium text-white shadow-sm hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2 disabled:opacity-50 disabled:cursor-not-allowed"
  type="button"
>
  Button Text
</button>
```

## 👍 Best Practices

### Coding Best Practices

1. **Component-first approach**: Create reusable Astro components with Tailwind classes
2. **Use @apply sparingly**: Prefer inline Tailwind classes for better maintainability
3. **Leverage CSS variables** from the reset for consistent theming
4. **Group related classes** for better readability:
   ```html
   <button
     class="
     /* Positioning & Layout */
     relative block w-full
     /* Typography */
     font-medium text-sm
     /* Visual styling */
     bg-blue-500 hover:bg-blue-600 text-white rounded-lg
     /* Spacing & Size */
     px-4 py-2 mt-3
     /* Interactivity */
     transition-colors duration-200
   "
   >
     Button Text
   </button>
   ```

### Optimization Best Practices

1. **Use the `@astro/tailwind` integration** (already included)
2. **Enable content-visibility**: For large pages with many components
3. **Implement view transitions**: For smoother page navigation
4. **The build process automatically removes unused styles**
5. **For larger projects, consider code-splitting your styles**

### Maintenance Best Practices

1. **Read Release Notes**: Always check release notes for breaking changes before updating
   - [Astro Releases](https://github.com/withastro/astro/releases)
   - [Tailwind CSS Releases](https://github.com/tailwindlabs/tailwindcss/releases)
2. **Update in Stages**: Update major frameworks separately to isolate any issues
3. **Test After Updating**: Run your application thoroughly after updates
4. **Use Version Control**: Commit before updating to easily revert if needed
5. **Maintain Documentation**: Update your project's documentation when adding new patterns

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

## 🔄 Keeping Dependencies Updated

### Checking Current Versions

To see your current package versions:

```sh
pnpm list astro tailwindcss
```

Or check all outdated packages:

```sh
pnpm outdated
```

### Upgrading Packages

#### Upgrading Astro

```sh
# Update to the latest version
pnpm up astro --latest

# For major version upgrades, check the migration guide:
# https://docs.astro.build/en/guides/upgrade-astro/
```

#### Upgrading Tailwind CSS

```sh
# Update Tailwind and its dependencies
pnpm up tailwindcss postcss autoprefixer --latest
```

#### Upgrading All Dependencies

```sh
# Update all dependencies (use with caution)
pnpm up --latest
```

### Update package.json

For Tailwind plugins, update them in package.json:

```
"devDependencies": {
  "@astrojs/tailwind": "^x.y.z",
  "tailwindcss": "^4.x.y",
  // Other dependencies
}
```

### Automated Dependency Updates

Consider setting up [Renovate](https://github.com/renovatebot/renovate) or [Dependabot](https://github.com/dependabot) for automated dependency update PRs.

## 📚 Recommended Resources

### Tailwind CSS

- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Tailwind CSS Cheat Sheet](https://tailwindcomponents.com/cheatsheet/)
- [Headless UI Components](https://headlessui.com/) - Accessible, unstyled components for Tailwind
- [Heroicons](https://heroicons.com/) - Beautiful hand-crafted SVG icons

### Astro

- [Astro Documentation](https://docs.astro.build)
- [Astro + Tailwind Integration](https://docs.astro.build/en/guides/integrations-guide/tailwind/)
- [Astro Components](https://astro.build/components/)

### Learning Resources

- [Learn Astro](https://docs.astro.build/en/tutorial/0-introduction/)
- [Tailwind CSS: From Zero to Production](https://www.youtube.com/playlist?list=PL5f_mz_zU5eXWYDXHUDOLBE0scnuJofO0)
- [Full Stack Astro](https://www.youtube.com/watch?v=cuPNY8s6EYI)
- [Astro Crash Course](https://www.youtube.com/watch?v=e-hTm5VmofI)
