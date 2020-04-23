# AB350 Gaming Hackintosh
My EFI files for my desktop hack. Motherboard is a Gigabyte AB350 Gaming 1.

**I will not be providing support for this EFI if you have issues copy/pasting it to use yourself but if you find actual issues with the EFI (eg. a boot arg to make it work better), please leave a GitHub issue.**
Contributions are welcomed to make this better for everyone.

## Intended system config
- A Gigabyte AB350 Gaming 1 motherboard, rev 1.0 on the F50 BIOS
- AMD Ryzen 5 1600 CPU
- Gigabyte reference RX Vega 56 GPU in first PCIe x16 slot
- Apple AirPort BCM943602CS Wireless card in first PCIe x1 slot

## "features"
- Onboard audio configured properly
- I *think* sleep works but don't quote me on that
- All NVMe drives in the M.2 slot will be properly detected as internal and not external 
- anything in the first PCIe x1 slot will be set as BuiltIn
- Working Ethernet + it has been set as BuiltIn
- Wi-Fi, BT, AirDrop, Continuity, Handoff, Apple Watch unlock, and everything else works **if you use the card listed here**. Not sure if any other cards will work (although they likely will if they're natively supported)
- Kernel slide has been calculated and set so it'll actually boot macOS lol

## Known issues
- Displays sometimes won't initialize properly on boot and nothing will be visible after the graphics driver loads. Workaround is to restart until displays do initialize properly when the video driver loads.
- Sidecar doesn't work (supposedly other people got it to work but I never could (tried different SMBIOS and many boot args).
- Apple Watch simulator in Xcode doesn't work (normal for AMD hacks apparently)
- Apple Watch unlock sometimes randomly doesn't work 

## Other
- I have not configured DRM since I don't need it. I don't know if it works, it may or may not work.

## Basic Installation Instructions
For the record, I don't condone the use of pre-made EFIs for hackintoshes, everyone's computers can be different even if the hardware seems identical. I want to offer this EFI as a starting point for people who are having trouble setting up their hackintosh, and I would prefer if you just looked at the config.plist to see what you need to make your EFI work.
Nevertheless, if you still want to use this entire EFI for your hack, some intentionally vauge instructions are below.
1. Clone the repo and extract the zip file
2. Copy the 'EFI' folder to the EFI partition of your macOS installer USB
3. Generate SMBIOS for iMacPro1,1 and add it to the config.plist
4. Boot PC

These instructions are intentionally vauge as starting fresh with a 'vanilla install' is recommended.
A vanilla install guide can be found [here](https://dortania.github.io/OpenCore-Desktop-Guide).

## Credits
- everyone developing for the hackintosh community
- the [dortania team](https://github.com/orgs/dortania/people)
