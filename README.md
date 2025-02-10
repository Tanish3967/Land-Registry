# Land Registry System

## Overview
The **Land Registry System** is a blockchain-based solution that ensures secure, transparent, and tamper-proof land registration and ownership transfers. Built using Solidity, this smart contract automates verification, prevents forgery, and ensures that only rightful owners can transfer land.

## Features
- **Land Registration:** Users can register a new land parcel with a unique ID, location, and area.
- **Ownership Transfer:** Only the registered owner can transfer land ownership to another address.
- **Land Details Retrieval:** Anyone can query land details such as ID, location, area, owner, and registration status.
- **Tamper-Proof Records:** Ensures security and transparency through blockchain immutability.

## Smart Contract
### Functions
1. **registerLand(uint256 _id, string memory _location, uint256 _area)**
   - Registers a new land parcel with a unique ID, location, and area.
   - Emits `LandRegistered` event upon successful registration.

2. **transferOwnership(uint256 _id, address _newOwner)**
   - Transfers ownership of a registered land parcel to a new owner.
   - Emits `OwnershipTransferred` event upon successful transfer.

3. **getLand(uint256 _id)** *(view function)*
   - Returns land details including ID, location, area, owner, and registration status.

4. **isLandRegistered(uint256 _id)** *(view function)*
   - Checks whether a land parcel is registered.

### Events
- **LandRegistered(uint256 indexed landId, string location, uint256 area, address indexed owner)**
- **OwnershipTransferred(uint256 indexed landId, address indexed oldOwner, address indexed newOwner)**

## Prerequisites
- Solidity ^0.8.0
- Ethereum development environment (Remix, Hardhat, or Truffle)
- MetaMask or any Web3-compatible wallet

## Deployment
1. Open Remix IDE or set up Hardhat/Truffle.
2. Compile the contract using Solidity ^0.8.0.
3. Deploy the contract to a blockchain network (local testnet, Goerli, or mainnet).
4. Interact using Remix, Web3.js, or Ethers.js.

## License
This project is licensed under the **MIT License**.

## Contact
For any queries or contributions, feel free to open an issue on this repository!

