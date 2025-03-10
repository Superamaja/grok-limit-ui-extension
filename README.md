# Grok Rate Limit UI

A simple Chrome extension that displays your Grok rate limits directly in the Grok web interface.

![Grok Rate Limit UI Screenshot](screenshots/preview.png)

## Description

This Chrome extension enhances your Grok experience by providing real-time visibility into your rate limits. Instead of wondering how many requests you have left, the extension adds a small counter directly in the Grok interface that displays your remaining requests out of your total allocation.

The counter updates automatically whenever you send a message to Grok, as that's when the site fetches rate limit information from the API.

## Features

- 📊 Displays remaining/total API requests
- 🎨 Color-coded indicator (green → yellow → red) based on usage
- 🔄 Automatically updates after each message
- ⚡ Lightweight with minimal performance impact
- 🛡️ Requires no additional permissions beyond accessing Grok

## Installation

<!-- ### From Chrome Web Store (Recommended)

1. Visit the [Chrome Web Store page](https://chrome.google.com/webstore/)
2. Click "Add to Chrome"
3. Confirm the installation -->

### Manual Installation

#### Option 1: From Release ZIP

1. Download the latest release ZIP file from the [Releases page](https://github.com/yourusername/grok-extension/releases)
2. Extract the ZIP file to a location on your computer
3. Open Chrome and navigate to `chrome://extensions`
4. Enable "Developer mode" in the top-right corner
5. Click "Load unpacked" and select the extracted folder
6. The extension is now installed and active when you visit grok.com

#### Option 2: From Source

1. Clone this repository or download the source code
2. Open Chrome and navigate to `chrome://extensions`
3. Enable "Developer mode" in the top-right corner
4. Click "Load unpacked" and select the `src` folder from this repository
5. The extension is now installed and active when you visit grok.com

## Usage

1. Visit [grok.com](https://grok.com)
2. You'll see a small counter in the top bar showing your remaining requests
3. The counter updates each time you send a message
4. Color changes indicate your remaining capacity:
   - White/Green: Plenty of requests left
   - Orange: Under 30% remaining
   - Red: Under 10% remaining

## Roadmap

Potential future enhancements:

- Chrome Web Store release if it gains traction
- Proactive updates when switching models or using different features
- Automatic refresh of rate limit data
- Visual countdown to rate limit reset
- Customizable notification thresholds

## Development

This extension consists of:

- `contentScript.js`: Injects display element and handles DOM interactions
- `networkMonitor.js`: Monitors network requests to capture rate limit data
- `rateLimitDisplay.html`: Contains the UI element and styling

To contribute:

1. Fork this repository
2. Make your changes
3. Test locally using the manual installation steps
4. Submit a pull request

## License

MIT License - See [LICENSE](LICENSE) file for details

## Author

Created by [Connor](https://connorlin.dev/) - A Grok enthusiast who got tired of hitting rate limits unexpectedly.

<!-- If you find this extension useful, consider [buying me a coffee](https://www.buymeacoffee.com/) or starring the repository! -->
