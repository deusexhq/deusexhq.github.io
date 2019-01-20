# HX
## What is HX?

HX is a Deus Ex Overhaul mod that adds cooperative gameplay to the story mode, developed by Hanfling, a dev behind the Revision mod.

On top of that, there is HXExt, a third-party mod developed by Bogie of OTP, which fixes a few bugs, adds new features, skins, taunts, etc. This guide will help to install HX and HXExt for playing, and hosting.

## Installing for Playing
<div class="tcalert">Note: It is recommended that you use a fresh game install for this, to avoid mistaking errors in setting up HX for just being mismatches with other mods.</div>
<div class="tcalert">Note: HXExt is at version 2.2 at the time of writing. Latest files will always be available in the Discord #deusex-coop channel if this link becomes outdated.</div>

First, grab the files, download [HX core files](https://builds.hx.hanfling.de/) and [HXExt files](https://drive.google.com/uc?id=1EbUNTZrsvc6OZM3Q8Sgk-PY3YK1-zxiR).

Extract these files in to your games /System folder, which will be one of these;
```
C:\Deus Ex\System\
C:\GOG Games\Deus Ex\System\
C:\Program Files\DeusEx\System\
C:\Program Files (x86)\DeusEx\System\
C:\Program Files\Steam\SteamApps\common\Deus Ex\System\
C:\Program Files (x86)\Steam\SteamApps\common\Deus Ex\System\
```

Then, in your HX.ini (see text box below), find the line that reads `Root=HX.HXRootWindow` and change that to read `Root=HXExt.HXRootWindowExt`.

<div class="tcalert">
HXDefault.ini if that HX.ini doesn't exist. If HX.ini doesn't exist, it generates one from HXDefault when you start the game, so any time you want to edit the config **AFTER** this, **THEN** edit HX.ini
</div>

### Skins
You can set up your player class by changing your `Class=` line in HXUser.ini 
(or HXUserDefault.ini if that doesn't exist, see the note about HXDefault.ini above). There is a list of player classes included, in 
`Player Class List.txt` or seen below this text. For example; `Class=HXExt.HXBobPage`, or `Class=HXExt.HXAlexDentonMale2`. Remember to add the `HXExt.` part otherwise you'll get a `Class not found` error when you try to start the game!

Alternatively, classes can be changed in game using the `SetPlayerSkin` command, along side the class name. For example; `SetPlayerSkin HXExt.HXAlexDentonFemale`, or `SetPlayerSkin HXExt.HXPaulStrange` (Hidden skin discovered! Congratulations, you actually read the readme!).

```
HXJCDentonMale1Ext (JC Denton White)
HXJCDentonMale2Ext (JC Denton Black)
HXJCDentonMale3Ext (JC Denton Latino)
HXJCDentonMale4Ext (JC Denton Ginger)
HXJCDentonMale5Ext (JC Denton Pale)
HXJCDentonUnaugged (JC Denton Unaugmented)
_____________________________________

HXJCDentonFemale1 (JC Denton White)
HXJCDentonFemale2 (JC Denton Black)
HXJCDentonFemale3 (JC Denton Latino)
HXJCDentonFemale4 (JC Denton Ginger)
HXJCDentonFemale5 (JC Denton Pale)
_____________________________________

HXPaulDentonMale1Ext (Paul Denton White)
HXPaulDentonMale2Ext (Paul Denton Black)
HXPaulDentonMale3Ext (Paul Denton Latino)
HXPaulDentonMale4Ext (Paul Denton Ginger)
HXPaulDentonMale5Ext (Paul Denton Pale)
HXPaulDentonUnaugged (Paul Denton Unaugmented)
_____________________________________

HXAlexDentonMale1 (Alex Denton White)
HXAlexDentonMale2 (Alex Denton Black)
HXAlexDentonMale3 (Alex Denton Latino)
HXAlexDentonMale4 (Alex Denton Ginger)
HXAlexDentonMale5 (Alex Denton Pale)
HXAlexDentonFemale (Alex Denton White)
_____________________________________

HXJCDentonMaleBeta1 (JC Denton White)
HXJCDentonMaleBeta2 (JC Denton Pale)
HXJCDentonMaleBeta3 (JC Denton Brunette)
HXJCDentonMaleBeta4 (JC Denton White)
HXJCDentonMaleBeta5 (JC Denton Black)
_____________________________________

HXPaulDentonMaleBeta1 (Paul Denton White)
HXPaulDentonMaleBeta2 (Paul Denton Pale)
HXPaulDentonMaleBeta3 (Paul Denton Brunette)
HXPaulDentonMaleBeta4 (Paul Denton White)
HXPaulDentonMaleBeta5 (Paul Denton Black)
_____________________________________

HXAdamJensen (Adam Jensen)
HXWaltonSimonsExt (Walton Simons)
HXWaltonSimonsAlt (Walton Simons Suit)
HXBobPageExt (Bob Page)
HXBobPageAlt (Bob Page Trench Coat)
HXJockExt (Jock)
_____________________________________
HXArmageddon (Armageddon)
HXCozmo (Cozmo)
HXKaiser (Kaiser)
HXKnifeworld (Knifeworld)
HXLexichu (Lexichu)
HXNobody ([FGS]Nobody)
HXSolid (Solid)
HXJohnCochranDenton (JS38)
HXBogie (Bogie)
HXDefaultPlayer001 (DefaultPlayer001)
HXEvilEmperor (Evil Emperor)
```

## Installing for Hosting
<div class="tcalert">
Firstly, make sure you check [here](../hosting/) if you're unsure of how to host. The rest of this guide will assume you know how to host basic servers at least, and will only tell you how to install HX and HXExt.
This also assumes you've installed HX and HXExt for Playing as seen above, as that is required to host it.
</div>

1. Open HX.ini and find the line that reads `DefaultServerGame=HX.HXGameInfo`, and change that to `DefaultServerGame=HXExt.HXGameInfoExt`.
2. Find the block that starts with `[HX.HXGameEngine]`, and add the following to the end of that list;
```
ServerPackages=HXExt
ServerPackages=HXExtCharacters
ServerPackages=HXExtSounds
ServerPackages=HXExtUI
```
3. (a) If you want to use a serverstarter batch file, check out [here](https://deusexhq.github.io/hosting/#server-starter), follow the same instructions but change the `game=` value to `HXExt.HXGameInfoExt`.
3. (b) To launch from the game, do like you usually would, in the server browser click Host, change settings as desired there.

