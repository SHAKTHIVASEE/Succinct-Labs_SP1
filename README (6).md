# SP1-Proof
![sp1](https://github.com/user-attachments/assets/54dc9640-b3a6-4e3f-aa95-05332e7c42ef)
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
<img width="614" alt="Screenshot 2024-08-09 at 11 59 46 AM" src="https://github.com/user-attachments/assets/02abfdf1-76d6-4541-8b58-75b590126138">

2. execut the program with proof
   ```
   RUST_LOG=info cargo run --release -- --prove
   ```
   <img width="866" alt="Screenshot 2024-08-09 at 12 02 45 PM" src="https://github.com/user-attachments/assets/59699bfc-1f7c-42d9-a9a2-240c37b01530">

