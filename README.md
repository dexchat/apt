# DexChat APT repository

This repository hosts the signed Debian packages and APT metadata for DexChat.

It is updated automatically by releases from
[`dexchat/dex`](https://github.com/dexchat/dex).

## Installation

```sh
curl -fsSL https://dexchat.org/apt/dexchat-keyring.gpg \
  | sudo tee /usr/share/keyrings/dexchat-keyring.gpg >/dev/null

echo 'deb [signed-by=/usr/share/keyrings/dexchat-keyring.gpg] https://dexchat.org/apt stable main' \
  | sudo tee /etc/apt/sources.list.d/dexchat.list >/dev/null

sudo apt update
sudo apt install dexchat
```

## Signing key

Packages and repository metadata are signed with the dedicated DexChat APT key:

```text
F02A 2832 0D62 E66B 9E76  E50F 8BFF D736 A3C3 2798
```

The public key is available as [`dexchat-keyring.gpg`](./dexchat-keyring.gpg).
