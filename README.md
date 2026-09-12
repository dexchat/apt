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
