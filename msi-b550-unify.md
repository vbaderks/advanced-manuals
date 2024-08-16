# MSI B550 Unify Advanced Manual

## Introduction

This manual describes the MSI B550 Unify motherboard. This motherboard comes with a manual
and online help in the BIOS. There is still a lot of information missing.

Latest BIOS version: v1.D (AMD AGESA ComboAm4v2PI 1.2.0.C), 2024-8-5
Latest Manual version: v1.3, 2022-3

## Temperature sensors

- CPU (called CPU Core in Hardware Monitor): what the CPU itself reports
- Motherboards (called System in Hardware Monitor): General motherboard temperature based on temperature sensor(s) somewhere on the board.
- MOS: VRM temperature
- CHIPSET: Chipset (B550) temperature
- CPU Socket: Temperature of the CPU socket, based on mobo sensor
- PCI-E (PCIE 1) - First PCIe slot, where the graphics card typically is, so GPU temperature

## BIOS

The MSI B550 Unify comes with click bios 5

### Settings not enabled by default

The following settings are not enabled by default. In general most of these
settings are disabled to ensure a configuration that can boot.
In recent BIOS updates some of these settings are now default enabled.

|Name       |Default |Recommendation|
|-----------|--------|--------------|
|A-XMP      |Disabled|Disabled|
|ASPM Control for CPU PCIe|
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

Setting Wake Up Event By to OS in the BIOS allows the operating system to manage wake-up events instead of the BIOS. This gives the OS more control and flexibility, enabling advanced power management features and greater customization. It's a good choice for modern systems where the OS is equipped to handle these tasks effectively, offering better compatibility and user-specific settings.

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

XHCI Hand-off is the process by which control of USB devices (specifically those connected to USB 3.0/3.1 ports) is transferred from the system BIOS to the operating system during boot-up. This setting is crucial for ensuring that USB devices function correctly across different operating systems, especially older ones that may not have native support for xHCI.
XHCI = eXtensible Host Controller Interface
Disabled: When disabled, the operating system is expected to take over control of the xHCI controller directly without any hand-off from the BIOS. Modern operating systems with native xHCI support (like Windows 10 and newer Linux kernels) can handle this scenario.
Use Case: Disable this setting if you are running a modern operating system that fully supports xHCI, as it can simplify the boot process.

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

ASPM stands for Active State Power Management, a power management protocol for PCIe devices. It defines a set of power states (L0, L0s, L1, etc.) that devices can transition into when not in active use:
L0 State: The device is fully operational and active, with no power-saving features enabled.
L0s State: A low-power state that allows rapid transition back to L0. It's a shallow sleep state that provides minimal power savings but can reduce latency when the device wakes up.
L1 State: A deeper sleep state with greater power savings, but with a longer wake-up latency compared to L0s. The device is almost entirely powered down.
L2/L3 States: Further deep sleep states, rarely used in standard PCIe configurations due to significant wake-up latencies.
Auto: The system automatically decides the best ASPM settings based on the current workload and connected devices. It allows the BIOS to optimize power management dynamically without user intervention.
Use Case: Ideal for users who prefer a balance between performance and power savings without manual tuning.

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

PSS Support: Use this to enable or disable the generation of ACPI_PPC, _PSS, and _PCT objects. PPC tells the OS what Power States are available.
PSS defines the Power States. PCT is what allows the OS to control Power State. In the UEFI the PPC is configurable and the higher the value you set it to, the more levels of Power States are available for the O/S to dynamically change between.

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

Power supply idle control is a motherboard setting for older (or cheaper) power supplies.
A power supply requires a positive power draw to continue to feed power to the motherboard,
if it detects a low power draw it assumes that the motherboard is in sleep mode,
so it turns off until there's noticeable power draw. The problem is that older power supplies 
were designed where a minimum draw setting may be 5w, whereas a newer motherboard and CPU may 
only draw 1w at idle. So Idle control is used when your computer actually powers off 
instead of going to sleep on idle - it sets the threshold of low power draw at idle to like 
7.5w so it won't trigger the PSU to turn off.`
To prevent this issue from happening, it is important to ensure that the power supply supports 0A minimum 
load on the +12V circuit. These PSUs became commonplace starting in 2013.

AMD CBS - DF Common Options
|Name|Default|Options|Description|
|---|---|---|---|
|NUMA nodes per socket|Auto|Auto, NPS0, NPS1, NPS2, NPS4|NPS = Node per Socket?|

DF =  Data Fabric (or Infinity Fabric) which is AMD's interconnect architecture that links various components of the CPU, such as cores, memory controllers
NUMA stands for Non-Uniform Memory Access

AMD CBS - NBIO Common Options
|Name|Default|Options|Description|
|---|---|---|---|
|IOMMU|Auto|Auto, Disabled, Enabled|
LN2 Mode 1 => Auto
Package Power Limit => Auto
CPPC => Auto
CPPC Preferred Cores => Auto

NBIO =  North Bridge Input/Output. Historicly NB was a chip on the motherboard to control I/O with CPU and PCIe/memory. Now build in into the Ryzen CPU.


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

## MSI Loadline Calibration Control

mode 4

1050 - 1175 mV
1175 - 1375 mv
>1386 mV (mainly heat)

https://www.msi.com/blog/LLC_what_is_it_and_why_are_MSI_Z370_motherboards_the_best_choice_for_overclocking

(0%, 25%, 50%, 75%, 100% or Mode 1, Mode 2 etc.).
=> mode 1 more aggresive?

Its the Highest, I know right, its kind of backwards,
LLC level 1 is the tightest and LLC Level 8 is the lowest (the most vdroop)
