# Clonner

A minimal AI-powered no-code app builder that lets you clone and build apps with AI.

## Features

- Natural language app description input
- AI-powered code generation (OpenAI/Claude integration)
- Real-time code editor with syntax highlighting
- Live app preview
- Version history and rollback functionality

## Architecture

```
clonner/
├── backend/          # Node.js/Express API
│   ├── server.js     # Main server file
│   ├── routes/       # API routes
│   └── services/     # AI integration services
├── frontend/         # React/Vite app
│   ├── src/
│   │   ├── components/  # React components
│   │   ├── services/    # API calls
│   │   └── utils/       # Helper functions
└── README.md
```

## Quick Start

1. Install dependencies:
```bash
npm run install-all
```

2. Set up environment variables:
```bash
# In backend/.env
OPENAI_API_KEY=your_openai_key
# or
ANTHROPIC_API_KEY=your_claude_key
```

3. Start development servers:
```bash
npm run dev
```

## Implementation Phases

1. **Project Setup** - Basic structure and dependencies
2. **Backend API** - Express server with AI integration
3. **Frontend Core** - React app with prompt input
4. **Code Editor** - Monaco editor with syntax highlighting
5. **Live Preview** - Real-time app preview functionality
6. **Version History** - Save and restore previous versions
7. **Integration** - Connect all components together