# MST — Technical Token Information

## 1. Basic Identification

| Field | Value |
|---|---|
| Project Name | Master Sovereign Token |
| Token Symbol | MST |
| Contract Name | MasterSovereignToken |
| Blockchain | Polygon PoS Mainnet |
| Chain ID | 137 |
| Token Standard | ERC-20 |
| Decimals | 18 |
| Contract Address | `0xC7068EF42Ec42CAE249a856e29ab7f6ca28067c0` |
| Initial Creator / Owner | `0x29c7e457644f9D5d744bf52455AA2ad85aA8BF50` |
| Deployment Transaction | `0xb382efcdf650f0dd2176d21cec61052a5dfe59e59b1a4e58b5b6149b7296d1f9` |

## 2. Source Code and Compilation

| Parameter | Information |
|---|---|
| Programming Language | Solidity |
| Compiler Version | v0.8.20+commit.a1b79de6 |
| EVM Version | Paris |
| Optimization | Disabled |
| Optimization Runs Setting | 200 |
| Contract Source Verification | Verified – Exact Match (previously reported) |
| Contract License | MIT (reported in explorer) |

Source verification confirms correspondence between published source code and deployed bytecode. It does not constitute a security audit.

## 3. Software Components

The contract uses OpenZeppelin components:

- ERC20
- ERC20Burnable
- Ownable

These components provide standard token transfer, burning, and ownership-management functionality.

## 4. Token Functions

### Mint

The contract includes an owner-restricted mint function:

`mint(address to, uint256 amount)`

This function permits the authorized contract owner to issue additional MST tokens.

There is no fixed maximum supply enforced by this mint function.

### Burn

The contract supports token burning by holders through:

`burn(uint256 amount)`

### Burn From

The contract also supports:

`burnFrom(address account, uint256 amount)`

This function allows burning tokens from another account subject to the required allowance.

### Ownership

The Ownable component provides ownership-management functionality, including ownership transfer and renunciation.

The initial creator address must not automatically be assumed to be the current owner. Current ownership requires an up-to-date blockchain check.

## 5. Nominal Valuation Constant

The source code contains:

`uint256 public constant NOMINAL_BACKING_VALUATION = 500000000000 * 10**18;`

This expression represents a nominal numerical constant of 500 billion MST units expressed using 18-decimal token precision.

It is not a dollar balance, bank deposit, reserve, collateral valuation, supply cap, or proof of asset ownership.

It does not establish a guaranteed token price or redemption value.

## 6. Supply and Circulation

The actual total supply and circulating supply must be obtained from current on-chain data.

No fixed maximum supply is established by the owner-controlled mint function.

This documentation does not publish an unverified current supply figure.

## 7. Security and Audit Status

The contract source was previously reported as verified on PolygonScan.

An independent security audit has not been established by the available project records.

Users should review the source code, ownership status, mint permissions, and transaction history before interacting with MST.

## 8. Blockchain References

**Contract Explorer:**

https://polygonscan.com/address/0xC7068EF42Ec42CAE249a856e29ab7f6ca28067c0

**Deployment Transaction:**

https://polygonscan.com/tx/0xb382efcdf650f0dd2176d21cec61052a5dfe59e59b1a4e58b5b6149b7296d1f9

**Official GitHub Repository:**

https://github.com/rwab-official/MasterSovereignToken

## 9. Important Notice

MST is a blockchain token and does not currently represent independently verified financial reserves or guaranteed asset-backed value.

Any future reserve or collateral arrangements will require separate documentation and verification.

Future market prices, if an active market develops, will be determined by market conditions and supply and demand.

---

**Document:** MST Technical Token Information  
**Version:** 1.0  
**Status:** Public Technical Disclosure  
**Network:** Polygon PoS Mainnet
