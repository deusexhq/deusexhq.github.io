## Binds
A bind is a combination or stand alone command(s) assigned to a specific button in order to simplify gameplay (e.g., to make
reloading faster or to decreasing of healing time by medkits). Binds are used by much of the Deus Ex community, from simple
name binds to sophisticated binds.

Firstly, we need to open the User.ini. This is located in C:/DeusEx/System.
Once you have found it, open it. The start should look something similar to:

```
[DefaultPlayer]
Name=Player
Class=DXMTL152b1.MTLJCDenton
Team=0
Skin=
Face=
```

Sections will be different for you however, such as the Name and Class. In this file is where all binding occurs. Binding
is, however, very simple. We need to find an empty "Letter" somewhere in the .ini file first.
For example, the letter "O" is empty by default, and will simply look like "O=".

Now, we want to add something after this, for this guide, I am going to use a simple "say" bind. A say bind automatically	generates a set message for you when you press the key. After the empty letter, add the	sentence

```
Say Taking Fire, need assistance!
```

Now, you may notice that each letter is repeated twice throughout the .ini file. This is because one affects singleplayer and one affects multiplayer. For safety's sake, I would advise placing the commands after both of the same letters to avoid confusion.

Save the file, close it, and we're done! For more detailed information about what binds there are, view the other pages concerning	binding.

Now in-game, pressing the 'o' button will execute your "Say" command, which can be anything you want it to be.
Make sure your team knows when you need help!


### Popular Binds
#### Items
For any of the binds using ActivateBelt, you can change the numbers to decide what to equip, example; ActivateBelt 9 is usually medkit, 0 is usually biocells, 1 is your Slot 1 weapon etc.

Grabbing your medkit or biocell:
```
ActivateBelt 9|onrelease ParseLeftClick
```

Uses a med then pulls out weapon in belt 2:
```
ActivateBelt 9|onrelease ParseLeftClick|ActivateBelt 2
```

Advanced medkit bind (may have problems in lag or bad ping) <em>- bind was compiled by Clix:</em>
* First create Aliases[...] bind <br />
	```
	Aliases[23]=(Command="ActivateBelt 9|onrelease ParseLeftClick",Alias=MedKit)
	```
* Then find a button to bind it to. For example, button H:<br />
	```
	H=ParseRightClick|ParseRightClick|MedKit|OnRelease ActivateBelt 1
	```

The following bind could be useful for a sniper rifle. After it&#39;s used, a sniper rifle with enabled scope pulls out.
Adjust "3" in it to an inventory slot, which you usually use to keep a sniper rifle:
```
Activatebelt 3|Onrelease ToggleScope
```

#### Movement
Strafes diagonally (forward left):
```
Aliases[22]=(Command="Axis aBaseY Speed=+300.0|Axis aStrafe Speed=-300.0",Alias=ForwardLeft)
```

Strafes diagonally (forward right):
```
Aliases[22]=(Command="Axis aBaseY Speed=+300.0|Axis aStrafe Speed=+300.0",Alias=ForwardRight)
```

Circles left:
```
Aliases[22]=(Command="Axis aBaseX Speed=-180.0|Axis aBaseY Speed=+050.0",Alias=CircleLeft)
```

Circles right:
```
Aliases[22]=(Command="Axis aBaseX Speed=+180.0|Axis aBaseY Speed=+050.0",Alias=CircleRight)
```
Turns you around, so you can face behind you instantly:

```
Aliases[22]=(Command="Axis aBaseX Speed=+2900.0",Alias=TurnAround)
```

#### Augmentations

This bind enables Targetting/Ballistic Protection, then fires, and when you let go of the mouse button, it disables Targetting/Ballistic
Protection. Great if you want to conserve bio:

```
LeftMouse=ActivateAugmentation 3|Fire|onrelease ActivateAugmentation 3
```

Just keeps on ADS as long as you hold down the key; useful in fights when low on bio or if you want to conserve bio:

```
Aliases[22]=(Command="ActivateAugmentation 6|onrelease ActivateAugmentation 6",Alias=ADS)
```

Med bind + regeneration &mdash; will withdraw a medkit and activate the Regeneration aug. This is useful when you are in
serious trouble in a fight:
```
Aliases[22]=(Command="ActivateBelt 9|ActivateAugmentation 1")
```
#### Skills

Updates skills and equips the relevent belt item. 1 is Heavy Weapons, 2 is Pistols, 3 is Rifles, 4 is Melee, 5 is Grenades,
6 is Environment Resistance, 7 is Lockpicks, 8 is Multitools, 9 is Medicine, 0 is Hacking.

```
ActivateBelt 1|BuySkills|ActivateBelt 1|BuySkills|ActivateBelt 1<br /> ActivateBelt 2|BuySkills|ActivateBelt 2|BuySkills|ActivateBelt
2<br /> ActivateBelt 3|BuySkills|ActivateBelt 3|BuySkills|ActivateBelt 3<br /> ActivateBelt 4|BuySkills|ActivateBelt 4|BuySkills|ActivateBelt
4<br /> ActivateBelt 5|BuySkills|ActivateBelt 5|BuySkills|ActivateBelt 5<br /> ActivateBelt 6|BuySkills|ActivateBelt 6|BuySkills|ActivateBelt
6<br /> ActivateBelt 7|BuySkills|ActivateBelt 7|BuySkills|ActivateBelt 7<br /> ActivateBelt 8|BuySkills|ActivateBelt 8|BuySkills|ActivateBelt
8<br /> ActivateBelt 9|BuySkills|ActivateBelt 9|BuySkills|ActivateBelt 9<br /> ActivateBelt 0|BuySkills|ActivateBelt 0|BuySkills|ActivateBelt
0
```
#### Statistics

This shows the score as long as you keep the scores button pressed:

```
ShowScores|onRelease ShowScores
```

This shows your netstats (ping, packetloss etc), and your current FPS (<em>frame per second</em> value):

```
stat net|stat fps
```

## Coloured text (WIP)
`Editor's Note: Adding eventually.`

## No-CD patch
`Note: Only relevant if you're using the original disc version of the game.`

<p>
	When installing, the game copies itself entirely to your hard drive, but it may require an original CD when you run it. Using
	CD slows down the game, takes more energy, activates the drive for no reason and restrains you from using other CDs instead.
</p>
<p>
	The problem is easy to solve:
</p>
<ul>
	<li style="font-weight: bold">Step 1.
		<ol>
			<li>Find your Deus Ex directory. Usually it's either on your C: drive or C:\Program Files\. </li>
			<li>Open /System/ folder from your Deus Ex directory.</li>
			<li>Open a file called DeusEx.ini.<br />
				<img alt=" " src="http://www.dxalpha.com/assets/images/kb/deusex-ini.gif" width="177" /> <br /> If you're running Windows,
				it will open itself in Notepad and you will see these lines in the beginning: <br />
				<span class="code">[URL]<br />
	Protocol=deusex<br />
	ProtocolDescription=Deus Ex Protocol<br />
	Name=Player<br />
	...<br />
	</span> </li>
			<li>Then, scroll down a bit and find [Engine.Engine]. In this section, find a CdPath variable<span class="code">CdPath=...</span></li>
			<li>Set it to <br />
				<span class="code">CdPath=..\</span></li>
			<li>Save/close the file.</li>
		</ol>
	</li>
	<li><strong>Step 2.</strong> You only need it if you use Deus Ex SoldOut edition or the step above didn't help you.
		<ol>
			<li>Find your Deus Ex directory. Usually it's either on your C: drive or C:\Program Files\. </li>
			<li>Open /System/ folder from your Deus Ex directory.</li>
			<li>
				<a href="http://download.dxalpha.co.uk/DX1/patches/DeusEx-exe-patched.rar">Download the patch</a> (68 KB).</li>
			<li>Extract DeusEx.exe from the archive you downloaded to DeusEx/System/ folder. It will ask if you want to replace the file,
				choose "yes".</li>
		</ol>
	</li>
