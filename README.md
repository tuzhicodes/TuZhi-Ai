# 🤖 TuZhi AI Utility Bot

<div align="center">

![TuZhi Banner](https://img.shields.io/badge/TuZhi-AI%20Bot-orange?style=for-the-badge&logo=discord)
[![Discord.js](https://img.shields.io/badge/discord.js-v14-blue?style=for-the-badge&logo=discord)](https://discord.js.org)
[![Node.js](https://img.shields.io/badge/node.js-18+-green?style=for-the-badge&logo=node.js)](https://nodejs.org)
[![License](https://img.shields.io/badge/license-MIT-red?style=for-the-badge)](LICENSE)

**Advanced AI-Powered Discord Bot with Vision, Memory & Multi-Language Support**

[Features](#-features) • [Installation](#-installation) • [Commands](#-commands) • [Configuration](#-configuration) • [Support](#-support)

</div>

---

## 📖 About

TuZhi AI is a cutting-edge Discord bot powered by Google's Gemini AI, featuring advanced conversation memory, image recognition, and seamless bilingual support (English/Hindi/Hinglish). Built with modern Discord.js v14 and designed for optimal performance.

### 🎯 Key Highlights

- 🧠 **Smart Memory System** - Remembers conversation context per user
- 👁️ **Vision AI** - Can analyze and describe images
- 🌐 **Multi-Language** - Fluent in English, Hindi, and Hinglish
- 🎨 **Custom Emojis** - Uses your server's custom emojis
- 📧 **Reply Context** - Understands message replies
- ⚡ **Fast Response** - Optimized for speed
- 🔒 **Privacy-Focused** - User-specific memory isolation

---

## ✨ Features

### 🤖 AI Capabilities

| Feature | Description |
|---------|-------------|
| **Contextual Conversations** | Maintains topic consistency throughout conversations |
| **Image Analysis** | Describes images with detailed AI-powered descriptions |
| **Code Assistant** | Expert in JavaScript, Python, Discord.js, Node.js, React |
| **Memory Management** | Remembers last 15 messages per user |
| **Topic Tracking** | Stays focused on current discussion topic |
| **Reply Understanding** | Reads and responds to message replies |

### 🎨 Customization

- **Configurable Identity** - Easy to customize bot name, age, personality
- **Custom Emojis** - Automatically uses server emojis
- **Flexible Responses** - Short for casual chat, detailed for complex queries
- **Language Matching** - Responds in user's language (English/Hindi/Hinglish)

### 🛠️ Advanced Features

```javascript
✅ Per-User Memory System
✅ Server-Wide AI Channels
✅ Attachment Processing (Images, Videos, Files)
✅ Sticker Recognition
✅ User Mention Detection
✅ Cooldown Management
✅ Error Recovery
✅ Typing Indicators
✅ Clean Message Handling

---

## 📁 Project Structure

```
tuzhi-ai/
├── commands/
│   └── ai/
│       ├── activate.js        # Enable AI in channel
│       ├── deactivate.js      # Disable AI in channel
│       ├── img.js             # Genrate Images everyone 
│       └── clear-memory.js    # Clear user memory
├── events/
│   └── messageCreate.js       # Main AI event handler
├── utils/
│   └── aiHandler.js           # AI processing logic
├── data/
│   └── ai/
│       ├── ai_channels.json   # Active AI channels
│       ├── memory.json        # User conversation history
│       └── server_data.json   # Server information
├── index.js                   # Bot entry point
├── package.json
├── .env                       # Configuration (create this)
└── README.md
```

---

## 💬 Commands

### AI Management

| Command | Description | Permission |
|---------|-------------|------------|
| `/activate` | Enable AI in a channel | Admin Only |
| `/deactivate` | Disable AI in a channel | Admin Only |
| `/clear-memory` | Clear your AI conversation history | Everyone |
| `/img` | View AI system Gen Image | Everyone |

### Usage Examples

```
/activate channel:#general
→ Enables AI in #general channel

/clear-memory
→ Clears your personal conversation history

/ai-test message:"hello"
→ Tests AI response without saving to memory
```

---

## ⚙️ Configuration

### Bot Identity (Customizable)

Edit `utils/aiHandler.js` to customize:

```javascript
const BOT_CONFIG = {
    name: "TuZhi",                    // Bot name
    age: 17,                           // Bot age
    location: "Madhya Pradesh, India", // Location
    creator: "TuZhi Codes",            // Your name
    youtubeChannel: "...",             // Your channel
    expertise: [...],                  // Bot skills
    customEmojis: [...]                // Custom emojis
};
```

### AI Models

| Model | Best For | Quota |
|-------|----------|-------|
| `gemini-1.5-flash` | ✅ General use, best free quota | High |
| `gemini-1.5-pro` | Complex tasks, better quality | Medium |
| `gemini-2.0-flash-exp` | Experimental features | Low |

### Memory Settings

```javascript
const MAX_CONTEXT = 15;        // Messages to remember
const COOLDOWN_TIME = 3000;    // Cooldown in ms
```

---

## 🎨 Customization Guide

### Adding Custom Emojis

```javascript
// In utils/aiHandler.js
customEmojis: [
    '<:your_emoji:emoji_id>',
    '<:another_emoji:emoji_id>',
]
```

### Changing Personality

```javascript
personality: "friendly, helpful, your_traits_here",
expertise: ["Skill1", "Skill2", "Skill3"],
```

### Adjusting Response Style

```javascript
// For shorter responses
const MAX_CONTEXT = 5;

// For more detailed responses
const MAX_CONTEXT = 20;
```

---

## 🔧 Advanced Features

### Image Recognition

The bot can analyze images using Google's Gemini Vision:

```
User: [uploads image of code]
Bot: "Ye JavaScript code hai jo async/await use kar raha hai..."
```

### Memory System

- **Per-User Memory**: Each user has isolated conversation history
- **Topic Tracking**: AI maintains conversation topics
- **Context Awareness**: References previous messages naturally
- **15-Message Buffer**: Keeps recent conversation in memory

### Reply Context

```
User A: "Code sikha do"
Bot: "Haan! Kaunsi language?"

User A: [replies to bot] "JavaScript"
Bot: [understands context] "Sure! JavaScript basic se..."
```

---

## 📊 Performance

- **Response Time**: < 2 seconds average
- **Memory Usage**: ~50-100 MB
- **Concurrent Users**: Handles multiple users simultaneously
- **Uptime**: 99.9% (with proper hosting)

---

## 🐛 Troubleshooting

### Common Issues

**Bot not responding:**
```bash
1. Check if AI is activated: /ai-debug
2. Verify API key in .env
3. Check console for errors
```

**"API limit khatam" error:**
```bash
1. Wait 1-2 minutes (quota resets hourly)
2. Get new API key from aistudio.google.com
3. Update AI_API_KEY in .env
```

**Memory not working:**
```bash
1. Check data/ai/ folder exists
2. Verify memory.json file permissions
3. Use /clear-memory and try again
```
---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🌟 Acknowledgments

- **Discord.js** - Powerful Discord API wrapper
- **Google Gemini AI** - Advanced AI capabilities
- **TuZhi Codes** - Original creator and developer

---

## 📞 Support

### Need Help?

- 📺 **YouTube**: [TuZhi Codes](https://www.youtube.com/@TuZhiCodes)
- 💬 **Discord**: [Official Server](https://discord.gg/mnbQFftqby)
- 🐛 **Issues**: [GitHub Issues](https://github.com/tuzhicodes/TuZhi-Ai/issues)

### Community

Join our Discord server for:
- Live support
- Feature requests
- Bot updates
- Community discussions

---

<div align="center">

### 🔥 Made with ❤️ by [TuZhi Codes](https://www.youtube.com/@TuZhiCodes)

**⭐ Star this repo if you found it helpful!**

[![GitHub Stars](https://img.shields.io/github/stars/tuzhicodes/TuZhi-Ai?style=social)](https://github.com/YourUsername/tuzhi-ai-bot)
[![GitHub Forks](https://img.shields.io/github/forks/tuzhicodes/TuZhi-Ai?style=social)](https://github.com/tuzhicodes/TuZhi-Ai/fork)

---

**© 2024 TuZhi Codes. All rights reserved.**

</div>
