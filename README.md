# 🎲 Foundry Smart Contract Lottery

A decentralized lottery smart contract built with **Solidity** and **Foundry**, powered by:

- 🔐 Chainlink VRF v2.5 (Verifiable Randomness)
- 🤖 Chainlink Automation (Keepers)
- 🧪 Unit Testing
- 🔁 Fuzz Testing

The contract automatically selects a provably random winner after a fixed time interval.

---

## 🚀 Features

- Users can enter the raffle by paying an entrance fee
- Automated winner selection using Chainlink Automation
- Provably random winner using Chainlink VRF
- Secure state machine (OPEN → CALCULATING → OPEN)
- Fully tested with Foundry
- Fuzz testing included
- Deployment & interaction scripts included

---

## 🛠 Tech Stack

- Solidity ^0.8.x
- Foundry
- Chainlink VRF v2.5
- Chainlink Automation
- Sepolia Testnet

---

## 📂 Project Structure
foundry-smart-contract-lottery/
│
├── src/ # Smart contracts
├── script/ # Deployment & interaction scripts
├── test/ # Unit & fuzz tests
├── foundry.toml # Foundry config
├── .gitignore
└── README.md

---

# ⚙️ Installation

## 1️⃣ Install Foundry

If you don’t have Foundry installed:

```bash
curl -L https://foundry.paradigm.xyz | bash
source ~/.bashrc
foundryup
```

2️⃣ Clone the Repository
git clone https://github.com/vedantghate18/foundry-smart-contract-lottery.git

3️⃣ Install Dependencies
forge install

🔐 How It Works

1. Users enter the raffle by sending ETH.

2. After a fixed interval, Chainlink Automation triggers performUpkeep.

3. Chainlink VRF requests randomness.

4. A random winner is selected.

5. The winner receives the contract balance.

6. The raffle resets.

🧠 Security Features

- Custom errors (gas optimized)

- Strict state management

- Prevents entry during CALCULATING phase

- Validates upkeep before execution

- Ensures valid VRF request before fulfillment

📚 What This Project Demonstrates

- Smart contract architecture

- Chainlink VRF integration

- Automation integration

- Foundry testing framework

- Fuzz testing

- Deployment scripting

- Proper Git project structure

📜 License

MIT

👨‍💻 Author

Vedant Ghate
