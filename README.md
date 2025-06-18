# Nautilus Airdrop System

A comprehensive airdrop management system for the Voi Network and Algorand ecosystems, supporting token distribution to eligible users across various protocols and platforms.

## Overview

This airdrop system manages token distributions for various projects within the Voi Network and Algorand ecosystems, including:

- **Power ($POW)** - Governance token for Humble & Pact Protocol (Voi Network | Algorand)
- **Pixel Dust ($PXD)** - Reward token for Nautilus NFT Marketplace users (Voi Network)

## Project Structure

```
airdrop/
├── README.md           # This documentation
├── CHANGELOG.md        # Version history and changes
├── LICENSE.md          # MIT License
├── BLACKLIST.md        # Blacklist management and batches
├── index.json          # Airdrop configuration and metadata
├── blacklist.json      # Addresses excluded from airdrops
├── data/               # Airdrop data files
│   ├── 000-pow.json    # Power token airdrop data
│   ├── 000-pow.png     # Power token logo
│   ├── 000-pow.mp4     # Power token promotional video
│   └── 001-pxd.json    # Pixel Dust airdrop data
└── .gitignore          # Git ignore rules
```

## Available Airdrops

### 1. Power ($POW) Airdrop
- **Status**: Active (Started June 23, 2025)
- **Duration**: 90 days
- **Eligibility**: Humble & Pact Historic Users
- **Description**: POW is the governance token for Pact Protocol, enabling community participation in protocol governance.
- **Networks**: Voi Network, Algorand
- **Asset IDs**: 
  - Voi: 0
  - Algorand: 2994233666
- **Token IDs**:
  - Voi: 0
  - Algorand: 3080081069
- **Airdrop Address**: SDSKGUS5AEIQATOLCSNC4PUK5GK6G6JRWMKUJY5GQRWMNXUTWURVUIQV3U
- **Claim URL**: https://powapp.xyz

### 2. Pixel Dust ($PXD) Airdrop
- **Status**: Active (Started June 1, 2025)
- **Duration**: 365 days
- **Eligibility**: Nautilus NFT Marketplace Historic Users
- **Description**: Pixel Dust is reward token for Nautilus NFT Marketplace historic users.
- **Networks**: Voi Network
- **Token ID**: 419714
- **Airdrop Address**: NXPRBWKSBICV7P3YDK5CAQVQEJEJ7A7B33QRDBOVQWIOCU2TM4ZWQUFQ5Q
- **Claim URL**: https://pxd.nautilus.sh

## Data Format

### Airdrop Configuration (index.json)
Each airdrop entry contains:
- `id`: Unique identifier for the airdrop
- `name`: Display name of the airdrop
- `description`: Detailed description of the token and its purpose
- `eligibility`: Criteria for user eligibility
- `image`: URL to the token logo
- `start_date`: When the airdrop begins (YYYY-MM-DD format)
- `period`: Duration of the airdrop
- `status`: Current status (pending, active, completed)
- `url`: Claim URL (if available)
- `airdrop_address`: Contract address for the airdrop (if available)
- `networks`: Array of supported networks (e.g., ["Voi", "Algorand"])
- `type`: Airdrop type format ("asset_id_and_token_id" or "token_id_only")
- `asset_ids`: Object mapping networks to asset IDs (for multi-network airdrops)
- `token_ids`: Object mapping networks to token IDs (for multi-network airdrops)
- `token_id`: Single token ID (for single-network airdrops)

### Airdrop Data Files
Individual airdrop data files contain the list of eligible addresses and their allocated amounts. These files are typically large JSON files with the following structure:

#### Multi-Network Airdrops (e.g., 000-pow.json)
```json
{
  "Address": "VOI_OR_ALGO_ADDRESS",
  "Voi": 0.0,
  "Algo": 46327.13709,
  "Total": 46327.13709
}
```

#### Single-Network Airdrops (e.g., 001-pxd.json)
```json
{
  "address": "VOI_ADDRESS",
  "amount": "TOKEN_AMOUNT",
  "eligibility_reason": "REASON_FOR_ELIGIBILITY"
}
```

## Blacklist

The `blacklist.json` file contains addresses that are excluded from all airdrops. This typically includes:
- Exchange addresses
- Contract addresses
- Known bot addresses
- Addresses that have violated terms of service

## Usage

### For Developers

1. **Adding New Airdrops**:
   - Create a new entry in `index.json`
   - Add corresponding data file in `data/` directory
   - Update this README with new airdrop information

2. **Updating Airdrop Status**:
   - Modify the `status` field in `index.json`
   - Update `start_date` and other relevant fields as needed

3. **Managing Blacklist**:
   - Add addresses to `blacklist.json` to exclude them from all airdrops
   - Ensure addresses are in the correct network format

4. **Multi-Network Airdrops**:
   - Set `networks` array to include all supported networks
   - Use `type: "asset_id_and_token_id"` for multi-network airdrops
   - Provide `asset_ids` and `token_ids` objects mapping networks to their respective IDs
   - Structure data files with network-specific amount fields

### For Users

1. **Check Eligibility**:
   - Visit the claim URL for active airdrops
   - Connect your wallet to check eligibility
   - Review the eligibility criteria for each airdrop

2. **Claim Tokens**:
   - Follow the instructions on the claim page
   - Ensure you have sufficient VOI/ALGO for transaction fees
   - Complete the claim transaction through your wallet

## Technical Details

- **Networks**: Voi Network, Algorand
- **Token Standard**: ARC-200 (Algorand Request for Comments 200)
- **Blockchain**: Algorand-based L1 blockchain (Voi Network), Algorand Mainnet
- **Wallet Support**: Compatible with all Voi Network and Algorand wallets

## Security

- All airdrop addresses and token IDs are verified on-chain
- Blacklist prevents distribution to ineligible addresses
- Smart contracts handle the actual token distribution
- Users must sign transactions to claim tokens

## Contributing

To contribute to the airdrop system:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

For detailed information about project changes and version history, see [CHANGELOG.md](CHANGELOG.md).

## Support

For questions or issues related to airdrops:
- Check the specific airdrop's claim page
- Review the eligibility criteria
- Ensure your wallet is compatible with the required networks

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

The Nautilus Airdrop System is part of the Voi Network ecosystem and follows open-source best practices for transparency and community collaboration.
