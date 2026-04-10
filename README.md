# GigVault — Decentralized Escrow & Gig Economy on Stellar

![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)
![Stellar](https://img.shields.io/badge/Built_on-Stellar-black.svg?logo=stellar)
![Soroban](https://img.shields.io/badge/Smart_Contracts-Soroban-orange.svg)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)

GigVault is a decentralized, milestone-based escrow and payment streaming protocol built on the Stellar network. It empowers freelancers, contractors, and clients to transact safely without high-fee intermediaries. Funds are locked in Soroban smart contracts and programmatically released as project milestones are achieved, with a built-in multi-sig dispute resolution mechanism.

## ✨ Key Features

* **Self-Custodial Escrow:** Client funds are locked safely on-chain using Soroban smart contracts.
* **Milestone Payouts:** Freelancers receive payouts instantly as portions of the work are verified.
* **Multi-Token Support:** Transact natively in XLM, USDC, or any Stellar asset.
* **DAO Dispute Resolution:** Built-in multi-sig voting for resolving contract disputes fairly.
* **Transparent History:** Fully auditable on-chain history of all agreements and payouts.

## 🏗️ Architecture

GigVault uses a modular architecture for security, scalability, and developer experience.

| Layer | Technology |
| --- | --- |
| **Blockchain** | Stellar Network |
| **Smart Contracts** | Rust (Stellar Soroban) |
| **Frontend** | Next.js 14, React, TypeScript, Tailwind CSS |
| **Wallet Integration**| Freighter (Stellar) |
| **Backend / Indexer** | Node.js, Express, PostgreSQL |

## 🚀 Quick Start

### Prerequisites
* [Node.js](https://nodejs.org/en/) (v18 or higher)
* [Rust & Cargo](https://rustup.rs/) (v1.79+)
* [Stellar CLI](https://developers.stellar.org/docs/build/smart-contracts/getting-started/setup)
* Docker & Docker Compose (Recommended)

### Local Development Setup

**1. Clone the repository:**
```bash
git clone https://github.com/yourusername/GigVault.git
cd GigVault
```

**2. Install Monorepo Dependencies:**
```bash
npm install
```

**3. Configure Environment Variables:**
```bash
cp backend/.env.example backend/.env
cp frontend/.env.example frontend/.env
```

**4. Start the Application:**
We use npm workspaces to manage the monorepo.
```bash
# Start the Next.js frontend (Runs on port 3000)
npm run dev:frontend

# Start the Node.js backend (Runs on port 3001)
npm run dev:backend
```

### Smart Contract Development

To build and test the Soroban contracts, you need to navigate into each specific contract directory.

**1. Build and test the Escrow Contract:**
```bash
cd contracts/escrow_contract
cargo build --target wasm32v1-none --release
cargo test
```

**2. Build and test the Dispute Registry Contract:**
```bash
# Go back to the root contracts folder, then into dispute_registry
cd ../dispute_registry
cargo build --target wasm32v1-none --release
cargo test
```

## 📂 Project Structure

```text
gigvault/
├── contracts/               # Soroban smart contracts (Rust)
│   ├── escrow_contract/     # Core locking and releasing logic
│   └── dispute_registry/    # Arbitrator/DAO voting logic
├── frontend/                # Next.js web application (TypeScript)
│   ├── src/components/      # UI components (Tailwind)
│   └── src/hooks/           # Custom hooks for Freighter wallet
├── backend/                 # Node.js API (TypeScript)
│   ├── src/routes/          # API endpoints for metadata
│   └── src/indexer/         # Listens to Soroban events
└── docs/                    # Architecture diagrams and APIs
```

## 🤝 Contributing

We welcome contributions from developers of all skill levels. 

Please see our [CONTRIBUTING.md](./CONTRIBUTING.md) for detailed guidelines on how to get started, claim issues, and contribute.

## 📄 License

This project is licensed under the Apache License 2.0 - see the [LICENSE](./LICENSE) file for details.
