# Paylis - WooCommerce Plugin For Accepting Stablecoin Payment

Paylis is a non-custodial payment gateway that allows online merchants to seamlessly accept cryptocurrency payments on the Lisk blockchain. Our primary goal is to simplify the crypto payment experience for both merchants and their customers, driving adoption of the Lisk ecosystem in real-world commerce.

![Project Screenshot](https://github.com/fahmixls/paylis/blob/main/assets/demo-site.png)

## 🎥 Live Demo & Pitch Deck

- **Demo Video:** [Watch on YouTube](https://youtu.be/80O5W5rgSg8)
- **Pitch Deck:** [View on Google Drive](https://drive.google.com/file/d/1OnHlKDCaX1FwucOiucmPUGvdGccH960S/view?usp=sharing)

## 🚀 Submission Links

| Item                            | Link                                                                                                                      |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| **Live Project URL**            | [https://paylis.app](https://paylis.netlify.app)                                                                          |
| **Smart Contract**              | [View on Lisk Sepolia Blockscout](https://sepolia-blockscout.lisk.com/address/0x65653f7fD8ac409D3C812294eC2FfE8CF5e98a7f) |
| **Mock IDRX**                   | [View on Lisk Sepolia Blockscout](https://sepolia-blockscout.lisk.com/address/0xcA0A2cE00d5b6Dd22C65731D8F64939537595D01) |
| **Mock USDC**                   | [View on Lisk Sepolia Blockscout](https://sepolia-blockscout.lisk.com/address/0x0A218c6a23Ede0395474e9d875c7fE2BF859Cf10) |
| **Web Application Repository**  | [View on GitHub](https://github.com/fahmixls/paylis-webapp)                                                               |
| **Relayer Repository**          | [View on GitHub](https://github.com/fahmixls/paylis-relayer)                                                              |
| **Wordpress Plugin Repository** | [View on GitHub](https://github.com/fahmixls/paylis-woocomerce-payment-gateway)                                           |
| **Smart Contract Repository**   | [View on GitHub](https://github.com/fahmixls/paylis-contract)                                                             |

---

## 🎯 Feature

- **Onboarding Mainstream Merchants:** Our flagship integration is a **WordPress plugin**. With WordPress powering over 43% of all websites, Paylis provides an immediate and accessible way for a massive market of e-commerce stores to start accepting LSK and Lisk-based tokens.
- **Increasing Network Activity:** By simplifying crypto payments, we lower the barrier for everyday transactions, from buying a coffee to paying for digital goods. This directly translates to increased, sustained transaction volume on the Lisk network.
- **User Acquisition:** We introduce a new wave of non-crypto-native users (both merchants and customers) to the Lisk ecosystem through a familiar e-commerce interface, fostering organic growth.
- **Gasless Transactions:** We utilize a `PaymentForwarder` smart contract and a relayer system. This allows customers to pay for goods using stablecoins without needing to hold Lisk's native token for gas fees. The relayer covers the gas, and the merchant can sponsor this cost, creating a frictionless "one-click" payment experience similar to Web2.
- **Non-Custodial by Design:** Unlike many crypto payment processors, Paylis is completely non-custodial. Funds are sent directly from the customer to the merchant's wallet via our smart contract, ensuring full self-sovereignty.
- **E-commerce First:** Our architecture is built from the ground up for e-commerce, with deep integration into platforms like WordPress/WooCommerce, rather than being a generic crypto wallet.
- **For Merchants:** A simple onboarding process, an intuitive dashboard to view payment history, and a one-time setup via the WordPress plugin.
- **For Customers:** A clean, familiar checkout process. The "gasless" feature means they only need to approve the token transfer, without worrying about network fees, significantly reducing friction and cart abandonment.

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
