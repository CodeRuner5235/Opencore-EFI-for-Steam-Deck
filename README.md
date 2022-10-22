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

What works-

1. Battery readout

2. Controller as keyboard (R2 is left click, L2 is right click, the right mouse pad is the mouse)

3. The usb type-C port

and thats basicly it.

What doesnt work-

1. Acceleration

2. Screen orientation (likeley to be fixed when we get acceleration working)

3. Wifi, bluetooth (may never work)

4. Touch screen

5. SD card reader


#IT IS NOT RECOMENDED TO USE THIS EFI AS IS.
#IT IS HERE TO HELP YOU BUILD YOUR OWN.

This can be accomplished by following the dortania guide for Rzyen as linked below
and changing these things.

1. you need to use SSDT-Time to build an EC for a laptop and add it
   to your APCI folder
   
2. You need SSDT-CPUR in you APCI folder

3. You will need the VooDooI2C.kext and VooDooI2CHID.kext

4. You will need USBToolbox.kext and to make a USBMap.kext as detailed
   in dortania's opencore gathering files USB section
   
5. You will also need genericUSBXHCI.kext

6. Set UEFI-> Output-> ProvideConsoleGOP to FALSE and Resolution to 1024x768 if you have a garbled screen

I recomment using the MacBookPro16,3 smbios.

**EDIT: TRYING EDID PATCH TO FIX SCREEN ORIENTATION**

If you have anything you want to add or any ideas, discussions
are always open!

Opencore- https://dortania.github.io/OpenCore-Install-Guide/

WhateverRed- https://github.com/NootInc/WhateverRed
