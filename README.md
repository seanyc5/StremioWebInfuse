# Stremio Web with Infuse Integration

A modified version of [Stremio Web](https://github.com/Stremio/stremio-web) with **Infuse external player support** for macOS users.

## 🎬 What's New

This fork adds **Infuse** as an external player option in Stremio Web, allowing you to stream content directly to Infuse on macOS using the `infuse://` URL scheme.

### ✨ Features Added

- **Infuse External Player**: Added to the external players list for macOS
- **Direct Streaming**: Content opens directly in Infuse without downloading M3U files
- **Real-Debrid Integration**: Works seamlessly with Real-Debrid and other debrid services
- **URL Scheme Support**: Uses `infuse://x-callback-url/play?url=...` for direct playback

## 🚀 Installation

### Prerequisites

- **macOS** (required for Infuse integration)
- **Node.js** (v14 or higher)
- **Infuse app** installed on your Mac
- **Real-Debrid account** (or similar debrid service)

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/seanyc5/StremioWebInfuse.git
   cd StremioWebInfuse
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm start
   ```

4. **Open in browser**
   Navigate to `https://localhost:8080`

5. **Configure Infuse**
   - Go to **Settings** → **Player**
   - Select **"Infuse"** from the external player dropdown
   - Save your settings

## 🎯 How to Use

1. **Browse content** in Stremio as usual
2. **Click on any stream** to play
3. **Content opens directly in Infuse** on your Mac
4. **Enjoy streaming** with Infuse's excellent playback features

## 🔧 Development

### Making Changes

1. **Start development server**
   ```bash
   npm start
   ```

2. **Make your changes** (live reload enabled)

3. **Build for production**
   ```bash
   npm run build
   npm run start-prod
   ```

### Project Structure

- **Modified Files**:
  - `src/common/CONSTANTS.js` - Added Infuse to external players list
  - `src/routes/MetaDetails/StreamsList/Stream/Stream.js` - Added Infuse URL generation

## 📱 Infuse Integration Details

The integration works by:

1. **Detecting Infuse player type** in user settings
2. **Generating Infuse URL scheme**: `infuse://x-callback-url/play?url=<encoded_stream_url>`
3. **Opening content directly** in Infuse without intermediate downloads

### URL Format

```
infuse://x-callback-url/play?url=https%3A//real-debrid.com/d/...
```

## 🤝 Contributing

This is a fork of the official Stremio Web repository. To contribute:

1. Fork this repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📄 License

This project is based on [Stremio Web](https://github.com/Stremio/stremio-web) and is licensed under the same GPL-2.0 license.

## 🙏 Credits

- **Original Stremio Team** - For the amazing Stremio Web application
- **Infuse Team** - For the excellent URL scheme support
- **Real-Debrid** - For their debrid service API

## 🔗 Links

- [Original Stremio Web](https://github.com/Stremio/stremio-web)
- [Infuse App](https://firecore.com/infuse)
- [Real-Debrid](https://real-debrid.com/)
- [Stremio Community](https://www.stremio.com/)

## 🐛 Troubleshooting

### Infuse not opening
- Ensure Infuse is installed on your Mac
- Check that the Infuse protocol is registered
- Try manually opening `infuse://` links in your browser

### Stream not playing
- Verify your Real-Debrid account is active
- Check that the content is available in your debrid library
- Ensure you have sufficient debrid points

### Development issues
- Clear browser cache and local storage
- Restart the development server
- Check browser console for errors

---

**Enjoy streaming your media with Stremio + Infuse! 🎬✨**
