# fieldwatch-signatures

**Additional Wi-Fi and BLE signatures for [Fieldwatch](https://github.com/OffGridPete/Fieldwatch).**

A community catalog of radio signatures in Fieldwatch's signature interchange format
(`radio-signatures`, `formatVersion: 1`), maintained by [DragonXen](https://github.com/DragonXen).

## ℹ️ About Fieldwatch

[Fieldwatch](https://github.com/OffGridPete/Fieldwatch), by [OffGridPete](https://github.com/OffGridPete),
is a receive-only Wi-Fi and Bluetooth LE observer for Android: entirely passive, no account,
no server, works offline. It uses an extensible signature library to identify radio sources
around you — tracker tags, drones (Remote ID), body cameras, vehicles, and more.

This repository extends that library with community-contributed signatures.

## 📡 Included signatures

Device families covered by this catalog:

- **Apple** — devices and services (beacons via `MANUFACTURER_DATA`, companyId `0x004C`)
- **Google** — additional service UUIDs and datatypes
- **Samsung** — Galaxy devices
- **Xiaomi** — devices and accessories
- **ZTE** — network equipment / devices
- **Intebras** — devices
- **MXT Tracker** — trackers
- **Fitness Machine** — gym equipment over BLE (FTMP)
- **YSCCU** — *Yamaha Small Communication Control Unit*, the BLE module built into
  Yamaha motorcycles and scooters, used by the official Y-Connect app (`kind: VEHICLE`)

## 🔢 Catalog state

| Field | Value |
|-------|-------|
| File | `fieldwatch-signatures.json` |
| Format | `radio-signatures` (formatVersion 1) |
| Reference app version | 1.2.2 |
| catalogVersion | 118 |

## 📥 How to use

1. Download [`fieldwatch-signatures.json`](./fieldwatch-signatures.json).
2. Import the catalog in Fieldwatch through the signature library
   (the app supports adding new signatures on the fly).
3. Enable/disable each signature as needed — all come with `enabled: true`.

> ⚠️ Keep the file name when sharing. Signatures marked with
> `builtIn: false` are community additions to Fieldwatch's original catalog.

## 🤝 Contributing

Found a device that isn't identified, or a wrong signature?
Open an [issue](../../issues) with as much detail as possible:
the BLE advertisement type (`SERVICE_DATA`, `MANUFACTURER_DATA`),
observed UUIDs / company IDs, and the device that transmitted them.

## 🙏 Credits

- [OffGridPete/Fieldwatch](https://github.com/OffGridPete/Fieldwatch) — the app and
  the radio signature interchange format. This project only extends its library;
  it is not affiliated with Off Grid Pete LLC.