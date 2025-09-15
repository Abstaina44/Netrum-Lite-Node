# ⚡ Netrum Lite Node – Quick Setup Guide

Netrum Lite Node CLI is a **lightweight command-line tool** to join the Netrum decentralized compute network.  
With it, you can:  
✅ Create or import wallets  
✅ Register your node  
✅ Sync uptime & heartbeat data  
✅ Mine NPT tokens  
✅ Claim rewards directly from your terminal  

---

## 📋 Prerequisites

### Minimum Requirements

| Component | Minimum      | Recommended   |
|-----------|-------------|---------------|
| CPU       | 2 Cores     | 2+ Cores      |
| RAM       | 4 GB        | 6 GB+         |
| Disk      | 50 GB SSD   | 100 GB SSD    |
| Network   | 10 Mbps     | Stable high-speed |

### Software Requirements
- Ubuntu 20.04/22.04 (Linux VPS or WSL on local machine)  
- Node.js v20 (required)  
- npm (bundled with Node.js)  

---

## ⚡ Installation

### 1. Clone Repository  
➡ **On VPS**
```bash
git clone https://github.com/NetrumLabs/netrum-lite-node.git
cd netrum-lite-node 

➡ On Local PC (WSL)
⚠ Install inside ~ (home directory), not in /mnt/c/ (to avoid permission & speed issues).
cd ~
git clone https://github.com/NetrumLabs/netrum-lite-node.git
cd netrum-lite-node 

2. Install Dependencies
sudo apt update && sudo apt install -y curl bc jq speedtest-cli nodejs npm 

3. Install Node.js v20 (if needed)
node -v    # check version
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt install -y nodejs 

4. Install Project Dependencies
npm install 

5. Link CLI Globally
npm link
6. Test CLI
netrum
Expected output:
Netrum CLI  Version v2.0.0
Light-weight node & wallet toolkit for the Netrum network.
🚀 Step-by-Step Usage
⚠️ Always back up your private keys before starting.
1️⃣ Import or Create Wallet
netrum-import-wallet   # paste your private key
# OR
netrum-new-wallet      # generate new wallet
2️⃣ Check Base Name
netrum-check-basename
💡 Example output:
✅ Your Base name: mynode.base
3️⃣ Check Node ID
netrum-node-id
4️⃣ Sign Node ID
netrum-node-sign
5️⃣ Register Node
netrum-node-register
💡 Requires ~0.0002–0.0005 BASE gas.
6️⃣ Sync Node
netrum-sync
Check logs:
netrum-sync-log
7️⃣ Start Mining
netrum-mining
Logs:
netrum-mining-log
Alternative log:
journalctl -u netrum-node.service -f -n 100 --no-pager
💡 Earns NPT based on uptime.
8️⃣ Claim Rewards
netrum-claim
💡 Claim after ~24h mining (Gas: 0.00002–0.00003 BASE).
9️⃣ Check Wallet & Balance
netrum-wallet
Wallet management:
netrum-wallet-key
netrum-wallet-remove
⚡ Quick Commands Cheat Sheet
Step	Command	Purpose
1	netrum-import-wallet / netrum-new-wallet	Import or create wallet
2	netrum-check-basename	Check Base domain name
3	netrum-node-id	Show Node ID
4	netrum-node-sign	Sign Node ID
5	netrum-node-register	Register node on-chain
6	netrum-sync	Start syncing
–	netrum-sync-log	View sync logs
7	netrum-mining	Start mining
–	netrum-mining-log	View mining logs
8	netrum-claim	Claim rewards
9	netrum-wallet	Check wallet & balance
📞 Support
Need help? Join the Official Netrum Discord to get support.

