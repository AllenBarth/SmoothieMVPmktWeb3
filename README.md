# SmoothieMVPmktWeb3
This project is a decentralized application (dApp) for a smoothie recipe auction, built on a hybrid Web2/Web3 architecture. It showcases the integration of a blockchain smart contract with a secure backend and a modern frontend.
🚀 Key Features
Decentralized Auction: Recipes are minted as unique NFTs (XRC721) on the XDC Network, where an English auction manages bidding and ownership.

Trustless Automation: An auction TimeLimit and finalization process are managed by Chainlink Keepers, ensuring auctions close automatically without manual intervention.

Decentralized Storage: Private recipe data (mixing details, ingredients) is stored off-chain on IPFS via Pinata, while the on-chain NFT references the IPFS content identifier (CID).

Secure & Optimized Backend: A Vercel serverless function acts as a secure intermediary, protecting sensitive API keys from public exposure. This backend handles all AI content generation and IPFS uploads.

Real-time Data: The application fetches and displays live commodity prices and updates auction status in real-time by listening to on-chain events.

Configurable Parameters: An "Admin" card on the frontend allows the contract owner to configure the initial auction price and time limit.

⚙️ Tech Stack
Blockchain: XDC Protocol (XDCtestnet)

Smart Contracts: Solidity

Frontend: HTML, Tailwind CSS, JavaScript (Ethers.js)

Backend: Node.js (Vercel Serverless Function)

Decentralized Storage: IPFS (via Pinata)

Oracles & Automation: Chainlink (Functions & Keepers)

AI: Gemini API

Wallet: XDCpay

📦 File Structure
README.md: This file.

SmoothieAuction.sol: The Solidity smart contract.

api/create-recipe.js: The Vercel serverless function.

SmoothieMVPmktWeb3.html: The single-file frontend.

🏁 Getting Started
1. Deploy the Smart Contract
Use a tool like Remix IDE to compile and deploy SmoothieAuction.sol to the XDCtestnet. Once deployed, copy the contract address and the ABI (Application Binary Interface) JSON.

2. Configure Your Backend
This project uses a secure backend to protect API keys.

Create an account on Vercel.

Import your GitHub repository.

Go to Project Settings > Environment Variables and add the following keys:

GEMINI_API_KEY: Your API key for the Gemini model.

PINATA_API_KEY: Your API key for Pinata.

PINATA_SECRET_API_KEY: Your secret API key for Pinata.

3. Update the Frontend
Open SmoothieMVPmktWeb3.html and replace the placeholder values for the CONTRACT_ADDRESS and CONTRACT_ABI with the values you obtained in step 1.

4. Run the Application
Once your Vercel project is deployed, visit the live URL. Make sure your browser has the XDCpay wallet extension installed and is connected to the XDCtestnet. You can now create a new recipe, and the application will securely handle all on-chain and off-chain interactions.
