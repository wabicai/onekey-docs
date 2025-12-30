---
description: Request permissions, get accounts, and track state for OneKey Sui provider
---

# Connecting & Accounts

```ts
// Request permissions
await provider.requestPermissions()

// Get accounts
const accounts = await provider.getAccounts()
const [account] = accounts

console.log({
  address: account.address,
  publicKey: account.publicKey, // hex string
})

// Active chain
const chain = await provider.getActiveChain() // e.g., 'sui:testnet'

// Connection status
const isConnected = provider.isConnected()
```

## Events

```ts
provider.onAccountChange((account) => {
  if (account) {
    console.log('Account changed:', account.address)
  } else {
    console.log('Disconnected')
  }
})

provider.onNetworkChange((network) => {
  console.log('Network changed:', network)
})
```

## Supported chains

| Chain   | Identifier   |
|---------|--------------|
| Testnet | `sui:testnet`|
| Devnet  | `sui:devnet` |
