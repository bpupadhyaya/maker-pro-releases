# Maker Pro — downloads & guide

**[Maker Pro](https://equalinformation.com/tools/maker-pro.html)** is the professional edition of
the free, MIT-licensed **[Maker](https://github.com/bpupadhyaya/maker)** — a local-first AI that
builds runnable tools from a conversation, 100% on your device. Nothing you type or index ever
leaves your machine.

**Without a license key, Maker Pro runs as the complete free Maker — forever, nothing crippled.**
A subscription unlocks the Pro features (personal quality engine, private knowledge/RAG, data
connectors, coding agent, publishing, sync, model pass, premium packs, and more).

---

## 1 · Download & install

Grab your platform from **[the latest release](../../releases/latest)**:

| Platform | File |
|---|---|
| macOS (Apple Silicon — M1 and newer) | `Maker-Pro-macos-arm64.dmg` |
| macOS (Intel) | `Maker-Pro-macos-x64.dmg` |
| Windows 10/11 (x64) | `maker-pro-windows-x64.zip` |
| Linux (x64) | `maker-pro-linux-x64.zip` |

**macOS** — native app, signed & notarized by Apple ✓
1. Open the downloaded **.dmg**.
2. Drag **Maker Pro** into your **Applications** folder.
3. Launch it from Applications (or Launchpad/Spotlight) — a real app window opens
   with the workshop. Quit any time with ⌘Q.

**Windows**
1. Unzip, double-click `maker-pro.exe`.
2. If SmartScreen shows "Windows protected your PC": **More info → Run anyway** (early builds are
   unsigned).

**Linux**
1. Unzip, then: `chmod +x maker-pro && ./maker-pro`

**First run (all platforms):** open **⛁ Models** (top right) and download a local model —
Qwen2.5-Coder 3B (~2 GB) is a fast start. One-time download; after that everything runs offline.

---

## 2 · Start your 14-day free trial

1. Go to **[equalinformation.com/tools/maker-pro.html](https://equalinformation.com/tools/maker-pro.html)**
   and click **Start 14-day free trial**.
2. Checkout is by Stripe ($0 today; $11.99/month after the trial — cancel anytime before it ends
   and you pay nothing).
3. Your **license key** (`MPRO-…`) arrives by email shortly after signup.

## 3 · Activate

1. In Maker Pro, click the purple **PRO** badge (top right).
2. Paste your license key into the **License** box → **Activate**.
3. You'll see **✓ Pro active**. Pro keeps working offline between renewals (a generous grace
   window — a trip or an outage never locks you out).

## 4 · Manage or cancel

- **[Manage your subscription](https://billing.stripe.com/p/login/cNi7sLeUmcNo4mwcQ56AM00)** —
  update your card, download invoices, or cancel (takes effect at the end of the period).
- Canceling never breaks the app: it simply returns to the full free Maker, and every tool you
  built stays yours.

## Help

Reply to your receipt email, or open an issue here. — © EqualInformation, LLC. Binaries only;
Maker Pro's source is proprietary. The bundled Maker core is MIT.

---

## Is it safe? (yes — here's how to verify)

**Downloading outside the App Store doesn't mean skipping Apple's malware check.**

- **Apple scanned it for malware.** The macOS builds are **notarized** — Apple's automated
  malware/virus scan ran on the exact file you download and issued a cryptographic pass. This is
  the *same* security scan the Mac App Store performs. macOS confirms it silently when you open the
  app (that's why there's no "unidentified developer" warning).
- **The publisher is verified by Apple** as **EqualInformation, LLC** (Apple Developer Team
  `XDC8C9HH9K`). You can check it yourself — right-click the app → *Get Info*, or in Terminal:
  ```sh
  codesign -dv --verbose=2 "/Applications/Maker Pro.app"    # → Authority: Developer ID Application: Bhim Upadhyaya
  spctl --assess -vv "/Applications/Maker Pro.app"          # → accepted, source=Notarized Developer ID
  ```
- **Verify the download wasn't tampered with.** Every release lists **SHA-256 checksums**
  (`SHA256SUMS.txt`). Compare after downloading:
  ```sh
  shasum -a 256 Maker-Pro-macos-arm64.dmg    # must match SHA256SUMS.txt
  ```
- **Open source you can read.** Maker Pro is built on the **MIT-licensed
  [Maker](https://github.com/bpupadhyaya/maker)** core — the engine that runs on your machine is
  public and auditable.
- **It stays on your machine.** Maker is local-first: your prompts, files, and work never leave
  your device (the Pro features that do use a server — Publish/Sync — are opt-in and clearly labeled).

- **Independently scanned clean.** Every build passed **VirusTotal** with **0 of 60+ antivirus
  engines** flagging anything — including the Windows/Linux binaries:

  | File | VirusTotal |
  |---|---|
  | `Maker-Pro-macos-arm64.dmg` | [0 / 60 engines](https://www.virustotal.com/gui/file/95b8a6d07abed9bca7d4872aaeffbca831f6fe45c0b74c900c43182f3b832c10) |
  | `Maker-Pro-macos-x64.dmg` | [0 / 60 engines](https://www.virustotal.com/gui/file/93d76583aae91beda25c5468bc50a5089719f53829df211ca2dfb2223878fb97) |
  | `maker-pro-windows-x64.zip` | [0 / 63 engines](https://www.virustotal.com/gui/file/6f8630f89d7c5dfc4ee47081d1dbc64d03066ceb72eb7e5aa865c8bc9e3f8b5f) |
  | `maker-pro-linux-x64.zip` | [0 / 65 engines](https://www.virustotal.com/gui/file/7562525d8ee385515558ea3f02e542d6f1b1c9f4eca5f32ca72b347f0791c8c0) |

*A signed Windows build (Authenticode) is on the roadmap; until then, Windows/Linux downloads carry
no OS-level scan, so the VirusTotal reports + SHA-256 checksums above are your verification.*
