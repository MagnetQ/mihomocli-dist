# mihomocli

Command-line tool for managing [Mihomo](https://github.com/MetaCubeX/Mihomo) proxy service.

## Prerequisites

- [Mihomo](https://github.com/MetaCubeX/Mihomo) must be installed and running with external API enabled
- `curl` and `jq` installed on your system

> **Note:** Make sure Mihomo service is running before using this tool. Start it with:
> ```bash
> brew services start mihomo
> ```

## Install

```bash
curl -fsSL https://raw.githubusercontent.com/MagnetQ/mihomocli-dist/v1.0.2/mihomocli -o /opt/homebrew/bin/mihomocli && chmod +x /opt/homebrew/bin/mihomocli
```

## Usage

```bash
# Show help
mihomocli help

# Show current status
mihomocli status

# Switch to US (auto-selects lowest latency node)
mihomocli switch us

# Switch to Japan (auto-selects lowest latency node)
mihomocli switch jp

# Switch to Auto (URLTest - auto selects globally lowest latency)
mihomocli switch auto

# Show latency for all nodes in group
mihomocli latency us
mihomocli latency jp
mihomocli latency all

# Change mode
mihomocli mode rule
mihomocli mode global
mihomocli mode direct

# TUN mode
mihomocli tun on
mihomocli tun off

# Service control
mihomocli start
mihomocli stop
mihomocli restart

# Show current node
mihomocli node
```

## License

MIT