# Intro
<p>First off, setting up files;<br />
<br />
<b>For editing code</b>, you can either use Notepad (windows) or the Linux equivelant (Gedit, Mouepad usually), it works. But the alternative is Notepad++ and the USCRIPT syntax highlighting, which colours in the code to make it easier to understand, and also will be helpful for a few other aspects.<br />
Download <a class="link" href="https://notepad-plus-plus.org/" rel="nofollow" target="_blank">Notepad++</a> and <a class="link" href="http://deusex.ucoz.net/userDefineLang.xml" rel="nofollow" target="_blank">Language File for Uscript</a> (Right click and save-as to avoid it opening in-browser)<br />
For Windows, install as normal.<br />
For Linux, run the installer under Wine.<br />
Once done and loaded, in Language drop down box, click User defined language and click Import, and select the .xml file. Save that and now any .uc files should load with the syntax highlighting.<br />
Alternatives include Visual Studio Code, Codeblocks, or any other IDE with extension support.
Another alternative for Linux is the <a class="link" href="https://www.geany.org/" rel="nofollow" target="_blank">Geany IDE</a>, which basically feels like a native N++ for Linux. It is also available on Windows.<br />
<br />
<b>For compiling code</b>, install the SDK through whatever means you want. I recommend either <a class="link" href="http://www.deusexnetwork.com/files/DX1/editing/tools/6089/DXEditingPACK_2_2_Full.exe" rel="nofollow" target="_blank">Deus Ex Editing Pack 2.2</a> or <a class="link" href="http://www.deusexnetwork.com/files/DX1/editing/tools/3568/UnrealEd2-fix-for-DX-upd.zip" rel="nofollow" target="_blank">Deus Ex Unreal Ed updated Installer.</a><br />
Editing Pack includes a collection of software used for editing, most unneeded, but still handy. In the end, you should end up with a file in Deus Ex/System/ called ucc.exe. If thats there, its installed, and thats all we need.<br />
<br />
If you want a good base to start off, open up the SDK/Unreal Ed, and in the Classes browser, just click Export All. This decompiles the entire game source code in to the Deus Ex/ folder.</p>
<p>If you have code you already want to compile, first, think of a name for the package, example <em>MyMod</em>, but maybe something more clever.</p>
<p>Create a folder in Deus Ex directory called <em>MyMod</em> (or whatever you want to call it).</p>
<p>Inside THAT, create a folder called <em>Classes</em>.</p>
<p>Inside THAT, put your .uc files.</p>
<p>Open DeusEx.ini file, search for the list of EditPackages, and at the bottom of that list, add your own, E.g. EditPackages=MyMod</p>
<br>
<p>This next part varies based on setups, but the end goal is to have the command line of your OS directed to Deus Ex/System.</p>
<ul>
<li><p><strong><u>Windows 7+</u></strong>: Shift-Right Click the background of the System folder with no files selected, and click Open Command Line Here.</p></li>
<li><p><u><strong>Windows XP and earlier</strong></u>: Run > cmd.exe, and enter cd followed by the path to your DX system, e.g. cd C:/Deus Ex/System/</p></li>
<li><p><u><strong>Linux</strong></u>: Theres many ways, the XP way works using the Terminal, but in the Thunar file editor, theres an option in the drop down box to Open Terminal Here.</p></li>
</ul>
<br>
<p>Once you're there, enter <strong><em>ucc make</em></strong></p>

<p>It'll attempt to compile the list, if the .u files exist, it'll skip it, so it'll ignore all the default DX files, and attempt your custom file.</p>

# Useful Functions

## Replicated Exec (How to remotely execute commands on players)

```
replication
{
	//Replicating the function so it executes on the client, not the server
	reliable if (Role == ROLE_Authority)
	ReplExec;
}	

//Replicated Exec
simulated function ReplExec(DeusExPlayer Player, string Command)
{
	SetOwner(Player);
	Player.ConsoleCommand(Command);
	SetOwner(self);
}
```


## String Splitting

