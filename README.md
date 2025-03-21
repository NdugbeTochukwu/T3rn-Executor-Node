# T3rn-Executor-Node

---

## Minimum Hardware Requirements

- **CPU:** 4-core CPU or equivalent
- **Architecture:** x86-64 (also known as x64, x86_64, AMD64, and Intel 64)
- **RAM:** 6 GB of RAM
- **Operating System:** Ubuntu 22.04.2 LTS or later (x86-64 compatible)
- **Storage:** 400 GB

---


# Updates and Installation 🫡
To set up your Executor Node, run the following commands in your terminal:

```bash
sudo apt upgrade
sudo apt install screen
sudo apt-get update

```


# Create Screen & continue

```bash
screen -S t3rn
sudo apt install tmux -y
tmux new -s t3rn

```

## Install T3rn
```
cd $HOME
wget https://github.com/t3rn/executor-release/releases/download/v0.56.0/executor-linux-v0.56.0.tar.gz
```
Verify the SHA256 checksum
```
wget https://github.com/t3rn/executor-release/releases/download/v0.56.0/executor-linux-v0.56.0.tar.gz.sha256sum
```
```
tar -xvzf executor-linux-v0.56.0.tar.gz
```
```
cd executor/executor/bin
```

# Configuring settings and variables
To configure the settings, paste the following codes one after the other

Make sure you have eth balances on all the chains about 5-10eth each

```bash
export NODE_ENVIRONMENT=testnet
export LOG_LEVEL=debug
export LOG_PRETTY=false
export EXECUTOR_PROCESS_BIDS_ENABLED=true
export EXECUTOR_PROCESS_ORDERS_ENABLED=true
export EXECUTOR_PROCESS_CLAIMS_ENABLED=true
export ENABLED_NETWORKS='arbitrum-sepolia,base-sepolia,unichain-sepolia,optimism-sepolia,l1rn'
export RPC_ENDPOINTS='{
    "l2rn": ["https://b2n.rpc.caldera.xyz/http"],
    "arbt": ["https://arbitrum-sepolia.drpc.org", "https://sepolia-rollup.arbitrum.io/rpc"],
    "bast": ["https://base-sepolia-rpc.publicnode.com", "https://base-sepolia.drpc.org"],
    "opst": ["https://sepolia.optimism.io", "https://optimism-sepolia.drpc.org"],
    "unit": ["https://unichain-sepolia.drpc.org", "https://sepolia.unichain.org"]
}'
export EXECUTOR_ENABLE_BATCH_BIDING=true
export EXECUTOR_MAX_L3_GAS_PRICE=1000
export PRIVATE_KEY_LOCAL="your private key"
export EXECUTOR_PROCESS_PENDING_ORDERS_FROM_API=false
```

## Run T3rn Node
```
./executor
```
