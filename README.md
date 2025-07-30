# Pipe-Firestarter-Storage
Installation and Usage Flow This runs on Solana DevNet and uses DevNet SOL. — DO NOT USE MAINNET SOL.


## Use Codespace
- Go to: https://github.com/codespaces

1. Install Prerequisites
```
sudo apt update && sudo apt install -y \
  build-essential \
  pkg-config \
  libssl-dev \
  git \
  curl
```

2. 2. Install Rust (for building from source)
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source "$HOME/.cargo/env"
```

3. Install pipe CLI
```
git clone https://github.com/PipeNetwork/pipe.git
cd pipe
```
```
cargo install --path .
```
- Create path 
```
echo 'export PATH="$HOME/.cargo/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

4. Create a User
```
pipe new-user <your_username_here>
```
- Check your credentials:
```
cat ~/.pipe-cli.json
```
## Fund with DevNet SOL
- Go to 👉 https://faucet.solana.com
- Connect github 
- Paste your Solana DevNet wallet address you generate 

 5. Swap SOL for PIPE Tokens
```
pipe swap-sol-for-pipe 0.5
```
- Check balances:
```
pipe check-sol
pipe check-token
```
6. Upload & Download Files
```
echo "Hello Pipe!" > photo.jpg
```
- Then run:
```
pipe upload-file photo.jpg my-photo
```
- Download file:
```
pipe download-file my-photo photo-downloaded.jpg
```

## Token Usage Report
```
pipe token-usage --period 30d --detailed
```
- Expected Output:
<img width="689" height="287" alt="image" src="https://github.com/user-attachments/assets/2f72617b-3177-4479-ba1e-e16f19c864e8" />





























