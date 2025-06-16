BuilderPayMCP – Empower Builders, Directly
BuilderPayMCP is a donation platform built to support builders directly on the Celo blockchain. No scores, no badges — just direct support from individuals or organizations to builders they believe in. Now integrated with Self.xyz (DID/identity on Ceramic) for decentralized identity and profile sharing.
Features
- Explore builders and their projects
- Send donations directly to a builder’s wallet (Celo / cUSD)
- Builders can authenticate and manage their identity via Self.xyz
- Fully open-source React + Express app
Tech Stack
Frontend: React, Tailwind CSS
Backend: Node.js, Express
Identity: Self.xyz (Ceramic, 3ID)
Wallets: MetaMask, Valora (Celo)
Storage: JSON data (easily extendable)
Local Development
1. Clone and Setup
git clone https://github.com/cryptochitty/builderpaymcp.git
cd builderpaymcp
2. Run Backend
cd backend
npm install
node server.js
3. Run Frontend
cd ../frontend
npm install
npm start
Self.xyz (Ceramic) Identity Integration
What it does
- Connects builder’s Ethereum wallet to DID (Decentralized ID)
- Fetches & sets builder profile (name, description, emoji)
- No backend storage needed — identity is decentralized
How to Use
1. Click “Connect with Self.xyz” on the homepage
2. Sign with MetaMask / Valora
3. Builder info is fetched/set on Ceramic
4. Profile appears with name, bio, and emoji
Folder Structure
builderpaymcp/
├── frontend/
│   ├── src/
│   │   ├── App.js
│   │   ├── pages/
│   │   │   ├── Home.js
│   │   │   └── BuilderProfile.js
│   │   ├── components/
│   │   │   ├── BuilderCard.js
│   │   │   └── SelfConnect.js
│   └── package.json
└── backend/
    ├── server.js
    ├── routes/
    │   └── builders.js
    ├── data/
    │   └── builders.json
    └── package.json
Self.xyz Developer Notes
- App must be run on HTTPS (Ceramic mainnet requires secure context)
- Recommended: Self.ID Docs (https://developers.ceramic.network/build/self-id/overview/)
- You may extend SelfConnect.js for:
  • Profile editing
  • Linking to builder dashboard
  • On-chain proof storage
Contributing
Want to list yourself as a builder?
- Fork the repo
- Add yourself to backend/data/builders.json
- Or build DID-based onboarding
Roadmap
- [x] Self.xyz DID profile integration
- [ ] Smart contract donations (Celo + ReFi tokens)
- [ ] Decentralized builder registry
- [ ] Reputation / trust via attestations
License
MIT — free to build and fork.
