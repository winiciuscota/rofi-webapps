# rofi-webapps

A Rofi-based interface for managing web applications as desktop entries — with icon search, CRUD operations, and isolated profile support.

## Features

- 🚀 **Quick Launch** — Browse and open web apps with fuzzy search
- ➕ **Easy Creation** — Create new web apps with just a name and URL
- ✏️ **Full Edit Support** — Edit name, URL, and isolated mode
- 🎨 **Icon Search** — Search and download icons from DuckDuckGo with live preview
- 📄 **Pagination** — Browse through unlimited icon results
- 🔔 **Visual Feedback** — Progress notifications for long operations
- 🔒 **Isolated Profiles** — Support for isolated browser profiles
- ⚡ **Fast Downloads** — Parallel icon downloads for speed

## Dependencies

- Python 3.6+
- rofi (with icon support)
- libnotify (`notify-send`)
- Standard Python libraries: `urllib`, `json`, `subprocess`, `concurrent.futures`

## Installation

### Arch Linux (from PKGBUILD)

```bash
git clone https://github.com/winiciuscota/rofi-webapps.git
cd rofi-webapps
makepkg -si
```

### Manual Installation

```bash
git clone https://github.com/winiciuscota/rofi-webapps.git
cd rofi-webapps
sudo install -Dm755 rofi-webapps /usr/bin/rofi-webapps
sudo install -Dm755 webapps-backend /usr/lib/rofi-webapps/webapps-backend
```

## Usage

```bash
rofi-webapps
```

### Actions

| Action | Description |
|--------|-------------|
| **Create Webapp** | Enter a name and optional URL to create a new desktop entry |
| **Open** | Launch the selected web app |
| **Delete** | Remove the web app |
| **Edit** | Update name or URL |
| **Change Icon** | Search DuckDuckGo for icons and pick one interactively |

## How it Works

Web apps are stored as `.desktop` files under `~/.local/share/applications/` with a `webapp-` prefix. The backend (`webapps-backend`) handles creation, deletion, and listing. The frontend (`rofi-webapps`) provides a rofi-powered UI with icon support.

## License

MIT
