# genpass

A simple, secure password generator with logging and usage tracking.

This script generates secure passwords using `pwgen`, copies them to the clipboard, and logs usage per day. It produces monthly usage reports in both Markdown and HTML formats.

## 🔐 Features

- Generates secure, readable passwords (`pwgen -c -n -y -s -B 17 1`)
- Automatically copies password to clipboard
- Logs each usage with timestamp
- Generates monthly stats:
  - `~/genpass-usage/YYYY-MM.md`
  - `~/genpass-usage/YYYY-MM.html`

## 🚀 Installation

```bash
mkdir -p ~/bin
cp genpass ~/bin/genpass
chmod +x ~/bin/genpass
```

Make sure `~/bin` is in your `$PATH`.

## 🧪 Usage

```bash
genpass             # Generate password and update logs
genpass --stats     # Stats for current month
genpass --stats 2025-07    # Stats for specific month
genpass --html      # HTML for current month
genpass --html 2025-07     # HTML for specific month
genpass --help      # Help
```

Alias suggestion:

```bash
alias czam="$HOME/bin/genpass"
```

## 📋 Requirements

- `pwgen` for password generation
- `xclip` or `wl-copy` for clipboard support

Install via:

```bash
sudo apt install pwgen xclip
```

## 📁 Output

Stats and logs are stored in:

```
~/genpass-usage/
├── genpass.log
├── 2025-08.md
└── 2025-08.html
```

## 📄 License

MIT (or your preferred license)
