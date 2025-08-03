# Paylis - Decentralized Payments for Lisk

Paylis is a non-custodial payment gateway that allows online merchants to seamlessly accept cryptocurrency payments on the Lisk blockchain. Our primary goal is to simplify the crypto payment experience for both merchants and their customers, driving adoption of the Lisk ecosystem in real-world commerce.

![Project Screenshot](https://)

## 🎥 Live Demo & Pitch Deck

- **Demo Video:** [Watch on YouTube](https://[YOUR_YOUTUBE_DEMO_URL_HERE])
- **Pitch Deck:** [View on Google Drive](https://[YOUR_PITCH_DECK_URL_HERE])

## 🚀 Submission Links

| Item                  | Link                                                                       |
| --------------------- | -------------------------------------------------------------------------- |
| **Live Project URL**  | [https://paylis.app](https://[YOUR_LIVE_PROJECT_URL_HERE])                 |
| **Smart Contract**    | [View on Lisk Sepolia Blockscout](https://[YOUR_LISK_BLOCKSCOUT_URL_HERE]) |
| **Public Repository** | [View on GitHub](https://github.com/fahmi/Project/paylis)                  |

---

## 🎯 Judging Criteria Breakdown

### 1. DApp Use Case & Impact towards the Lisk Ecosystem (30/100)

Paylis is designed to directly address the challenge of bringing real-world utility and transaction volume to the Lisk ecosystem.

- **Onboarding Mainstream Merchants:** Our flagship integration is a **WordPress plugin**. With WordPress powering over 43% of all websites, Paylis provides an immediate and accessible way for a massive market of e-commerce stores to start accepting LSK and Lisk-based tokens.
- **Increasing Network Activity:** By simplifying crypto payments, we lower the barrier for everyday transactions, from buying a coffee to paying for digital goods. This directly translates to increased, sustained transaction volume on the Lisk network.
- **User Acquisition:** We introduce a new wave of non-crypto-native users (both merchants and customers) to the Lisk ecosystem through a familiar e-commerce interface, fostering organic growth.

### 2. Innovation & Uniqueness (20/100)

Paylis differentiates itself through a focus on user experience, abstracting away blockchain complexities.

- **Gasless Transactions:** We utilize a `PaymentForwarder` smart contract and a relayer system. This allows customers to pay for goods using stablecoins without needing to hold Lisk's native token for gas fees. The relayer covers the gas, and the merchant can sponsor this cost, creating a frictionless "one-click" payment experience similar to Web2.
- **Non-Custodial by Design:** Unlike many crypto payment processors, Paylis is completely non-custodial. Funds are sent directly from the customer to the merchant's wallet via our smart contract, ensuring full self-sovereignty.
- **E-commerce First:** Our architecture is built from the ground up for e-commerce, with deep integration into platforms like WordPress/WooCommerce, rather than being a generic crypto wallet.

### 3. Technical Implementation (20/100)

Paylis is a full-stack dApp composed of three core components:

- **Smart Contracts (`/contract`):**
  - Written in **Solidity** and built with **Foundry**.
  - The core contract, `PaymentForwarder.sol`, is an Ownable, Pausable, and Reentrancy-guarded contract that securely forwards payments to the merchant's address.
  - Deployed and verified on **Lisk Sepolia Testnet**.

- **Web Application (`/apps`):**
  - A modern frontend built with **React**, **Vite**, and **TypeScript**.
  - Provides a dashboard for merchants to track transactions, manage their profile, and generate API keys.
  - Handles the customer-facing payment modal.
  - The backend logic for our relayer service is built with **Node.js**, handling the meta-transactions for the gasless payment feature.

- **WordPress Plugin (`/wp-plugin`):**
  - A standard **PHP-based** plugin that integrates Paylis as a payment gateway for **WooCommerce**.
  - Allows for simple, no-code setup for merchants already on the WordPress platform.

### 4. UI/UX & Usability (10/100)

Simplicity is our core design principle.

- **For Merchants:** A simple onboarding process, an intuitive dashboard to view payment history, and a one-time setup via the WordPress plugin.
- **For Customers:** A clean, familiar checkout process. The "gasless" feature means they only need to approve the token transfer, without worrying about network fees, significantly reducing friction and cart abandonment.

### 5. Project Documentation & Code Quality (10/100)

- **Code Quality:** The codebase is organized into modular components (`contract`, `apps`, `wp-plugin`) with clear separation of concerns. We follow industry-standard practices for each stack (e.g., ESLint/Prettier for frontend, Forge formatting for Solidity).
- **Documentation:** This `README.md` serves as the central hub for understanding the project. The code itself is commented where logic is complex.

### 6. Pitch & Presentation Quality (10/100)

Our pitch deck and demo video clearly articulate the problem, our unique solution, and the value proposition for the Lisk ecosystem. We are committed to launching on the Lisk Mainnet and believe our project has a strong potential for real-world impact.

---

## 🛠️ How to Run Locally

### Prerequisites

- [Node.js](https://nodejs.org/en/) with `pnpm`
- [Foundry](https://getfoundry.sh/)
- A local WordPress installation (for the plugin)

### 1. Smart Contract

```bash
# Navigate to the contract directory
cd contract

# Install dependencies
forge install

# Build contracts
forge build

# Run tests
forge test
```

### 2. Web Application

```bash
# Navigate to the apps directory
cd apps

# Install dependencies
pnpm install

# Copy environment variables
cp .env .env.local

# Run the development server
pnpm dev
```

### 3. WordPress Plugin

1.  Navigate to the `wp-plugin` directory.
2.  Compress the contents into a `paylis.zip` file.
3.  In your WordPress admin dashboard, go to `Plugins > Add New > Upload Plugin`.
4.  Upload `paylis.zip` and activate it.
5.  Configure the Paylis gateway in your WooCommerce settings.
