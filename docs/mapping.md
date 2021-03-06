## Where to start?
`Editor's Note: The links here may be outdated or broken. Let us know in the Discord if you want to help revive this page!`

<p>
	So many articles have been written about Deus Ex mapping in the Internet, so we decided to write only those things which
	were not mentioned anywhere. Therefore, you will not find any newbie guides to mapping in our Knowledge Base &mdash; instead,
	you may check one of the links below.
</p>
### A sneak peak
<p>
	A software development kit for Deus Ex was released in 2000 as a free download. &quot;Software development kit&quot; stands
	for a set of programs that you may use to alter the original game or make add-ons. SDK includes: UnrealEd &mdash; a program
	for designing levels and mods, ConEdit &mdash; a program to create conversations and also some documentation with C++ headers.
	You may
	<a href="http://download.dxalpha.co.uk/DX1/editing/tools/DeusExSDK1112f.exe">download SDK</a> (6.3 MB). If your SDK doesn't start, most likely you don't have ConEdit installed &mdash; it's required.
	Screenshot &mdash; UnrealEd 1 from SDK:
</p>

`Editor's Note: MISSING - Need an image of UED`

<p>
	UnrealEd may seem to be a complicated program, but after reading a small guide you'll realize that it isn't. Many people
	used it: there are over 350+ maps created for the multiplayer and a plenty of single-players mods which present that UnrealEd
	may be used in a variety of styles and aims. Mapping for Deus Ex doesn't require knowledge of any programming language,
	unless you want to add something custom. Mapping doesn't require knowledge of 3D Studio Max or any simular modelling programs,
	because Deus Ex doesn't use static meshes.
</p>
<p>
	Deus Ex editing community could be divided into those, who prefer UnrealEd 1 and those, who prefer UnrealEd 2. Originally
	Deus Ex SDK comes with UnrealEd 1, but later fans of Deus Ex have managed to adapt UnrealEd 2 for Deus Ex, too. Though
	there was a problem of not displaying models in the game, it was later fixed. UnrealEd 2 is the next version of UnrealEd
	1 and it includes many bug fixes and new features, yet it has a new interface which may not seem comfortable for those
	who got used to UnrealEd 1. However, you can't replace SDK with UnrealEd 2 - you should have SDK installed too.
<p>
	There are some problems with both editors.
