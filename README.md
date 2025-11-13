# LLM App Prototyper 🚀

A web application that generates self-contained, single-file HTML applications using AI. Works with any OpenAI-compatible API endpoint, including local LLM installations. Simply describe what you want, and the LLM will create a complete, downloadable web app for you.

<img width="1917" height="910" alt="image" src="https://github.com/user-attachments/assets/81ae4fd5-d5b9-4211-9ee1-421fa9bd4d51" />

## Features

- **Chat Interface**: Intuitive chat-based interaction for describing your app requirements
- **AI-Powered Generation**: Uses any OpenAI-compatible LLM to create fully functional web applications
- **Flexible API Configuration**: Works with OpenAI, local LLMs (Ollama, LM Studio, etc.), or any compatible endpoint
- **Single-File Output**: All generated apps are self-contained HTML files with embedded CSS and JavaScript
- **Live Preview**: See your generated app in real-time before downloading
- **Dark/Light Mode**: Toggle between themes for comfortable viewing
- **Context Management**: "New App" button to clear conversation and start fresh
- **No Backend Required**: Runs entirely in the browser - just open the HTML file
- **Secure**: API keys and settings stored locally in your browser using localStorage

## Quick Start

1. **Open the App**: Simply open `index.html` in any modern web browser
2. **Configure API Settings**: Click "⚙️ API Settings" and enter:
   - **API URL**: Your LLM endpoint (e.g., `https://api.openai.com/v1/chat/completions` or `http://localhost:11434/v1/chat/completions` for Ollama)
   - **Model**: Model name (e.g., `gpt-4o`, `llama3`, `codellama`)
   - **API Key**: Your API key (or leave empty for local LLMs that don't require authentication)
3. **Describe Your App**: Type what you want to create (e.g., "A weekly scheduling system for a label printing company with 7 pieces of equipment")
4. **Generate**: Click "Send" and wait for the AI to generate your app
5. **Preview & Download**: Review the app in the preview pane and download when satisfied

## Setting Up Local LLMs

Want to run this completely offline with a local LLM? Here's how:

### Using Ollama (Recommended for Beginners)

1. **Install Ollama**: Download from [ollama.com](https://ollama.com)
2. **Pull a model**: `ollama pull codellama` (or `llama3`, `mistral`, etc.)
3. **Verify it's running**: Ollama runs automatically; test with `ollama list`
4. **Configure the app**:
   - API URL: `http://localhost:11434/v1/chat/completions`
   - Model: `codellama` (or your chosen model)
   - API Key: Leave empty or use any placeholder

### Using LM Studio

1. **Download LM Studio**: Get it from [lmstudio.ai](https://lmstudio.ai)
2. **Load a model**: Download a code-capable model from the built-in browser
3. **Start the server**: Click "Local Server" tab and start the server
4. **Configure the app**:
   - API URL: `http://localhost:1234/v1/chat/completions` (check LM Studio for actual port)
   - Model: Check the model name in LM Studio's server tab
   - API Key: Leave empty

### Using Text Generation WebUI

1. **Install**: Follow [installation guide](https://github.com/oobabooga/text-generation-webui)
2. **Enable API**: Start with `--api --extensions openai`
3. **Load a model**: Use the web interface to load your model
4. **Configure the app**:
   - API URL: `http://localhost:5000/v1/chat/completions` (check your port)
   - Model: The name of your loaded model
   - API Key: Leave empty

**Note**: Code-capable models like CodeLlama, DeepSeek Coder, or Qwen Coder work best for generating applications.

## Example Prompts

- "A weekly scheduling system for a label printing company with 7 pieces of equipment"
- "A simple todo list app with priorities and due dates"
- "A calculator for calculating mortgage payments"
- "A recipe organizer with search and filtering"
- "A time tracking app for freelancers"
- "A simple inventory management system for a small retail store"

## Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- An OpenAI-compatible LLM API endpoint:
  - **OpenAI**: [Get API key here](https://platform.openai.com/api-keys)
  - **Ollama**: Install locally from [ollama.com](https://ollama.com)
  - **LM Studio**: Download from [lmstudio.ai](https://lmstudio.ai)
  - **Text Generation WebUI**: [oobabooga/text-generation-webui](https://github.com/oobabooga/text-generation-webui)
  - **LocalAI**: [localai.io](https://localai.io)
  - Or any other OpenAI-compatible endpoint
- Internet connection (only required for cloud-based APIs)

## Compatible LLM Services

This app works with any service that implements the OpenAI chat completions API format:

### Cloud Services
- **OpenAI** (GPT-4, GPT-4o, etc.)
- **Azure OpenAI**
- **OpenRouter**
- **Together AI**
- **Anthropic** (via compatibility layers)

### Local LLM Solutions
- **Ollama**: Run models locally (llama3, codellama, mistral, etc.)
- **LM Studio**: Desktop app with OpenAI-compatible server
- **Text Generation WebUI**: Full-featured local LLM interface
- **LocalAI**: Self-hosted OpenAI-compatible API
- **llama.cpp**: With `--api` flag for OpenAI compatibility

## Technical Details

- **No Installation**: Zero dependencies, no build process
- **Pure HTML/CSS/JavaScript**: Single file contains everything
- **Universal API Support**: Compatible with any OpenAI-format chat API
- **Client-Side Only**: All processing happens in your browser
- **localStorage**: API settings persist between sessions
- **Customizable Endpoint**: Configure API URL, model, and authentication

## API Security

Your API credentials are:
- Stored only in your browser's localStorage
- Sent only to the API endpoint you configure
- Never logged or transmitted to any third party
- Can be deleted by clearing browser data or using "Clear" in settings

## Customization

You can modify the system prompt in the JavaScript section to:
- Change the style of generated apps
- Add specific frameworks or libraries
- Adjust the output format
- Fine-tune the generation behavior

## Limitations

- Generated apps are limited by your LLM's token/context limits (varies by model)
- Complex applications may require multiple iterations or conversation refinement
- Apps are single-file only (no multi-file projects)
- Requires internet connection for cloud-based APIs (local LLMs work offline)
- Quality of generated apps depends on the capabilities of your chosen model

## Troubleshooting

### API Connection Issues
- **Cloud APIs**: Verify your API key is valid and has credits/quota
- **Local LLMs**: Ensure the local server is running and accessible (e.g., Ollama: `ollama serve`)
- **CORS Errors**: Some local LLMs may need CORS configuration; check server documentation
- **URL Format**: Make sure the API URL ends with `/v1/chat/completions` or appropriate endpoint

### Generation Issues
- **No Response**: Check browser console (F12) for error messages
- **Poor Quality**: Try a more capable model (e.g., upgrade from smaller to larger model)
- **Incomplete Apps**: Provide more detailed descriptions or break complex requests into steps
- **No Preview**: Ensure generated HTML is valid; check console for syntax errors

### General Issues
- **Download Not Working**: Ensure your browser allows downloads from local files
- **Settings Not Saving**: Check that localStorage is enabled in your browser
- **Dark Mode Issues**: Clear browser cache and reload the page

## License

MIT License - Feel free to use, modify, and distribute

## Contributing

Contributions welcome! This is a simple single-file project, so feel free to enhance it.

## Support

For issues or questions, please open an issue on the GitHub repository.
