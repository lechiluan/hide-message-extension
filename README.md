## Messenger Message Hider

Messenger Message Hider is a lightweight Chrome/Chromium-based browser extension that **blurs your Messenger conversations and sidebar by default**. Messages are revealed only when you hover them, helping you keep your chats private in shared or public environments.

### Features

- **Auto-blur conversations**: Blurs message bubbles and the conversation list/sidebar.
- **Hover to reveal**: Move your mouse over a blurred area to temporarily reveal it.
- **Multi-site support**:
  - `https://www.messenger.com/*`
  - `https://www.facebook.com/messages/*`
  - `https://chat.zalo.me/*`
- **CSS-only implementation**: Uses a `content.css` stylesheet injected via a Manifest V3 content script (no JavaScript or extra permissions).

### Installation (Developer Mode)

1. **Clone or download** this repository to your machine.
2. Open your Chromium-based browser (e.g. Chrome, Edge, Brave).
3. Go to the Extensions page:
   - Chrome: `chrome://extensions/`
   - Edge: `edge://extensions/`
4. Enable **Developer mode** (toggle in the top-right corner).
5. Click **“Load unpacked”**.
6. Select the folder containing this project (`hide-message-extension`).

The extension should now be installed and active on supported Messenger sites.

### How It Works

- The extension is defined in `manifest.json` (Manifest V3).
- A content script entry injects `content.css` into supported Messenger/Zalo URLs.
- The CSS file applies blur and hover effects to relevant UI elements to hide message content until you hover.

### Development

- **Modify styles**: Edit `content.css` to tweak which elements are blurred, how strong the blur is, and the hover behavior.
- **Update metadata**: Edit `manifest.json` to change the extension name, description, or target URLs.
- After making changes, go back to the Extensions page and click **“Reload”** on the extension to apply updates.

### Limitations

- The extension relies on the current DOM structure and CSS classes of Messenger/Facebook/Zalo. If those platforms change their layout, the blur rules might need updates.
- Only supports the URLs listed in the manifest. Additional sites would need to be added manually.

### License

Add your preferred license here (e.g. MIT) if you plan to share or publish this extension.

