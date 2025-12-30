---
description: Sui integration via OneKey’s Sui Wallet Standard provider (window.$onekey.sui)
slug: /dapp/chains/sui
---

# Sui

Use OneKey’s Sui provider (implements Sui Wallet Standard). Remember to pass `account`/`chain` to signing & transaction calls.

## Quick links

- [Detecting the Provider](detecting-the-provider.md)
- [Connecting & Accounts](connecting-and-accounts.md)
- [Transactions](transactions.md)
- [Signing](signing.md)

## Minimal pattern

```ts

const provider = window?.$onekey?.sui
if (!provider) throw new Error('OneKey Sui provider not detected')

// Request permission & accounts
await provider.requestPermissions()
const [account] = await provider.getAccounts()
const chain = await provider.getActiveChain() // e.g., 'sui:testnet'

// Sign + execute a TransactionBlock
const txb = new TransactionBlock()
txb.transferObjects([txb.object('0xobject_id')], txb.pure('0xrecipient'))

const result = await provider.signAndExecuteTransactionBlock({
  account,
  chain,
  transactionBlock: txb,
})
console.log(result.digest)
```

## Supported chains

| Chain   | Identifier   |
|---------|--------------|
| Testnet | `sui:testnet`|
| Devnet  | `sui:devnet` |

## APIs quick view

- TransactionBlock APIs: `signAndExecuteTransactionBlock`, `signTransactionBlock`
- Transaction APIs (newer): `signAndExecuteTransaction`, `signTransaction` — use `Transaction` from `@mysten/sui.js/transactions`
- Message: `signPersonalMessage` (recommended), `signMessage` (legacy)

## Common errors

- 4001: user rejected
- 4100: unauthorized / no permission
- -32603: internal error

## Mobile & deeplinks

- Use OneKey deeplinks carrying WalletConnect URI for mobile handoff
- See [Use deeplinks](../../guides/use-deeplinks.md)