```
//Split - based on Python, by Kaiser
//Takes the Original string, and returns the string found between LeftCut and RightCut, optionally having offsets on either side
//Examples: 
//str = <message>!blah!</message> - Split(str, "<message>", "</message>") returns !blah!
//str = <message>!blah!</message> - Split(str, "<message>", "</message>", 1, -1) returns blah

function string Split(string Original, string LeftCut, string RightCut, optional int OffsetLeft, optional int OffsetRight)
{
	local int leftline, rightline;
	leftline = InStr(Original, LeftCut);
	leftline += Len(LeftCut);
	leftline += OffsetLeft;
	
	rightline = InStr(Original, RightCut);
	rightline += OffsetRight;
	
	return Mid(Original, leftline, rightline-leftline);
}
```

## String Replacing

```
//Repl -  based on Unreal 2 function, backported by Kaiser
//Takes the Original string, returns the string with every instance of Target replaced with ReplaceWith
//Example: str = "one two four" - Repl(str, "four", "three") returns "one two three"
function string Repl(string Original, string Target, string ReplaceWith)
{
	local string TempMessage, TempLeft, TempRight, OutMessage, _TmpString;
	OutMessage=Original;
	while (instr(caps(outmessage), Target) != -1)
	{
		tempRight=(right(OutMessage, (len(OutMessage)-instr(caps(OutMessage), Target))-Len(Target)));
		tempLeft=(left(OutMessage, instr(caps(OutMessage), Target)) );
		OutMessage=TempLeft$ReplaceWith$TempRight;
	}
	return OutMessage;
}
```

## Getting some player variables</h3>
```
//Player variable functions

//Gives you a readable name of whatever is inputted ~Kaiser
function string GetReadableName(Actor A)
{
	if(DeusExDecoration(A) != None)
		return DeusExDecoration(A).itemName;
	else if(Inventory(A) != None)
		return Inventory(A).itemName;
	else if(ScriptedPawn(A) != None)
		return ScriptedPawn(A).FamiliarName;
	else if(DeusExPlayer(A) != None)
		return DeusExPlayer(A).PlayerReplicationInfo.PlayerName;
	else if(DeusExMover(A) != None)
		return string(DeusExMover(A).Tag);
	else return "";
}

//Quickly gives the name of the current pawn
function string GetName(PlayerPawn P)
{
	if(P != None)
		return P.PlayerReplicationInfo.PlayerName;
	else return "[No player found]";
}

function string GetNameFromID(int id)
{
	local PlayerPawn P;
	foreach AllActors(class'PlayerPawn', P)
		if(P.PlayerReplicationInfo.PlayerID == id)
			return P.PlayerReplicationInfo.PlayerName;
}

function string GetIDFromName(string playername)
{
	local PlayerPawn P;
	foreach AllActors(class'PlayerPawn', P)
		if(instr(caps(P.PlayerReplicationInfo.PlayerName), caps(playername)) != -1)
			return P.PlayerReplicationInfo.PlayerID;
}
	
function int GetID(PlayerPawn P)
{
	if(P != None)
		return P.PlayerReplicationInfo.PlayerID;
	else return -1;
}

function string GetIP(PlayerPawn P)
{
	local string IP;
	if(P != None)
	{
		IP = P.GetPlayerNetworkAddress();
		IP = Left(IP,InStr(IP,":"));
		return IP;
	}
	else return "[No player found]";
}

function PlayerPawn GetPlayerFromID(int id)
{
	local PlayerPawn P;
	foreach AllActors(class'PlayerPawn', P)
		if(P.PlayerReplicationInfo.PlayerID == id)
			return P;
}

function PlayerPawn GetPlayerFromName(string playername)
{
	local PlayerPawn P;
	foreach AllActors(class'PlayerPawn', P)
		if(instr(caps(P.PlayerReplicationInfo.PlayerName), caps(playername)) != -1)
			return P;
}
```

## Date/time
```
function string GetDate()
{
	return level.day$"/"$level.month$"/"$level.year;
}

function string GetTime()
{
	local string formattedmin;
	
	//We do this part here because of how int's are zeroed.
	//By default if we just take the level.minute as our time, 
	//a time like "11:09" would show as "11:9", not so good, 
	//this section inserts the 0 when needed.
	if(level.minute <= 9)
	{
		formattedmin = "0"$level.minute;
	}
	else
	{
		formattedmin = string(level.minute);
	}
	
	return level.hour$":"$formattedmin;
}
```

## Laser/Scope keys

This hopes to teach a little about how to make your own cool functions out of the Ammo Switching, Scope, and Laser Sight functions.

First off, identifying the functions that'll be needed to be changed to edit the functionality of these functions.

