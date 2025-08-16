# Clonner - Setup Guide

## Quick Start

### 1. Install Dependencies

```bash
# Install all dependencies (root, backend, and frontend)
npm run install-all
```

### 2. Configure Environment Variables

Create a `.env` file in the `backend/` directory:

```bash
# Copy the example file
cp backend/env.example backend/.env
```

Edit `backend/.env` and add your API keys:

```env
# AI Provider Configuration
AI_PROVIDER=openai
OPENAI_API_KEY=your_openai_api_key_here
ANTHROPIC_API_KEY=your_anthropic_api_key_here

# Server Configuration
PORT=3001
NODE_ENV=development
```

### 3. Get API Keys

#### OpenAI (Recommended)
1. Go to [OpenAI Platform](https://platform.openai.com/api-keys)
2. Create an account and add payment method
3. Generate an API key
4. Add it to `OPENAI_API_KEY` in your `.env` file

#### Claude (Alternative)
1. Go to [Anthropic Console](https://console.anthropic.com/)
2. Create an account
3. Generate an API key
4. Add it to `ANTHROPIC_API_KEY` in your `.env` file

### 4. Start Development Servers

```bash
# Start both backend and frontend
npm run dev
```

This will start:
- Backend server on http://localhost:3001
- Frontend app on http://localhost:5173

## Usage

1. **Open the app** in your browser at http://localhost:5173
2. **Enter a prompt** describing your app idea
3. **Generate code** and see it in real-time
4. **Edit the code** in the Monaco editor
5. **Save projects** and view version history
6. **Configure settings** for different AI providers

## Example Prompts

- "Create a todo app with a modern design, add/delete functionality, and local storage"
- "Build a weather app that shows current conditions and 5-day forecast"
- "Make a calculator with a clean interface and basic math operations"
- "Create a note-taking app with markdown support and dark mode"

## Features

- ✅ **AI Code Generation** - Generate React apps from natural language
- ✅ **Live Preview** - See your app in real-time
- ✅ **Code Editor** - Monaco editor with syntax highlighting
- ✅ **Version History** - Save and restore previous versions
- ✅ **Multiple AI Providers** - Support for OpenAI and Claude
- ✅ **Modern UI** - Beautiful, responsive interface
- ✅ **Project Management** - Save and organize your projects

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
│   │   └── App.jsx      # Main app component
└── package.json      # Root package.json
```

## Troubleshooting

### Common Issues

1. **API Key Errors**
   - Make sure your API key is correct
   - Check that you have sufficient credits
   - Verify the AI provider setting

2. **Port Conflicts**
   - Change the PORT in backend/.env if 3001 is in use
   - Update the frontend API calls if you change the port

3. **CORS Errors**
   - The backend is configured with CORS for localhost
   - Make sure both servers are running

4. **Code Generation Fails**
   - Check the browser console for errors
   - Verify your prompt is clear and specific
   - Try a different AI provider

### Development

```bash
# Run only backend
npm run server

# Run only frontend
npm run client

# Install dependencies individually
cd backend && npm install
cd frontend && npm install
```

## Next Steps

- [ ] Add database persistence (PostgreSQL/MongoDB)
- [ ] Implement user authentication
- [ ] Add more AI providers
- [ ] Support for TypeScript
- [ ] Export to different frameworks
- [ ] Collaborative editing
- [ ] Template library

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

MIT License - feel free to use this project for your own applications! 