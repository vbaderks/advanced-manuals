# Advanced Manual for Windows 10

## Introduction

This manual is intended to provide background information about Windows 10 and how to configure it.
By design it is intended for the latest release, currently: 19042.782

## References

https://www.ghacks.net/2016/06/18/turn-off-windows-10-features/

## Windows features that can be turned on and off

The generic advice is to only install/enable features that will be used. A minimal system
is easier to maintain and more secure.

### .NET Framework 3.5 (includes .NET 2.0 and 3.0)

- Default: not installed.
- Purpose: .NET Framework is a framework to execute application build for .NET 3.5 and older.
- Advice: Keep it disabled. This is only needed to run legacy .NET applications. Windows will install it when it needs it.

### Active Lightweight Directory Services

Default: not installed.

### Device Lockdown

- Purpose: TODO

### Containers

Default: not installed.

### Hyper-V

Default: not installed.

- Hyper-V Management Tools

### Internet Explorer 11

- Default: installed.
- Purpose: The legacy Interbrowser based on the Trident 7.0 HTML engine.
- Advice: uninstall, unless needed to view a legacy web site that only works with IE.

### Microsoft XPS Document Writer

Default: installed.
Advice: uninstall

### Virtual Machine Platform

Default: not installed.
What is it: Supports virtualization for WSL2 Windows Subsystem for Linux v2.
Advice: install when you want to use Linux distributions.

### Windows Sandbox

Default: not installed.
What is it: ?
Advice: install when you need often to try out applications from sources that may be unreliable or could have a
big impact on your Windows installation.

### Windows Subsystem for Linux

- Default: not installed.