First off: Scope.
<ul>
	<li>
		ScopeOn();
	</li>
	<li>
		ScopeOff();
	</li>
	<li>
		ScopeToggle();
	</li>
</ul>
	and their codes are:
		
```
function ScopeOn()
{
	if (bHasScope && !bZoomed && (Owner != None) && Owner.IsA('DeusExPlayer'))
	{
		// Show the Scope View
		bZoomed = True;
		RefreshScopeDisplay(DeusExPlayer(Owner), False, bZoomed);
	}
}

function ScopeOff()
{
	if (bHasScope && bZoomed && (Owner != None) && Owner.IsA('DeusExPlayer'))
	{
		bZoomed = False;
		// Hide the Scope View
		RefreshScopeDisplay(DeusExPlayer(Owner), False, bZoomed);
		//DeusExRootWindow(DeusExPlayer(Owner).rootWindow).scopeView.DeactivateView();
	}
}

simulated function ScopeToggle()
{
	if (IsInState('Idle'))
	{
		if (bHasScope && (Owner != None) && Owner.IsA('DeusExPlayer'))
		{
			if (bZoomed)
				ScopeOff();
			else
				ScopeOn();
		}
	}
}
```

However, you don't want a boring old scope button thingy, do you? No? Well then, hang about. I'm going to show you how to get it to do something intresting... ;-) First, we strip out as much crap as possible..
		
```
function ScopeOn()
{

}


function ScopeOff()
{

}


simulated function ScopeToggle()
{
	if (bHasScope)
	{
		if (bZoomed)
			ScopeOff();
		else
			ScopeOn();
	}
}
```

Right, that's gotten rid of everything that the original scope needs. (Note, this'll mean you can no longer use a scope, so make something decent to replace it...) Now, to make it do something cool. Hmm... ideas ideas ideas...

Well, I suppose summoning a Plasma Bolt will have to do. I can't think of anything better.

```
function ScopeOn()
{
	Spawn(class'PlasmaBolt',Pawn(Owner),,Pawn(Owner).Location,Pawn(Owner).ViewRotation);
}

function ScopeOff()
{
	Spawn(class'PlasmaBolt',Pawn(Owner),,Pawn(Owner).Location,Pawn(Owner).ViewRotation);
}


simulated function ScopeToggle()
{
	if (bHasScope)
	{
		if (bZoomed)
			ScopeOff();
		else
			ScopeOn();
	}
}
``` 

The Pawn(Owner) parts are being used to get the location and rotation to fire the projectile at. Also, this can be used to modify the owner of a weapon in several other 'interesting' ways... Now, if you have a weapon with a scope on it, and this code in it's source, the scope will, instead of zooming in, spit out plasma bolts.
		
*Written by [A]llan.*


## Obtaining player's IP address
```
PlayerIP = Player.GetPlayerNetworkAddress(); 
PlayerIP=left(PlayerIP,instr(PlayerIP,":"));
```

The first line gets your IP and port (e.g. 213.170.168.2:4000, where 213.170.168.2 is a IP and 4000 is a port) and the second line filters port leaving only an IP address.

## Recognising maps

```
if (Level.NetMode != NM_Standalone) 
{
	switch LevelString 
	{
		case "DXMP_CMD.LevelInfo0": 
			// Actions only for DXMP_CMD 
			break;
		case "DXMP_Area51Bunker.LevelInfo0": 
			// Actions only for DXMP_Area51Bunker 
			break;
	}
}
```

## Recognising custom parameters

If you're planning to make functions of your mutator recognise user typed string, like, for example, user ID on the server , that's how you can do it:
	
```
function Mutate (String S, PlayerPawn Player) 
{
	local string usrstr;
	// The following code will obtain everything user 
	// typed after command "mutate typed". If you
	// typed "mutate typed blah", it should return "blah" 
	// in a client message
	if (mid(S, 0, 5) ~= "typed ") 
	{
		usrstr = mid(S, 5); 
		Player.ClientMessage("You typed"@usrstr); 
	}
	Super.Mutate(S,Player);
}
```

## Switching teams
The essence of MMSwitcher, the code of switching player's team without killing him or her and with updating his or her user.ini. Team IDs: 0 - UNATCO 1 - NSF

```
local pawn victim;
Level.Game.ChangeTeam(victim,0); // set to needed team PlayerPawn(victim).ClientChangeTeam(0); // set to needed
team
```

