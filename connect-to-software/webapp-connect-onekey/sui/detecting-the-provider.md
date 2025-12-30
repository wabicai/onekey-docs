---
description: Detect the injected Sui provider from OneKey (window.$onekey.sui)
---

# Detecting the Provider

```ts
const provider = window?.$onekey?.sui
if (!provider) {
  throw new Error('OneKey Sui provider not detected')
}
```

- Prefer `window.$onekey.sui`; avoid mixing with other Sui wallets to prevent conflicts.
- OneKey implements Sui Wallet Standard.
