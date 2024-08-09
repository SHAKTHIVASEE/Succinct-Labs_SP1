# SP1-Proof

SP1 is a performant, open-source zero-knowledge virtual machine (zkVM) that verifies the execution of arbitrary Rust (or any LLVM-compiled language) programs.

## Genrating ZK Proof with Succinct SP1

### Install dependencies
``` 
sudo apt update && sudo apt upgrade -y
sudo apt install cmake pkg-config libssl-dev build-essential -y

# install Rust
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source "$HOME/.cargo/env"

# install SP1
curl -L https://sp1.succinct.xyz | bash
source /root/.bashrc
sp1up

# check version
cargo +succinct --version
```

### Create an SP1 Project
```
cargo prove new fibonacci
cd fibonacci/script
```
1. execute the program without proof
   ```
   RUST_LOG=info cargo run --release -- --execute
   ```

2. execut the program with proof
   ```
   RUST_LOG=info cargo run --release -- --prove
   ```
 