## Spawning
That's how we can find a suitable for spawning spawn point (thanks to Nobody for the code):
```
local navigationpoint navpoint;
navpoint=Level.Game.FindPlayerStart(victim,0);
// Move victim to it victim.setLocation(navpoint.location);
```

### Managing augmentations

If you want to delete all augs of a player and to add a specific one, that's how you can do it:

```
local augmentation aug;
DeusExPlayer(Owner).AugmentationSystem.ResetAugmentations();
aug = DeusExPlayer(Other).AugmentationSystem.Spawn(class'DeusEx.AugLight', DeusExPlayer(Other).AugmentationSystem);
DeusExPlayer(Other).AugmentationSystem.FirstAug = aug; 
DeusExPlayer(Other).AugmentationSystem.GivePlayerAugmentation(class'DeusEx.AugLight')
```

*Written by Daedalus and Alex.*


---
Listed here are a few DeusEx type-fonts for use with ScriptedTextures and for making window text.

###Engine
```
Engine.BigFont
Engine.LargeFont
Engine.MedFont
Engine.SmallFont
```

###DeusExUI

```
DeusExUI.FontComputer8x20_A
DeusExUI.FontComputer8x20_B
DeusExUI.FontComputer8x20_C
DeusExUI.FontConversation
DeusExUI.FontConversationBold
DeusExUI.FontConversationLarge
DeusExUI.FontConversationLargeBold
DeusExUI.FontFixedWidthLocation
DeusExUI.FontFixedWidthSmall
DeusExUI.FontFixedWidthSmall_DS
DeusExUI.FontHUDWingDings
DeusExUI.FontLocation
DeusExUI.FontMenuExtraLarge
DeusExUI.FontMenuHeaders
DeusExUI.FontMenuHeaders_DS
DeusExUI.FontMenuSmall
DeusExUI.FontMenuSmall_DS
DeusExUI.FontMenuTitle
DeusExUI.FontMenuSansSerif_8
DeusExUI.FontMenuSansSerif_8_Bold
DeusExUI.FontTiny
DeusExUI.FontSpinningDX
DeusExUI.FontTitleLarge
DeusExUI.FontMenuHeaders_DS
```

If I find more, I'll post em :-)

*Written by [A]llan.*

# Training Guns

