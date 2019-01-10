# B2S-Backglass PINUP System inspired version
# (not official version)
B2S Backglass Server and Designer for use with Visual Pinball


Fork of sourceforge project:  https://sourceforge.net/projects/b2s-backglass/

Changes in this PinUP System 'inspired' version.

a>no more fuzzy logic. directb2s should only load when exact filenames match. everything else will not show backglass.

b>directb2s is not 'on-top'. it is sent to back so that if PuPPacks or other things like dmds want to display over it.

c> I made a new function/property on the controller that you can disable pinup player plugin from starting up during controller init . 

example in table_init script:
```
Sub Table1_Init
vpmInit Me
With Controller
.GameName = cGameName
If Err Then MsgBox "Can't start Game " & cGameName & vbNewLine & Err.Description:Exit Sub
.SplashInfoLine = "Batman, Data East 1991" & vbNewLine & "VPX table by Javier v1.0"
.HandleKeyboard = 0
.ShowTitle = 0
.ShowDMDOnly = 1
.ShowFrame = 0
.HandleMechanics = 0
.Hidden = 0
.PuPHide = 1
.Games(cGameName).Settings.Value("sound") = 1
On Error Resume Next
.Run GetPlayerHWnd
If Err Then MsgBox Err.Description
End With
On Error Goto 0
```
Notice the .PuPHide = 1   (1=disable pupb2s plugin, 0 = enable..default if not set )

If anyone wants to test it out. make backup copy of your b2sbackglassserver.dll and exe and try this out. REMEMBER to unblock the zip prior to unzipping.

compiled with VS2015

