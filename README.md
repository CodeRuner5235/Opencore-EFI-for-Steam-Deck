# Opencore-EFI-for-Steam-Deck
This project is for using Opencore to MacOS on the Valve Steam Deck.
_________________________________________________________________________________________
The MacOS versions that I will be targeting are Catalina (10.15) and Big Sur (11)

My reasoning is that Apple changed a lot of things between Big Sur and Monterey so
I will be focusing on these two versions for now. I will deninetly try to get Montery
and up running in the future. 
_________________________________________________________________________________________

As of right now, there are many, MANY, issues the must be overcome before MacOS is even
remotely usable in the Steam Deck. My first and foremost concern is getting the installer
to boot using successfully while using the built in screen. This should be (hopefully) 
possible by spoofing the custom APU to an Intel iGPU. If by some miracle this works, the
next issue is graphics accelleration. Hopefully, this issue can be fixed with what the
guys at WhateverRed are working on. In fact, their project is why I am limiting the MacOS
versions to Catalina and Big Sur. If (and big if) we can get these two issues sorted out,
we only have a couple other things to worry about.

1. Wifi/Bluetooth-
   Unfortunelty, it looks like the wifi chipset that the Steam Deck uses is from Realtek
   wich basicly means that it will by unsupported with no fixing it. So if you want wifi
   you will probably have to use an external wifi dongal though the type-C port.
 
2. Type-C and SD card reader-
   Kinda nessecary to do anything. Shouldnt be too hard to get working.
 
 
3. Touch screen/mouse pads- 
   Maybe some ACPI patching will get this to work??

4. Audio

5. Controller controls- 
   I am hoping this can be fixed by installing steam and using its mapping. If not, 
   ACPI patching will probably be needed...

6. Everything else-
   Things like the webcam, microphone, etc...


Any and all help is welcome form people who want 
to test to people who know how to use Opencore.

If you have anything you want to add or any ideas, discussions
are always open!

Opencore- https://dortania.github.io/OpenCore-Install-Guide/

WhateverRed- https://github.com/NootInc/WhateverRed
