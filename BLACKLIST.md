# Blacklist Management

This document tracks the blacklist functionality and address batches for the Nautilus Airdrop System.

## Overview

The blacklist system prevents specific addresses from participating in airdrops. This includes:
- Exchange addresses
- Contract addresses  
- Known bot addresses
- Addresses that have violated terms of service
- Test addresses and development wallets

## Blacklist File

- **File**: `blacklist.json`
- **Format**: JSON array of Voi Network addresses
- **Total Addresses**: 249 addresses (as of current version)
- **Last Updated**: 2025-06-01

## Address Categories

### Exchange Addresses
Addresses belonging to centralized exchanges and trading platforms that should not receive airdrops.

### Contract Addresses
Smart contract addresses that cannot directly claim tokens.

### Bot Addresses
Known automated trading bots and scripts that may attempt to claim multiple times.

### Violation Addresses
Addresses that have violated airdrop terms of service or engaged in fraudulent activities.

### Development Addresses
Test addresses and development wallets used during system testing.

## Batch History

### Batch 1 - Initial Blacklist (2025-06-15)
- **Addresses Added**: 249
- **Reason**: myalgo hack inpacted and hacker addresses
- **Source**: d13 myalgo hack report

<https://d13.co/myalgo-hack-first-wave-addresses-data/>
<https://d13.co/myalgo-hack-fifth-wave-addresses-data/>

### Batch 2 - Exchange Addresses (2025-05-20)
- **Addresses Added**: 0 (already included in Batch 1)
- **Reason**: Additional exchange address verification
- **Status**: No new addresses needed

### Batch 3 - Contract Verification (2025-05-25)
- **Addresses Added**: 0 (already included in Batch 1)
- **Reason**: Smart contract address verification
- **Status**: All known contracts already blacklisted

## Blacklist Validation

### Address Format
All addresses in the blacklist follow the Voi Network address format:
- 58-character alphanumeric strings
- Base32 encoding
- Checksum validation

### Validation Process
1. **Format Check**: Verify address format and checksum
2. **Network Check**: Confirm addresses are valid Voi Network addresses
3. **Duplicate Check**: Ensure no duplicate addresses in the list
4. **On-chain Verification**: Verify address existence on Voi Network

## Management Procedures

### Adding Addresses
1. Identify address that should be blacklisted
2. Verify address format and validity
3. Add to `blacklist.json` array
4. Update this documentation
5. Commit changes with descriptive message

### Removing Addresses
1. Verify address should be removed from blacklist
2. Remove from `blacklist.json` array
3. Update this documentation
4. Commit changes with descriptive message

### Regular Maintenance
- Monthly review of blacklist effectiveness
- Quarterly audit of address categories
- Annual cleanup of outdated entries

## Technical Implementation

### File Structure
```json
[
  "ADDRESS1",
  "ADDRESS2",
  "ADDRESS3"
]
```

### Integration
The blacklist is automatically checked during:
- Airdrop eligibility verification
- Token distribution processes
- Claim validation

### Performance
- O(1) lookup time using hash-based checking
- Minimal impact on airdrop processing speed
- Efficient memory usage

## Security Considerations

### Access Control
- Only authorized administrators can modify blacklist
- All changes require code review
- Changes are logged and tracked

### Data Integrity
- Regular backups of blacklist data
- Checksum validation of file integrity
- Version control for all changes

### Privacy
- Addresses are stored in plain text for efficiency
- No personal information associated with addresses
- Public transparency for audit purposes

## Monitoring and Analytics

### Blacklist Effectiveness
- Track attempted claims from blacklisted addresses
- Monitor for new patterns of abuse
- Analyze effectiveness of current blacklist

### Metrics
- Number of blocked attempts
- Categories of blocked addresses
- Success rate of blacklist enforcement

## Future Improvements

### Planned Enhancements
1. **Dynamic Blacklisting**: Real-time address addition
2. **Category Tags**: Enhanced categorization of addresses
3. **Expiration Dates**: Time-based blacklist entries
4. **Reason Tracking**: Document reasons for blacklisting

### Research Areas
- Machine learning for address pattern detection
- Automated abuse detection systems
- Integration with external blacklist sources

## Contact and Support

For questions about the blacklist system:
- Review this documentation
- Check the main [README.md](README.md)
- Contact the development team

## Version History

- **v1.0.0**: Initial blacklist with 249 addresses
- **v0.9.0**: Basic blacklist structure
- **v0.8.0**: Blacklist planning and design

---

**Last Updated**: 2025-06-01  
**Maintainer**: Nautilus Development Team  
**Status**: Active and Maintained