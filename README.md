<div align="center">

<img src="docs/banner.png" alt="PXN Shield VPN for Linux" width="100%">

<br><br>

### [⬇ Download for Linux][latest]

<sub>64-bit Linux desktop · free with any [PXN Stores][site] plan</sub>

</div>

---

## What this is

The Linux client for **[PXN Stores LK][site]**.

Sign in with the account you bought your plan on and every config you own is
already here — no links to paste, no files to import, no QR codes to scan. Press
one button and your whole computer goes through the tunnel.

It is the same account, the same configs and the same Store as the phone and
Windows apps.

## Download

<div align="center">

### [⬇ PXN-Shield-VPN-linux-x64.tar.gz][tarball]

<sub>Extract it anywhere and run `./pxn-shield.sh`</sub>

</div>

```bash
tar -xzf PXN-Shield-VPN-linux-x64.tar.gz
cd PXN-Shield-VPN
./pxn-shield.sh
```

Everything the app needs is already inside — there is no runtime to install
first. It asks for your password once before the window opens, because creating
a network device needs it.

<details>
<summary><b>Install it properly</b> — adds it to your applications menu</summary>

<br>

```bash
sudo mkdir -p /opt/pxn-shield
sudo cp -r ./* /opt/pxn-shield/
sudo install -Dm644 pxn-shield.desktop /usr/share/applications/pxn-shield.desktop
sudo install -Dm644 pxn-shield.png /usr/share/icons/hicolor/256x256/apps/pxn-shield.png
```

</details>

## What it does

|  |  |
|---|---|
| 🛡️ **Covers the whole PC** | A real network device, so games, launchers, and anything with its own network stack go through the tunnel too — not only apps that happen to honour a proxy setting. |
| 📊 **Your plans, live** | Data used and days left for every config on your account, straight from the panel. |
| 🛒 **Buy and renew in the app** | Same packages, same prices, same banks and the same transfer remark as the website. Add store credit without leaving the app. |
| 🚫 **Block ads** | Optional, off by default. Ad and tracker domains are dropped inside the tunnel, so games and apps are covered too — not just your browser. |
| 🌐 **Routing rules** | Cloudflare Warp+ or a Sri Lankan exit, switched from the app. The tunnel reconnects itself so the change takes effect straight away. |
| 📱 **Per-app tunnelling** | Send everything through, or pick exactly which programs use it. |
| 📡 **Ping and uptime** | A real round trip to the server, measured outside the tunnel so the number means something. |
| 📖 **Guides** | English, සිංහල and தமிழ். |
| 🌗 **Dark and light** | Dark by default. |

## What it needs

- A **64-bit Linux desktop** (x86_64) using glibc — Debian, Ubuntu, Mint,
  Fedora, Arch and their relatives. Alpine and other musl-only systems are not
  supported.
- **WebKitGTK 4.1** and **libnotify**, for the window. Most desktops already
  have both.

If the window does not open, install them once:

```bash
sudo apt install libwebkit2gtk-4.1-0 libnotify4     # Debian · Ubuntu · Mint
sudo dnf install webkit2gtk4.1 libnotify            # Fedora
sudo pacman -S webkit2gtk-4.1 libnotify             # Arch · Manjaro
```

> Note the **4.1**. The older `4.0` packages will not work.

## Getting started

1. **Download and extract** using the button above.
2. **Run `./pxn-shield.sh`** and sign in with your PXN account. Every config you
   own arrives on its own. No account yet? Paste a `vless://` link instead — it
   works without one.
3. **Press the button.** That is the whole thing.

## If something goes wrong

**Nothing happens when I run it.** The window needs WebKitGTK 4.1 — see
[What it needs](#what-it-needs). Run it from a terminal and the missing library
will be named in the error.

**Permission denied.** The launcher lost its executable bit, usually from being
unzipped by a file manager. `chmod +x pxn-shield.sh PxnShield` fixes it.

**It starts but says whole-device mode is unavailable.** It could not ask for
administrator rights. Install `pkexec` (`policykit-1` on Debian and Ubuntu), or
run it with `sudo ./pxn-shield.sh`.

**It says "Couldn't connect".** Try another config from the Configs screen. If
none of them connect, your package may be out of data or expired — the Usage
screen says which.

**Anything else.** Open **Settings → Connection log → Open**, copy what it says,
and send it to us on WhatsApp. That log is the fastest route to an answer.

<div align="center">

### [💬 WhatsApp support][whatsapp] · [🌐 pxnstores.lk][site]

</div>

## Also available

| | |
|---|---|
| **Android** | [pxn-shield-android][android] |
| **Windows** | [pxn-shield-windows][windows] |
| **Linux** | you are here |

---

<div align="center">
<sub>

Built by **[PXN Stores LK][site]** in Sri Lanka · [Every release][releases]

This repository is the download channel. The source is private.

</sub>
</div>

[latest]: https://github.com/NightRiderr77/pxn-shield-linux/releases/latest
[releases]: https://github.com/NightRiderr77/pxn-shield-linux/releases
[tarball]: https://github.com/NightRiderr77/pxn-shield-linux/releases/latest/download/PXN-Shield-VPN-linux-x64.tar.gz
[site]: https://www.pxnstores.lk
[whatsapp]: https://wa.me/94761546544
[android]: https://github.com/NightRiderr77/pxn-shield-android
[windows]: https://github.com/NightRiderr77/pxn-shield-windows
