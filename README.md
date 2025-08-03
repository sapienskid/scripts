# Scripts Collection

A collection of useful scripts for system administration, productivity, and automation.

## Scripts Available

### 🔒 WeBlock - Website Blocker

A powerful, easy-to-use command-line tool for blocking distracting websites system-wide. Perfect for improving focus and productivity by eliminating digital distractions.

#### Features
- ✅ **System-wide blocking** - Works across all browsers and applications
- 🕐 **Timer functionality** - Block sites for a specific duration
- 📝 **Flexible blocklists** - Temporary and permanent blocking lists
- 🎯 **Individual site control** - Block/unblock specific websites instantly
- 🎨 **Colorful CLI interface** - Easy-to-read colored output
- 📊 **Activity logging** - Track your blocking activity
- 🔧 **Easy configuration** - Simple text-based configuration files
- 📦 **Single file** - Everything contained in one script

#### Quick Start

```bash
# Install WeBlock
sudo cp weblock /usr/local/bin/
sudo chmod +x /usr/local/bin/weblock

# Initialize configuration
weblock init

# Lock a website immediately
sudo weblock lock facebook.com

# Start a 2-hour focus session with all websites in blocklist
sudo weblock timer 2h

# Check status
weblock list
```

#### Installation
```bash
sudo cp weblock /usr/local/bin/
sudo chmod +x /usr/local/bin/weblock
```

#### Basic Commands

| Command | Description | Example |
|---------|-------------|---------|
| `weblock init` | Initialize WeBlock configuration | `weblock init` |
| `weblock lock <site>` | Lock (block) specific website | `weblock lock facebook.com` |
| `weblock lock-all` | Lock all websites from blocklist | `sudo weblock lock-all` |
| `weblock unlock [site]` | Unlock specific website or all | `sudo weblock unlock facebook.com` |
| `weblock remove <site>` | Remove site from blocklist | `weblock remove facebook.com` |
| `weblock list` | Show all blocklists and status | `weblock list` |

#### Timer Commands

| Command | Description | Example |
|---------|-------------|---------|
| `weblock timer <duration> [site]` | Lock websites for specified time | `sudo weblock timer 30m` |
| `weblock status` | Check timer status | `weblock status` |
| `weblock stop [site]` | Stop active timers | `sudo weblock stop` |

**Duration formats:** `30s`, `15m`, `2h`, `1d`

#### Example Usage
```bash
# Focus session workflow
weblock lock facebook.com
weblock lock twitter.com
sudo weblock timer 2h                    # Block for 2 hours

# Quick lock/unlock
sudo weblock lock facebook.com           # Lock immediately
sudo weblock unlock facebook.com         # Unlock later

# Permanent security blocks
weblock lock malware-site.com --permanent
```

#### Configuration
WeBlock stores configuration in `~/.config/weblock/`:
- `blocklist.txt` - Temporary websites to block
- `permanent_blocklist.txt` - Permanently blocked websites
- `weblock.log` - Activity log

#### Requirements
- **Linux** (systemd-based distributions)
- **Root access** (sudo) for blocking/unblocking operations

---

## Installation

### Individual Scripts
```bash
sudo cp <script-name> /usr/local/bin/
sudo chmod +x /usr/local/bin/<script-name>
```

### All Scripts
```bash
# Copy all scripts to system PATH
for script in *; do
    if [[ -f "$script" && -x "$script" ]]; then
        sudo cp "$script" /usr/local/bin/
    fi
done
```

## Contributing

Feel free to submit issues, feature requests, or pull requests! When adding new scripts:

1. Include proper documentation and help text
2. Follow similar coding standards as existing scripts
3. Test thoroughly before submitting

## License

This project is open source. Feel free to modify and distribute.
