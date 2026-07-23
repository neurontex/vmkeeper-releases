# VMKeeper releases

Official release mirror for **VMKeeper**, backup and recovery for standalone VMware ESXi hosts (including free ESXi, no vCenter required).

- Product page, documentation and 30-day trial: **https://neurontex.eu/vmkeeper**

## Downloads

Grab the latest installer from the [Releases](../../releases) page. The same file is served from the product page; this mirror exists for convenience and download-reputation reasons.

## Verify your download

Every installer is Authenticode-signed by **SIA VSM (Riga, LV)**.

PowerShell:

```powershell
Get-AuthenticodeSignature .\VMKeeper-Setup-1.0.10.exe | Format-List Status, SignerCertificate
Get-FileHash .\VMKeeper-Setup-1.0.0.exe -Algorithm SHA256
```

Compare the hash with `SHA256SUMS.txt` attached to the release.

## What VMKeeper does

- Scheduled host-side backups with short-lived snapshots (agent over SSH, nothing inside guest VMs)
- Verification: chain check, sha256 baseline, test recovery into an isolated VM
- Offsite deduplicated copies to QNAP over SSH or Amazon S3 (3-2-1)
- Fail-closed capacity prechecks, delta monitoring, email reports
- Recovery is never license-gated

Console languages: EN, LV, RU, DE, FR, ES.

VMKeeper by NEURONTEX. Legal seller: SIA VSM.
