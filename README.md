# LLM App Prototyper 🚀

An OpenAI API-compatible web application that generates self-contained, single-file HTML applications using AI. Simply describe what you want, and the LLM will create a complete, downloadable web app for you.

## Features

- **Chat Interface**: Intuitive chat-based interaction for describing your app requirements
- **AI-Powered Generation**: Uses OpenAI's GPT-4 to create fully functional web applications
- **Single-File Output**: All generated apps are self-contained HTML files with embedded CSS and JavaScript
- **Live Preview**: See your generated app in real-time before downloading
- **No Backend Required**: Runs entirely in the browser - just open the HTML file
- **Secure**: API keys stored locally in your browser using localStorage

## Quick Start

1. **Open the App**: Simply open `index.html` in any modern web browser
2. **Set API Key**: Click "⚙️ API Settings" and enter your OpenAI API key
3. **Describe Your App**: Type what you want to create (e.g., "A weekly scheduling system for a label printing company with 7 pieces of equipment")
4. **Generate**: Click "Send" and wait for the AI to generate your app
5. **Preview & Download**: Review the app in the preview pane and download when satisfied

## Example Prompts

- "A weekly scheduling system for a label printing company with 7 pieces of equipment"
- "A simple todo list app with priorities and due dates"
- "A calculator for calculating mortgage payments"
- "A recipe organizer with search and filtering"
- "A time tracking app for freelancers"
- "A simple inventory management system for a small retail store"

## Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- OpenAI API key ([Get one here](https://platform.openai.com/api-keys))
- Internet connection (for API calls)

## Technical Details

- **No Installation**: Zero dependencies, no build process
- **Pure HTML/CSS/JavaScript**: Single file contains everything
- **OpenAI API**: Uses GPT-4 for generation (compatible with any OpenAI-compatible API)
- **Client-Side Only**: All processing happens in your browser
- **localStorage**: API key persists between sessions

## API Key Security

Your API key is:
- Stored only in your browser's localStorage
- Never sent anywhere except OpenAI's API
- Never logged or transmitted to any third party
- Can be deleted by clearing browser data

## Customization

You can modify the system prompt in the JavaScript section to:
- Change the style of generated apps
- Add specific frameworks or libraries
- Adjust the output format
- Fine-tune the generation behavior

## Limitations

- Generated apps are limited by OpenAI's token limits (~4000 tokens for output)
- Complex applications may require multiple iterations
- Apps are single-file only (no multi-file projects)
- Requires active internet connection for generation

## Troubleshooting

**API Key Error**: Make sure your OpenAI API key is valid and has credits
**No Preview**: Check browser console for errors, ensure generated HTML is valid
**Download Not Working**: Ensure your browser allows downloads from local files

## License

MIT License - Feel free to use, modify, and distribute

## Contributing

Contributions welcome! This is a simple single-file project, so feel free to enhance it.

## Support

For issues or questions, please open an issue on the GitHub repository.
