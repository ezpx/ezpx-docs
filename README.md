# Untethered data exchange
EZPX leverages untethered wireless transport protocols to exchange data between devices in close range, using minimal and noninvasive UI to manage user consent on both ends and asymmetric encryption to protect your data in transit.

## How it works?
EZPX uses **Bluetooth** discovery to limit its operational range to devices in close proximity, while data is transmitted over **WiFi**. Direct **untethered** transmission is also possible between mobile devices that support a common protocol:
* **[WiFi P2P](https://developer.android.com/guide/topics/connectivity/wifip2p.html)** or **[WiFi Aware](https://developer.android.com/guide/topics/connectivity/wifi-aware.html)** can be used between supporting Android devices.
* **AWDL** can be used between supporting Apple devices.

Devices publicly announce the availability of some data using multicast DNS (**Bonjour/mDNS**), thereby enabling EZPX on the receiving device. Upon activation (and user confirmation) on that end, a grant request popup appears on the source device. Once approved, connection is established is data is transmitted.

## Applications
EZPX's most obvious application is cross-device credential transmission. If your user is signed in an app on a tablet and opens your app on their phone, you could use EZPX to reveal a `Login with your tablet` button. This allows multiple devices to share credentials without requiring any roundtrip to your servers (the alternative would be to e.g. generate a one-time QR code on the source device).

## Requirements
* Android 4.1 or later (API level 16).
* iOS 8.0 or later.
