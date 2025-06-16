# Changelog

All notable changes to the Nautilus Airdrop System will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Initial project structure and documentation
- Support for multiple airdrop campaigns
- Blocklist functionality for address exclusion
- Comprehensive README with usage instructions

### Changed
- Updated airdrop status tracking system
- Improved data format standardization

### Fixed
- Address validation and formatting
- Token ID verification process

## [1.0.0] - 2025-06-01

### Added
- **Pixel Dust ($PXD) Airdrop Launch**
  - Active airdrop for Nautilus NFT Marketplace historic users
  - Token ID: 419714
  - Airdrop Address: NXPRBWKSBICV7P3YDK5CAQVQEJEJ7A7B33QRDBOVQWIOCU2TM4ZWQUFQ5Q
  - Claim URL: https://pxd.nautilus.sh
  - Duration: 365 days
  - Eligibility criteria implementation
  - Automated distribution system

- **Power ($POW) Airdrop Preparation**
  - Governance token airdrop for Humble & Pact Protocol users
  - Scheduled start date: June 23, 2025
  - Duration: 90 days
  - Eligibility: Historic users of Humble & Pact Protocol

- **Core System Features**
  - JSON-based configuration system (`index.json`)
  - Address blocklist functionality (`blocklist.json`)
  - Modular data structure for individual airdrops
  - Support for multiple token types and networks
  - Comprehensive documentation and usage guidelines

### Technical Implementation
- ARC-200 token standard support
- Voi Network integration
- Multi-wallet compatibility
- Smart contract integration for secure distribution
- Automated eligibility verification

### Security Features
- Address validation and sanitization
- Blacklist for excluded addresses (exchanges, contracts, bots)
  + eg. [d13 myalgo impacted addresses](https://d13.co/myalgo-hack-first-wave-addresses-data/)
- On-chain verification of airdrop addresses
- Transaction signature requirements for claims

## [0.9.0] - 2025-05-15

### Added
- Initial project setup
- Basic airdrop configuration structure
- Documentation framework
- Git repository initialization

### Changed
- Project structure optimization
- Configuration format standardization

## [0.8.0] - 2025-05-01

### Added
- Project planning and architecture design
- Token distribution strategy development
- Eligibility criteria definition
- Security protocol planning

---

## Version History

- **v1.0.0**: First production release with active PXD airdrop
- **v0.9.0**: Beta release with core functionality
- **v0.8.0**: Alpha release with basic structure

## Contributing

When adding entries to this changelog, please follow these guidelines:

1. **Added** for new features
2. **Changed** for changes in existing functionality
3. **Deprecated** for soon-to-be removed features
4. **Removed** for now removed features
5. **Fixed** for any bug fixes
6. **Security** for security-related changes

## Links

- [Voi Network Documentation](https://docs.voi.network)
- [Nautilus Platform](https://nautilus.sh)
- [Pact Protocol](https://pact.fi)
- [Nautilus Airdrop Center](https://nautilus.sh/airdrop)