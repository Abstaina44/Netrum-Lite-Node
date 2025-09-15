Perfect 👌 — here’s an upgraded **professional `README.md`** with badges at the top. If you copy this whole thing into `README.md` in VSCode, you’ll see the markdown styling locally **and** it’ll look great on GitHub.

````markdown
# 🚀 Netrum Lite Node – Quick Setup Guide  

![Node.js](https://img.shields.io/badge/Node.js-v20-green?logo=node.js)  
![npm](https://img.shields.io/badge/npm-latest-red?logo=npm)  
![Ubuntu](https://img.shields.io/badge/Ubuntu-20.04%20%7C%2022.04-orange?logo=ubuntu)  
[![Discord](https://img.shields.io/badge/Discord-Join%20Community-blue?logo=discord)](https://discord.gg/)

---

**Netrum Lite Node CLI** is a lightweight tool to join the **Netrum decentralized compute network** — create/import wallets, register your node, sync, mine, and claim rewards all from your terminal.  

---

## 📋 Prerequisites  

### Minimum Requirements  

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| CPU       | 2 Cores | 2+ Cores   |
| RAM       | 4 GB    | 6 GB+      |
| Disk      | 50 GB SSD | 100 GB SSD |
| Network   | 10 Mbps up/down | Stable high-speed |

### Software Requirements  
- Ubuntu **20.04/22.04** (Linux VPS or WSL local machine)  
- Node.js **v20** (required)  
- npm (bundled with Node.js)  

---

## ⚡ Installation  

### 1. Clone Repository  

**VPS**  
```bash
git clone https://github.com/NetrumLabs/netrum-lite-node.git
cd netrum-lite-node
````

**Local PC (WSL)**
⚠ Install inside your Linux home directory (`~`), not `/mnt/c/` (avoids permission & speed issues).

```bash
cd ~
git clone https://github.com/NetrumLabs/netrum-lite-node.git
cd netrum-lite-node
```

### 2. Install Dependencies

```bash
sudo apt update && sudo apt install -y curl bc jq speedtest-cli nodejs npm
```

### 3. Install Node.js v20 (if needed)

```bash
node -v    # check version
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt install -y nodejs
```

### 4. Install Project Dependencies

```bash
npm install
```

### 5. Link CLI Globally

```bash
npm link
```

### 6. Test CLI

```bash
netrum
```

Expected output:

```
Netrum CLI  Version v2.0.0
Light-weight node & wallet toolkit for the Netrum network.
```

---

## 🚀 Step-by-Step Usage

⚠️ Always **back up your private keys** before starting.

### 1️⃣ Import or Create Wallet

```bash
netrum-import-wallet   # paste your private key
# OR
netrum-new-wallet      # generate new wallet
```

### 2️⃣ Check Base Name

```bash
netrum-check-basename
```

Example:

```
✅ Your Base name: mynode.base
```

### 3️⃣ Check Node ID

```bash
netrum-node-id
```

### 4️⃣ Sign Node ID

```bash
netrum-node-sign
```

### 5️⃣ Register Node

```bash
netrum-node-register
```

💡 Requires \~0.0002–0.0005 BASE gas.

### 6️⃣ Sync Node

```bash
netrum-sync
```

Logs:

```bash
netrum-sync-log
```

### 7️⃣ Start Mining

```bash
netrum-mining
```

Logs:

```bash
netrum-mining-log
# or alternative
journalctl -u netrum-node.service -f -n 100 --no-pager
```

💡 Earns **NPT** based on uptime.

### 8️⃣ Claim Rewards

```bash
netrum-claim
```

💡 Claim after \~24h mining. Gas: **0.00002–0.00003 BASE**.

### 9️⃣ Check Wallet & Balance

```bash
netrum-wallet
```

Wallet management:

```bash
netrum-wallet-key
netrum-wallet-remove
```

---

## ⚡ Quick Commands Cheat Sheet

| Step | Command                                      | Purpose                 |
| ---- | -------------------------------------------- | ----------------------- |
| 1    | `netrum-import-wallet` / `netrum-new-wallet` | Import or create wallet |
| 2    | `netrum-check-basename`                      | Check Base domain name  |
| 3    | `netrum-node-id`                             | Show Node ID            |
| 4    | `netrum-node-sign`                           | Sign Node ID            |
| 5    | `netrum-node-register`                       | Register node on-chain  |
| 6    | `netrum-sync`                                | Start syncing           |
| –    | `netrum-sync-log`                            | View sync logs          |
| 7    | `netrum-mining`                              | Start mining            |
| –    | `netrum-mining-log`                          | View mining logs        |
| 8    | `netrum-claim`                               | Claim rewards           |
| 9    | `netrum-wallet`                              | Check wallet & balance  |

---

## 📞 Support

Need help? 👉 [Join the Official Netrum Discord](https://discord.gg/)

---

```

Would you like me to also add a **diagram/flowchart of the process (wallet → register → sync → mine → claim)** in the README so contributors see the lifecycle visually?
```