</ul>
	
## Renderers
<p>
	In this tutorial I will explain how to change your 3D renderer to one that may enchance the performance of Deus Ex on your
	computer. A renderer is "a carefully engineered program, based on a selective mixture of disciplines related to: light
	physics, visual perception, mathematics, and software development" <em>(taken from Wikipedia)</em>. In other words,
	it&#39;s a program that helps the game output 3D graphics.
</p>
<p>
	Firstly, I am going to suggest downloading an extra renderer that isn&#39;t supplied with Deus Ex. New enhanced OpenGL can
	be downloaded from
	<a href="http://cwdohnal.home.mindspring.com/utglr/">here</a>. Now, once you have downloaded the .zip folder, extract the contents and you should be left with a file similar
	to the looks of this:
</p>
<div style="text-align: center">
	<img alt=" " src="http://www.dxalpha.com/assets/images/kb/opengldrv-dll.gif" width="177" />(Windows XP)&nbsp;
</div>
<div style="text-align: center">
</div>
<div style="text-align: center">
</div>
<p>
	A renderer included with Deus Ex is Direct 3D (Not advised to use with older graphics cards!). An update for that is avaliable
	<a href="http://cwdohnal.home.mindspring.com/utglr/dxd3d8r12.zip" title="Here">here</a>. Download the .zip folder and extract it to Deus Ex/System. This looks like:
</p>
<div style="text-align: center">
	<img alt="D3D" height="48" src="http://www9.imagocentre.com/images/2/D3D_15.bmp" width="121" />&nbsp;(Windows Vista)
</div>
<p>
	Choose one of those you feel would be more appropiate. You can try both if you are not satisfied with the result.&nbsp;Simply
	place that file in your Deus Ex/System folder.
</p>
<p>
	Now we want to switch to OpenGL/Direct 3D&nbsp;in Deus Ex: Go to Start &gt; Deus Ex (unless you moved it) and click on "Run
	Deus Ex in SafeMode". You will be displayed with a screen identical to this:
</p>
<p>
	<img alt="Safe Mode Menu" height="443" src="http://www.mafiawar.biz/imagehost/images/ChangingVideo_87277.jpeg" width="530"
	/>
</p>
<p>
	Now, click on Change your 3D video device. You will be displayed with 2 options, Direct 3D support and Software Rendering.
	If Direct 3D isn&#39;t highlighted, click it and continue though the Wizard.&nbsp;
</p>
<p>
	<strong><u>For OpenGl Users:</u></strong>&nbsp;
</p>
<p>
	(Read on if you are planning to use OpenGl) Now you&#39;ll notice that OpenGL isn&#39;t displayed, so we want to click the
	tab "Show all devices". You&#39;ll notice some new devices are displayed including OpenGl if you added it right.
	Click on OpenGL and finish the installation process. Now your Deus Ex will run with the new renderer!
</p>
<p>
	If your newly installed OpenGL driver lags, set NumAASamples to 4 or UseAA to False in DeusEx.ini.
</p>
<p>
	Finally, start Deus Ex and on the main screen (Before the menu appears, if the menu is there, press escape) Press your assigned
	talk button (T by default) and type :
</p>
<span class="code">Preferences</span>
<p>
	&nbsp;<strong>Before typing this, make sure you press Alt + Enter first! If you hae not, your Deus Ex will crash!</strong>&nbsp;
</p>
<p>
	&nbsp;You will be displayed with a screen similar to this, there may be alterations because of mods that I am running:
</p>
<p>
	&nbsp;<img alt="Preferences" height="512" src="http://www2.imagocentre.com/images/2/Preferences_25.bmp" width="352" />
</p>
<p>
	&nbsp;You can see that I have expanded <em>Rendering</em> and then <em>OpenGl Support. </em>If you have placed the file
	in your /System folder, you should see the OpenGl Support bracket there.
</p>
<p>
	Expand this bracket and you will be displayed with a lot of options, which don&#39;t really need to be altered. One option,
	however, does need to be!
</p>
<p>
	About half-way down the list you&#39;ll see an option called <em>SceneNodeHack</em>. You&#39;ll notice in your preferences
	it is set to <em>False.</em> Instead, we want to set this to <em>True</em>, so click on the word <em>False</em> and change
	the option to <em>True</em>! Here&#39;s what it should look like:
</p>
<p>
	<img alt="SceneNode" height="162" src="http://www3.imagocentre.com/images/2/SceneNode_28.bmp" width="352" />
</p>
<p>
	This needs to be done so that the whole display can be shown (Such as the Spy Drone window).
</p>
<p>
	Once this is done, close the Preferences box and hit Alt + Enter again to resume your full-screen. Enjoy your new device!
</p>
	
## Resolutions
<p>
	In some cases, Deus Ex doesn&#39;t recognise your screen resolution and doesn&#39;t add an option with your resolution to
	"Settings -&gt; Screen" window. Instead you may set it manually:
</p>
<ul>
	<li>Press "T" (to enable the console), erase "Say" and type <span class="code">setres 1680x1050</span>			if your screen resolution is 1680x1050 pixels.</li>
	<li>If that didn&#39;t work, close Deus Ex, go to DeusEx/System, open DeusEx.ini. Find [WinDrv.WindowsClient]. Set the variables
		above it (again, as an example &mdash; 1680x1050): FullscreenViewportX to 1680 and FullscreenViewportY to 1050.&nbsp;</li>
</ul>
<p>
	You may want to adjust FOV according to your widescreen proportions. Go to DeusEx/System, then open User.ini, find [Engine.PlayerPawn],
	<a href="http://www.widescreengamingforum.com/fovcalc.php">calculate your FOV</a> and adjust both DesiredFOV and DefaultFOV.
</p>
<p>
	In high resolutions, there is a problem with the user interface, which becomes bigger than it should be. Unfortunately, there
	is no solution presently.
</p>
<p>
	<em>Thanks to al&#39;be:do for the provided information.</em>
</p>
	
## Virtual Memory

<p>
	<em>The article was written by Clix and permitted to be published here.</em>
</p>
<p>
	Virtual Memory is a part of the total memory available on your Hard Disk assigned to act like normal RAM. While this isn&#39;t
	as good as actual RAM, it still is good enough to improve the overall performance, when setup proper that is. If you let
	Windows manage your Virtual memory, it often resizes the swap file (the part of the HD-memory that acts like ram), which
	might actually work out worse for your performance, as it uses some of the resources while resizing the swapfile.
</p>
<p>
	Anyway, there is a way to set the swap file size to a fixed amount, which will increase your overall performance.
</p>
<p>
	Go to Start -&gt; Control Panel -&gt; System -&gt; Performance -&gt; Virtual Memory. For best performance, it&#39;s recommended
	to assign twice your amount of RAM for the swap file size. Make both maximum and minimum swap file size the same. For example,
	if you have 512MB ram, specify 1024MB ram minimum and maximum for the swap file.
