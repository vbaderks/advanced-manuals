# MSI B550 Unify Advanced Manual

## Introduction

This manual describes the MSI B550 Unify motherboard. This motherboard comes with a manual
and online help in the BIOS. There is still a lot of information missing.

Latest BIOS version: 7D13v1D (AMD ComboAm4v2PI 1.2.0.C), 2024-8-9
Latest Manual version: v1.3, 2022-3

## Temperature sensors

- CPU (called CPU Core in Hardware Monitor)
- Motherboards (called System in Hardware Monitor)
- MOS?
- CHIPSET
- CPU Socket
- PCI-E

## BIOS

The MSI B550 Unify comes with click bios 5

### Settings not enabled by default

The following settings are not enabled by default. In general most of these
settings are disabled to ensure a configuration that can boot.
In recent BIOS updates some of these settings are now default enabled.

|Name       |Default |
|-----------|--------|
|A-XMP      |Disabled|Disabled|
|ASPM Control for CPU PCIe|
|SVM Mode (Secure Virtual Mode)|Disabled|
|SR-IOV Support|Disabled|
|Data Link Feature Exchange|Disabled|

### EZ Mode

Game Boost
 CPU
 A-XMP Profile 1
 A-XMP Profile 2

### Advanced Mode

Settings\Boot

Full Screen Logo Display [Enabled Disabled]

Bootup NumLock State [On Off]

Info Block effect [Unlock]

POST Beep [Disabled]

#### Settings\System Status

This page provides an overview of detected components and the CPU
It does not provide configuration items.

#### Settings\Advanced

This page provides several sub menus and 1 option.

|Name|Default|Options|Description|
|---|---|---|---|
|MSI Driver Utility Installer|Enabled|Enabled, Disabled|Allowing platform drivers download through Windows Update.

#### Settings\Advanced\Wake Up Event Setup

|Name|Default|Options|Description|
|---|---|---|---|
|Wake Up Event By|BIOS|BIOS, OS|Select the wake up event by BIOS or OS

Settings\Security\Trusted Computing

Security Device Support [Enabled Disabled]
AMD fTPM switch [AMD CPU fTPM]

SHA-1 PCR Bank [Enabled Disabled]
SHA256 PCR Bank [Enabled Disabled]

#### Settings\Advanced\AMD Overclocking\AMD Overclocking\Precision Boost OVerdrive

- Precision Boost Overdrive [Advanced]
This is main option to enable or disable Precision Boost Overdrive
Options: 
 - 

#### Settings\Advanced\USB Configuration

|Name|Default|Options|Description|
|---|---|---|---|
|XHCI Hand-off|Enabled|Enabled, Disabled|TODO|
|Legacy USB Supports|Enabled|Auto, Enabled, Disabled|Required for the legacy OS such as ms-dos and the bios itself (screenshot ) |
|Enhance Mouse Pointer Speed|1|?|TODO|

#### Settings\Advanced\ACPI Settings

ACPI = Advanced Configuration and Power Interface

|Name|Default|Options|Description|
|---|---|---|---|
|Power LED|Blinking|Blinking, Dual Color|This controls if the Power LED will blink or change color. Dual Color work by chaning the polarity and requires a Bi-color LED.|
|Legacy USB Supports|Enabled|Auto, Enabled, Disabled|Required for the legacy OS such as MS-Dos. The MSI BIOS itself also uses for the screenshot functionality.|

PBO Limits [Auto]

#### Settings\Advanced\Integrated Peripherals

|Name|Default|Options|Description|
|---|---|---|---|
|VGA Detection|Auto|Auto, Ignore|This controls of the BIOS tries to detect a discrete video card.|
|Onboard Lan Controller|
|LAN Option ROM|
|Network stack|
|SATA Mode|AHCI Mode|AHCI Mode, RAID Mode|
|SATA1 Hot Plug|Disabled|Disabled, Enabled|
|SATA2 Hot Plug|Disabled|Disabled, Enabled|
|SATA3 Hot Plug|Disabled|Disabled, Enabled|
|SATA4 Hot Plug|Disabled|Disabled, Enabled|
|SATA5 Hot Plug|Disabled|Disabled, Enabled|
|SATA6 Hot Plug|Disabled|Disabled, Enabled|
|HD Audio Controller|

#### Settings\Advanced\PCI Subsystems Settings

|Name|Default|Options|Description|
|---|---|---|---|
|Re-Size BAR Support|Enabled|
|Above 4G memory/Crypto Currency mining|Enabled|
|PCI_E1 Gen Switch|Auto|
|Chipset Gen Switch|Auto|
|PCI_E1 Lanes Configuration|Auto|
|M2_2/M2_3 Lanes Source|Chipset|
|SR-IOV Support|Disabled|Disabled, Enabled|The SR-IOV (Single Root I/O Virtualization) interface is an extension to the PCI express (PCIe) specification. It enables the BIOS to allocate more PCI resources to PCIe devices. Allows better performance for virtualized PCIe hardware.|
|Data Link Feature Exchange|Disabled|Disabled, Enabled|PCIe 4.0.7 feature to improve bandwidth (for PCIe device that support it).|
|ASPM Control for CPU PCIe|Disabled|Disabled, L0s Entry, L1 Entry, L0 and L1 Entry, Auto|

