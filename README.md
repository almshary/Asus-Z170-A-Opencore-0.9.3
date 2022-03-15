# Asus-Z170-A-Opencore 0.7.9

This is an OpenCore version of ASUS Z170-A Hackintosh EFI. It works on macOS Monterey 12.3 (21E230). FCPX GPU rendering works smoothly. HDR can be enabled.

![Z170A](https://github.com/almshary/Asus-Z170-A-Opencore/blob/main/ScreenShot12.3.png)

## Notes
1. I chose 15 USB ports in my USB map. 2x USB 3.0(front) + 4x USB 3.0(back) + 2x USB 2.0(back) + Bluetooth(internal via M.2) = 15 ports. Generally there's no front USB 2.0 port on ITX cases so I didn't include onboard USB 2.0 ports(HS11/HS12). I believe this is a reasonable trade-off for most people. However if you bought some strange Wi-Fi card which requires USB 2.0 header, you need follow [this guide](https://dortania.github.io/USB-Map-Guide/) to create your own USB map.
2. For onboard 3.5mm audio output you need to plug into the green(line out) jack. If you restart from Windows, there will be no sound. This is a issue in the Windows Realtek driver as they modified the DSDT. Always shutdown from windows then boot to macOS.

![Z170A](https://user-images.githubusercontent.com/5692682/137645705-51759558-6d42-4e23-a6f8-bee58bf773fa.jpg)

## Hardware
| Item | Brand | Model | Driver | Comment |
|-----|-----|-----|-----|-----|
| Motherboard | ASUS | Z170-A | | |
| CPU | Intel | i7-6700K | | |
| RAM | Corsair | Vengeance LPX 32GB (4x8GB) DDR4 DRAM 3200MHz | | |
| iGPU | Intel | HD Graphics 530 | built-in | Headless mode |
| dGPU | MSI | RX 580 Armor 4GB | built-in | 2304 SP |
| SSD | Kingston | HyperX Predator 240GB PCIe Gen2 x4 (M.2) | [NVMeFix](https://github.com/acidanthera/NVMeFix) | |
| Wireless | Fenvi | T919 Wi-Fi 2.4/5GHz and Bluetooth 4.0 PCI-E Card | built-in | |
| Ethernet | Intel | I219-V | [IntelMausi](https://github.com/acidanthera/IntelMausi) | |
| Audio | Realtek | ALC1150 | [AppleALC](https://github.com/acidanthera/AppleALC) | |
| PSU | EVGA | SuperNOVA 650 G1 | | |
| Case | inWin | 303 | | |
| Monitor | Benq | VZ2470 | | |

 

## BIOS Setup
| Name | Option |
| --- | --- |
| SW Guard Extensions (SGX) | Disabled |
| CFG Lock | Disabled |
| VT-d | Disabled |
| Above 4G Decoding | Enabled |
| Primary Display | PCIE |
| iGPU-Multi-Monitor | Enabled |
| DVMT Pre-Allocated | 128M |
| IOAPIC 24-119 Entries | Disabled |
| Network Stack | Disabled |
| Legacy USB Support| Enabled |
| Fast Boot | Disabled |
| OS Type | Other OS |
| Launch CSM | Disabled |

## Acknowledgement
Apple for macOS

acidanthera for OpenCore etc.

headkaze for Hackintool
