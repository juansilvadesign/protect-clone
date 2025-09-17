<div align="center">

# 🤖 ProtectClone: Telegram Channel Cloner & Downloader

[![Python](https://img.shields.io/badge/Python-3.7%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Pyrogram](https://img.shields.io/badge/Pyrogram-Telegram%20API-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://docs.pyrogram.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Windows](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey?style=for-the-badge&logo=windows&logoColor=white)]()

![GitHub stars](https://img.shields.io/github/stars/juansilvadesign/protect-clone?style=social)
![GitHub forks](https://img.shields.io/github/forks/juansilvadesign/protect-clone?style=social)
![GitHub issues](https://img.shields.io/github/issues/juansilvadesign/protect-clone?style=social)

*A powerful Python tool to clone, forward, and download messages and media from private Telegram channels!* 🚀

</div>

---

## 📋 Overview

**ProtectClone** is a robust Python script that allows you to **clone messages and media** from private Telegram channels, even when forwarding is restricted. It supports three modes: full channel cloning, real-time chat listening, and batch media downloading. Perfect for backup, migration, or archiving!

---

## ✨ Features

<table>
<tr>
<td>

### 🔄 Channel Cloning
- Clone all messages from a source channel to a destination channel
- Option to mention or hide the original author
- Handles restricted forwarding (downloads and reuploads media)

</td>
<td>

### 🕒 Real-Time Listener
- Listen for new messages in a channel
- Instantly clone new posts to another channel
- Flexible mention/hide options

</td>
</tr>
<tr>
<td>

### 📥 Media Downloader
- Download all media from a channel to your PC
- Resumes interrupted downloads
- Organizes files with custom naming

</td>
<td>

### ⚙️ User-Friendly
- Interactive CLI prompts
- Progress feedback for downloads/uploads
- State saving for resuming operations

</td>
</tr>
</table>

---

## 🚀 Quick Start

### Prerequisites

- Python 3.7+
- [Pyrogram](https://docs.pyrogram.org/) & [cryptg](https://pypi.org/project/cryptg/) (Windows-friendly alternative to tgcrypto)

### Installation

#### Step 1: Clone the Repository
```bash
git clone https://github.com/juansilvadesign/protect-clone.git
cd protect-clone
```

#### Step 2: Set Up Virtual Environment (Recommended)
```powershell
# Windows
pip install virtualenv
virtualenv .env
.env\Scripts\activate

# Linux/macOS
python3 -m venv .env
source .env/bin/activate
```

#### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

#### Step 4: Verify Installation
```bash
python main.py --help
```

### 🚀 Running the Script

```bash
python main.py
```

**First Run:** You'll be prompted to enter your Telegram API credentials from [my.telegram.org](https://my.telegram.org/)

---

## 🛠️ Modes & Usage

When you run the script, choose one of the following modes:

| Mode | Description | Icon |
|------|-------------|------|
| 1 | **Cloner**: Clone all messages from one channel to another | 🔄 |
| 2 | **Chat Listener**: Listen and clone new messages in real-time | 🕒 |
| 3 | **Chat Downloader**: Download all media from a channel | 📥 |

### Example Workflow

1. **Run the script:** `python main.py`
2. **Enter your Telegram API ID and Hash** (first run only)
3. **Select mode** (1, 2, or 3)
4. **Follow prompts** for channel IDs, mention options, and file/folder names
5. **Watch progress in the terminal!**

---

## 📦 Dependencies

| Package   | Purpose                        |
|-----------|--------------------------------|
| Pyrogram  | Telegram API interaction       |
| cryptg    | Fast cryptography for Pyrogram (Windows-friendly) |
| configparser | Config file management      |

Install all dependencies with:
```bash
pip install -r requirements.txt
```

---

## 💡 Tips & Notes

### 🔐 Security & Privacy
- **API Credentials:** Get your `api_id` and `api_hash` from [my.telegram.org](https://my.telegram.org/)
- **🔒 Keep credentials safe:** Never share your API credentials publicly
- **⚖️ Respect copyright:** Only clone content you have permission to use
- **🤝 Follow Telegram ToS:** Use responsibly and respect Telegram's Terms of Service

### 📋 Usage Guidelines
- **Channel IDs:** Use `@username` or numeric ID (e.g., `-1001234567890`)
- **Resuming:** The script saves progress so you can resume cloning or downloading later
- **Forward Restrictions:** If a channel restricts forwarding, the script will download and re-upload media automatically
- **Rate Limits:** The script respects Telegram's rate limits to avoid account restrictions

---

## � Troubleshooting

### Common Issues & Solutions

#### ❌ "Invalid API ID or Hash" Error
- **Solution:** Double-check your credentials from [my.telegram.org](https://my.telegram.org/)
- Make sure there are no extra spaces or characters

#### ❌ "CHAT_FORWARDS_RESTRICTED" Error
- **Solution:** This is normal for protected channels - the script will automatically download and re-upload media
- No action needed, the script handles this automatically

#### ❌ "FLOOD_WAIT" Error
- **Solution:** You've hit Telegram's rate limit. Wait the specified time before trying again
- The script will automatically handle short waits

#### ❌ "CHANNEL_PRIVATE" Error
- **Solution:** Make sure you're a member of the source channel
- Check that the channel ID/username is correct

#### ❌ Permission Denied Errors
- **Solution:** Ensure you have admin rights in the destination channel
- For downloads, check that the destination folder is writable

#### ❌ "Microsoft Visual C++ 14.0 is required" Error (Windows)
- **Problem:** This occurs when trying to install `tgcrypto` on Windows
- **Solution:** The project uses `cryptg` instead, which has pre-built wheels
- **Alternative:** If you need `tgcrypto`, install [Microsoft C++ Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/)

#### 💻 Performance Issues
- **Large files:** Use a stable internet connection for better performance
- **Memory usage:** Close other applications if experiencing high memory usage
- **Network errors:** The script will retry failed operations automatically

### 📞 Getting Help
- Check existing [GitHub Issues](https://github.com/juansilvadesign/protect-clone/issues)
- Create a new issue with detailed error messages
- Include your Python version and operating system

---

## �🗺️ Roadmap

- [ ] 📥 Batch channel support
- [ ] 📝 Logging improvements
- [ ] 🖼️ Media type filters
- [ ] 🧪 Unit tests
- [ ] 🌐 Multi-language support

---

## 🤝 Contributing

We welcome contributions from the community! Please read our:

- **📋 [Contributing Guidelines](CONTRIBUTING.md)** - How to contribute to the project
- **📜 [Code of Conduct](CODE_OF_CONDUCT.md)** - Community standards and expectations

Whether you're fixing bugs, adding features, or improving documentation, your contributions are valued!

---

## 📄 License

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This project is licensed under the **MIT License**. Feel free to use, modify, and distribute!

---

## 🙏 Acknowledgments

- [Pyrogram](https://docs.pyrogram.org/)
- [Telegram](https://telegram.org/)
- Open Source Community

---

<div align="center">

### ⭐ If you found this project helpful, please give it a star!

Made with 💜 by Juan Silva

</div>