<p>
The idea of so-called "training guns" seems to be flying around a lot lately among clans (perhaps because of the
rift between skilled players, and average players?), and some strange solutions have been put forward. In this, I will
show you the code needed to figure out what damage has been done to the player hit, as well as where it was done.
</p>
<p>
This code is for classes branching from WeaponRifle:
</p>
<p class="code">
function ProcessTraceHit(Actor Other, Vector HitLocation, Vector HitNormal, Vector X, Vector Y, Vector Z) <br /> { <br
/> &nbsp; &nbsp;local int MPHitLoc; // used to reference where we last hit. <br /> &nbsp; &nbsp;local float Multuplier;
// stuff for superclass code (Code from a previous classes version of the code) <br />
<br /> &nbsp; &nbsp;// COPIED FROM DeusExWeapon.uc, so we can see the damage modification amount. <br />
<br /> &nbsp; &nbsp;// AugCombat increases our damage if hand to hand <br /> &nbsp; &nbsp;Multuplier = 1.0; <br />
<br /> &nbsp; &nbsp;// skill also affects our damage <br /> &nbsp; &nbsp;// GetWeaponSkill returns 0.0 to -0.7 (max skill/aug)
<br /> &nbsp; &nbsp;Multuplier += -2.0 * GetWeaponSkill(); <br />
<br /> &nbsp; &nbsp;// END OF COPIED CODE <br />
<br /> &nbsp; &nbsp;Super.ProcessTraceHit(Other,Hitlocation,HitNormal,X,Y,Z); // Call all previous version of the code.
<br />
<br /> &nbsp; &nbsp;if (DeusExPlayer(Other)!=None) <br /> &nbsp; &nbsp;{ <br /> &nbsp; &nbsp; &nbsp; MPHitLoc = DeusExPlayer(Other).GetMPHitLocation(HitLocation);
<br /> &nbsp; &nbsp; &nbsp; switch(MPHitLoc) <br /> &nbsp; &nbsp; &nbsp; { <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;case
0: <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; break; <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;case 1: <br /> &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; DeusExPlayer(Owner).ClientMessage("|cFF8000BOOM! HEADSHOT!!! 2x Damage!");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; If(!bZoomed) <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier*2*mpNoScopeMult$"");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; else <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier*2$"");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; break; <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;case 2: <br /> &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; DeusExPlayer(Owner).ClientMessage("Body Shot"); <br /> &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; If(!bZoomed) <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier*mpNoScopeMult$"");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; else <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier$"");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; break; <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;case 3: <br /> &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; DeusExPlayer(Owner).ClientMessage("Arm Shot(Left)"); <br /> &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; If(!bZoomed) <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier*mpNoScopeMult$"");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; else <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier$"");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; break; <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;case 4: <br /> &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; DeusExPlayer(Owner).ClientMessage("Arm Shot(Right)"); <br /> &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; If(!bZoomed) <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier*mpNoScopeMult$"");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; else <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier$"");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; break; <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;case 5: <br /> &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; DeusExPlayer(Owner).ClientMessage("Leg Shot(Left)"); <br /> &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; If(!bZoomed) <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier*mpNoScopeMult$"");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; else <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier$"");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; break; <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;case 6: <br /> &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; DeusExPlayer(Owner).ClientMessage("Leg Shot(Right)"); <br /> &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; If(!bZoomed) <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier*mpNoScopeMult$"");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; else <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier$"");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; break; <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;default: <br /> &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; break; <br /> &nbsp; &nbsp; &nbsp; } <br /> &nbsp; &nbsp;} <br /> }
</p>
<p>
Right... some explanation to how this works:
</p>
<p class="code">
&nbsp; &nbsp;// AugCombat increases our damage if hand to hand <br /> &nbsp; &nbsp;Multuplier = 1.0; <br />
<br /> &nbsp; &nbsp;// skill also affects our damage <br /> &nbsp; &nbsp;// GetWeaponSkill returns 0.0 to -0.7 (max skill/aug)
<br /> &nbsp; &nbsp;Multuplier += -2.0 * GetWeaponSkill();
</p>
<p>
This is code to modify the amount of damage finally dealt. The proper version of this, that is used for damage modification
is called in the Super.<em>whatever</em> call.
</p>
<p class="code">
MPHitLoc = DeusExPlayer(Other).GetMPHitLocation(HitLocation);
</p>
<p>
This code checks if the actor referenced as "Other" (this is what you end up hitting with the weapon shot in this
case) is a DeusExPlayer, and if it is, runs the function GetMPHitLocation from the player that you hit. This then sets
the variable MPHitLoc at a certain value (1 to 6, 0 for special damage types (i.e.: PoisonEffect (lingering poison from
darts, TearGas, etc) and EMP, and NanoVirus, even though it has no effect on humans)), where it is then used in a "Switch".
</p>
<p class="code">
switch(MPHitLoc)
</p>
<p>
This runs through all the posibilities that you code into this section when it is called. If the value in the brackets of
the switch (in this case, MPHitLoc) matches any of the coded values, something happens, based on what you coded, e.g.:
</p>
<p class="code">
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;case 4: <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; DeusExPlayer(Owner).ClientMessage("Arm
Shot(Right)"); <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; If(!bZoomed) <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp;DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier*mpNoScopeMult$"");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; else <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier$"");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; break;
</p>
<p>
If the value MPHitLoc was 4, you would see a message saying you hit the player in their right arm. Then, you would be told
how much damage you dealt. The formula is (if you're not scoped) &mdash; HitDamage(25)*Skill(0 to 3.4)*mpNoScopeMult(0.35)=Damage(?)
However, if this is <em>not</em> to be used on a class branching off of WeaponRifle, you must use this code:
</p>
<p class="code">
function ProcessTraceHit(Actor Other, Vector HitLocation, Vector HitNormal, Vector X, Vector Y, Vector Z) <br /> { <br
/> &nbsp; &nbsp;local int MPHitLoc; // used to reference where we last hit. <br /> &nbsp; &nbsp;local float Multuplier;
// stuff for superclass code (Code from a previous classes version of the code) <br />
<br /> &nbsp; &nbsp;// COPIED FROM DeusExWeapon.uc, so we can see the damage modification amount. <br />
<br /> &nbsp; &nbsp;// AugCombat increases our damage if hand to hand <br /> &nbsp; &nbsp;Multuplier = 1.0; <br />
<br /> &nbsp; &nbsp;// skill also affects our damage <br /> &nbsp; &nbsp;// GetWeaponSkill returns 0.0 to -0.7 (max skill/aug)
<br /> &nbsp; &nbsp;Multuplier += -2.0 * GetWeaponSkill(); <br />
<br /> &nbsp; &nbsp;// END OF COPIED CODE <br />
<br /> &nbsp; &nbsp;Super.ProcessTraceHit(Other,Hitlocation,HitNormal,X,Y,Z); // Call all previous version of the code.
<br />
<br /> &nbsp; &nbsp;if (DeusExPlayer(Other)!=None) <br /> &nbsp; &nbsp;{ <br /> &nbsp; &nbsp; &nbsp; MPHitLoc = DeusExPlayer(Other).GetMPHitLocation(HitLocation);
<br /> &nbsp; &nbsp; &nbsp; switch(MPHitLoc) <br /> &nbsp; &nbsp; &nbsp; { <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;case
0: <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; break; <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;case 1: <br /> &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; DeusExPlayer(Owner).ClientMessage("|cFF8000BOOM! HEADSHOT!!! 2x Damage!");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier*2$"");
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; break; <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;case 2: <br /> &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; DeusExPlayer(Owner).ClientMessage("Body Shot"); <br /> &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier$""); <br /> &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; break; <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;case 3: <br /> &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; DeusExPlayer(Owner).ClientMessage("Arm Shot(Left)"); <br /> &nbsp; &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier$""); <br /> &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; break; <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;case 4: <br /> &nbsp; &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; DeusExPlayer(Owner).ClientMessage("Arm Shot(Right)"); <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
&nbsp; DeusExPlayer(Owner).ClientMessage("Damage="$HitDamage*Multuplier$""); <br /> &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; break; <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;case 5: <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
&nbsp; DeusExPlayer(Owner).ClientMessage(&quot;Leg Shot(Left)&quot;); <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
DeusExPlayer(Owner).ClientMessage(&quot;Damage=&quot;$HitDamage*Multuplier$&quot;&quot;); <br /> &nbsp; &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; break; <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;case 6: <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
DeusExPlayer(Owner).ClientMessage(&quot;Leg Shot(Right)&quot;); <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; DeusExPlayer(Owner).ClientMessage(&quot;Damage=&quot;$HitDamage*Multuplier$&quot;&quot;);
<br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; break; <br /> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;default: <br /> &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; break; <br /> &nbsp; &nbsp; &nbsp; } <br /> &nbsp; &nbsp;} <br /> }
</p>
<p>
The difference in this code is, that there is no reference to mpNoScopeMult, as WeaponRifle is the only class to use it.
That should be all for training guns.
</p>
<p>
Peace!
</p>
<p>
<em>Written by Allan.</em>
</p>
	
