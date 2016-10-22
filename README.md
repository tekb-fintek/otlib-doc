Open Trading Library - Documentation - FinTek @ TekB
====================================================

# Description

*...*

# Editor Notes

## Binary Options Networks

* Forex
* Forex ECN

**Ed. Note:** OTC - TBD

## Trading Platforms - Binary Options Trading

* MetaTrader (MT4, MT5)
* Ctrader
* Others
  * **Ed. Note: Disributed by Broker**

## Building a Trading Terminal

### Introduction

*...*

### Operating System Compatibility - Microsoft Windows Emulation

*...*

#### 64-Bit and 32-Bit Architectures

> **Ed. Note:** Many brokers may be distributing editions of the
> respective trading platforms as compiled for 32-bit instruction set
> architecture (ISA) frameworks.
> 
> Short of building an independent multi-arch WINE ([advice at
> WINEHQ)[winemulti]), it may be advisable to select exactly one of a
> 64-bit or 32-bit installation of WINE, when installing.
>
> In order to manually verify that any single trading platform
> distribution is compiled for either a 32-bit or 64-bit Microsoft
> Windows architectures, beginning with a 64-bit edition of a Microsoft 
> Windows platform, a "Quick" way to check for the platform's ISA
> compatibility would be: To *install* the trading plaform, then verify
> which Microoft Windows "Program Files" directory the platform is
> installed to -- whether  the "Program Files" directory for the WoW64
> framework's 32-bit compatiblity (x86) features, or the main "Program
> Files" directory for the containing 64-bit operating system.
>
> **Theoretically, there *should be* a shell command available**
> - such as in the Cygwin platform - for analyzing any single
> *application program* or *shared library file*, for producing an
> automated analysis of the platform's compatibility features.
> Failing any *immediate solution*, as such, a "Manual check" may at
> least allow for a manner of a high-level perspective about the
> OS compatibiliy of the respective trading platform.

#### WINE on Ubuntu

**Advice via WINE HQ**

* [Installing WineHQ packages][wineubuntu]
* [Building Biarch Wine On Ubuntu][winemulti]

**Ubuntu Community Help Wiki**

* [Multi-Arch][ubuntumulti]


**Debian Wiki**

* [Multiarch HOWTO][debmulti]

**FIXME: Ubuntu WINE Team PPA may not be distributing packages for
Ubuntu 16.04 LTS (Xenial)? See repository**

**Short Example - Install 32-bit WINE, Wine Tricks, and Additional Fonts**

> `sudo dpkg --add-architecture i386`
> `# sudo add-apt-repository ppa:wine/wine-builds #` **See previous note**
> `sudo aptitude update`
> `sudo aptitude install wine:i386 winetricks msttcorefonts`

**TBD: Configuring a WINE Environment**

**Task: Determine Diagnostic Platform Information, Using winetricks**

> `script winetricks.log`
> `winetricks`
**Ed. Note: PC's processor may delay for a period of time, while
wineboot runs**

...Subsequently, selecting the **menu entry** in the GUI:
> Select the Default wineprefix

The winetricks application will create a `~/.wine/` directory, along
with appropriate configuration files.

...lastly
> Run Winecfg

To exit the GUI:
> Cancel

**Short Example - Installing a Trading Platform**

> `wine installer.exe`

Subsequently, determine the pathname of the installed application.

> `ls "~/.wine/drive_c/Program Files/"`

The installed application may then be run from the shell command line.

> `wine "~/.wine/drive_c/Program Files/path to app/app.exe"`

Similarly, the appropriate `wine` **shell command** may be added to a
**desktop** launcher or **menu** entry.


[wineubuntu]: https://wiki.winehq.org/Ubuntu
[winemulti]: https://wiki.winehq.org/Building_Biarch_Wine_On_Ubuntu
[ubuntumulti]: https://help.ubuntu.com/community/MultiArch
[debmulti]: https://wiki.debian.org/Multiarch/HOWTO
