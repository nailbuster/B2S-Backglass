# B2S-Backglass
B2S Backglass Server and Designer for use with Visual Pinball


Fork of sourceforge project:  https://sourceforge.net/projects/b2s-backglass/

Changes in this PinUP System 'inspired' version.

a>no more fuzzy logic. directb2s should only load when exact filenames match. everything else will not show backglass.

b>directb2s is not 'on-top'. it is sent to back so that if PuPPacks or other things like dmds want to display over it.

c> I made a new function/property on the controller that you can disable pinup player plugin from starting up during controller init . I'll show you in wiki some examples of how that works....

If anyone wants to test it out. make backup copy of your b2sbackglassserver.dll and exe and try this out. REMEMBER to unblock the zip prior to unzipping.

www.nailbuster.com/pinupdates/PinUPSystem_B2S_Server_Custom.zip
