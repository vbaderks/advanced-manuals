# MSI B550 Unify Advanced Manual

## Temperature sensors

- CPU (called CPU Core in Hardware Monitor)
- Motherboards (called System in Hardware Monitor)
- MOS?
- CHIPSET
- CPU Socket
- PCI-E

## BIOS

The MSI B550 Unify comes with click bios 5

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

#### Settings\Advanced Wake Up Event Setup

Wake Up Event By [BIOS - OS]

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

#### Overclocking\Advanced CPU Configuration

AMD Overclocking

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

AMD CBS

This will open the AMD CBS screen (CBS = Common BIOS Settings)


SVM Mode

SVM stands for Secure Virtual Machine and it the same option as Intel VT-x
It will enable additional CPU instructions (VMRUN, VMLOAD, VMSAVE, CLGI, VMMCALL, INVLPGA, SKINIT, and STGI) to provide hardwar assisted virtualization.
When this option is enabled Windows will activated additional security features like Core isolation.
It is required to use WSL version 2 in Windows 10.

Options: Enabled \ Disabled
Default: Disabled. It is by default disabled, because the additional security features of Windows 10 may have a (mininal) impact on performance benchmarks.

NX Mode

PSS Support

Performance Regulator

Spread Spectrum

CPU VDD_SoC Current Optimization

CPU Temperature Display
Options: Enabled \ Disabled
Default: Enabled

#### Overclocking\Advanced CPU Configuration\AMD Overclocking

This screen is a main MSI overclock configuration screen. It is duplicate
of the Settings\Advanced\AMD Overclocking\AMD Overclocking\ screen


Overclocking\Advanced CPU Configuration\AMD Overclocking\Curve Optimizer

Overclocking\Advanced CPU Configuration\AMD CBS

AMD CBS - CPU Common Options
Core Performance Boost => Auto
Global C-state Control => Auto
Power Supply Idle Control => Auto

AMD CBS - DF Common Options
Numa nodes per socket => Auto

AMD CBS - NBIO Common Options
IOMMU => Auto
LN2 Mode 1 => Auto
Package Power Limit => Auto
CPPC => Auto
CPPC Preferred Cores => Auto


xHCI (Extensible Host Controller Interface) Specification for Universal Serial Bus 3.0
Motherboards with USB 3.0 might have a xHCI configuration. It controls how the USB 3.0 ports behave. You can enable it, so USB 3.0 ports always act as USB 3.0
XHCI Mode is Disabled - The on-board USB 3.0 port function like a 2.0 port
XHCI Mode is Enabled - The on-board USB 3.0 port function like a 3.0 port

For reference: http://answers.microsoft.com/en-us/...hand-off/edff12b1-b38c-4e16-8149-8441032b6771
