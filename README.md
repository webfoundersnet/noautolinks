No Auto Links - phpBB Extension

A phpBB extension that disables automatic URL linking (magic_url) while preserving manual [url] BBCode functionality.
📝 Description
This extension solves the common issue where phpBB automatically converts plain text URLs into clickable links. With this extension installed, URLs typed in posts will remain as plain text, but users can still create links using the [url] BBCode tag when they want to.
What it does:

✅ Disables automatic URL detection and linking
✅ Keeps [url] BBCode functionality intact
✅ Gives users control over when links are created
✅ Reduces unwanted automatic formatting

Perfect for:

Forums where you want to prevent accidental link creation
Communities that prefer manual link control
Boards where plain text URLs should stay as text
Sites wanting cleaner post formatting

🚀 Installation
Method 1: Manual Installation

Download the extension files
Upload the webfounders folder to your phpBB ext/ directory
Navigate to your phpBB Admin Control Panel (ACP)
Go to Customise → Manage Extensions
Find "No Auto Links" and click Enable

Method 2: Git Clone

cd /path/to/your/phpbb/ext/
git clone https://github.com/webfoundersnet/noautolinks.git webfounders/noautolinks

Then follow steps 3-5 from Method 1. 

📁 File Structure

ext/webfounders/noautolinks/
├── composer.json
├── ext.php
├── config/
│   └── services.yml
└── event/
    └── listener.php

⚙️ Requirements

phpBB: 3.2.0 or higher
PHP: 7.1 or higher

🔧 How It Works
The extension uses phpBB's event system to intercept text processing before display and removes automatically generated links while preserving manually created BBCode links.
Technical Details:

Listens to core.modify_text_for_display_before event
Uses regex to remove auto-generated <a class="postlink"> tags
Leaves [url] BBCode processing untouched

🛠️ Configuration
No configuration needed! The extension works immediately after installation.
To disable: Go to ACP → Customise → Manage Extensions → No Auto Links → Disable

🐛 Troubleshooting
Extension not showing in Extensions Manager?

- Check file permissions (644 for files, 755 for directories)
- Ensure all files are uploaded correctly
- Clear phpBB cache: ACP → General → Purge Cache
- Verify the config/services.yml file exists

Still seeing auto-links?

Make sure the extension is enabled in ACP
Clear browser cache
Check if other extensions might be conflicting

🤝 Support

Issues: GitHub Issues
Website: WebFounders.net
Email: board@webfounders.net

📄 License
This extension is licensed under the GPL-2.0 License.

🏢 About WebFounders

Visit WebFounders.net for more web development resources and phpBB extensions.

Made with ❤️ by WebFounders
