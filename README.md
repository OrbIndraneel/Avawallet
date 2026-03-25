Authors: 
1. Indraneel Mandal (B.tech AI & DS)
2. Saugat Sharma (B.tech CSE)
3. Vanshik Bavashiya (B.tech AI & DS)
4. Manan Chauhan (B.tech AI & DS)



# 🛡️ AvaWallet: The Universal Offline-First Crypto Wallet

**AvaWallet** is a decentralized, multi-currency wallet system designed to bridge the gap between online liquidity and offline utility. Built for a high-performance hackathon, it solves the "No Internet" barrier in blockchain by enabling secure Offline-to-Offline (P2P) transfers using cryptographic signatures.

[![Live Demo]](https://avawallet.vercel.app)
[![Blockchain]](https://polygon.technology/)

---

## 🚀 The Problem
Standard crypto wallets require a constant internet connection to broadcast transactions. In areas with poor connectivity or during travel, users cannot utilize their digital assets. **AvaWallet** introduces a "Physical Cash" experience for digital assets.

## ✨ Key Features
- **Online-to-Offline (O2O) Locking:** Securely "vault" your on-chain assets into a local device-bound balance.
- **Offline-to-Offline (P2P) Payments:** Transfer funds to another device without Wi-Fi or Cellular data using **NFC/QR Code** exchange.
- **Double-Spend Prevention:** Uses sequential nonces and cryptographic commitments to ensure offline funds can only be spent once.
- **Reconciliation:** The recipient can claim funds on-chain as soon as they regain internet access.
- **Multi-Currency Support:** Architecture ready for ETH, USDC, and simulated cross-chain assets.

## 🛠️ Technical Architecture

AvaWallet operates on a **Vault & Voucher** model:
1. **Locking:** Users deposit funds into the `OfflineVault` smart contract.
2. **Signing:** The app generates an **ECDSA signature** (the Voucher) containing `[Sender, Receiver, Amount, Nonce]`.
3. **Transmission:** This signature is passed via NFC or QR code to the recipient.
4. **Settlement:** The recipient submits the signature to the blockchain to unlock the funds from the Vault.

### Tech Stack
- **Smart Contracts:** Solidity (OpenZeppelin)
- **Frontend:** React Native / Expo
- **Blockchain Interface:** Ethers.js / Viem
- **Communication:** NFC / Bluetooth LE / QR Codes
- **Network:** Polygon Amoy (for low-cost, fast settlement)

---
