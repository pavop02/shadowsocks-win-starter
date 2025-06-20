# Shadowsocks Windows Starter

A simple and reliable way to run Outline VPN (shadowsocks) on Windows with just a double-click without heavy and complicated GUI clients.

This lightweight .bat script launches `sslocal.exe` and enables the system proxy automatically until the console window is closed.

## What it does

• Starts `sslocal.exe`
• Enables system-wide proxy on `127.0.0.1:1080`  
• Keeps the proxy active while the cmd window is open  
• On key press, disables proxy and terminates `sslocal.exe`

## Required file structure

shadowsocks/
├── proxy.bat
├── config.json
└── sslocal.exe

## Quick guide

1. Download Shadowsocks-Rust for Windows (MSVC version):  
   [https://github.com/shadowsocks/shadowsocks-rust/releases](https://github.com/shadowsocks/shadowsocks-rust/releases)  
2. Place `sslocal.exe` and `proxy.bat` in the same folder  
3. Obtain your Outline Access Key (starts with `ssconf://...`)  
4. Edit it to start with `https://` instead of `ssconf://`, e.g.:  
   `https://example.com/en/abc123/xyz456#abc123`  
5. Open the link in a browser — it shows your VPN config JSON  
6. Remove the `"prefix":` line from the config  
7. Save the result as `config.json` in the same folder  
8. Run `proxy.bat` (preferably as Administrator)

## Keywords

shadowsocks, shadowsocks-rust, sslocal, vpn, proxy, windows, batch, batch-script, batch-file, vpn-client, script, starter, launcher

## Author:

by [@pavop02](https://github.com/pavop02)
