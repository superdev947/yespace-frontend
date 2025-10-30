# YeSpace Frontend

A multi-chain NFT showcase platform that allows users to create personalized spaces to display their NFT collections from Ethereum, Solana, and Algorand blockchains.

## 🌟 Features

- **Multi-Chain Support**: Connect and display NFTs from Ethereum, Solana, and Algorand
- **Wallet Integration**: 
  - MetaMask for Ethereum
  - Phantom Wallet for Solana
  - MyAlgo Connect for Algorand
- **Personal Space**: Create and customize your own NFT gallery
- **Explore**: Discover top NFT holders and their collections
- **Responsive Design**: Optimized for both desktop and mobile devices
- **Material-UI**: Modern and clean interface with Material-UI components

## 🛠️ Tech Stack

- **Framework**: React 18 with TypeScript
- **State Management**: Redux Toolkit with Redux Persist
- **UI Library**: Material-UI (MUI) v5
- **Routing**: React Router v6
- **Blockchain Integration**:
  - `@web3-react` for Ethereum
  - `@solana/wallet-adapter` for Solana
  - `algosdk` for Algorand
- **Styling**: Sass/SCSS
- **HTTP Client**: Axios
- **Build Tool**: React App Rewired with custom webpack configuration

## 📋 Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- MetaMask browser extension (for Ethereum)
- Phantom browser extension (for Solana)
- MyAlgo Connect (for Algorand)

## 🚀 Getting Started

### Installation

1. Clone the repository:
```bash
git clone https://github.com/superdev947/yespace-frontend.git
cd yespace-frontend
```

2. Install dependencies:
```bash
npm install
```

3. Configure environment:
   - Update API endpoints in `src/config.tsx` if needed
   - Default API: `https://space.yenft.io/api/`

### Available Scripts

#### `npm start`
Runs the app in development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload when you make changes.\
Source maps are disabled for faster builds.

#### `npm run build`
Builds the app for production to the `build` folder.\
Optimizes the build for best performance with minification and hashing.

#### `npm test`
Launches the test runner in interactive watch mode.

## 📁 Project Structure

```
src/
├── assets/          # Static assets (images, styles)
├── components/      # Reusable components (Loader, Snackbar)
├── contexts/        # React contexts (API, Wallets)
├── hooks/           # Custom hooks (useApi, useWallets)
├── layout/          # Layout components (Header, Footer, MainLayout)
├── routes/          # Route configuration
├── store/           # Redux store and reducers
├── themes/          # MUI theme configuration
├── types/           # TypeScript type definitions
├── ui-component/    # UI components (EmptyContent, Loading, SvgIcon)
├── utils/           # Utility functions (axios, metamask, snackbar)
└── views/           # Page components
    ├── Error/       # Error page
    ├── Explore/     # Explore spaces and top holders
    ├── Home/        # Landing page and space creation
    ├── MyYeSpace/   # User's personal NFT space
    └── Public/      # Public profile view
```

## 🔧 Configuration

### Webpack Override

The project uses `react-app-rewired` with custom webpack configuration (`config-overrides.js`) to:
- Add TypeScript support with ts-loader
- Configure Node.js polyfills for browser compatibility
- Support blockchain libraries (crypto, stream, buffer, etc.)

### Base Configuration (`src/config.tsx`)

```typescript
export const BASE_PATH = "";
export const HOME_PATH = "/explore";
export const API_URL = "https://space.yenft.io/api/";
export const BASE_URL = "https://space.yenft.io/";
export const RENDERNUM = 3;
```

## 🔐 Wallet Connection

The application supports three blockchain networks:

1. **Ethereum (EVM)**: Connect via MetaMask
2. **Solana**: Connect via Phantom Wallet
3. **Algorand**: Connect via MyAlgo

Users can connect multiple wallets from different chains to showcase all their NFTs in one space.

## 🎨 Key Features

### Create Your Space
1. Connect your wallet(s)
2. Add wallet addresses from different blockchains
3. Set up your profile (name, avatar, bio)
4. Customize your NFT gallery

### Explore
- View top NFT holders across chains
- Discover unique NFT collections
- Browse public spaces

### My YeSpace
- Manage your connected wallets
- Show/hide specific NFTs
- Organize your NFT showcase