</p>
<ul>
	<li>The biggest problem is crashing (aka "general protection faults""). Editors crash from time to time and if you
		work wasn't saved, it is most likely gone. Therefore, save your maps and also make backups. </li>
	<li>The second problem is BSP geometry bugs. This thing is so complicated by nature as it is called. To put it simply, sometimes
		when you don't attach brushes properly and don't use grid snapping, there may appear big black holes in geometry or invisible
		walls, which sometimes cause player's death. However, this doubtfully will happen in small maps.</li>
</ul>
<p>
	There are a few things you won't be able to do without dealing with certain problems:
</p>
<ul>
	<li>Day, because Deus Ex engine isn't so good to process day shadows properly.</li>
	<li>Terrain. The only type of terrain you may use in the current engine - BSP based terrain - is quite glitchy
		and laggy, even on good computers. It has to be as simple as possible, and you have to build the rest of geometry accurately.</li>
</ul>
<p>
	There are no alternative programs to Unreal Editors for building maps.
</p>
<p>
	There are not many differences between mapping for the singleplayer and multiplayer, except multiplayer maps don't require
	pathnodes (unless it's supposed to be a TNAG modification map). For multiplayer maps, don't forget to add bots (medical
	and repair ones), goodies such as medkits and biocells, and spawnpoints. You may also use non-standard textures, music
	and scripts for your map.&nbsp;
</p>
### Where to start from
<p>
	Don't forget that Deus Ex is based on Unreal engine, which was also used for Unreal Tournament, Unreal, Rune, Lineage, Pariah
	and dozens of other games. Unreal Editing community is one of the biggest modding communities in the world, and they wrote
	many good tutorials, so you're not limited only to Deus Ex editing sites.
</p>
<ul>
	<li>
		<a href="http://www.offtopicproductions.com/tacks/">Tack's Deus Ex Lab</a> &mdash; one of the best sites about editing.&nbsp;</li>
	<li>
		<a href="http://www.planetdeusex.com/constructor">Constructor</a> &mdash; also, a very good site with tutorials for beginners.</li>
	<li>
		<a href="http://z14.invisionfree.com/DX_Mappers_Society/index.php?showforum=15">Deus Ex Mappers Society</a>
	</li>
	<li>
		<a href="http://unreal.gamedesign.net/">Wolf's Unreal</a> + see also:
		<a href="http://unreal.gamedesign.net/tutorials/basic/basic.html">beginners tutorial</a>,
		<a href="http://unreal.gamedesign.net/keyboard.txt">keyboard shotcuts</a>.
		<a href="http://unreal.gamedesign.net/">
		</a>
	</li>
	<li>
		<a href="http://wiki.beyondunreal.com">Unreal Wiki</a> &mdash; the biggest resource for all Unreal Engine based games.</li>
</ul>
<p>
	If you got a question which wasn't answered anywhere, feel free to ask on our
	Discord (Linked in the sidebar).
</p> 

## Adding mods.
<p>
	<span class="postbody">Contents:  <br />
<br />
I: Information on installing a Mod  <br />
II: Information on gathering Summon Commands.  <br />
III: FAQ ( Frequently Asked Questions )  <br />
IIII: Contact Help  <br />
<br />
<br />
<span style="text-decoration: underline">I: Information on installing a Mod</span> </span>
	<a name="Installing" title="Installing"></a><br />
	<span class="postbody">
<br />
Installing a mod can be simple enough, if you understand it. If you
have not installed a mod before however, it can appear to be abit
complicated. I am going to try to explain how to install Mods
correctly. If I make any mistakes or anyone feels that something else
should be included here, please post below. <br />
<br />
Before we begin, it is essential that you make sure you actually <span style="font-weight: bold">HAVE</span> a mod on your
	computer. But it can't just be anywhere, you must place it in: <br />
	<br /> C: &gt;&gt; DeusEx &gt;&gt; System. By Default this will be where you need to put it unless <br /> you custom configured
	it. <br />
	<br /> However, it requires more than just placing the file in your system folder. Next we need to find something called
	the DeusEx INI. Never heard of it? Not a problem. <br />
	<br /> By default, the file will be located in C: &gt;&gt; DeusEx &gt;&gt; System. The file will be called &quot;DeusEx.&quot;
	If you can't find it, here&rsquo;s a picture to help you out: <br />
	<br />
	<img border="0" src="http://img391.imageshack.us/img391/5461/inipicxr2.png" /> <br />
	<br /> Ok, hopefully you have found it now. Don't go on unless you have found it. <br />
	<br /> Right, so you have now found the INI. This is a general picture of what it should look like when it&rsquo;s been
	opened. If it doesn&rsquo;t look like this then you have the wrong file: <br />
	<br />
	<img border="0" src="http://img315.imageshack.us/img315/2808/insideinics5.png" /> <br />
	<br /> Inside the INI you can do a lot of things apart from alter what Mods you have including; Changing the server name,
	altering the server stats (E.g. what augs you start with, skill level E.C.T.) What your admin password is, controlling
	who is banned from your server and a few other things. However, we are going to be concentrating on adding Mods for the
	time being. <br />
	<br /> You will probably notice titles at the top of each category, such as in the screen shot above, you can see the titles:
	<br />
	<br /> [URL] <br />
	<br /> [FirstRun] <br />
	<br /> And <br />
	<br /> [Engine.Engine] <br />
	<br />
	<br /> Ok, well we want to find the title: <br />
	<br />
	<span style="font-weight: bold">[Editor.EditorEngine]</span> (Located about half way down the page) <br />
	<br /> Scroll down abit from that title and you should notice a section that looks like: <br />
	<br />
	<img border="0" src="http://img430.imageshack.us/img430/4458/inieditsln1.png" /> <br />
	<br /> That&rsquo;s basically the hardest part out of the way, now you just need to add the correct EditPackages in. <br
	/>
	<br /> If you take my example (I am using CaroneElevatorSet) then I would add in the line EditPackages=CaroneElevatorSet
	<br />
	<br /> However, you must make sure you add the line in the correct place, at <span style="font-weight: bold">The Bottom </span>of
	the list. <br />
	<br /> If you are unsure of what to add after EditPackages= for your mod, then firstly, check if there was a ReadMe with
	the mod you got. That may have instructions in that tell you what to call it. If you don't have that, then your best chance
	is either to contact the Mod maker, or simply add the entire mod name after the EditPackages= <br /> But, also make sure
	that you do not add the file extension. For example, a system folder should have the file extension .u, like my CaroneElevatorSet
	mod. But you do not add the file extension on the end of the Editpackages=. <br />
	<br /> EditPackages=CaroneElevatorSet <br /> Right
	</span>
</p>
<p>
	<span class="postbody">
When This Is Wrong: <br />
<br />
EditPackages=CaroneElevatorSet.u   <br />
<span style="font-weight: bold">   WRONG</span><br />
	<br /> Ok, so once you have added the line, Click file,<span style="font-weight: bold"> Save</span>. Or if your technical
	Ctrl + S. <br />
	<br /> And that&rsquo;s it! <br />
	<br />
	<span style="text-decoration: underline">II:  Information on gathering Summon Command Info.</span> </span>
	<a name="summon commands"
		title="summon commands"></a><br />
	<span class="postbody">
<br />
If you wish to add a mod that allows you to summon items such as
special guns E.C.T into your map, then you will have to contact the Mod
maker for information on the summon codes. Or you can do this:<br />
<br />
To find Summon names of items... <br />
<br />
If you have SDK (Deus Ex Level editor)... <br />
Go to it. On the right side, click on classes, then items. From there,
you can find all of the names for each item, weapon and decoration in
the game. If you have installed a mod, the weapons or whatever will
also appear in the list, in another section. </span>
</p>
<p>
	<span class="postbody"><br />
<br />
<span style="text-decoration: underline">III: FAQ ( Frequently Asked Questions )</span> </span>
	<a name="FAQ" title="FAQ"></a><br />
	<span class="postbody">
<br />
Q: What if I'm trying to add something but it requires more than just being added  <br />
into the EditPackages= List. <br />
<br />
A: If you are adding something like a MTL mod, then there may be extra things  <br />
you need to add to your INI to get it to work. But you should have a ReadMe  <br />
with your mod for that anyway. However if you don't, contact the mod maker  <br />
or someone else with info on how to correctly install this mod. <br />
<br />
Q: I can't find any of the DeusEx files in the directory you specified. <br />
<br />
A: If your files are not in the directory I specified earlier, than you have set a  <br />
custom installation folder. When you installed the game, you may have choosen  <br />
a specific place for the DeusEx files to be installed. If you can't remember  <br />
where this is, go to Start&gt;&gt;&gt;Search, and search for the term DeusEx. <br />
<br />
Q: I don't have SDK so I can't look at the summons like, what else can I do? <br />
<br />
A: You may  find this tool useful known as The WOTGReal Exporter. It works with any unreal   <br />
engine game ( DeusEx Included ofcourse ) and can let you see source and   <br />
classnames. You can export with it: meshes, models, textures sounds etc.  <br />
Download it at  <br />
<a class="postlink" href="http://www.wotgreal.com/" target="_blank">www.WOTGreal.com</a>( Thanks to Cozmo for the info on that one. ) <br />
<br />
In addition, alot of mods are protected by Nobodys Mod Protecter. <br />
<br />
Q: I have a mod but i'm not sure where to put it in my DeusEx Folder. <br />
<br />
A: This is a common question, this list should provide the info you need: <br />
<br />
.u ---&gt; System <br />
.dx ---&gt;Maps <br />
.uax ---&gt;Sounds <br />
.umx ---&gt;Music <br />
.utx ---&gt;Textures <br />
<br />
<span style="text-decoration: underline">IIII: Contact Help.</span> </span>
	<a name="Contact" title="Contact"></a><br />
	<span class="postbody">
<br />
If you have any questions or theirs still anything your unsure about, feel free to email me or post on <a href="www.dxalpha.com" target="_blank">www.dxalpha.com</a></span>
</p>
<p>
	(This is an old guide imported by myself, sorry for the somewhat poor layout, also hence the old logo at the bottom).&nbsp;
</p>

