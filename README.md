# mRLs - Mini PHP Shell

mRLs v1.0 PHP-based shell terminal emulator with file management and reverse shell capabilities.

## Quick Start

```bash
php -S localhost:8000
# Open http://localhost:8000/mrls.php
# Default password: mRLs
```

## Commands

| Command                      | Description           |
|------------------------------|-----------------------|
| `cd <dir>`                   | Change directory      |
| `ls`                         | List files            |
| `cat <file>`                 | View file contents    |
| `download <file>`            | Download file         |
| `upload <path>`              | Upload file           |
| `reverse <IP> [LANG] [PORT]` | Create reverse shell  |
| `pwd`, `history`, `env`      | System info           |
| `help`                       | Show all commands     |

## Disclaimer

**This tool is intended for authorized, legitimate server administration purposes only.**

- Any use of this tool for unauthorized access, intrusion, or malicious activities is **illegal** and punishable by law.
- The developer(s) assume **no liability** for misuse, damage, or legal consequences.
- By using this tool, you confirm that you have **explicit authorization** from the server owner.
- This tool must not be used on any system without prior written consent.

**Your actions are your own responsibility.**

---

## Features

- Shell command execution
- File upload/download
- Tab completion
- Command history
- Variables & aliases
- Reverse shell payloads (PHP, Python, Perl, Ruby, Bash, Netcat)
- Encoding support for payloads

## Info Display

On connect, displays:
- Server IP & Hostname
- Web Server & OS
- User info (UID/GID)
- Available languages & versions
- Disabled PHP functions