</p>
<p>
	Note: If you do not know how many MB RAM you have,
	<a href="http://hp.vector.co.jp/authors/VA002374/src/download.html">check this</a>
	<a href="http://hp.vector.co.jp/authors/VA002374/src/download.html" target="_blank"></a> and download the file called wcpu330.exe. The file is a self-extractor, so just extract it wherever you want, then
	open the file called wcpuid.exe/ You should see your amount of RAM specified on the right, under "Memory".
</p>

## Widescreen
<p>
	Hi!
</p>
<p>
	I bought an Eizo 21" Widescreen monitor some weeks ago and wanted to play several of "ye olde games", especially
	DX with the new experience (look at my sig).<br /> For all of you who also share this ultimate gaming experience but
	had problems with setting up the right values, here's my help:
</p>
<p>
	In the DeusEx.ini change the following values to your widescreen monitor settings:
</p>
<p>
	<br />
	<span class="code">[WinDrv.WindowsClient]<br />
WindowedViewportX=[color=red]1680[/color]<br />
WindowedViewportY=[color=red]1050[/color]<br />
WindowedColorBits=32<br />
FullscreenViewportX=[color=red]1680[/color]<br />
FullscreenViewportY=[color=red]1050[/color]<br />
FullscreenColorBits=32</span>
</p>
<p>
	Simply put you screen resolution there.
</p>
<p>
	This leads to a horizontally wider picture.
</p>
<p>
	If you want to adjust the FOV according to widescreen proportions (some degrees more than normal) you have to change two
	settings in the file user.ini:
</p>
<p>
	<br />
	<br />
	<span class="code">DesiredFOV=<strong>85.28127</strong><br />
DefaultFOV=<strong>85.28127</strong></span>
</p>
<p>
	<br /> These are the appropriate values for 16:10 monitors.<br /> The strange values are the result of the unusual DeusEx
	default values of 75&Acirc;&deg; for the FOV. If you leave the FOV then the top and bottom portions of the view are simply
	cut off to fit the 16:10 ratio. The hud is not cut off but fit into the view.
</p>
<p>
	The HUD is rendered in low resolution, but the whole 3D stuff is high-res :)
</p>
<p>
	Here are screenshots for direct comparison:
</p>
<p>
	Standard:
</p>
<p>
	<img border="0" height="262" src="http://i38.photobucket.com/albums/e102/albedo-co/DX-Ssmall.jpg" width="349" />
</p>
<p>
	<br /> &nbsp;
	<a href="http://i38.photobucket.com/albums/e102/albedo-co/DX-S.jpg">Link</a> Full Res 4:3 is here (1400x1050)
</p>
<p>
	<br /> Widescreen:
</p>
<p>
	<a href="http://i38.photobucket.com/albums/e102/albedo-co/DX-WSsmall.jpg"><img border="0" height="262" src="http://i38.photobucket.com/albums/e102/albedo-co/DX-WSsmall.jpg" width="420" /></a>
</p>
<p>
	<br />
	<a href="http://i38.photobucket.com/albums/e102/albedo-co/DX-WS.jpg">Link</a>&nbsp;Full Res 16:10 is here (1680x1050)
</p>
<p>
	Quite a difference :)
</p>
<p>
	See you,
</p>
<p>
	al'be:do
</p>

## Windows

<p>
	If your monitor is wide you might experience problems with sniping. You may try playing in a smaller window.
</p>
<p>
	The problem about it is that by default window mode in Deus Ex is very dark and you&#39;ll be unable to see anything even
	if brightness is on max level. Though there is a solution:
