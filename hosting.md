## Server Starter
<h3>Windows</h3>
Create a text file in your Deus Ex/System folder. Open it up, and place in the following code: <br>

```
@ECHO OFF title Server starter

echo. Starting...

deusex.exe DXMP_CMD?Game=DXMTL152b1.MTLTeam -server -LOG=server.log > NUL
```
<br>
<br>Edit the code to your desire. 
<br>
<br>`DXMP_CMD` - Your map of choice.
<br>
<br>`?Game=xxx` - Your gametype, leave default if you don't know what you're doing. THIS requires the DXMTL mod installed. Other options include DXMTL152b1.MTLDeathmatch. It is possible to use without MTL, but it is NOT RECOMMENDED. But if you insist, the format is DeusEx.DeathMatchGame or DeusEx.TeamDeathmatch
<br>
<br>Additional, adding `?Mutator=x` after the Game string lets you force load mutators, example; `map?Game=gametypestring?Mutator=mPack1.WeaponSelector`
<br>
<br>The `-Log=xxx` flag lets you define a custom log file name, default is Server.log, which keeps a track of your entire server log while running. Renaming this isn't important really, but its an option.
<br>Another optional flag is `-ini=xxx`, which lets you define a seperate .ini file, instead of using the default `DeusEx.ini`.
<br>
<br>Once modified to your choice, save the file as `ServerStarter.bat` From now on, clicking on the new file will execute that code, starting the server. To edit it later, just right click and Edit.
<br>
<h3>Linux</h3>
<br>(Specifically Debian XFCE environment, others may vary. Also assuming you installed via Wine and running the Windows install since DX isn't officially supported.)
<br>In your environment of choice, create a new Launcher file or .desktop file, through whatever package you use to manage those. For the Command, enter
<br>
```
wine "C:\Deus Ex GOTY\System\deusex.exe" DXMP_CMD?Game=DXMTL152b1.MTLTeam -server -LOG=server.log > NUL
```
<br>
<br>The Path to the deusex.exe varies, this is the default for GOG. And varies depending on how you installed it, through Wine or Steam Linux, check that up yourself. The rest of the code functions the same as the Windows version.
<br>
<br>Give it a name, untick Run in Terminal to save screen clutter and make it run more seamlessly, and save. 

*Written by Kaiser*

## Victory Conditions
<p>
	Altering the Victory trigger of your server is a common alteration, and varies from server to server. The two default triggers
	are Frags and Time limit. Depending on the server, you will want to assign an appropiate &quot;trigger&quot;. When this
	trigger is reach (The time limit ends or a player gets enough kills) then the match will end.
</p>
<p>
	There are two ways to alter the Victory trigger of your server, I will show you the Basic method (Recommended) and the Advanced
	method. I recommend using the Basic methods, but if this is not possible (Due to errors) then attempt the Advanced method.
	You only need to do one, so choose before going on.
</p>
<address>
	&nbsp;&nbsp;&nbsp;Basic Method:</address>
<p>
	Firstly, run Deus Ex. Once the application has loaded, click on Multiplayer;
</p>
<p>
	<img alt="Multiplayer Tab" height="37" src="http://www7.imagocentre.com/images/2/Mulitop_138.png" width="277" />&nbsp;
</p>
<p>
	Then Internet Game;
</p>
<p>
	<img alt="OnlineTab" height="39" src="http://www8.imagocentre.com/images/2/Internetop_139.png" width="259" />
</p>
<p>
	Then on Host Game;
</p>
<p>
	<img alt="Host Tab" height="56" src="http://www1.imagocentre.com/images/2/Hostop_140.png" width="136" />
</p>
<p>
	You will be displayed with an image similar to this:
</p>
<p>
	<img alt="OnlineOptions" height="506" src="http://www7.imagocentre.com/images/2/TabOptions_141.png" width="529" />
</p>
<p>
	This is my default server set-up, yours will be different if you haven&#39;t changed it however. You can see that my mouse
	is over the Victory Trigger (Refered to as the &quot;Condition&quot; here.) Clicking on this will alter and rotate between
	these two options:
</p>
<p>
	<img alt="TimeOption" height="61" src="http://www6.imagocentre.com/images/2/TimeOp_142.png" width="458" />
</p>
<p>
	This is the Time Limit trigger. When the set time limit runs out (Here you can see it is 30 Minutes), the game will end.
</p>
<p>
	<img alt="KillLimit" height="55" src="http://www3.imagocentre.com/images/2/TrigOp_143.png" width="461" />
</p>
<p>
	This is the Kill Limit trigger. When any player reachers the kill limit (Here you can see it is 100 Kills, abit high!), the
	game will end.
</p>
<p>
	After choosing the option you would like, continue to alter the other settings (Initial Augumentations, Maximum Players,
	Map etc). Once this is done, decide what server you would prefer to run, Dedicated (The game will close and be run in a
	console, you can re-join the game), or Non-Dedicated (Your game will not close and you will be running the server directly.
	You will not be able to quit the game without disconnecting the server).
</p>
<p>
	Finally, hit Start Game!
</p>
<address>
	&nbsp;&nbsp; Advanced Method: </address>
<p>
	Open DeusEx.ini, (<img alt="DXINI" height="52" src="http://www3.imagocentre.com/images/2/DXINI_146.png" width="228" />&nbsp;)
	and locate this area:
</p>
<p>
	<img alt="MPOptions" height="496" src="http://www3.imagocentre.com/images/2/MPOptions_144.png" width="800" />
</p>
<p>
	You will notice these two areas:
</p>
<p>
	<img alt="TrigOp" height="30" src="http://www6.imagocentre.com/images/2/TriggerINI_145.png" width="247" />
</p>
<p>
	These can be altered, but entering the wrong details can result in&nbsp;host instability, so stick with the Basic Option
	unless you know what your doing!
</p>
<p>
	After the = sign before VictoryCondition, you can enter two options (As was shown above), Frags and Time. As you can see
	above, Frags is already entered. If a server were hosted with the above settings, the Trigger would be 100 kills to win.
	Once again, the two options are:
</p>
<p class="code">
	VictoryCondition=Frags
</p>
<p class="code">
	VictoryCondition=Time
</p>
<p>
	&nbsp;
</p>
<p>
	You can copy and paste one of the above into your DeusEx.ini if you wish.
</p>
<p>
	The ScoreToWin can be altered to anything between 0-99999999. Whatever your victory condition is, it will be applicable to
	the ScoreToWin.
</p>
<p>
	Happy Hosting!
</p>

## Installing mods
Place files in the propor directories inside the Deus Ex game folder;
```
.u - /System/
.utx - /Textures/
.uax - /Sounds/
.umx - /Music/
.int - /System/
.ini - /System/
```

Open up `DeusEx.ini` and find the ServerPackages list, it'll look like;
```
[DeusEx.DeusExGameEngine]
CacheSizeMegs=4
UseSound=True
ServerActors=IpDrv.UdpBeacon
ServerActors=Nephthys.NptServerQuery
ServerActors=Nephthys.NptServerUplink MasterServerAddress=master.333networks.com MasterServerPort=27900 ServerActors=Nephthys.NptServerUplink
MasterServerAddress=master0.gamespy.com MasterServerPort=27900 ServerActors=Nephthys.NptServerUplink MasterServerAddress=master.epicgames.com MasterServerPort=27900
ServerActors=Nephthys.NptServerUplink MasterServerAddress=master.fragaholic.com MasterServerPort=27900
ServerPackages=DXMTL152b1
```

At the end of that list, add the .u file name to the list, without the .u, for example, if we have a mod called `AM.u`, we'll add `ServerPackages=AM`
If the mod has a mutator or actor that should be spawned always in the server, the format is `ServerActors=PackageName.ClassName`, example; `ServerActors=AM.AMutator`


## Port Forwarding
<strong>Note; Some information here may be outdated.</strong>
<p>
	A router blocks a lot of unknown Internet connections, so if you try to host a Deus Ex server, and you have a router, it
	is possible that your server will not show up in the server list. We are going to solve that.
</p>
<p>
	First, go
	<a href="http://www.portforward.com/routers.htm" target="_blank">here</a> and look up your router for the manual on how-to-forward-ports (in the list of games find &quot;Dues Ex&quot;,
	apparently it&#39;s mispelt there). When you fully understand the manual on portforward.com, we may continue.
</p>
<p>
	For a Deus Ex server, you need to forward the following ports: 7790, 7791, 7792, 8777, 27900. You need to open these ports
	in these ways: TCP + UDP. I have no experience in TCP or UDP alone, so if you can&#39;t choose both, try TCP first.
</p>
<p>
	So... if you know how to forward ports, and you forwarded those ports, it should be just fine, and you should be able to
	host. Sometimes it is not only the router which blocks it. After you opened the ports, and it&#39;s still not solved, disable
	the Windows Firewall, just for a test, you can enable this again after testing your server.
</p>
<p>
	<h3>How to disable Windows Firewall (it&#39;s present only in Windows XP):</h3><br /> Start -&gt; Configuration -&gt; Classic
	View (only if you have Windows XP) -&gt; Network Connections -&gt; Right click on your connection -&gt; Properties -&gt;
	Advanced. In that window, you may disable it. Notice: It is possible that your Windows Firewall configuraration is somewhere
	else. Try to
	<a href="http://www.google.com/">Google</a> where it is located in your operational system.
</p>
<p>
	<em>Written by Alex.</em>
</p>


## Nephthys Web support

<p>
	I will explain in detail how to operate Nephthys WebSupport on your server. I will split this tutorial up into 5 core sections.
</p>
<p>
	I. What does it do? <br /> II. Getting started (the basics) <br /> III. Starting WebSupport <br /> IV. Finer details <br
	/> V. Questions/comments.
</p>
<h3>What does it do? </h3>
<p>
	Nephthys is a &quot;native mod for Unreal1 engine based servers which intends IpDrv by efficient attack blocking, banning,
	player logging and other features&quot; (taken from Nephthys Documentation). Simply put, it blocks attacks and other glitches/bugs
	on the server. It also includes other features such as WebSupport which we will be concentrating on today.
</p>
<h3>Getting started</h3>
<p>
	Firstly, make sure you have at least one map or mod. You will require one of these before continuing. Next we need to place
	it in a ZIP Folder. If you&rsquo;re un-aware how to do this; Here&rsquo;s a brief explanation:
</p>
<p>
	Go to My Documents -&gt; File -&gt; New -&gt; ZIP folder.
</p>
<p>
	Depending on what program you have, it may look different or have a different name. The 3 most popular known to me are...
</p>
<p>
	WinRar. This looks like:
</p>
<p>
	&nbsp;
</p>
<div style="text-align: center">
	<img border="2" height="293" src="http://www.mafiawar.biz/imagehost/images/WinRarZip_19544.jpeg" width="353" />
</div>
<p>
	&nbsp;
</p>
<p>
	Default Zip Folder. Looks Like:
</p>
<p>
	&nbsp;
</p>
<div style="text-align: center">
	<img border="2" height="283" src="http://www.mafiawar.biz/imagehost/images/zip-zipped-folder_11445.jpeg" width="389" />
</div>
&nbsp;
<p>
	&nbsp;
</p>
<p>
	WinZip. This looks like:
</p>
<p>
	&nbsp;
</p>
<div style="text-align: center">
	<img alt="WinZip" border="2" height="276" src="http://www.mafiawar.biz/imagehost/images/WinZip_1761.jpeg" width="390" />
</div>
<p>
	&nbsp;
</p>
<p>
	Ok, so trusting you have now created a Zip Folder, give it a suitable name, perhaps the name of your mod/map. Drag either
	your map or mod into it so you now have a copy of it in your Zip folder.
</p>
<p>
	This is the slightly more complicated part. We need to find an upload server which allows GameServer support files.&nbsp;
	I suppose they wouldn't technically know unless someone informed the site staff that&rsquo;s what you were using it for.
	Once you have found an upload server that allows this, upload your ZIP file with your file in it. You should be given a
	URL which you can click to download your map/mod from the internet.
</p>
<p>
	<strong>Note: If you have a server with FTP access E.C.T. Or forums with an attachment mod,&nbsp;then simply use that. If not, heres my alternative:</strong>
</p>
<p>
	Ok, I&rsquo;ve found a free&nbsp;upload server; seems simple enough:
	<a href="http://www.100webspace.com/" title="100webspace.com">http://www.100webspace.com</a> Register, login, click FileManager. You&nbsp;can&nbsp;adjust the other settings later on.&nbsp;Now
	we need to get to your directory (Or 'path'). You can tell if your there by looking at this section:
</p>
<p>
	&nbsp;
</p>
<div style="text-align: center">
	<img border="2" height="193" src="http://www.mafiawar.biz/imagehost/images/Direct_16925.jpeg" width="660" />
</div>
<p>
	&nbsp;
</p>
<p>
	The part in red should display your UserName.100webspace.net/
</p>
<p>
	If it just displays something like Current Path: / Then click on the folder &quot;www.&quot; This Looks like:
</p>
<p>
	&nbsp;
</p>
<div style="text-align: center">
	<img border="2" height="257" src="http://www.mafiawar.biz/imagehost/images/Www_66588.jpeg" width="648" />
</div>
<p>
	&nbsp;
</p>
<p>
	Then click on your website name which should be displayed in the folder, and you should now see your directory bar&nbsp;is
	displaying your full web address.
</p>
<p>
	Don't worry if it already displays your full 'Path' Name, just ignore that last part and continue from here:
</p>
<p>
	Ok, now&nbsp;your there, click&nbsp;'create&nbsp;folder'&nbsp;at the bottom of the&nbsp;page&nbsp;(put in a desciptive name
	like &quot;Server Files&quot; first). Then click on the&nbsp;created&nbsp;folder. Now your inside that folder, click&nbsp;Browse
	and upload your DeusEx file&nbsp;<strong>thats inside&nbsp;the&nbsp;zip Folder!</strong>). In your conformation email,
	you would have been informed of your Web URL. Click this link now and see if your recently created folder with the file
	in is their. If not, youv'e done something wrong and need to go back and do it again!
</p>
<p>
	Now, assuming you can see your uploaded file, right click the filename and click on properties, for help look at this:
</p>
<div style="text-align: center">
	<img border="2" height="494" src="http://www.mafiawar.biz/imagehost/images/Proper_51169.jpeg" width="540" />
</div>
<p>
	Now, when properties is clicked, you should be displayed with a box like this:
</p>
<div style="text-align: center">
	<img border="2" height="450" src="http://www.mafiawar.biz/imagehost/images/Properties_54087.jpeg" width="365" />
</div>
<p>
	&nbsp;
</p>
<p>
	You see Address (URL): then - a website address. Copy that address (highlight it, then Ctr +l C) To make sure it works, paste
	the URL into a web browser, where the address is displayed and you should be given the download.
</p>
<h3>Starting WebSupport </h3>
<a href="/#Starting%20WebSupport" name="Starting WebSupport" title="Starting WebSupport"></a>
<p>
	This part is quite simple in comparison to previous. Firstly, we need to run DeusEx and start a dedicated server (Multiplayer
	&gt; Internet games -&gt; Host a Server -&gt; Change Server Type to Dedicated -&gt; Start server). This can also be done
	with non-dedicated severs, but it&rsquo;s tedious and takes a long time. You should now be on your windows screen as DeusEx
	would have closed itself if you started a dedicated server. In the ToolTray (by the clock in the bottom right hand corner)
	you will see a little Deus Ex sign. This indicated your dedicated server is running.&nbsp;Right click this and you should
	be displayed with 3 options. ServerConsole, Advanced Settings and Close server. Click on ServerConsole. You will notice
	you are displayed with a lot of highly useless information which you needn't pay attention too. Now at the bottom of the
	ServerConsole you will see a &gt;| indicating you can type. Now you can't perform commands such as kick or ban, but you
	can perform specialist Nephthys commands. All Nephthys commands must begin with npt before them. So it would look like
	npt god (but you will be displayed with an error trying to do that command). For WebSupport, we need to type:
</p>
<p>
	npt web support *URL* The URL being the one you got earlier from uploading your mod/map.
</p>
<p>
	So it may look something like...
</p>
<p>
	npt web support http://www.ExampleHost.com/upload/ExampleLink/ServerFile.zip
</p>
<p>
	You should now be displayed with &quot;Processing *URL*&quot; Then &quot;Downloading *URL*&quot; Then it should say something
	like...
</p>
<p>
	Needed: http://www..... E.C.T... Your URL should be here.
</p>
<p>
	Heres a screenshot if you&rsquo;re confused:&nbsp;
</p>
<p>
	&nbsp;
</p>
<div style="text-align: center">
	<img height="263" src="http://www.mafiawar.biz/imagehost/images/ServerConsole_75843.jpeg" style="width: 847px; height: 263px"
		width="847" />
</div>
<p>
	&nbsp; (Sorry, picture is really blurry! But you can make out what it says; Needed *Then a URL*)
</p>
<p>
	And were done! Restart your server and when someone with Nephthys installed needs to download a map/mod you have uploaded
	they will download from&nbsp;the URL&nbsp;creating 0 download-lag for you and increased download speed for them!
</p>
<h3>Finer details
	<a name="Finer details" title="Finer details"></a>
</h3>
<ul>
	<li>Your ZIP Folder must not have a password.</li>
	<li>If you use a different upload server from my suggested one, you must make sure when you click the link to download the
		mod it doesn't respond with stuff like &quot;Please copy this conformation code to start your download&quot;, &quot;Please
		wait 10 seconds for your download to begin&quot; E.C.T.. It must start immediately once you click the link without any
		user interference.</li>
	<li>You may require 7-Zip for this to function correctly. When installing Nephthys, you are promoted to install 7-Zip but you
		may have skipped past it. You may download 7-Zip
		<a href="http://www.7-zip.org/" title="7-Zip Official Site">here</a>.</li>
	<li>You may recieve an error like &quot;Failing to create the target file&quot;. Problem is, that the folder which Nephthys
		downloads the archives to, <strong>NephthysDownloadedArchives</strong>,&nbsp;may not exist; Nephthys&nbsp;is supposed
		to create it automatically&nbsp;but&nbsp;may fail on&nbsp;occasion. Therefore it&nbsp;is &quot;Failing to create the target
		file.&quot; <br /> It's&nbsp;easy to fix. For anyone&nbsp;who has this problem, you will need to go into your main <strong>DeusEx</strong>			folder (Not DeusEx&gt;System), and create a folder named <strong>NephthysDownloadedArchives</strong>. Thats it. It will
		work now!</li>
</ul>
<h3>Questions/comments
	<a name="Questions" title="Questions"></a>
</h3>
<p>
	Please download Nephthys from
	<a href="forum/download.php?id=2907">http://www.dxalpha.com/forum/download.php?id=2907</a>&nbsp;
</p>
<p>
	If you don't have an&nbsp;above standard&nbsp;connection,&nbsp;(I myself don't) and you host a server, download lag IS a
	problem, please help to avert this by downloading Nephthys, so you download from the URL rather than the server. Thanks.
</p>
<p>
	Special Thanks to Zora for help, and of course Gishank for his Server as an example!
</p>
