# ab350-gaming-hack
My EFI files for my desktop hack. Motherboard is a Gigabyte AB350 Gaming 1.

-=**no support is provided for this repo**=- - but if you do find actual issues, feel free to leave a github issue

Actual files will be uploaded soon

## Intended system config
- A Gigabyte AB350 Gaming 1 motherboard, rev 1.0 on the F50 BIOS
- AMD Ryzen 5 1600 CPU
- Gigabyte reference RX Vega 56 GPU in first PCIe x16 slot
- Apple AirPort BCM943602CS Wireless card in first PCIe x1 slot

## "features"
- Onboard audio configured properly, requires no further config
- All NVMe drives in the M.2 slot will be properly detected as internal and not external 
- AirPort card PCIe slot set as BuiltIn
- Working Ethernet + it has been set as BuiltIn
- Wi-Fi, BT, AirDrop, Continuity, Handoff, Apple Watch unlock, and everything else works **if you use the card listed here**. Not sure if any other cards will work (although they likely will if they're natively supported)
- Kernel slide has been calculated and set so it'll actually boot macOS lol

## Known issues
- Displays sometimes won't initialize properly on boot and nothing will be visible after the graphics driver loads. Workaround is to restart until displays do initialize properly when the video driver loads.
- Sidecar doesn't work (normal for AMD hacks)
- Apple Watch simulator in Xcode doesn't work (again, normal for AMD hacks)
- Apple Watch unlock sometimes randomly doesn't work 

## Other
- I have not configured DRM. It may or may not work.
- you will need to generate SMBIOS for iMacPro1,1 and put the info into the config.plist if you want working iServices
