# Scripts Collection

A collection of useful scripts for system administration, productivity, and automation.

## Available Scripts

### 🔒 `weblock` - Website Blocker
System-wide website blocking for Arch Linux.

**Quick usage:** `weblock lock facebook.com`, `weblock list`, `weblock unlock facebook.com`

| Command | Description |
|---------|-------------|
| `weblock init` | Initialize configuration |
| `weblock lock <site> [-n]` | Block website immediately (use -n to skip adding to list) |
| `weblock block <site>` | Block website without adding to list |
| `weblock lock-all` | Block all sites in blocklist |
| `weblock unlock [site]` | Unblock website or all sites |
| `weblock list` | Show blocklist and currently blocked sites |
| `weblock remove <site> [-u]` | Remove from blocklist (use -u to also unblock) |
| `weblock reset [-f]` | Reset all configuration and unblock ALL websites |

**Requires:** sudo for blocking operations | **Config:** `~/.config/weblock/`

#### Features
- Block websites system-wide using /etc/hosts file
- Maintains a persistent blocklist
- Beautiful color-coded terminal output
- DNS cache flushing for immediate effect
- Both www and non-www versions of domains are blocked

---

## Installation

**Individual script:**
```bash
sudo cp <script-name> /usr/local/bin/
sudo chmod +x /usr/local/bin/<script-name>
```

**For weblock:**
```bash
sudo cp weblock /usr/local/bin/
sudo chmod +x /usr/local/bin/weblock
```

## Uninstallation

**For weblock:**
```bash
sudo rm /usr/local/bin/weblock
rm -rf ~/.config/weblock  # (optional, removes your configuration)
```

## Quick Reference

| Script | Purpose | Key Commands |
|--------|---------|--------------|
| `weblock` | Website blocking | `lock`, `list`, `unlock`, `remove`, `reset` |

**Get help:** All scripts support `--help` or `help` command

## Contributing

Feel free to submit issues, feature requests, or pull requests! When adding new scripts:
- Include proper documentation and help text
- Follow similar coding standards as existing scripts  
- Test thoroughly before submitting

## License

This project is open source. Feel free to modify and distribute.

## Last Updated

August 3, 2025