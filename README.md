# LLM Playground

A lightweight, extensible chat interface for interacting with Large Language Models. Built with modern web tooling and designed for flexibility across multiple AI providers.

## Features

- **Multi-Provider Support**: Connect to any OpenAI-compatible API endpoint. Manage multiple providers and switch between them seamlessly.
- **Streaming Responses**: Real-time token streaming for a native chat experience.
- **Personas**: Create, edit, and manage custom AI characters with distinct system prompts, avatars, and accent colors.
- **Theme System**: Built-in light and dark themes with support for fully custom color palettes.
- **Conversation Management**: Persistent chat history stored locally. Start, continue, and delete conversations at will.
- **Image Generation**: Generate images within the chat context when supported by the provider.
- **Message Editing & Regeneration**: Edit past messages or retry the last assistant response.

## Tech Stack

- **React 19** with TypeScript
- **Vite** for fast builds and HMR
- **Tailwind CSS** for styling
- **shadcn/ui** primitives via Radix UI
- **React Router** for client-side routing
- **Framer Motion** for animations
- **React Markdown** with syntax highlighting for rich message rendering

## Quick Start

```bash
git clone https://github.com/vinilouz/LLMPlayground.git
cd LLMPlayground
npm install
```

### Configuration

Copy the example environment file and set your API endpoint:

```bash
cp .env.example .env
```

Edit `.env`:

```
VITE_API_BASE_URL=https://api.openai.com/v1
VITE_DEBUG=false
```

Substitute `https://api.openai.com/v1` with the base URL of your preferred OpenAI-compatible provider.

### Development

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173).

### Production Build

```bash
npm run build
```

## Project Structure

```
src/
  pages/          # Route-level pages (Home, Chat)
  components/     # UI components (chat, sidebar, modals)
  hooks/          # Custom React hooks (conversations, personas, providers, theme)
  lib/            # Utilities and configuration
  data/           # Static data (default personas, themes)
  types/          # Shared TypeScript interfaces
```

## Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start the development server |
| `npm run build` | Type-check and build for production |
| `npm run preview` | Preview the production build |
| `npm run lint` | Run ESLint |
| `npm run test:e2e` | Run Playwright end-to-end tests |

## License

MIT
