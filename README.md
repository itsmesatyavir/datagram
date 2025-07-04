# 📡 Datagram Node - CLI Version (Linux Setup Guide)

This guide helps you install and run the official **Datagram Node CLI** on any Linux system (Ubuntu/Debian). No coding knowledge needed — just follow the steps below.

---

## 📦 Requirements

- Linux VPS or Server (Ubuntu 20.04+ recommended)
- Basic terminal access (SSH)
- Your **Datagram API key** (from: https://dashboard.datagram.network/?ref=206244961)

---

## ⚙️ Step-by-Step Installation

### 1️⃣ Update your system
```bash
sudo apt update && sudo apt upgrade -y
```

### 2️⃣ Install necessary packages
```bash
sudo apt install wget screen -y
```

### 3️⃣ Create working directory
```bash
mkdir ~/datagram
cd ~/datagram
```

### 4️⃣ Download the latest CLI binary
```bash
wget -O datagram-cli https://github.com/Datagram-Group/datagram-cli-release/releases/latest/download/datagram-cli-x86_64-linux
```

### 5️⃣ Make the binary executable
```bash
chmod +x datagram-cli
```

### 6️⃣ Create the required temp directory
```bash
sudo mkdir -p /home/datagram/tmp
sudo chmod -R 777 /home/datagram
```

---

## 🚀 Run the Node

### 7️⃣ Start a screen session
```bash
screen -S datagram
```

### 8️⃣ Run the CLI node (replace with your API key)
```bash
./datagram-cli run -- -key YOUR_API_KEY
```

> 🔐 Example:
```bash
./datagram-cli run -- -key 5abf0f02b6410330781d73a17d7e7e30
```

### 9️⃣ Detach screen to keep node running in background
```text
Press: Ctrl + A, then press D
```

### 🔁 To reconnect later:
```bash
screen -r datagram
```

---

## 📘 Extra Tips

- Want auto-start on reboot? Ask in issues or community.
- Your node runs continuously unless stopped or server is rebooted.
- You can run multiple nodes using different keys and folders.

---

## 🙋 Need Help?

- 🧑‍💻 Author Telegram: [@itsmesatyavir](https://t.me/itsmesatyavir)
- 📬 Telegram Community: [t.me/datagramxyz](https://t.me/datagramxyz)
- 🌐 Website: [https://datagram.xyz](https://datagram.xyz)
- 📖 Docs: [https://docs.datagram.xyz](https://docs.datagram.xyz)

---

## 🛡️ Disclaimer

This software is maintained by the Datagram team. Use responsibly and never share your private API key publicly.
