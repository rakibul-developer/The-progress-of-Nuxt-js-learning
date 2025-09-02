# Nuxt App

A modern web application built with Nuxt 4, featuring blog and user management functionality with dynamic routing and page transitions.

## Features

- 🏠 **Home Page** - Landing page with navigation
- 📝 **Blog System** - Dynamic blog posts with nested routing
  - Individual blog posts (`/blog/[id]`)
  - Blog post comments (`/blog/[id]/comments`)
  - Blog listing (`/blog`)
- 👥 **User Management** - User profiles with settings
  - User profiles (`/users/[id]`)
  - User settings (`/users/[id]/settings`)
  - User listing (`/users`)
- 🎨 **Page Transitions** - Smooth page transitions with `out-in` mode
- 🛠️ **Developer Tools** - Nuxt DevTools enabled for development

## Tech Stack

- **Framework**: Nuxt 4.0.3
- **Frontend**: Vue 3.5.20
- **Routing**: Vue Router 4.5.1
- **Package Manager**: Bun (lockfile present)
- **TypeScript**: Full TypeScript support

## Project Structure

```
nuxtApp/
├── app/
│   ├── pages/
│   │   ├── blog/
│   │   │   ├── [id]/
│   │   │   │   ├── comments.vue    # Blog post comments
│   │   │   │   └── index.vue       # Blog post content
│   │   │   ├── [id].vue            # Blog post layout
│   │   │   └── index.vue           # Blog listing
│   │   ├── users/
│   │   │   ├── [id]/
│   │   │   │   ├── index.vue       # User profile
│   │   │   │   └── settings.vue    # User settings
│   │   │   ├── [id].vue            # User layout
│   │   │   └── index.vue           # User listing
│   │   └── index.vue               # Home page
│   └── app.vue                     # Root component
├── public/
│   ├── favicon.ico
│   └── robots.txt
├── nuxt.config.ts                  # Nuxt configuration
└── package.json
```

## Routes

The application uses Nuxt's file-based routing:

| Route | Description |
|-------|-------------|
| `/` | Home page |
| `/blog` | Blog listing |
| `/blog/[id]` | Individual blog post |
| `/blog/[id]/comments` | Blog post comments |
| `/users` | User listing |
| `/users/[id]` | User profile |
| `/users/[id]/settings` | User settings |

## Setup

Make sure to install dependencies:

```bash
# bun (recommended)
bun install

# npm
npm install

# pnpm
pnpm install

# yarn
yarn install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# bun
bun run dev
# or
bun run dev -o ( Run With Server Engine )

# npm
npm run dev

# pnpm
pnpm dev

# yarn
yarn dev
```

## Production

Build the application for production:

```bash
# bun
bun run build

# npm
npm run build

# pnpm
pnpm build

# yarn
yarn build
```

Locally preview production build:

```bash
# bun
bun run preview

# npm
npm run preview

# pnpm
pnpm preview

# yarn
yarn preview
```

## Configuration

The app is configured with:

- **Page Transitions**: `out-in` mode for smooth navigation
- **DevTools**: Enabled in development
- **Compatibility Date**: 2025-07-15
- **TypeScript**: Full support with auto-generated types

## Development

- Nuxt DevTools are enabled for enhanced development experience
- Hot module replacement for instant updates
- Auto-imports for Vue composables and Nuxt utilities
- File-based routing with nested layouts

## Learn More

- [Nuxt Documentation](https://nuxt.com/docs/getting-started/introduction)
- [Vue 3 Documentation](https://vuejs.org/)
- [Deployment Guide](https://nuxt.com/docs/getting-started/deployment)