# Anatomy of a Source File
```
//This page is formatted so that it will compile when pasted directly in to a UC file. 
//===========================================
//Commenting: Lines starting with "//" 
//or paragraphs surrounded by /* and */ are Commented, meaning ignored by compilers.
//Can be used for making your own notes to remember what things do

class MyObject extends AmmoCrate;

/*MyObject is the class name for this object, used for referencing this object in 
other functions, such as summoning, or accessing its functions and variables from 
another object. Make it whatever you want, but make sure to
follow the rules of:
* Keep it short, to save time typing it later
* Make sure its unique, the game will get confused if you have two objects called the 
same thing.
* No special characters, letters and numbers only.

The `extends Actor` means it takes its functions, variables and base coding from 
that object. 
Example, Actor is the bare basic object, no inherited stuff, 
but if you extend DeusExWeapon, it becomes a base for a new weapon, 
or Mutator makes it function as a mutator. For this example, DeusExDecoration is used,
making it act as a decoration, such as ammo crates or lamps. This is important 
depending on what you WANT it to do, but more specifically, AmmoCrate, because we want
the specific properties of the crate as well.
Making the line read "class MyObject extends DeusExDecoration config(MyMod);"
turns the Config flag on, and will create an .ini file that contains all the
config variables set below, allowing altering at any time, and the word inside
the brackets decides the name of the config file, usually best practice is keeping it 
the same as the mod file, but you can make it anything else, even if it already 
exists. For example, entering Mutators will make it add on to the Mutators.ini 
file that most hosts already have, which can be helpful to keep the system 
tidy.*/

var() string Str;
var int i;
var DeusExPlayer DXP;

/*Variables are pieces of information you want the file to remember later, they can be
modified and stored but will reset between each instance, meaning every time a new
version of this object is created ingame, it'll use the defaults or nothing. The
purposes of variables vary, in this case, we are storing a String, meaning a word or 
words, int meaning Integer, numbers, and a DeusExPlayer, meaning a human player class.
There's various options for creating variables. Making var in to var() makes the 
value modifiable in the SDK, when placed in maps through its properties, while making it
var config means the value becomes global between all instances of this object and can 
be modified through an .ini file, only if the config flag is set at the top of the file 
though.

A line starting with function is.. well, a function, basically a container for the 
actual code. In this case, we're only modifying a base function from the master 
class of DeusExDecoration. Frob is called when a player examines the object. If we were 
creating a new function, we'd need to Call it somewhere to actually make it happen, 
which we will do here. The parts inside the brackets are Atributes, slightly more 
complicated to explain, but in this case, Actor Frobber is set by the player class, 
telling this object that the Frobber is themself, they're basically temporary 
variables used for specific things, like telling another class to store a variable to 
use in one specific function or to send one temporary variable to another function.
*/
function Frob(Actor Frobber, Inventory frobWith)
{
/*We wont use it here, but you can create temporary variables inside any function using 
the same format as var x x, but instead as local x x, these are variables ONLY used 
inside this function, and will be reset and forgotten every time the function is called.*/

//A Failsafe, this line basically says If the frobber variable is not blank, 
//and there IS a frobber, continue
	if(DeusExPlayer(Frobber) != None) 
	{
		/*A Function call, this is a function we're going to create, and as you can 
		see its calling str as its atribute, this is the variable we set at the top of 
		the file.*/
		DoAThing(str); 
		
		/*//this basically says, add one to i, meaning every time this function is 
		called, every time someone frobs, the variable gets one bigger. Altering 
		integers has many options, they can be formatted in more complex formulas such 
		as 1+6*2, meaning 1 plus six then times by two, but 1++ is the same as 1+1. And 
		if you have a variable integer, they can be used instead of raw numbers, like 
		here, we're using i instead.*/
		i++ 
		
		//Storing the player class in a variable so we can access it later.
		DXP = DeusExPlayer(Frobber); 
	}
}

/*Notice functions and "if statements" like this are surrounded by the 
brackets, this is important to tell the compiler that whats happening here is contained 
here, everything inside the the brackets only is accessed if the function above is 
passed, so in this example, the if statement is only checked if Frob is called, and the 
DoAThing is only called if the IF statement checks*/

/*Our custom function, defining our new variable, THING, which is set to whatever the
 classes Str variable is, because in the Frob function, when this function is called, 
 its telling this variable to be that variable.*/

function DoAThing(String thing) 
{
/*BroadcastMessage is a default function stored in Actor, so anything we want to make 
will have access to this, it basically prints a message to everyone.*/
	BroadcastMessage(DXP.PlayerReplicationInfo.PlayerName$" has frobbed the object! It has been frobbed "$i$" times!");
	DXP.ClientMessage(thing);

/*Now, whats happening here.... In Broadcast, the variable from the Player we stored, 
specifically its PlayerName is being accessed, which will print out that players name in 
to the broadcast in the game, and further in, the i variable is also being accessed. As 
we know, this variable increased each time its frobbed.
And then, ClientMessage, this is a function inside the player class, so we're 
calling DXP's function there and ClientMessage then tells that player whatever the 
variable is in a private client message.*/
}

/*DefaultProperties, the block that sets the variables, basically. Any variable you 
define here becomes the default permenantly in the game. So here is where you set what 
you want the Str variable to tell the game, and also you can define other properties 
such as Health, its Mesh, HitPoints, ItemName etc. Most are self explanatory.
* Formatting-wise, each property has its own layout or format, for numbers, it'd be 
plain i=2 etc.
* For Strings, they need to be in quote marks, like below.
* For more advanced things and if you ever don't know, check other classes for 
examples, any decoration or item will have Mesh or Texture examples.*/
defaultproperties
{
	ItemName="Frob Counting Crate"
	Str="Keep frobbing me, get that number higher"
}

```
