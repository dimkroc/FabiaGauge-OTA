# FabiaGauge OTA

Public OTA payload repository for `dimkroc/FabiaGauge-ESP32`.

This repository intentionally contains no application source code and no signing private keys.

Release automation will publish, in this order:

1. `firmware.bin`
2. `latest.sig`
3. `latest.json` last

Publishing the manifest last prevents devices from seeing a version whose firmware payload has not been uploaded yet.

`latest.json` is intentionally absent until the first signed firmware release exists.

The device must verify the Ed25519 manifest signature and firmware SHA-256 before switching OTA partitions.
