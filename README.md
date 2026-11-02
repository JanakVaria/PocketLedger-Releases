# PocketLedger — free Android downloads

PocketLedger is a free, offline Android app for personal budgeting and shared expenses. Each installation has its own local ledger; other people are contacts you enter, and they do not need accounts.

**[Download PocketLedger.apk](https://github.com/JanakVaria/PocketLedger-Releases/releases/latest/download/PocketLedger.apk)** · **[Latest release and checksums](https://github.com/JanakVaria/PocketLedger-Releases/releases/latest)**

Requires Android 8.0 (API 26) or newer. No subscription, sign-in, bank connection, or money-transfer service is involved. This repository contains downloads and documentation; the app's source code is maintained privately.

## Install

1. Download `PocketLedger.apk` from the latest release on this repository.
2. Open the downloaded APK on your Android phone.
3. If Android asks, allow the browser or file manager you are using to install apps from this source, then install PocketLedger.
4. Open the app and add your contacts and expenses. The ledger starts empty; optional sample data is an explicit action in More.

No GitHub account is needed to download the public APK. Installation prompts can differ by Android version and manufacturer. You do not need to root the phone or disable Play Protect.

## Features

- Personal and shared expenses with equal, exact-amount and percentage splits.
- Contacts, groups, net balances and full or partial repayment records.
- Monthly overall and category budgets based only on your allocated shares.
- Day-first `dd-MM-yyyy` dates, participant Select all, and safe contact deletion that protects financial history.
- JSON backup/restore and CSV export through Android's system file picker.
- Light/dark themes and launcher shortcuts for expenses, repayments and budgets.

Recording a repayment only updates the ledger; the app does not transfer money. Contacts with expenses or repayments can be archived, and cannot be deleted even when their balance is zero.

## Updates and data

Install a newer production APK over your existing production installation without uninstalling the app. Future versions will use the same signing identity and increasing version codes. Updates are manual; check the latest-release link for new versions.

Export regular JSON backups from **More → Export JSON backup**. Keep backups outside app-private storage and retain a second copy. Uninstalling the app or clearing its storage deletes the local ledger. The app does not provide cloud recovery.

### Switching from an earlier debug APK

The old debug build and this production release have different signing keys, so Android cannot install the release directly over the debug build.

Before uninstalling the debug build, export a JSON backup, open it to check that it contains your expected records, and keep another copy. Save it in Downloads, an external drive, or another location retained after uninstalling. Then manually uninstall the debug app, install this release, and use **More → Restore JSON backup**. Verify your restored balances and records before deleting any backup copies. No script in this public repository uninstalls your debug app.

## Privacy

PocketLedger stores the people, groups, expenses, repayments, notes and budgets you enter in local app storage. It has no sign-in, analytics, advertising, external server, or internet permission. It does not read your phone's address book. Android system cloud backups and device-transfer backups are disabled for the app.

Exports and backups contain the records you entered. They are written only when you choose to export, to the location/provider you select in Android's file picker; that provider may be a cloud service if you select one. Keep those files private. Visiting GitHub or downloading an APK is subject to GitHub's own privacy policy.

## Verify the download

Every release includes `SHA256SUMS` with the APK's SHA-256 digest and `SIGNING-CERTIFICATE.txt` with its public signing-certificate fingerprint. On macOS or Linux, place the APK and checksum file in one directory and run:

```sh
shasum -a 256 -c SHA256SUMS
```

On Windows PowerShell, run `Get-FileHash .\PocketLedger.apk -Algorithm SHA256` and compare it with `SHA256SUMS`.

Permanent production signing-certificate SHA-256:

```
e82befa8959ba97a0c395e64b0da3ee5cec253129fc17b97f70021e7acd119fe
```

This certificate fingerprint identifies the app signer; it is different from the per-file APK checksum, which changes between releases.

## Regional availability

This initial direct-download release is intended mainly for India. Android's developer-verification rules may affect installation in other regions and during the announced global expansion in 2027. See [Android's current verification guidance](https://developer.android.com/developer-verification/guides). Free GitHub downloads do not constitute Google Play publication or developer verification.