</p>
<ol>
	<li>
		<a href="kb/improvements/changing-rendering-devices">Download and install an enhanced OpenGL renderer</a>.</li>
	<li>Open DeusEx.ini from DeusEx/System.<br />
		<img alt=" " src="assets/images/img.php?f=kb/deusex-ini.gif&w=177" width="177" /></li>
	<li>Find a section called [Engine.Engine] and change <em>WindowedRenderDevice</em> variable under it to <em>OpenGLDrv.OpenGLRenderDevice</em>,
		so it the end it will be<br />
		<span class="code">WindowedRenderDevice=OpenGLDrv.OpenGLRenderDevice</span></li>
	<li>Find a section called [WinDrv.WindowsClient] and change <em>StartupFullscreen</em> to <em>False </em>(so, you won&#39;t
		have to switch to windowed mode each time you run Deus Ex)<span class="code">StartupFullscreen=False</span></li>
	<li>Then optionally you may change <em>WindowedViewportX</em> to something like 1110 and <em>WindowedViewportY</em> to 800.
		These are width and height of a window you&#39;ll be playing at. These values depend on your own preferences and screen
		size. You may not edit these values manually, but change the size of the window when you&#39;re already in game.</li>
	<li>Then optionally you may set brightness (<em>Brightness </em>variable) to 1.000000 (that&#39;s maximum level).</li>
	<li>Save and close the file. <br />
	</li>
</ol>
<p>
	Tips for Windows users:
</p>
<ul>
	<li>If you want to change back to Windows, press "Windows" button on your keyboard if you have it. You may also try
		pressing Alt+Enter two times. </li>
	<li>If you want to change back to full screen mode, press Alt+Enter or type "togglefullscreen" in console (console
		may be activated by pressing "T", then delete "Say" in bottom left corner of your screen).</li>
	<li>You may change window size by dragging it&#39;s corners (you may need to change to Windows though).</li>
</ul>

## INI settings
`Editor's Note: Needs rewriting`
	<p>
		Theres a file called DeusEx.ini in your DeusEx/System folder.
	</p>
	<div style="text-align: center">
		<img alt="DeusEx.ini" src="http://www.dxalpha.com/assets/images/kb/deusex-ini.gif" width="177" />
	</div>
	<p>
		While some people usually just leave this behind, thinking there's nothing special in it, it actually does contain some changable
		properties, which can increase performance, especially if you're using one of the
		<a href="http://cwdohnal.home.mindspring.com/utglr/">updated renderers</a>.
	</p>
	<p>
		Here's an example of what your DeusEx.ini contains, along with some information on it.
	</p>
	<ul>
		<li>Comments on the line, are announced with "//". </li>
		<li>Lines which are not in bold, should not be changed, as your DX might not work properly anymore when changing those.
		</li>
	</ul>
	<div class="code">
		<p>
			[URL]<br /> Protocol=deusex
			<br /> ProtocolDescription=Deus Ex Protocol<strong><br />
Name=Player // This is <u>not</u> your in-game name, changing this entry will not make a difference. If you want to change your playername, do it in your user.ini.</strong><br
			/> Map=Index.dx
			<br /> LocalMap=DX.dx
			<br /> Host=
			<br /> Portal=
			<br /> MapExt=dx
			<br /> SaveExt=dxs
			<br />
			<strong>Port=7790 // This is the port which your server is at, it's not recommended to change it, as you might have to open new ports, for your server to work properly on another port.<br />
Class=DXMTL152b1.MTLJCDenton // Should not be changed. However, if your entry is different than the one mentioned here, I recommend that you get MTL, as it adds several features, like being able to see who are playing in a server. Get MTL <a href="http://download.dxalpha.co.uk/DX1/multiplayer/mods/DXMTL-v152b1-installer.zip" target="_blank">here</a> <br />
</strong><br /> [FirstRun]
			<br /> FirstRun=1100
			<br />
			<br /> [Engine.Engine]
			<br />
			<strong>GameRenderDevice=D3D8Drv.D3D8RenderDevice // This is, as it says, the device that renders your game. There's a chance yours will look different, but that's no problem. It should be one of the following, however.</strong><strong> Either D3D8Drv.D3D8RenderDevice, </strong><strong>D3DDrv.D3DRenderDevice or OpenGLDrv.OpenGLRenderDevice</strong><br
			/> AudioDevice=Galaxy.GalaxyAudioSubsystem
			<br /> NetworkDevice=IpDrv.TcpNetDriver
			<br /> DemoRecordingDevice=Engine.DemoRecDriver
			<br /> Console=Engine.Console
			<br /> Language=int
			<br /> GameEngine=DeusEx.DeusExGameEngine
			<br /> EditorEngine=Editor.EditorEngine
			<br /> WindowedRenderDevice=SoftDrv.SoftwareRenderDevice
			<br /> RenderDevice=GlideDrv.GlideRenderDevice
			<strong><br />
DefaultGame=MMUserInterface160.MMUIGameInfo // If you have something different here, it's recommended to get MMUserInterface. Get MMUserInterface <a href="forum/viewtopic.php?t=8719" target="_blank">here</a>  
</strong>
		</p>
		<p>
			<strong> DefaultServerGame=DXMTL152b1.MTLDeathMatch // </strong><strong>Should not be changed. However, if your entry is different than the
one mentioned here, I recommend that you get MTL, as it adds several
features, like being able to see who are playing in a server. Get MTL <a href="http://download.dxalpha.co.uk/DX1/multiplayer/mods/DXMTL-v152b1-installer.zip" target="_blank">here</a></strong><br
			/> ViewportManager=WinDrv.WindowsClient
			<br /> Render=Render.Render
			<br /> Input=Extension.InputExt
			<br /> Canvas=Engine.Canvas
			<br /> Root=DeusEx.DeusExRootWindow
			<br />
			<strong>CdPath=..\&nbsp; // Setting it to "..\" will let you run Deus Ex without a CD</strong><br />
			<br /> [Core.System]
			<br />
			<strong>PurgeCacheDays=0 // Put this to 0, this way, you won't have to redownload maps from a server, as your cached files won't get deleted. </strong><br
			/> SavePath=..\Save
			<br /> CachePath=..\Cache
			<br /> CacheExt=.uxx
			<br /> Suppress=DevLoad
			<br /> Suppress=DevSave
			<br /> Suppress=DevNetTraffic
			<br /> Suppress=DevGarbage
			<br /> Suppress=DevKill
			<br /> Suppress=DevReplace
			<br /> Suppress=DevSound
			<br /> Suppress=DevCompile
			<br /> Suppress=DevBind
			<br /> Suppress=DevBsp
			<br /> Paths=..\System\*.u
			<br /> Paths=..\Maps\*.dx
			<br /> Paths=..\Textures\*.utx
			<br /> Paths=..\Sounds\*.uax
			<br /> Paths=..\Music\*.umx
			<br />
			<br /> [DeusEx.DeusExGameEngine]
			<br />
			<strong>CacheSizeMegs=32 // It's recommended to put this value at 32, as it will cause the game to run smoother.</strong><br
			/>
			<strong>
UseSound=True // Pretty obvious, whether to use sound or not</strong><br /> ServerActors=IpDrv.UdpBeacon
			<br /> ServerActors=IpServer.UdpServerQuery
			<br />
			<strong>ServerActors=Nephthys.NptServerQuery<br />
ServerActors=Nephthys.NptServerUplink MasterServerAddress=master0.gamespy.com MasterServerPort=27900</strong>
		</p>
		<p>
			<strong>ServerActors=Nephthys.NptServerUplink MasterServerAddress=master.dxmtl.eu MasterServerPort=27900 // If you're a serverhoster, make sure you got nephthys, as it provides several fixes against exploits which for example could just make your server crash.</strong>			<strong>If you don't host though, there's no need to install nephthys. Get Nephtys <a href="forum/viewtopic.php?t=8684" target="_blank">here</a> </strong>
		</p>
		<p>
			<strong>ServerPackages=DXMTL152b1 // As mentioned a few times earlier, recommended mod, even for serverhosters, as it will make the game much smoother, amongst other good things. Get MTL <a href="http://download.dxalpha.co.uk/DX1/multiplayer/mods/DXMTL-v152b1-installer.zip" target="_blank">here</a> </strong><br
			/>
			<br /> [WinDrv.WindowsClient]
			<br /> WindowedViewportX=640
			<br /> WindowedViewportY=480
			<br /> WindowedColorBits=32
			<br /> FullscreenViewportX=1024
			<br /> FullscreenViewportY=768
			<br /> FullscreenColorBits=32
			<br /> Brightness=1.000000
			<br /> MipFactor=0.000000
			<br /> UseDirectDraw=True
			<br /> UseJoystick=False
			<br /> CaptureMouse=True
			<br /> StartupFullscreen=True
			<br /> CurvedSurfaces=False
			<br /> ScreenFlashes=False
			<br /> NoLighting=False
			<br /> SlowVideoBuffering=False
			<br /> DeadZoneXYZ=True
			<br /> DeadZoneRUV=False
			<br /> InvertVertical=False
			<br /> ScaleXYZ=1000.000000
			<br /> ScaleRUV=2000.000000
			<br />
			<strong>
SkinDetail=High // Set this to Low, or Normal, to increase performance at cost of quality.</strong>
		</p>
		<p>
			<strong><br />
TextureDetail=High </strong><strong>// Set this to Low, or Normal, to increase performance at cost of quality.</strong>
		</p>
		<p>
			<strong></strong><br />
			<strong>
Decals=True // Setting this option to false will increase performance, but will disallow you to see blood appear. While this might not sound bad at first, you'll have to remember that you can use the blood, as a way to see if you are actually hitting the player server-side. Very handy in somewhat laggy situations.</strong><br
			/>
			<strong></strong>
		</p>
		<p>
			<strong>
MinDesiredFrameRate=30.000000 // At this value, Deus Ex will cut down quality, if your fps drops below 30. This results in your fps being more stable, and being higher generally.</strong><br
			/> UseDirectInput=False
			<br />
			<strong>
NoDynamicLights=False // In Multiplayer, having this option set to true, will not do much, apart from your light augmentation not working properly. In SinglePlayer however it voids the lighting stuff, making all areas look the same:Previously shadowed areas would just look normal now.</strong><br
			/>
			<br /> [Engine.Player]
			<br /> ConfiguredInternetSpeed=20000
			<br /> ConfiguredLanSpeed=20000
			<br />
			<br /> [Galaxy.GalaxyAudioSubsystem]
			<br /> UseDirectSound=True
			<br /> UseFilter=True
			<br /> UseSurround=False
			<br /> UseStereo=False
			<br /> UseCDMusic=False
			<br /> UseDigitalMusic=True
			<br /> UseSpatial=False
			<br /> UseReverb=True
			<br /> Use3dHardware=False
			<br /> LowSoundQuality=False
			<br /> ReverseStereo=False
			<br /> Latency=40
			<br /> OutputRate=22050Hz
			<br /> EffectsChannels=16
			<br /> DopplerSpeed=6500.000000
			<br /> MusicVolume=153
			<br /> SoundVolume=204
			<br /> SpeechVolume=255
			<br /> AmbientFactor=0.700000
			<br />
			<br /> [IpDrv.TcpNetDriver]
			<br /> AllowDownloads=True
			<br /> ConnectionTimeout=15.0
			<br /> InitialConnectTimeout=500.0
			<br /> AckTimeout=1.0
			<br /> KeepAliveTime=1.0
			<br /> MaxClientRate=20000
			<br /> SimLatency=0
			<br /> RelevantTimeout=5.0
			<br /> SpawnPrioritySeconds=1.0
			<br /> ServerTravelPause=4.0
			<br /> NetServerMaxTickRate=20
			<br /> LanServerMaxTickRate=35
			<br /> StaticUpdateRate=12
			<br /> DynamicUpdateRate=40
			<br />
			<br /> [IpDrv.TcpipConnection]
			<br /> SimPacketLoss=0
			<br /> SimLatency=0
			<br />
			<br /> [IpServer.UdpServerQuery]
			<br /> GameName=deusex
			<br />
			<br /> [IpDrv.UdpBeacon]
			<br /> DoBeacon=True
			<br /> BeaconTime=0.50
			<br /> BeaconTimeout=5.0
			<br /> BeaconPort=7776
			<br /> BeaconProduct=DeusEx
			<br />
			<br /> [SoftDrv.SoftwareRenderDevice]
			<br /> Translucency=True
			<br /> VolumetricLighting=True
			<br /> ShinySurfaces=False
			<br /> Coronas=False
			<br /> HighDetailActors=True
			<br /> HighResTextureSmooth=True
			<br /> LowResTextureSmooth=False
			<br /> FastTranslucency=True
			<br />
			<br /> [GlideDrv.GlideRenderDevice]
			<br /> Translucency=True
			<br /> VolumetricLighting=True
			<br /> ShinySurfaces=True
			<br /> Coronas=True
			<br /> HighDetailActors=True
			<br /> DetailBias=-1.500000
			<br /> RefreshRate=100Hz
			<br /> DetailTextures=True
			<br /> FastUglyRefresh=False
			<br /> ScreenSmoothing=True
			<br /> Resolution=Default
			<br />
			<br /> [MetalDrv.MetalRenderDevice]
			<br /> Translucency=True
			<br /> VolumetricLighting=True
			<br /> ShinySurfaces=True
			<br /> Coronas=True
			<br /> HighDetailActors=True
			<br /> DetailTextures=True
			<br />
			<br />
			<strong>[OpenGLDrv.OpenGLRenderDevice] // This section assumes you have the updated OpenGL Renderer, if you do not, please skip this section.</strong>
		</p>
		<p>
			<strong>Translucency=True // Allows you to look through windows, shouldn't be disabled, even if you're struggling for performance, as it hardly affects performance</strong>
		</p>
		<p>
			<strong>VolumetricLighting=True // Should be set to to true, setting it to false might make lightbuttons not work anymore (including your light augmentation)</strong>
		</p>
		<p>
			<strong>ShinySurfaces=True // Setting it to false will make mirrors stop reflecting the environment.</strong>
		</p>
		<p>
			<strong></strong><strong>Coronas=False // Setting it to true will cause street lights to have a glare around the light. Doesn't really affect performance, so put it to whatever you like.</strong>
		</p>
		<p>
			<strong></strong><strong>HighDetailActors=False // Setting it to true will cause the actors to look more detailed, does affect performance quite a bit, so if you're struggling for fps, set it to false.</strong>
		</p>
		<p>
			<strong>DetailTextures=False // Setting it to true will cause objects to look more detailed, affects performance as well, so if you're struggling for fps, set it to false.<br />
</strong>UseTNT=False<br /> MinDepthBits=0
			<br /> MaxLogUOverV=8
		</p>
		<p>
			MaxLogVOverU=8
		</p>
		<p>
			UseMultiTexture=True
		</p>
		<p>
			<strong>
UsePalette=True // You should experiment around with this, some GFX cards perform better when this is toggled on, others do not.</strong><br
			/>
			<strong>
UseAlphaPalette=True // Should be set to True, unless you have a really old computer with very old buggy GeForce drivers</strong><br
			/> ShareLists=False
			<br /> AlwaysMipmap=True
			<br />
			<strong>
DoPrecache=0 // Changing the value to 1, will make DX precache the maps every time you load them, making you have a little fps boost. There seems to be a bug however, making it precache the map every time you go to menu, causing a lot of annoyance after a while.</strong>
		</p>
		<p>
			<strong>UseTrilinear=False // Makes the textures look a bit more nice than before, effects performance though, so keep it to false when you're struggling for fps.</strong><br
			/> MaxAnisotropy=0
			<br /> SupportsLazyTextures=0
			<br /> TruFormMinVertices=0
			<br /> TruFormTessellation=3
			<br /> UseTruForm=False
			<br /> AAFilterHint=0
			<br />
			<strong>
NumAASamples=0 // Makes the edges of surfaces look better, put it either to 0, 2, 4, 6 or 8. 0 is no AA, 8 is max AA. Putting this to an other value than 0 will hurt your performance, so recommended to keep it to 0, when you're in dire need of fps.</strong>
		</p>
		<p>
			<strong></strong><strong>UseAA=False // Whether to use AA or not</strong><br /> RequestHighResolutionZ=True
			<br /> MaskedTextureHack=True
			<br />
			<strong>
FrameRateLimit=0 //</strong>
			<strong>Computer controlled frame rate limiter in frames per second.  Set to 0 to disable.</strong>
		</p>
		<p>
			<strong></strong><strong>SwapInterval=-1 // Controls V Sync. If set to the default value of -1, the default buffer
swapping method is used. Set to 0 to disable V Sync. Set to 1 to enable
V Sync.</strong><br /> UseVertexProgram=False
			<br /> UseCVA=False
			<br /> UseMultiDrawArrays=False
			<br /> TexDXT1ToDXT3=False
			<br /> DynamicTexIdRecycleLevel=100
			<br /> CacheStaticMaps=True
			<br /> UseTexPool=True
			<br /> UseTexIdPool=True
			<br /> UseSSE=True
			<br /> BufferClippedActorTris=True
			<br /> SinglePassDetail=True
			<br /> ColorizeDetailTextures=False
			<br />
			<strong>
DetailClipping=True // Enables the use of a somewhat experimental detail texture mode. It
costs more CPU time, but may improve performance in fill rate limited
situations.</strong><br /> UseDetailAlpha=True
			<br />
			<strong>RefreshRate=100 // Allows you to set a specific limit for your FPS to be at. (usually done, to lessen the strain on your computer) VSync has to be toggled on for this to work.</strong><br
			/> MaxTMUnits=0
		</p>
		<p>
			NoFiltering=False<br />
			<strong>
Use16BitTextures=True // Setting it to false will let you use 32 bit textures, which look better, but again decrease performance, set it to True, if you're struggling for FPS</strong><br
			/> UseS3TC=False
			<br /> AutoGenerateMipmaps=False
			<br />
			<strong>
UsePrecache=False // </strong><strong>Changing the value to 1, will make DX precache the maps every time
you load them, making you have a little fps boost. There seems to be a
bug however, making it precache the map every time you go to menu,
causing a lot of annoyance after a while.</strong><br /> UseBGRATextures=True
			<br /> UseZTrick=False
			<br /> MaxLogTextureSize=0
			<br /> MinLogTextureSize=0
			<br /> OneXBlending=False
			<br /> GammaCorrectScreenshots=False
			<br /> GammaOffsetBlue=0.000000
			<br /> GammaOffsetGreen=0.000000
			<br /> GammaOffsetRed=0.000000
			<br /> GammaOffset=0.0000000
			<br />
			<strong>
LODBias=1.100000 // Putting this to a positive value, wil cut the detail of textures, if they're far away from you, which will avoid your fps dropping massively when looking at a big part of the map. Putting it to a negative value will make textures blur less at long range, causing them to look better, but it will cut on your performance massively, especially when looking at a big part of the map.</strong><br
			/> DescFlags=0
			<br /> Description=
			<br />
			<strong>
ZRangeHack=True // Setting this to true will fix problems with decals flickering at long range. Please note that this is a "hack" and can result in something not displaying properly.</strong><br
			/> SmoothMaskedTextures=False
			<br /> SceneNodeHack=True
			<br /> UseSSE2=True
			<br /> BufferTileQuads=True
			<br /> SinglePassFog=True
			<br /> DetailMax=0
			<br /> NoMaskedS3TC=False
			<br />
			<br /> [D3DDrv.D3DRenderDevice]
			<br />
			<strong>
Translucency=True // Setting it to false will make it impossible to look through windows and other translucent things</strong>
		</p>
		<p>
			<strong></strong><br />
			<strong>VolumetricLighting=True // Should be set to to true, setting it to
false might make lightbuttons not work anymore (including your light
augmentation)</strong>
		</p>
		<p>
			<strong></strong><strong>ShinySurfaces=True // Setting it to false will make mirrors stop reflecting the environment. </strong><br
			/>
			<strong></strong>
		</p>
		<p>
			<strong>Coronas=False // Setting it to true will cause street lights to have
a glare around the light. Doesn't really affect performance, so put it
to whatever you like.</strong><br />
			<strong></strong>
		</p>
		<p>
			<strong>HighDetailActors=False // Setting it to true will cause the
actors to look more detailed, does affect performance quite a bit, so
if you're struggling for fps, set it to false.</strong><strong></strong><br /> UseMipmapping=True
			<br />
			<strong>
UseTrilinear=True // Whether to use Bilinear or Trilinear filtering, when set to true, graphics might look a bit better, with a minor performance loss</strong><br
			/> UseMultitexture=True
			<br /> UsePageFlipping=True
			<br />
			<strong>
UsePalette=True // You should experiment around with this, some GFX cards perform better when this is toggled on, others do not.<br />
</strong><br />
			<strong>
UseFullscreen=True // Whether to use fullscreen for DX or not.</strong><br /> UseGammaCorrection=True
			<br />
			<strong>
DetailTextures=False // Setting it to false will increase performance at the cost of the quality of the texture detail.</strong><br
			/>
			<strong>
Use3dfx=False // Whether to use 3dfx or not, if you don't have a Voodoo card, leave this option on False</strong><br />			UseTripleBuffering=True
			<br /> UsePrecache=True
			<br />
			<strong>
Use32BitTextures=True // Setting it to false will increase performance at the cost of the quality of the textures.</strong><br
			/> DescFlags=1
			<br /> dwDeviceId=16712
			<br /> dwVendorId=4098
			<br /> UseVertexFog=False
			<br /> UseAGPTextures=True
			<br /> UseVideoMemoryVB=False
			<br />
			<strong>
UseVSync=True // Setting this to false will stop your fps getting limited at a number (usually 60) For some, setting this to false will let them have higher fps. Others however seem to get higher fps as well, but it feels like very low fps. (worse than before) So it's recommended to try this out for yourself.</strong><br
			/> Description=RADEON 9800 SERIES&nbsp; <br />
			<br /> [SglDrv.SglRenderDevice]
			<br /> Translucency=True
			<br /> VolumetricLighting=False
			<br /> ShinySurfaces=False
			<br /> Coronas=True
			<br /> HighDetailActors=False
			<br /> ColorDepth=16
			<br /> DetailTextures=False
			<br /> FastUglyRefresh=False
			<br /> TextureDetailBias=Near
			<br /> VertexLighting=False
			<br />
			<br /> [Editor.EditorEngine]
			<br /> UseSound=True
			<br /> CacheSizeMegs=32
			<br /> GridEnabled=True
			<br /> SnapVertices=True
			<br /> SnapDistance=10.000000
			<br /> GridSize=(X=16.000000,Y=16.000000,Z=16.000000)
			<br /> RotGridEnabled=True
			<br /> RotGridSize=(Pitch=1024,Yaw=1024,Roll=1024)
			<br /> GameCommandLine=-log
			<br /> FovAngleDegrees=90.000000
			<br /> GodMode=True
			<br /> AutoSave=False
			<br /> AutoSaveTimeMinutes=5
			<br /> AutoSaveIndex=6
			<br /> C_WorldBox=(R=0,G=0,B=107,A=0)
			<br /> C_GroundPlane=(R=0,G=0,B=63,A=0)
			<br /> C_GroundHighlight=(R=0,G=0,B=127,A=0)
			<br /> C_BrushWire=(R=255,G=63,B=63,A=0)
			<br /> C_Pivot=(R=0,G=255,B=0,A=0)
			<br /> C_Select=(R=0,G=0,B=127,A=0)
			<br /> C_AddWire=(R=127,G=127,B=255,A=0)
			<br /> C_SubtractWire=(R=255,G=192,B=63,A=0)
			<br /> C_GreyWire=(R=163,G=163,B=163,A=0)
			<br /> C_Invalid=(R=163,G=163,B=163,A=0)
			<br /> C_ActorWire=(R=127,G=63,B=0,A=0)
			<br /> C_ActorHiWire=(R=255,G=127,B=0,A=0)
			<br /> C_White=(R=255,G=255,B=255,A=0)
			<br /> C_SemiSolidWire=(R=127,G=255,B=0,A=0)
			<br /> C_NonSolidWire=(R=63,G=192,B=32,A=0)
			<br /> C_WireGridAxis=(R=119,G=119,B=119,A=0)
			<br /> C_ActorArrow=(R=163,G=0,B=0,A=0)
			<br /> C_ScaleBox=(R=151,G=67,B=11,A=0)
			<br /> C_ScaleBoxHi=(R=223,G=149,B=157,A=0)
			<br /> C_Mover=(R=255,G=0,B=255,A=0)
			<br /> C_OrthoBackground=(R=163,G=163,B=163,A=0)
			<br /> C_Current=(R=0,G=0,B=0,A=0)
			<br /> C_BrushVertex=(R=0,G=0,B=0,A=0)
			<br /> C_BrushSnap=(R=0,G=0,B=0,A=0)
			<br /> C_Black=(R=0,G=0,B=0,A=0)
			<br /> C_Mask=(R=0,G=0,B=0,A=0)
			<br /> C_WireBackground=(R=0,G=0,B=0,A=0)
			<br /> C_ZoneWire=(R=0,G=0,B=0,A=0)
			<br /> EditPackages=Core
			<br /> EditPackages=Engine
			<br /> EditPackages=Editor
			<br /> EditPackages=Fire
			<br /> EditPackages=IpDrv
			<br /> EditPackages=Extension
			<br /> EditPackages=DeusExUI
			<br /> EditPackages=ConSys
			<br /> EditPackages=DeusExConversations
			<br /> EditPackages=DeusExSounds
			<br /> EditPackages=DeusExItems
			<br /> EditPackages=DeusExDeco
			<br /> EditPackages=DeusExCharacters
			<br /> EditPackages=DeusExText
			<br /> EditPackages=DeusEx
			<br /> EditPackages=IpServer
			<br />
			<br /> [DeusEx.DeusExGameInfo]
			<br /> bNoMonsters=False
			<br /> bHumansOnly=False
			<br /> bCoopWeaponMode=False
			<br /> bClassicDeathmessages=False
			<br />
			<br /> [Engine.GameInfo]
			<br /> bLowGore=True
			<br /> bMuteSpectators=True
			<br /> bNoCheating=True
			<br /> bAllowFOV=False
			<br /> AutoAim=1.000000
			<br /> GameSpeed=1.000000
			<br /> MaxSpectators=2
			<br /> AdminPassword=AdminPass
			<br /> GamePassword=
			<br /> MaxPlayers=8
			<br /> IPPolicies[0]=ACCEPT,*
			<br /> IPPolicies[1]=
			<br /> IPPolicies[2]=
			<br /> IPPolicies[3]=
			<br /> IPPolicies[4]=
			<br /> IPPolicies[5]=
			<br /> IPPolicies[6]=
			<br /> IPPolicies[7]=
			<br /> IPPolicies[8]=
			<br /> IPPolicies[9]=
			<br /> IPPolicies[10]=
			<br /> IPPolicies[11]=
			<br /> IPPolicies[12]=
			<br /> IPPolicies[13]=
			<br /> IPPolicies[14]=
			<br /> IPPolicies[15]=
			<br /> IPPolicies[16]=
			<br /> IPPolicies[17]=
			<br /> IPPolicies[18]=
			<br /> IPPolicies[19]=
			<br /> IPPolicies[20]=
			<br /> IPPolicies[21]=
			<br /> IPPolicies[22]=
			<br /> IPPolicies[23]=
			<br /> IPPolicies[24]=
			<br /> IPPolicies[25]=
			<br /> IPPolicies[26]=
			<br /> IPPolicies[27]=
			<br /> IPPolicies[28]=
			<br /> IPPolicies[29]=
			<br /> IPPolicies[30]=
			<br /> IPPolicies[31]=
			<br /> IPPolicies[32]=
			<br /> IPPolicies[33]=
			<br /> IPPolicies[34]=
			<br /> IPPolicies[35]=
			<br /> IPPolicies[36]=
			<br /> IPPolicies[37]=
			<br /> IPPolicies[38]=
			<br /> IPPolicies[39]=
			<br /> IPPolicies[40]=
			<br /> IPPolicies[41]=
			<br /> IPPolicies[42]=
			<br /> IPPolicies[43]=
			<br /> IPPolicies[44]=
			<br /> IPPolicies[45]=
			<br /> IPPolicies[46]=
			<br /> IPPolicies[47]=
			<br /> IPPolicies[48]=
			<br /> IPPolicies[49]=
			<br /> ServerLogName=server.log
			<br /> bLocalLog=True
			<br /> bWorldLog=True
			<br /> bBatchLocal=False
			<br /> DemoBuild=0
			<br /> DemoHasTuts=0
			<br />
			<br /> [Engine.DemoRecDriver]
			<br /> DemoSpectatorClass=UnrealShare.UnrealSpectator
			<br /> MaxClientRate=25000
			<br /> ConnectionTimeout=15.0
			<br /> InitialConnectTimeout=500.0
			<br /> AckTimeout=1.0
			<br /> KeepAliveTime=1.0
			<br /> SimLatency=0
			<br /> RelevantTimeout=5.0
			<br /> SpawnPrioritySeconds=1.0
			<br /> ServerTravelPause=4.0
			<br /> NetServerMaxTickRate=60
			<br /> LanServerMaxTickRate=60
			<br />
			<br /> [DeusEx.MenuScreenJoinGame]
			<br /> MasterServerAddress=master0.gamespy.com
			<br />
			<br /> [Engine.GameReplicationInfo]
			<br /> ServerName=
		</p>
		<p>
			ShortName=<br /> [IpServer.UdpBeacon]
			<br /> BeaconProduct=DeusEx
			<br />
			<br /> [WindowPositions]
			<br /> GameLog=(X=335,Y=28,XL=637,YL=545)
			<br /> ConfigPageRenderer=(X=5,Y=96,XL=516,YL=280)
			<br /> ConfigPageDriver=(X=5,Y=96,XL=516,YL=280)
			<br /> ConfigPageDetail=(X=5,Y=96,XL=516,YL=280)
			<br /> ConfigPageFirstTime=(X=5,Y=96,XL=516,YL=280)
			<br /> WizardDialog=(X=247,Y=151,XL=530,YL=436)
			<br /> Preferences=(X=390,Y=32,XL=352,YL=512)
			<br /> ConfigPageSafeMode=(X=5,Y=96,XL=516,YL=280)
			<br /> ConfigPageSafeOptions=(X=5,Y=96,XL=516,YL=280)
			<br />
			<br /> [Engine.GameEngine]
			<br /> GameRenderDevice=Class'OpenGLDrv.OpenGLRenderDevice'
			<br /> AudioDevice=Class'Galaxy.GalaxyAudioSubsystem'
			<br /> Console=Class'Engine.Console'
			<br /> NetworkDevice=Class'IpDrv.TcpNetDriver'
			<br /> Language=None
			<br /> CacheSizeMegs=32
			<br /> UseSound=True
			<br />
			<br /> [DeusEx.dxmaplist]
			<br /> Maps[0]=DXMP_Silo
			<br /> Maps[1]=DXMP_Area51Bunker
			<br /> Maps[2]=DXMP_Cathedral
			<br /> Maps[3]=DXMP_Cmd
			<br /> Maps[4]=DXMP_Smuggler
			<br /> Maps[5]=
			<br /> Maps[6]=
			<br /> Maps[7]=
			<br /> Maps[8]=
			<br /> Maps[9]=
			<br /> Maps[10]=
			<br /> Maps[11]=
			<br /> Maps[12]=
			<br /> Maps[13]=
			<br /> Maps[14]=
			<br /> Maps[15]=
			<br /> Maps[16]=
			<br /> Maps[17]=
			<br /> Maps[18]=
			<br /> Maps[19]=
			<br /> Maps[20]=
			<br /> Maps[21]=
			<br /> Maps[22]=
			<br /> Maps[23]=
			<br /> Maps[24]=
			<br /> Maps[25]=
			<br /> Maps[26]=
			<br /> Maps[27]=
			<br /> Maps[28]=
			<br /> Maps[29]=
			<br /> Maps[30]=
			<br /> Maps[31]=
			<br /> MapSizes[0]=(6-10)
			<br /> MapSizes[1]=(8-14)
			<br /> MapSizes[2]=(8-14)
			<br /> MapSizes[3]=(12-16)
			<br /> MapSizes[4]=(2-6)
			<br /> MapSizes[5]=
			<br /> MapSizes[6]=
			<br /> MapSizes[7]=
			<br /> MapSizes[8]=
			<br /> MapSizes[9]=
			<br /> MapSizes[10]=
			<br /> MapSizes[11]=
			<br /> MapSizes[12]=
			<br /> MapSizes[13]=
			<br /> MapSizes[14]=
			<br /> MapSizes[15]=
			<br /> MapSizes[16]=
			<br /> MapSizes[17]=
			<br /> MapSizes[18]=
			<br /> MapSizes[19]=
			<br /> MapSizes[20]=
			<br /> MapSizes[21]=
			<br /> MapSizes[22]=
			<br /> MapSizes[23]=
			<br /> MapSizes[24]=
			<br /> MapSizes[25]=
			<br /> MapSizes[26]=
			<br /> MapSizes[27]=
			<br /> MapSizes[28]=
			<br /> MapSizes[29]=
			<br /> MapSizes[30]=
			<br /> MapSizes[31]=
			<br /> MapNum=4
			<br /> CycleType=0
			<br />
			<br /> [Engine.MapList]
			<br /> Maps[0]=
			<br /> Maps[1]=
			<br /> Maps[2]=
			<br /> Maps[3]=
			<br /> Maps[4]=
			<br /> Maps[5]=
			<br /> Maps[6]=
			<br /> Maps[7]=
			<br /> Maps[8]=
			<br /> Maps[9]=
			<br /> Maps[10]=
			<br /> Maps[11]=
			<br /> Maps[12]=
			<br /> Maps[13]=
			<br /> Maps[14]=
			<br /> Maps[15]=
			<br /> Maps[16]=
			<br /> Maps[17]=
			<br /> Maps[18]=
			<br /> Maps[19]=
			<br /> Maps[20]=
			<br /> Maps[21]=
			<br /> Maps[22]=
			<br /> Maps[23]=
			<br /> Maps[24]=
			<br /> Maps[25]=
			<br /> Maps[26]=
			<br /> Maps[27]=
			<br /> Maps[28]=
			<br /> Maps[29]=
			<br /> Maps[30]=
			<br /> Maps[31]=
			<br /> MapNum=0
			<br />
			<br /> [DeusEx.DeusExMPGame]
			<br /> SkillsTotal=2000
			<br /> SkillsAvail=0
			<br /> SkillsPerKill=0
			<br /> InitialAugs=0
			<br /> AugsPerKill=0
			<br /> ScoreToWin=25
			<br /> VictoryCondition=Time
			<br /> MPSkillStartLevel=3
			<br /> CurrentMap=DXMP_Cmd
			<br /> fFriendlyFireMult=0.000000
			<br /> bTrackWeapons=False
			<br /> bNoMonsters=False
			<br /> bHumansOnly=False
			<br /> bCoopWeaponMode=False
			<br /> bClassicDeathMessages=False
			<br />
			<br /> [IpServer.UdpServerUplink]
			<br /> DoUplink=False
			<br /> UpdateMinutes=1
			<br /> MasterServerAddress=779
			<br /> MasterServerPort=1544172281
			<br /> Region=0
			<br />
			<br /> [DeusEx.menuscreenhostgame]
			<br /> CurrentGameType=DeusEx.DeathMatchGame
			<br /> ServerMode=1
			<br />
			<br /> [DXMTL152b1.MTLAdvTeam]
			<br /> bNoMonsters=False
			<br /> bHumansOnly=False
			<br /> bCoopWeaponMode=False
			<br /> bClassicDeathMessages=False
			<br />
			<br /> [D3D8Drv.D3D8RenderDevice]
			<br />
			<strong>
ZRangeHack=True // Setting this to true will fix problems with decals
flickering at long range. Please note that this is a &quot;hack&quot; and can
result in something not displaying properly.</strong>
		</p>
		<p>
			<strong></strong><br />
			<strong>
NumAASamples=0 // Makes the edges of surfaces look better, put it
either to 0, 2, 4, 6 or 8. 0 is no AA, 8 is max AA. Putting this to an
other value than 0 will hurt your performance, so recommended to keep
it to 0, when you're in dire need of fps.</strong>
			<strong></strong>
		</p>
		<p>
			<strong>UseAA=False // Whether to use AA or not</strong><br /> RequestHighResolutionZ=True
			<br /> UseSoftwareVertexProcessing=False
			<br /> UsePureDevice=False
			<br /> UseTripleBuffering=False
			<br /> MaskedTextureHack=False
			<br /> SmoothMaskedTextures=False
			<br /> SceneNodeHack=False
			<br />
			<strong>FrameRateLimit=0 //CPU controlled frame rate limiter in frames per second.  Set to 0 to disable. (This won't work if your driver doesn't let the application decide on these options.)</strong><br
			/>
			<strong></strong>
		</p>
		<p>
			<strong>SwapInterval=-1 // Controls V Sync. If set to the default value of -1, the default buffer
swapping method is used. Set to 0 to disable V Sync. Set to 1 to enable
V Sync.</strong><br /> UseVertexProgram=False
			<br /> TexDXT1ToDXT3=False
			<br /> DynamicTexIdRecycleLevel=100
			<br /> CacheStaticMaps=False
			<br /> UseTexPool=True
			<br /> UseTexIdPool=True
			<br /> UseSSE2=True
			<br /> UseSSE=True
			<br /> BufferTileQuads=True
			<br /> BufferClippedActorTris=True
			<br /> SinglePassDetail=False
			<br /> SinglePassFog=False
			<br /> ColorizeDetailTextures=False
			<br />
			<strong>
DetailClipping=True // Enables the use of a somewhat experimental detail texture mode. It
costs more CPU time, but may improve performance in fill rate limited
situations.</strong><br /> UseDetailAlpha=True
			<br /> DetailMax=0
			<br />
			<strong>
RefreshRate=85 // Allows you to set a limit on your fps, sometimes it's required, for those who get a really messed up DX when there's no frame limit. Please note that if you have disabled vsync in your driver's options, that it simply won't work.</strong><br
			/> MaxTMUnits=0
			<br /> NoFiltering=False
			<br /> MaxAnisotropy=0
			<br />
			<strong>
Use16BitTextures=True // Setting this to False will make stuff look better, at the cost of performance</strong><br />			UseS3TC=False
			<br /> UseAlphaPalette=False
			<br /> UseTrilinear=False
			<br /> UsePrecache=False
			<br />
			<strong>
UsePalette=True // You should experiment around with this, some GFX cards perform better when this is toggled on, others do not.</strong><br
			/> UseMultiTexture=True
			<br /> MaxLogTextureSize=8
			<br /> MinLogTextureSize=0
			<br /> MaxLogVOverU=8
			<br /> MaxLogUOverV=8
			<br /> OneXBlending=True
			<br /> GammaCorrectScreenshots=False
			<br /> GammaOffsetBlue=0.000000
			<br /> GammaOffsetGreen=0.000000
			<br /> GammaOffsetRed=0.000000
			<br /> GammaOffset=0.000000
			<br />
			<strong>
LODBias=1.100000 // Putting this to a positive value, wil cut the
detail of textures, if they're far away from you, which will avoid your
fps dropping massively when looking at a big part of the map. Putting
it to a negative value will make textures blur less at long range,
causing them to look better, but it will cut on your performance
massively, especially when looking at a big part of the map.</strong><br />
			<strong></strong>
		</p>
		<p>
			<strong>
DetailTextures=True // Setting this option to false will increase performance at cost of quality</strong><br /> DescFlags=0
			<br /> Description=
			<br />
			<strong>HighDetailActors=False // Setting it to true will cause the
actors to look more detailed, does affect performance quite a bit, so
if you're struggling for fps, set it to false.</strong>
		</p>
		<p>
			<strong></strong><br />
			<strong>Coronas=False // Setting it to true will cause street lights to have
a glare around the light. Doesn't really affect performance, so put it
to whatever you like.</strong>
		</p>
		<p>
			<strong></strong><br />
			<strong>ShinySurfaces=True // Setting it to false will make mirrors stop reflecting the environment. </strong>
		</p>
		<p>
			<strong></strong><br />
			<strong>VolumetricLighting=True // Should be set to to true, setting it to
false might make lightbuttons not work anymore (including your light
augmentation)</strong><br />
			<br /> [DXMTL152b1.MTLGameInfo]
			<br /> bNoMonsters=False
			<br /> bHumansOnly=False
			<br /> bCoopWeaponMode=False
			<br /> bClassicDeathMessages=False
		</p>
	</div>
