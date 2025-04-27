# bd795ise
Notes on Minisforum BD795i SE.

This 16-core, 32-thread machine is very fast and capable, but like any modern ryzen, it loves to get very hot as well. I suggest you fiddle with the options in the BIOS to underclock and undervolt it to limit the thermal expansion of the chip. You can do so from BIOS version 1.09.

As it's a Zen4 chip, it's vulnerable to AMD's EntrySign vulnerability: https://bughunters.google.com/blog/5424842357473280/zen-and-the-art-of-microcode-hacking

## BD795i SE

Amazon link: https://www.amazon.es/-/en/dp/B0DQ9D3L35 

Minisforum EU store: https://minisforumpc.eu/products/bd

## Where can I find documentation

User manual: https://pc-file.s3.us-west-1.amazonaws.com/BD795i+SE/user+mannul/%E7%94%B5%E5%AD%90%E6%A1%A3%E8%AF%B4%E6%98%8E%E4%B9%A6+DRFXL+(MP_V1.0)+2024.10.14+(1).pdf

Installation guide: https://s3.us-west-1.amazonaws.com/pc.video.file/BD795I+SE+Install.mp4

## Bios update?

I bought it of Amazon and it came with the 1.09 BIOS. This version already allows you to underclock the CPU and set curve optimizers.

However, if you want you can update to 1.12: https://pc-file.s3.us-west-1.amazonaws.com/BD790i+BD770i/Bios/DRFXI_1.12_250213A.7z

I've read reports of people installing Windows and having tweaked options in the older bios and then updating to the 1.12 BIOS and running into some issues with secureboot as the BIOS update resets all previous choices. Something to watch out for.

Minisforum also has a questionable history of providing BIOS updates, so this might or might not happen...

## Bifurcation

Yes, it can do so, at least from 1.09: 8x8x 8x4x4x 4x4x4x4x.

## SATA

The BD795i SE doesn't have sata ports on the motherboard. If you want to use SATA drives, you can do so by using an M.2 PCIe to SATA card like this: https://www.amazon.es/dp/B0BCQ55NMB worked out of the box.

## Drivers for Windows

The drivers can be found here: https://pc-file.s3.us-west-1.amazonaws.com/BD795i+SE/Driver/DRFXL_AMD_MINISFORUM_Drivers_x64_240825.zip

You do not need to install the wifi drivers, there's no wifi onboard. However, it has the WiFi connectors for the backplate.

## Linux support?

Everything worked out of the box using a latest version of EndavourOS, it even detected an usb-wifi dongle I had attached.

## CPU undervolting and the BIOS

The BIOS is a bit... special and hides some option. The CPU also likes to run hot, idle it's easy 45c to ~50c. I thermally throttled to 70C myself and it works great. I also set the curve optimizer to -20 at least, you could push it further and stress testing it.

Another thing you can do is buy some PTM7950 from Honeywell from Ebuy7 as there's been some reports the thermal paste is dried out and the PTM7950 does a pretty good job at cooling the CPU: https://www.ebuy7.com/honeywell-7950-phase-change-thermal-pad-notebook-computer-phase-change-silicone-grease-cpu-thermal-paste-pad-patch-material-1.html - i'll post pictures once I got my PTM7950 in the mail.

<XXX: provide screenshots>

## NVME M.2 fan

Some photos show an NVME m.2 fan, it's not included in what I got.

## Fan support

The motherboard has 3 fan, 4-pin PWM headers, one to support the CPU and two others. You can always extend fans by using a fan hub, this worked well. I use ( ARCTIC Case Fan Hub 10 Fold PWM Fan Distributor with SATA Power, Black, ACFAN00175A ) https://www.amazon.es/dp/B0887VG14J

Noctua NF-P12 redux-1300 PWM keeps the case its located in cool.

## UEFI Shell

For some reason, i've only been able to get into the UEFI shell by disabling secureboot.. YMMV.

## Mounting motherboard in case

I use an older model Corsair 4000d, once you install a fan on the motherboard, I wanted to install another noctua non slim fan on the back exhaust, this is a couple mm too thick, I got a slim fan 120mm in the back and that worked just fine. Plan your fans! :)