#### Overclocking

|Name|Default|Options|Description|
|---|---|---|---|
|OC Explore Mode|Normal|Normal, Expert|
|CPU Ratio Apply Mode|All Core|All Core, Per CCX|
|CPU Ratio|Auto|Auto, ####|Sets the CPU ratio that is used to determine the CPU clock speed|
|Advanced CPU Configuration|||Opens the sub menu Advanced CPU Configuration|


#### Overclocking\Advanced CPU Configuration

|Name|Default|Options|Description|
|---|---|---|---|
|AMD Overclocking (sub menu)|
|AMD CBS (sub menu)|
|SVM Mode|Enabled|Disabled, Enabled|Enables/disables CPU virtualization suppport. SVM stands for Secure Virtual Machine and it the same option as Intel VT-x. It will enable additional CPU instructions (VMRUN, VMLOAD, VMSAVE, CLGI, VMMCALL, INVLPGA, SKINIT, and STGI) to provide hardware assisted virtualization. When this option is enabled Windows will activated additional security features like Core isolation. It is required to use WSL version 2 in Windows 11. It was by default disabled, because the additional security features of Windows 11 may have a (mininal) impact on performance benchmarks. Latest BIOS is is default enabled|
|NX Mode|Enabled|Enabled, Disabled|Controls the No-Execute page protection function.
|PSS Support|Auto|Auto, Enabled, Disabled|Enables/disables the generation of ACPI _PPC, _PSS and _PCT objects
|Performance Regulator|Disabled|Disabled, Cinebench R15, Cinebench R11.5, GeekBench, AIDA64 Memory, LN2 Mode||
|Spread Spectrum|Auto|Auto, Disabled, Enabled|Enables or disables the EMI generated by generator pulses|
|CPU VDD_SoC Current Optimization|Auto|Auto, Custom Setting|Custom setting will 4 more options visible|
|CPU Temperature Display|Enabled|Enabled,Disabled|Defines which info will be shown on POST leds, after system POST|

#### Overclocking\Advanced CPU Configuration\AMD Overclocking

This screen is a main MSI overclock configuration screen. It is duplicate
of the Settings\Advanced\AMD Overclocking\AMD Overclocking\ screen

Overclocking\Advanced CPU Configuration\AMD Overclocking\Curve Optimizer

#### Overclocking\Advanced CPU Configuration\AMD CBS

This will open the AMD CBS screen (CBS = Common BIOS Settings)

AMD CBS - CPU Common Options
|Name|Default|Options|Description|
|---|---|---|---|
|Core Performance Boost|Auto|Auto, Disabled|
|Global C-state Control|Auto|Auto, Disabled, Enabled|Controls IO based C-state generation and DF C-states.|
|Power Supply Idle Control|Auto|Auto, Low Current Idle, Typical Current Idle|

AMD CBS - DF Common Options
|Name|Default|Options|Description|
|---|---|---|---|
|NUMA nodes per socket|Auto|Auto, NPS0, NPS1, NPS2, NPS4|NPS = Node per Socket?|

AMD CBS - NBIO Common Options
|Name|Default|Options|Description|
|---|---|---|---|
|IOMMU|Auto|Auto, Disabled, Enabled|
LN2 Mode 1 => Auto
Package Power Limit => Auto
CPPC => Auto
CPPC Preferred Cores => Auto

|Name|Default|Options|Description|
|---|---|---|---|
|Precision Boost Overdrive|Auto|Auto, Disabled, Enabled, Enhanced Mode 1, Enhanced Mode 2, Enhanced Mode 3
Enhanced Mode 4, Eco-Mode (45W), Eco-Mode (65W), Eco-Mode (95W), Advanced |This controls the AMD PBO option.|

Disabled = Precision Boost Overdrive disabled
Enabled = PPT=500W, TDC=245A, EDC 215A
Enhanced Mode 1 = AutoOC ?
Enhanced Mode 2 = AutoOC, Boost Override CPU = 100 (PPT=142W, TDC=95A, EDC=140A)
Enhanced Mode 3 = AutoOC ?
Enhanced Mode 4 = AutoOC, Boost Override CPU = 200 (PPT=142W, TDC=95A, EDC=140A)
Advanced

Motherboard = PPT=500W, TDC=245A, EDC 220A

#### Overclocking\CPU Specifications

This page provides information about the installed CPU.
Most of the information can also be retrieved using tools like HWiNFO.
There are no configurable options in this page.

xHCI (Extensible Host Controller Interface) Specification for Universal Serial Bus 3.0
Motherboards with USB 3.0 might have a xHCI configuration. It controls how the USB 3.0 ports behave. You can enable it, so USB 3.0 ports always act as USB 3.0
XHCI Mode is Disabled - The on-board USB 3.0 port function like a 2.0 port
XHCI Mode is Enabled - The on-board USB 3.0 port function like a 3.0 port

For reference: http://answers.microsoft.com/en-us/...hand-off/edff12b1-b38c-4e16-8149-8441032b6771

Resizable Base Address Register
=> Allows better access to VRAM instead in 256MB chunks. Can have up to 10% more performance in viedeo games.

Above 4GB decoding
=> Allows PCI devices to be mapped above 4GB. Required for Resizable BAR. Requires a 64-bit OS.