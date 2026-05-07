# dapps

Whitelisted dapp listings for ZKX Wallet.

This repository maintains the official dapp list used by ZKX Wallet and the LibertySwap ecosystem.

### Dapp JSON Schema
Every dapp must follow this structure:

```json
{
  "id": "yourdapp.domain",
  "url": "https://yourdapp.domain",
  "name": "Dapp Name",
  "icon": "https://yourdapp.domain/icon.png",
  "description": "A short description of what the dapp does.",
  "chainIds": [369],
  "category": "Dexes",
  "twitter": "TwitterHandle"
}
```

Required fields: `id`, `url`, `name`, `icon`, `description`, `chainIds`, `category`.  
Optional fields: `twitter`.

#### Categories
Use one of the following values for `category`:

- `Dexes`
- `Analytics`
- `NFTs`
- `Gaming`
- `DeFi`
- `Social`
- `Tools`

#### Chain IDs
Common chain IDs:

| Chain | ID |
|---|---|
| PulseChain | 369 |
| Ethereum | 1 |
| BNB Chain | 56 |
| Base | 8453 |
| Arbitrum | 42161 |
| Polygon | 137 |

## How to Add or Update a Dapp

1. Fork this repository.
2. Add your dapp at the end of the `daps` array in **zkxwallet-dapplist.json**.
3. Ensure the entry strictly follows the schema above.
4. Place the dapp icon inside the **dapp-logo/** folder (use the dapp id as the filename, e.g. **yourdapp.domain.png**).
5. Commit your changes and open a **Pull Request** to the **dev** branch.

***Example Dapp Entry JSON***
```json
{
  "id": "libertyswap.finance",
  "url": "https://libertyswap.finance",
  "name": "Liberty Swap",
  "icon": "https://libertyswap.finance/android-icon-192x192.png",
  "description": "Experience instant, gasless cross-chain transfers to PulseChain. Our intent-based swap engine eliminates the need for native gas tokens, providing a free gas experience for effortless onboarding.",
  "chainIds": [369, 1, 56, 8453, 42161, 137],
  "category": "Dexes",
  "twitter": "LibertySwapFi"
}
```

# Important Notice:

* Not every dapp will be accepted.
* All submissions are subject to review and approval by the LibertyX team.
* You must provide a proper icon and accurate dapp details.

# Disclaimer
After submitting a Pull Request, please be patient. We review submissions as time allows and do not follow a strict first-come, first-served order.