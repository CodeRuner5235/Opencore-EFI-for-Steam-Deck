# Opencore-EFI-for-Steam-Deck

This project is for using [Opencore](https://dortania.github.io/OpenCore-Install-Guide/) to run MacOS on the Valve Steam Deck.
This is not to give you a free EFI, but to help you built your own.

The MacOS versions that I will be targeting are Catalina (10.15) and Big Sur (11).
The project can be found [here](https://github.com/CodeRuner5235/Opencore-EFI-for-Steam-Deck/)

My reasoning here is that Apple changed a lot of things between Big Sur and Monterey so
I will be focusing on these two versions for now. I will deninetly try to get Monterey
and up running in the future. 

As of right now, there are many, MANY, issues the must be overcome before MacOS is even
remotely usable in the Steam Deck. My first and foremost concern is getting the installer
to boot using successfully while using the built in screen. This should be (hopefully) 
possible by spoofing the custom APU to an Intel iGPU. If by some miracle this works, the
next issue is graphics accelleration. Hopefully, this issue can be fixed with what the
guys at [WhateverRed](https://github.com/NootInc/WhateverRed) are working on. In fact, 
their project is why I am limiting the MacOS versions to Catalina and Big Sur. 
If (and big if) we can get these two issues sorted out, we only have a couple other 
things to worry about.

1. Wifi/Bluetooth-
   Unfortunelty, it looks like the wifi chipset that the Steam Deck uses is from Realtek
   wich basicly means that it will by unsupported with no fixing it. So if you want wifi
   you will probably have to use an external wifi dongal or wired connection though the type-C port.
 
2. Type-C and SD card reader-
   Kinda nessecary to do anything. Shouldnt be too hard to get working.
 
 
3. Touch screen/mouse pads- 
   Hoping that the touch screen uses Multitouch HID and we can use a VoodooI2C plugin.

4. Audio

5. Controller controls- 
   I am hoping this can be fixed by installing steam and using its mapping. If not, 
   ACPI patching will probably be needed.

6. Everything else-
   Things like the brightness, microphone, etc...

#IT IS NOT RECOMENDED TO USE THIS EFI AS IS.
#IT IS HERE TO HELP YOU BUILD YOUR OWN.

This can be accomplished by following the dortania guide as linked below
and changing these things.

1. you need to use SSDT-Time to build an EC for a laptop and add it
   to your APCI folder
   
2. You need SSDT-CPUR in you APCI folder

3. You will need the VooDooI2C.kext and VooDooI2CHID.kext

4. You will need USBToolbox.kext and to make a USBMap.kext as detailed
   in dortania's opencore gathering files USB section
   
5. You will also need genericUSBXHCI.kext

6. Set ProvideConsoleGOP to FALSE if you have a garbled screen

I recomment using the MacBookPro16,3 or MacBookPro16,4 smbios

If you have anything you want to add or any ideas, discussions
are always open!

Laslty, no judging my webpage work. I know its not the best looking.

Opencore- https://dortania.github.io/OpenCore-Install-Guide/

WhateverRed- https://github.com/NootInc/WhateverRed
