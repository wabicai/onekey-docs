# Introduction

OneKey documentation unifies three integration paths. Choose based on your app and platform:

- dApp Integration (software wallet, injected provider)
- Hardware SDK (hardware wallet over USB/BLE/React Native)
- Air-Gap (hardware wallet via QR, offline signing)

## Start Here

- dApp Integration (software wallet)
  - Get started: [Overview](connect-to-software/README.md), [Web (Injected Provider)](connect-to-software/webapp-connect-onekey/README.md)
  - Next: [Wallet Kits](connect-to-software/support-wallet-kit/README.md), [Developer Guides](connect-to-software/guides/developer-guide.md)
  - Tip: Explore per‑chain docs (ETH, BTC, Solana, NEAR, Nostr, WebLN) from the sidebar under “Web (Injected Provider) → Chains”.

- Hardware SDK (hardware wallet over USB/BLE/React Native)
  - Get started: [Overview](connect-to-hardware/README.md), [Quick Start](connect-to-hardware/quick-start.md)
  - Next: Transports — [WebUSB](connect-to-hardware/transport-recipes/web-usb.md), [Native BLE](connect-to-hardware/transport-recipes/common-connect-1/README.md), [React Native BLE](connect-to-hardware/transport-recipes/react-native-ble.md); [API References](connect-to-hardware/hardware-sdk/README.md)
  - Playground: Expo Playground → https://hardware-example.onekey.so/

- Air-Gap (hardware wallet via QR, offline)
  - Get started: [Overview](connect-to-hardware/air-gap/air-gap.md), [Quick Start](connect-to-hardware/air-gap/quick-start.md)
  - Next: Reference — [Index](connect-to-hardware/air-gap/reference/README.md)
  - Note: Air‑Gap is offline by design (QR). Use the RN demo or your own app’s QR flow.



## Tips

- Detection: Prefer OneKey’s dedicated injections (e.g. `window.$onekey.ethereum`) before falling back to generic providers
- Mobile/WebViews: Use deeplinks or WalletConnect with a universal link fallback
- Emulator: For Hardware SDK development, use the Expo Playground and the emulator device → https://hardware-example.onekey.so/

## Support

- Help Center: [Help Center](https://help.onekey.so)
- OneKey App Web: [OneKey](https://onekey.so/)

## Related Repositories

- OneKey Hardware JS SDK: [hardware-js-sdk](https://github.com/OneKeyHQ/hardware-js-sdk)
- OneKey App Monorepo: [app-monorepo](https://github.com/OneKeyHQ/app-monorepo)
- OneKey Firmware: [firmware](https://github.com/OneKeyHQ/firmware)
