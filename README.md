# CheckUrl Extension - Real-time Malicious Link Scanner

🛡️ **CheckUrl browser extension that automatically scans and protects you from malicious links in real-time**

## Features

- ✅ **Real-time Link Scanning** - Automatically analyzes links as you browse
- 🤖 **AI-Powered Detection** - Uses OpenAI GPT for advanced threat analysis
- 🚨 **Visual Warnings** - Highlights dangerous links with colored borders
- 🛑 **Click Protection** - Blocks access to malicious sites with warning dialogs
- 📊 **Scan History** - Tracks all scanned URLs and statistics
- ⚡ **Fast Performance** - Cached results and batch processing
- 🎯 **Smart Whitelisting** - Trusted domains bypass scanning

## Installation Guide

### Step 1: Download the Extension

1. Download the extension as a ZIP file from the repository
2. Extract the ZIP file to a folder on your computer
3. You should see a folder named `CheckUrl-ext` containing all extension files

### Step 2: Set Up Your OpenAI API Key

1. Open the `CheckUrl-ext` folder
2. Find and open `background.js` in a text editor
3. Locate line 2 that contains:
   ```javascript
   const OPENAI_API_KEY = 'YOUR_API_KEY'; // REPLACE WITH YOUR KEY
   ```
4. Replace `'YOUR_API_KEY'` with your actual OpenAI API key:
   ```javascript
   const OPENAI_API_KEY = 'ADD YOUR OPEN AI KEY';
   ```
5. Save the file

### Step 3: Install in Firefox

1. Open Firefox browser
2. Type `about:debugging` in the address bar and press Enter
3. Click on **"This Firefox"** in the left sidebar
4. Click the **"Load Temporary Add-on..."** button
5. Navigate to your `CheckUrl-ext` folder
6. Select the `manifest.json` file and click **"Open"**
7. The extension should now appear in the list of temporary extensions

### Step 4: Verify Installation

1. Look for the CheckUrl icon in your Firefox toolbar (shield icon)
2. Click on the extension icon to open the popup dashboard
3. You should see:
   - Extension status showing "Protection: Active"
   - Current page scan results
   - Scan statistics (Safe: 0, Blocked: 0, Suspicious: 0)

### Step 5: Test the Extension

1. Visit any website (like Google.com)
2. The extension will automatically scan the page
3. Try searching for something on Google
4. The extension should analyze search result links
5. Check the extension popup to see scan history and statistics

## How It Works

### Automatic Scanning
- **Page Load**: Scans all links when a page loads
- **Dynamic Content**: Monitors for new links added to the page
- **Real-time Analysis**: Uses OpenAI GPT to analyze URL patterns and content

### Visual Indicators
- 🟢 **Safe Links**: No highlighting (trusted)
- 🟡 **Suspicious Links**: Yellow border with ⚠️ warning icon
- 🔴 **Malicious Links**: Red border with 🚨 danger icon

### Protection Levels
- **Malicious Sites**: Completely blocked with warning dialog
- **Suspicious Sites**: Warning dialog with option to proceed
- **Safe Sites**: No interference with browsing

## Extension Dashboard

Click the CheckUrl icon in your toolbar to access:

- **Current Page Status**: Real-time scan of the active page
- **Scan Statistics**: Total safe, blocked, and suspicious sites
- **Recent Scan History**: List of recently analyzed URLs
- **Manual Scan Button**: Force re-scan of current page

## Troubleshooting

### Extension Not Working?

1. **Check API Key**: Ensure your OpenAI API key is correctly added to `background.js`
2. **Reload Extension**: Go to `about:debugging` and reload the temporary add-on
3. **Check Console**: Open browser developer tools (F12) and check for error messages
4. **Permissions**: Make sure Firefox allows the extension to access websites

### Common Issues

- **"API key not configured"**: You need to add your OpenAI API key to `background.js`
- **No scan results**: The extension may be loading - wait a few seconds and check again
- **Extension disappeared**: Temporary add-ons are removed when Firefox restarts - reload it from `about:debugging`

### Making It Permanent

To keep the extension after Firefox restarts:
1. The extension needs to be signed by Mozilla
2. For development/personal use, you can reload it each time from `about:debugging`
3. For permanent installation, consider packaging it as a proper Firefox add-on

## Security Notes

⚠️ **Important**: This extension requires an OpenAI API key which may incur costs based on usage. Monitor your OpenAI usage dashboard.

🔒 **Privacy**: URLs are sent to OpenAI for analysis. Trusted domains are whitelisted to avoid unnecessary API calls.

## File Structure

```
CheckUrl-ext/
├── manifest.json          # Extension configuration
├── background.js          # Main analysis engine (ADD API KEY HERE)
├── content.js            # Page interaction script
├── content.css           # Visual styling
├── popup.html            # Extension popup interface
├── popup.js              # Popup functionality
└── icons/                # Extension icons
    ├── icon-16.png
    ├── icon-32.png
    ├── icon-48.png
    └── icon-128.png
```

## Support

If you encounter any issues:
1. Check the browser console for error messages
2. Verify your OpenAI API key is valid and has sufficient credits
3. Ensure all files are in the correct locations
4. Try reloading the extension from `about:debugging`

---

**Happy Safe Browsing! 🛡️**
