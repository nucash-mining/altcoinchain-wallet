# Altcoinchain Wallet

Official desktop wallet for the Altcoinchain blockchain - a hybrid PoW/PoS cryptocurrency with smart contract support.

## Download

Download the latest release for your platform:

| Platform | Download |
|----------|----------|
| Linux (Debian/Ubuntu) | `altcoinchain-wallet_2.0.0_amd64.deb` |
| Linux (Universal) | `Altcoinchain Wallet-2.0.0.AppImage` |
| Windows | `Altcoinchain Wallet Setup 2.0.0.exe` |

## Features

- **Full Wallet Management** - Create, import, and manage multiple wallets
- **Token Support** - View and send ALT, WATT, and custom ERC20 tokens
- **NFT Gallery** - Display Mining Game NFTs and custom ERC721/ERC1155 collections
- **Address Book** - Save and manage frequently used addresses
- **Fork Countdown** - Track upcoming network upgrades (Block 7,000,000)
- **Ethstats Integration** - Connect to network statistics dashboard
- **Console** - Advanced RPC commands for power users
- **CPU Mining** - Built-in mining support

## Installation

### Linux (Debian/Ubuntu)

```bash
sudo dpkg -i altcoinchain-wallet_2.0.0_amd64.deb
```

After installation:
- Find **"Altcoinchain Wallet"** in your application menu (Finance category)
- Search for "Altcoinchain" in your app launcher
- Run from terminal: `altcoinchain-wallet`
- Right-click the icon to add to favorites/taskbar

**Enable Autostart (optional):**
```bash
mkdir -p ~/.config/autostart
cp /etc/xdg/autostart/altcoinchain-wallet.desktop ~/.config/autostart/
sed -i 's/Hidden=true/Hidden=false/' ~/.config/autostart/altcoinchain-wallet.desktop
```

### Linux (AppImage)

```bash
chmod +x "Altcoinchain Wallet-2.0.0.AppImage"
./Altcoinchain\ Wallet-2.0.0.AppImage
```

### Windows

1. Run `Altcoinchain Wallet Setup 2.0.0.exe`
2. Choose installation directory
3. Optionally enable **"Start with Windows"**
4. Click Install

The wallet will be added to:
- Desktop shortcut
- Start Menu (Altcoinchain folder)
- Apps & Features (for easy uninstall)

To pin to taskbar: Right-click the desktop shortcut and select "Pin to taskbar"

## Network Information

| Property | Value |
|----------|-------|
| Chain ID | 2330 |
| RPC Port | 8332 |
| P2P Port | 31303 |
| Block Explorer | https://scout.altcoinchain.org |
| Website | https://altcoinchain.org |

## Mining Rewards

- **Before Block 7,000,000**: 2 ALT per block (100% to miner)
- **After Block 7,000,000**: 2 ALT per block (70% miner / 30% validators)

## Building from Source

### Prerequisites

- Node.js 18+
- npm
- Electron 29+

### Build Commands

```bash
# Install dependencies
npm install

# Run in development
npm start

# Build for Linux
npm run build:linux

# Build for Windows (requires Wine on Linux)
npm run build:win

# Build all platforms
npm run build:all
```

## Data Directory

All blockchain data is stored in:
- **Linux**: `~/.altcoinchain/`
- **Windows**: `%APPDATA%\altcoinchain\`

## Troubleshooting

### Wallet shows blank/black screen
- Try disabling hardware acceleration
- Update your graphics drivers

### Node not syncing
- Check firewall allows port 31303
- Verify internet connection

### Reset wallet data
```bash
# Linux
rm -rf ~/.altcoinchain/geth

# Windows (run in PowerShell)
Remove-Item -Recurse $env:APPDATA\altcoinchain\geth
```

## License

MIT License

## Links

- **Website**: https://altcoinchain.org
- **GitHub**: https://github.com/nucash-mining/altcoinchain-wallet
- **Explorer**: https://scout.altcoinchain.org
- **Discord**: https://discord.gg/altcoinchain
