## Launchers
### What is a Launcher?
A launcher is effectively a replacement for the base game executables that fixes the game to run on modern computers. It'll fix things like widescreen problems, CPU issues, etc.
Generally, there are two excepted Launchers for DX. Kenties, and Han's Launch.

### But which one do I choose?
Alot of people, mostly around the Steam forums, suggest using Kenties as the fix-all for every problem. The issue is, that is not entirely correct. Kenties fixes a few things, but it also adds its own problems, nameley;

- It causes menus to lag; Alot of users reported (me included) that the game will have a few second delay to opening menus. The delay was so much of a problem, that during multiplayer games, I would lag out of servers just from opening the menu.
- It moves your config files to an arbitrary location making configging things needlessly more difficult; By default, the game stores configs in /Deus Ex/System, Kenties moves that to a generic /Game/ folder in My Documents.
- It breaks hosting servers, dedicated servers wont work.
- It causes a game breaking crash in singleplayer; During LaGuardia, there is a known bug that makes the game unplayable without cheats, it's reported on Kentie's own website but as of yet, he has not fixed it.
- Compatibility problems with OS's and VB Runtime dependancies; Probably the one that effects the least people, but Kenties relies on VB runtimes, which makes the launcher unusable on other OS's like Linux.

Launch fixes alot of the same things that Kenties does (CPU, widescreen etc), but doesn't add aditional problems and load times, it seamlessly integrates with the game.
Kenties main draw is that it adds a GUI for quickly accessing certain config files properties, *but* alot of what's there can just be accessed from the config files yourself.

With that in mind, either launcher is available to download, [Launch](https://coding.hanfling.de/launch/#binaries), and [Kenties](http://www.kentie.net/article/dxguide/).



## General Gameplay
### Network
<p>
	Ping (or latency), accordingly to the
	<a href="http://en.wikipedia.org/wiki/Ping_%28video_games%29">Wikipedia article</a>, is &quot;the network latency seen between their computer and the game server (or another player)&quot;.
	The lower your ping is, the smoother you gameplay will be. In Deus Ex you can view your ping by using <em>&quot;ping&quot;</em>		or <em>&quot;stat net</em>&quot; commands (first press &quot;T&quot;, erase &quot;Say&quot; and only then type the command).
	Ping depends on:
</p>
<ul>
	<li><strong>Your</strong><br />
		<ul>
			<li><strong>Connection speed.</strong> Your ping will be higher if you have a, e.g. 56k modem, although it will not significantly
				change after you upgrade to something higher than 512 kbps. Don't mix your Internet speed with Local Area (LAN) speed,
				which may be higher. Also, in &quot;Player Settings&quot; it is important to set connection type as close to your connection
				speed as possible. You may want to install a mod called DXMTL, which adds a few new options there. When you download
				or upload something, your speed decreases. </li>
		</ul>
		<ul>
			<li><strong>Connection type.</strong> If you're connected to the Internet through satellite, radio ethernet, WiFi or use
				any other wireless devices, your ping will be higher. The fastest connection type is a fiber-optic broadband and ADSL
				(quality depends on phone line).</li>
		</ul>
		<ul>
			<li><strong>Location.</strong> You may have a 100 mbit fiber-optic broadband, but if you live in e.g. Australia and the server
				you're willing to play is from United Kingdom, you will still have a ping of 300-500 in Deus Ex.</li>
		</ul>
	</li>
	<li><strong>Server's</strong>
		<ul>
			<li><strong>Connection speed.</strong> The higher connection speed is, the better the ping is, when more players play. Also,
				the better the server's connection is, the less influenced the server is for downloaders. &quot;Downloaders&quot; are
				those, who download the files directly from the game server (in contrary to web server, like
				<a href="http://download.dxalpha.com">download.dxalpha.co.uk</a>). </li>
			<li><strong>Connection type.</strong> Same as above, in &quot;your connection type&quot;.</li>
			<li><strong>Location.</strong> Same as above, in &quot;your location&quot;.</li>
			<li><strong>Hardware.</strong> The better hardware specification is, the better the ping is&mdash;this is mostly relevant
				when the server is crowded.</li>
		</ul>
	</li>
</ul>

### Hardware
<p>
	Frame rate (or &quot;frame frequency&quot;; or &quot;FPS&quot;) accordingly the
	<a href="http://en.wikipedia.org/wiki/Frame_per_second">Wikipedia article</a>, is &quot;the measurement of how quickly an imaging device produces unique consecutive images called
	frames. Frame rates of approximately 25 to 30 fps are considered minimally acceptable&quot;. The most common FPS in Deus
	Ex on modern video cards is above 80. The bigger your frame rate per second is, the easier it is to react on things, and
	more comfortable to play (you may feel a headache or sickness after playing on low FPS).&nbsp; FPS depends on:
</p>
<ul>
	<li>
		<a href="http://en.wikipedia.org/wiki/Video_card">Video card</a>
	</li>
	<li>Other computer specs, including
		<a href="http://en.wikipedia.org/wiki/Central_processing_unit">CPU</a>,
		<a href="http://en.wikipedia.org/wiki/RAM">RAM</a>, etc. </li>
	<li>Monitor. Some monitors may not support high FPS rates, therefore fixing it on e.g. 60. </li>
</ul>
### Software
<p>
	Deus Ex requires you to not run any other processes which can take up quite a bit of your computer's resources. Even if Task
	Manager shows that both programs can run without totally using the computer, it is advisable to close any unneeded programs,
	such as instant messengers, or any other programs which you won't need while gaming.
</p>
<p>
	You may significantly improve performance of your Deus Ex by using another renderer. Accordingly to Wikipedia, a renderer
	is &quot;a carefully engineered program, based on a selective mixture of disciplines related to: light physics, visual
	perception, mathematics, and software development&quot;. Most of people run Deus Ex on the normal Direct3D renderer, but
	you may try
	<a href="http://cwdohnal.home.mindspring.com/utglr/">the enhanced OpenGL or Direct3D renderer</a> to increase performance. You may learn how to do that
	<a href="kb/improvements/changing-rendering-devices">here</a>.
</p>

### Commodity
<ul>
<li><strong>Mouse.</strong> You should be able to move your cursor precisely to any place of your screen in a short period
	of time. If you can't, you might want to check:
	<ul>
		<li>Sensivity setting. You may set mouse sensitivity in your operating system (in Windows, in Control Panel -&gt; Mouse)
			and in Deus Ex (Settings -&gt; Controls). Too sensitive mouse makes sniping harder, too insensitive mouse makes close
			range battles harder. </li>
		<li>Wireless/wired. Wireless mice (especially cheap ones) have a problem with response time&mdash;when you move it suddenly,
			the cursor may move to opposite direction.</li>
		<li>Weight. Wireless mice with batteries are heavier and take more effort to move.</li>
		<li>Type. Ball mice are the past, buy something new&mdash;optical mouse, at least. </li>
		<li>Mousepad. It's purely individual. The author prefers his heavy-weight
			<a href="http://hirschelectronics.com/products/products.asp?sectionid=8&amp;cat=21&amp;section=Promotion&amp;category=Promotional%20Items&amp;">&quot;Hirsch&quot; promotional mousepad</a>, brought from United States approximately 8 years ago.</li>
	</ul>
</li>
<li><strong>Monitor.</strong> Some people believe that it's harder to play on widescreens. Also it may be hard to play if you're
	sitting below level of your monitor. </li>
<li><strong>Personal space.</strong> Your legs shouldn't lie on the table, your hand which holds the mouse shouldn't be in
	the air, you shouldn't strain when sitting. But this depends on you. </li>
<li><strong>Controls.</strong> The author uses arrows for movement (&quot;Shift&quot; for jumping and &quot;Ctrl&quot; for
	crouching), although many people prefer WASD keys (W&mdash;forward, S&mdash;back, A&mdash;left, D&mdash;right). You should
	be able to jump and duck whenever you want without doing unnecessary movements. Some Deus Ex'ers prefer to have toggle
	scope action bound to middle button/wheel (scope toggles not when you scroll the wheel, but when you press on it). </li>
<li><strong>Binds.</strong> Getting a medkit and quick reload binds may significantly improve your gameplay.
		
## Tips for DXAG
<p>
	ArxGenus aka DXAG is a Deus Ex multiplayer modification, which involves division into classes and a factor of team work.
</p>
<ol>
	<li>Use ballistic protection as Medic.</li>
	<li>Use run silent when you are cloaked.</li>
	<li>Pretty much always have Energy Shield on as Engineer.</li>
	<li>Same with Targetting and Sniper.</li>
	<li>Look more than just in front of you when you are using vision.</li>
	<li>Medics may seem impossibly nuts, but any good player would exploit their weaknesses (EMP, Explosions, Flamethrowers)</li>
	<li>Always spray your allies when you have a free second.</li>
	<li>Stealth may seem a hard class to work with, but you need to use Cloak, Radar Trans and Lockpicks to their advantage, enemies
		DONT have eyes in the back of their heads, so go around the back.</li>
	<li>Engineers should always check up on turrets they have captured as protocol, the more turrets you own, the more control
		you have, and the more kills you will get.</li>
	<li>Pick your class by your strengths, if you like the Sniper rifle, pick the sniper, if you want to heal and make enemies
		call you a noob and get angry, go Medic &mdash; but on the flip side of that coin, if you play with more than one class,
		you can be flexible, making you a much more valuable team member. </li>
</ol>
<p>
	<em>Written by MrBlack.</em>
</p>

## Ping
<p>
	Ping (or latency), accordingly to the
	<a href="http://en.wikipedia.org/wiki/Ping_%28video_games%29">Wikipedia article</a>, is &quot;the network latency seen between their computer and the game server (or another player)&quot;.
	The lower your ping is, the smoother you gameplay will be. In Deus Ex you can view your ping by using <em>&quot;ping</em>&quot;
	or &quot;<em>stat net</em>&quot; commands (first press &quot;T&quot;, erase &quot;Say&quot; and only then type the command).
	Ping is evaluated in milliseconds (ms)
</p>
<p>
	You shouldn&#39;t be scared by these high values of ping in Deus Ex because due to yet uncovered reasons the ping appears
	to be higher than it is in fact. A ping of 100 in Deus Ex is actually the same as 25 in other games. Also if you happen
	to play on your own dedicated server, you&#39;ll see that your ping doesn&#39;t go below 25-30, although actually it&#39;s
	less than 1 (ms).
</p>
<p>
	In Deus Ex usually a ping of
</p>
<ul>
	<li>20&mdash;100 is considered very low, <br />
	</li>
	<li>101&mdash;150 is low,</li>
	<li>150&mdash;200 is moderate,</li>
	<li>201&mdash;250 is acceptable,</li>
	<li>250&mdash;320 is high,</li>
	<li>320+ &mdash; very high. </li>
</ul>
<p>
	When the ping is high, It&#39;s important to understand that <em>what</em> you see in your Deus Ex is not what <em>really</em>		happens, but the past which has already happened. How old is the &quot;past&quot; depends on ping. E.g., if your ping is
	1000 (that&#39;s very high)
</p>
<div style="text-align: center">
	<img alt="Ping explanation" src="assets/images/img.php?f=kb/factors/ping-explanation-en.gif&w=600" width="600" />
</div>
<br />
<p>
	Therefore, you always should always shoot a bit in front of an enemy.
</p>
	
## Tips for Playing
<p>
	Deus Ex provides you with a variety of ways of playing. You don't have to play like the rest &mdash; instead you may with
	your own style &mdash; it's harder yet interesting, but you shouldn't make these simple mistakes common for all the players.
	Some of them are described below &mdash; read and start winning.
</p>
<p>
	Don't laugh if you already knew something &mdash; the authors of this article meet experienced players who still don't know
	basic things.&nbsp;
</p>
<ul>
	<li>Medkits. For some reason many people ignore them and instead of using one they just surrender. If you desperate, at least
		don't leave a medkit in your inventory for an enemy. </li>
	<li>When playing, don't think about enemies in the first place &mdash; better find a good location which would give you an
		advantage, or collect inventory items such as medkits and LAMs, and while doing these things you may find someone easy
		to kill.</li>
	<li>Don't be afraid to run away! Just survive. Remember, success is never blamed. </li>
	<li>You may switch to other team. Press Esc (to open Main menu) -&gt; Multiplayer -&gt; Player Settings, change right icon
		e.g. of NSF to UNATCO or vice versa. Return back to game &mdash; your play should be blown to pieces.<br />
		<img alt="Switching teams" src="http://www.dxalpha.com/assets/images/kb/basics/teammodel.jpg" width="164" /></li>
	<li>Don't use flamethrower. Flamethrower is a good weapon indeed, but only in singleplayer. Fire doesn't make much damage as
		you think, and could be easily distinguished by using a medkit, medbot or just jumping to water.</li>
	<li>You may use 20mm shells with assault rifle. To do that, you need to find ammo first and then to change ammo (change ammo
		function should be bound to a key &mdash; see Settings -&gt; Keyboard/Mouse window).<br />
		<img alt="Changing ammo" src="http://www.dxalpha.com/assets/images/kb/basics/changingammo.jpg" width="345" /></li>
	<li>Buy skills (press &quot;B&quot;) in gametypes which require them. In ATDM (see &quot;
		<a href="kb/multiplayer/popular-gametypes">Gametypes</a>&quot; if you don't understand what does ATDM mean) people always forget about skills and complain about
		their guns being innacurate or medkits only healing 1/3 of what they should heal.<br />
		<img alt="Skills" src="http://www.dxalpha.com/assets/images/kb/basics/skills.jpg" width="283" /></li>
	<li>In Deus Ex the most used weapons are: sniper rifle, assault shotgun, assault rifle, although in ATDM many people use Dragon
		Tooth sword and throwing knives (usually with Combat Strength augmentation, which almost doubles their damage). In gametypes
		with augmentations there are protective augmentations against plasma rifle (&quot;Energy Shield&quot;) and GEP gun (&quot;Aggressive
		Defence System&quot;).</li>
	<li>Sniper rifle does triple damage when you shoot with scope. In fact, the damage it does without scope is unnoticable.</li>
	<li>Always aim at head even if you feel that the majority of bullets hit walls instead and even if 2 bullets out of 10 hit
		your enemy's head, its better than 10 out of 10 hit body. </li>
	<li>In gametypes with augmentations only newbies call GEP guns &quot;noobish&quot; (because they think it's &quot;cheap&quot;).
		There's an augmentation called &quot;Aggresive Defence System&quot; which could repulse any GEP rocket (not a LAM though!).
		If you manage to kill an enemy with it, it's entirely enemy's fault that he or she is vulnerable to such things. </li>
	<li>These weapons may be lethal with one shot to head:
		<ul>
			<li>Sniper Rifle (with scope).</li>
			<li>Assault shotgun.</li>
			<li>Sawed-off shotgun.</li>
			<li>Dragon Tooth sword.</li>
			<li>Throwing knife (when &quot;Combat Strength&quot; augmentation enabled).</li>
			<li>GEP Gun (indeed!).
			</li>
		</ul>
	</li>
	<li>You may stick grenades to walls &mdash; they will work as proximity mines.<br />
		<img alt="Placing a mine" src="http://www.dxalpha.com/assets/images/kb/basics/mine.jpg" width="300" /><br /> There are
		several things many people forget about this feature:
		<ul>
			<li>You may disable opponent's grenade by clicking on it. You may also use &quot;Radar Transparency&quot; augmentation if
				available, or throw an EMP grenade. </li>
			<li>Using an EMP grenade as a mine together with LAM or gas grenade doesn't make sense, as when EMP explodes it disables
				the rest.</li>
			<li>You don't need to place more than one LAM on one place unless you want your enemy to blow into even smaller pieces (the
				screenshot above was taken by newbies). If an enemy knows about your mine, eventually he or she will certainly manage
				to disable both grenades using any of possible ways. </li>
			<li>You need around 4-5 gas grenade mines to kill an enemy when they explode. You need to place them close to each other
				and if possible, closer to ceiling because then the gas will affect head, not only body. </li>
		</ul>
	</li>
	<li>Never stop running. It's not Counter Strike or Battlefield where you have to wait in an ambush and then suddenly attack
		your opponent. You getting sniped too often? It means that you should crouch and jump, and change direction more frequently.
		Of course you may make your way to a certain place, but trajectory should look like a zigzag. Just look how good players
		play and try to snipe them. Hard, yeah?&nbsp; </li>
	<li>Many elites are annoyed that others call them cheaters. In fact, a cheater is like a poltergeist: everyone heard, but hardly
		ever seen. In 95% cases it's not a cheater, but a good player. There are lots of good players in the community who play
		for a long time &mdash; the game was released long ago and they had time to train.</li>
	<li>In the beginning your scores may be depressing. Don't worry about that &mdash; very soon you'll become a lot better. You
		may try to watch some
		<a href="kb/multiplayer/recording-demos">demorecs</a> or
		<a href="kb/improvements/binding">setup binds</a>. </li>
</ul>
	
## Overviews
<h3>Augmentations overview</h3>
<p>
	<em>The information was taken from official Deus Ex readme file, written by Ion Storm.</em>
</p>
<h2>Slot 3 </h2>
<h3>Energy Shield</h3>
<p>
	<img align="left" alt="Energy Shield" src="assets/images/img.php?f=kb/augs/energy-shield.gif&w=52" width="52" /><em>Energy Drain: Moderate<br />
</em><em>Default button: F3</em><br /> Reduces the effectiveness of attacks from the plasma gun and flamethrower by 80%.
</p>
<p>
	<em>Advantages</em><br /> The energy shield has a fairly low power drain, and a high defensive percentage. This aug is
	particularly useful against a heavy weapons player, since it works on the flamethrower, plasma, and wp rockets. It is also
	helpful if you use it in conjunction with a plasma rifle at short range or point blank targets, since you don&#39;t have
	to worry about hitting yourself as hard with the plasma splash damage.
</p>
<p>
	<em>Disadvantages</em><br /> This aug is only useful against the aforementioned weapons. If no one in the game is using
	any of the heavy weapons, you have a wasted aug slot and might be burning energy uselessly if you use the &#39;allaugs&#39;
	hotkey.
</p>
<p>
	<em>Opposing</em><br /> The best offense against the energy shield is to notice if someone is using it. It&#39;s harder
	to notice the blue shield effect if you are firing energy weapons, so watch closely. If you are firing a flamethrower or
	plasma at them and they don&#39;t seem to care, it&#39;s time to switch weapons. If you are the heavy weapons player, you
	have fewer options, and your best bet is to get away from them and hit them with regular gep rounds.
</p>
<h3>Combat Strength</h3>
<p>
	<em><img align="left" alt="Combat Strength"   src="assets/images/img.php?f=kb/augs/combat-strength.gif&w=52" width="52" /></em><em>Energy Drain: Low<br />
</em><em>Default button: F3</em><br /> You do double damage with melee weapons (e.g., combat knife).
</p>
<p>
	<em>Advantages</em><br /> This aug has not been changed very much from the single player, but does have an added dimension
	in a multiplayer setting. This aug works well for a stealth player, especially when combined with a cloak. Hand to hand
	weapons will do quite a bit of extra damage if you have this aug turned on, and getting the drop on someone with a nanosword
	and combat strength usually means instant death. It should also be noted that this damage bonus also applies to throwing
	knives, which have limited range but a fairly high damage and a very fast rate of fire, making them a viable option for
	a low tech specialist.
</p>
<p>
	<em>Disadvantages</em><br /> No significant disadvantages to this aug, as it has a fairly low power drain.
</p>
<p>
	<em>Opposing</em><br /> This aug only affects weapons using the low-tech skill, and all weapons of this type can be shielded
	against using ballistic protection. A player using this aug will also have to get in fairly close in order to cause damage,
	and listening for their footsteps can make it difficult for them to get in close enough. Using the vision aug can also
	help defend against low-tech weapons, since if they are in close enough to hit you, they are close enough for you to see
	them.
</p>
<h2>Slot 4</h2>
<h3>Radar Transparency </h3>
<p>
	<img align="left" alt="Radar Transparency" src="assets/images/img.php?f=kb/augs/radar-transp.gif&w=52" width="52" /><em>Energy Drain: Very Low<br />
</em><em>Default button: F4</em><br /> Makes you invisible to electronic devices such as cameras, turrets and proximity mines
	(e.g., LAMs).
</p>
<p>
	<em>Advantages</em><br /> While this aug is turned on, you will be completely invisible to turrets and also to any placed
	grenade traps. This aug has a low power drain, and can be left on for a very long time when combined with the recirculator.
	Radar transparency is a must have if you are going to be hacking turrets with multitools or placing a lot of demolitions.
	It makes it incredibly easy to walk past turrets and remove enemy demolitions traps and make them your own.
</p>
<p>
	<em>Disadvantages</em><br /> First off, you cannot take the regeneration aug if you take radar transparency. Secondly,
	while turrets can&#39;t see you, other players still can. This means if you want full stealth, you will have to take cloak
	as well, which has a much higher power drain. Another important note is that while grenade traps won&#39;t go off on you
	directly, you can still be caught in blasts caused by other players.
</p>
<p>
	<em>Opposing</em><br /> The main defense for this aug is paranoia. Check previously safe grenade traps when you pass by
	them again. Keep an eye out at the turret and terminals, since opponents with this aug will probably be spending significant
	amounts of time there.
</p>
<h3>Regeneration</h3>
<p>
	<img align="left" alt="Radar Transparency" src="assets/images/img.php?f=kb/augs/healing.gif&w=52" width="52" /><em>Energy Drain: High <br />
Default button: F4</em><br /> When active, you heal, but at rate insufficient for healing in combat.
</p>
<p>
	<em>Advantages</em><br /> Healing is a good thing. Regen is very useful if you can find a place to hide for 30 seconds
	or so and get yourself combat-ready again. The drain is also fairly low.
</p>
<p>
	<em>Disadvantages</em><br /> Regeneration has been toned down a lot from the single player version. In multiplayer, you
	will only heal up 10 health per tick as opposed to the 40 in single player. The result of this is that you can no longer
	wade into combat with this aug turned on and expect to come out the other side unscathed.
</p>
<p>
	<em>Opposing</em><br /> The simplest way to oppose this is to cause damage faster than they can heal it. With almost all
	weapons, this is not a problem. This aug also makes a distinct sound when it is turned on, and if you are close enough
	you can hear your opponent healing. Half dead opponent hiding and trying to heal? Sounds like a good time for an attack.
</p>
<h2>Slot 5 </h2>
<h3>Environmental Resistance </h3>
<p>
	<img align="left" alt="Environmental Resistance" src="assets/images/img.php?f=kb/augs/er.gif&w=52" width="52" /><em>Energy Drain: Low<br />
</em><em>Default button: F5</em><br /> Reduces damage from poison and gas by 90% and eliminates poison and gas vision reduction
	entirely. Note that turning on this aug after you already have vision problems will not remove the vision effect.
</p>
<p>
	<em>Advantages</em><br /> This is another low cost aug that can be left on a lot of the time. Having it turned on beforehand
	will block the vision wavering effects of poison or gas, and greatly reduce the damage from gas clouds and dart poison.
	This is a great one against players too fond of the crossbow. It works well in conjunction with gas grenades. You can throw
	one into a room and then charge in and start shooting. In this respect, it acts much like a flashbang does in other multiplayer
	games.
</p>
<p>
	<em>Disadvantages</em><br /> Turning this aug on after your vision is already wavering will not remove the effect, though
	it will still block most of the poison damage. Another aug that is only useful in very specific situations.
</p>
<p>
	<em>Opposing</em><br /> Players blithely wandering through gas clouds are easy to spot as using this aug. Once you notice
	that, simply don&#39;t bother with the crossbow or more gas attacks and switch weapons.
</p>
<h3>EMP Shield</h3>
<p>
	<img align="left" alt="EMP Shield" src="assets/images/img.php?f=kb/augs/empshield.gif&w=52" width="52" /><em>Energy Drain: Very Low <br />
</em><em>Default button: F5</em><br /> Reduces the effectiveness of EMP attacks against you by 95%.
</p>
<p>
	<em>Advantages</em><br /> The emp shield has a very low drain and protects very well against emp damage. This is also a
	great aug to use in conjunction with emp grenades or the spy drone. Turn on your shield and fire off emp attacks at close
	range with near impunity. Your enemy is suddenly weaker, while your own energy is barely depleted.
</p>
<p>
	<em>Disadvantages</em><br /> This only blocks emp damage, and thus is of limited usefulness. It should also be noted that
	the shielding effect is lessened the closer you are to the center of the emp attack. Standing at the fringe of an emp blast
	with the shield on means you take minimal drain. Standing at the center of an emp grenade will still drain you for a significant
	amount.
</p>
<p>
	<em>Opposing</em><br /> Someone ignoring or lobbing emp attacks everywhere is easy to spot as using this aug. Stay as far
	away as possible and hit them as hard and fast as you can. If they are throwing emp attacks at you, that means they aren&#39;t
	actually causing damage, which is a perfect time to dish out some damage yourself.
</p>
<h2>Slot 6 </h2>
<h3>Targeting</h3>
<p>
	<img align="left" alt="Targeting" src="assets/images/img.php?f=kb/augs/targeting.gif&w=52" width="52" /><em>Energy Drain: Moderate<br />
</em><em>Default button: F6</em><br /> You do 40% more damage with all weapons. You can also see an enemy&#39;s health.
</p>
<p>
	<em>Advantages</em><br /> Targeting provides many advantages. It is effectively a skill increase of one level in all weapon
	skills. This means that you do more damage and have higher accuracy. The GEP gun will also lock onto opponents faster.
	Even preplaced grenades do more damage if placed while target is on. This is particularly nasty when combined with the
	sniper rifle or other high damage weapons. The other advantage is more subtle, in that you can see how much overall health
	your opponent has left.
</p>
<p>
	<em>Disadvantages</em><br /> The only real disadvantages are the drain, and the fact that you have to really pay attention
	to get the health info, and the health info is an overall number, and does not reflect specific body parts.
</p>
<p>
	<em>Opposing</em><br /> The direct defense against targeting is to use ballistic protection. This will more than make up
	for the targeting damage bonus.
</p>
<h3>Ballistic Protection</h3>
<p align="left">
	<img align="left" alt="Ballistic Protection" src="assets/images/img.php?f=kb/augs/ballistic-protection.gif&w=52" width="52"
	/><em>
Energy Drain: High</em><br />
	<em>Default button: F6</em><br /> Reduces the effectiveness of melee weapons and ballistic weapons (e.g., rifles and pistols)
	by 40%.
</p>
<p>
	<em> Advantages</em><br /> This will block 40% of the damage you receive from most weapons. This is a great aug to use
	right before or as you enter combat, and can keep you alive while you are being sniped until you can find cover. It is
	also very useful to turn on before you cross any large open area, especially when combined with the speed aug.
</p>
<p>
	<em> Disadvantages</em><br /> Significant power drain. This really isn&#39;t an aug you can leave on all the time unless
	you have a recirculator going and stop in at repairbots quite a bit.
</p>
<p>
	<em> Opposing</em><br /> This is one of the toughtest augs to oppose. Attacking someone with this aug going can make combat
	somewhat frustrating. The moment you see that blue shield, it&#39;s time to switch weapons or hit them with an emp attack.
	The crossbow or energy weapons are probably the best to switch to. Anything that will disorient the other player will help
	you take them out faster, and poison, fire, or plasma will usually distract them at least into trying to turn off the ballistic
	and turn on another defensive aug. Making the ballistic person multitask is essential to taking them out. The effectiveness
	of this aug can be reduced by using the targeting aug, which provides a damage bonus.
</p>
<h2>Slot 7</h2>
<h3>Speed Enhancement </h3>
<p>
	<img align="left" alt="Speed" src="assets/images/img.php?f=kb/augs/speed.gif&w=52" width="52" /><em>Energy Drain: Very High<br />
</em><em>Default button: F7</em><br /> Allows you to move twice as fast and jump twice as high.
</p>
<p>
	<em>Advantages</em><br /> Turning on this aug doubles your movement speed and makes very high and long leaps possible.
	This is a great aug for getting into or out of combat quickly, or just crossing a large open space while minimizing risk.
	While you are moving at this speed, you are much harder to hit, and incredibly difficult to get locked onto with the gep
	gun. All in all, this is one of the most powerful and versatile augs.
</p>
<p>
	<em>Disadvantages</em><br /> While it is harder for other enemies to hit you, it is also more difficult to target others
	when moving that fast. Combat can get very frantic very fast, and overcorrecting is a common problem. The drain on this
	is also the highest of all the augs. This is really only useful in short bursts, you simply don&#39;t have enough energy
	to leave it on for long, especially since if you have speed you cannot have the recirculator. Another important note: You
	do not jump as high while carrying the gep gun as you do with other weapons. So don&#39;t expect to be able to hop that
	fence with a gep drawn.
</p>
<p>
	<em>Opposing</em><br /> Trying to defeat someone who has speed, especially if you don&#39;t, can be incredibly difficult.
	Your best bet are weapons with some sort of spread, such as the shotgun, assault rifle, or plasma. Explosives also work
	well, but you have to remember to lead them pretty heavily. Hitting a jackrabbit with an emp blast can also be fairly rewarding,
	as most people who use this aug a lot come to rely on it heavily, and take time to adjust to moving at the regular speed.
	Also remember that even if you are moving, you will still have a slightly easier time aiming than the person blitzing across
	the map.
</p>
<h3>Power Recirculator </h3>
<p>
	<img align="left" alt="Power Recirculator" src="assets/images/img.php?f=kb/augs/recirculator.gif&w=52" width="52" /><em>Energy Drain: None<br />
</em><em>Default button: F7</em><br /> Reduces the energy drain of other augmentations. Note that the Power Recirculator
	is automatically activated when any other augmentations are activated.
</p>
<p>
	<em>Advantages</em><br /> This is probably the simplest aug available. If you turn on any other aug, the recirculator kicks
	in automatically. There is no drain on the recirculator, so it never adds to your power loss. This aug is also incredibly
	useful if you are fond of the &#39;allaugs&#39; hotkey. Combining the power recirculator with a few defensive augs and
	the &#39;allaugs&#39; key can make you very difficult to attack successfully.
</p>
<p>
	<em>Disadvantages</em><br /> Having this aug means you cannot have the speed augmentation. Get used to moving at the regular
	speed, and playing a slightly slower paced game.
</p>
<p>
	<em>Opposing</em><br /> There really isn&#39;t a very good way to oppose someone with this other than emp attacks or using
	the speed aug to your advantage if that is what you took. If your opponent has the recirculator, you are going to have
	to hit them more often, since they can keep their augs going for longer. This means hit hard and fast, since you probably
	won&#39;t win a war of attrition with this player.
</p>
<h2>Slot 8</h2>
<h3>Cloak</h3>
<p>
	<img align="left" alt="Cloak" src="assets/images/img.php?f=kb/augs/cloak.gif&w=52" width="52" /><em>Energy Drain: Moderate<br />
</em><em>Default button: F8</em><br /> Makes you invisible to enemy players. Electronic devices and players with the Vision
	Enhancement augmentation can detect you. Upon drawing a weapon you uncloak and become visible to all. In Team Death Match
	players who are cloaked are still visible to their allies.
</p>
<p>
	<em> Advantages</em><br /> This augmentation is great for avoiding enemy snipers and for avoiding enemies at a distance.
	When active, it is much safer to cross open spaces. When you wish to use the cloak to attack someone, the general strategy
	is to either maneuver around behind them, or wait for them to turn their back on you. When they do so, draw a weapon and
	fire at them. After you do this, it is often a good idea to put your weapon away, cloak again, and move. If you don&#39;t
	do this, then your opponent will most likely return fire. And since your opponent was not cloaked, he or she probably has
	a combat enhancing augmentation. Finally, the cloak prevents the GEP gun from locking onto you, and will break a lock if
	turned on after the lock is acquired.
</p>
<p>
	<em> Disadvantages</em><br /> It has a fairly high power drain, so you have to manage your energy carefully while using
	it. It doesn&#39;t mask your footsteps, so people can often tell when you are nearby. Finally, while it is active, you
	have no weapon out. If someone with the vision augmentation spots you while cloaked, you are at a disadvantage, as your
	opponent is armed and you are not.
</p>
<p>
	<em> Opposing</em><br /> The vision augmentation is the most useful anti-cloak power. At short to medium ranges, it will
	display cloaked enemies. Since these enemies are cloaked, they do not have weapons out, and are at a disadvantage if you
	choose to attack them. If you do not have the vision augmentation, be alert for footsteps. If you hear them, but don&#39;t
	see an opponent, you can try spraying the area with the flamethrower. If you hit someone, he or she will catch on fire
	and be easy to track. A WP rocket fills a similar role at longer ranges, if you suspect a cloaked person to be in a particular
	sniper spot. If you have a weapon equipped, and target a cloaked enemy, you will get white targeting crosshairs. You get
	the same crosshairs if you look at objects in the world, such as crates and doors, but if you get them when not looking
	at an object, then you may very well be targeting a cloaked enemy. Many cloaked players think of themselves as undetectable,
	so a shot at them while they are cloaked will often catch them by surprise.
</p>
<h3>Vision Enhancement </h3>
<p>
	<br />
	<img align="left" alt="Vision Enhancement" src="assets/images/img.php?f=kb/augs/vision.gif&w=52" width="52" /><em>Energy Drain: Moderate<br />
</em><em>Default button: F8</em><br /> Allows you to see enemy players in the dark from any distance. For a short distance
	you can see through walls and see cloaked enemies. Enemy players appear in red.
</p>
<p>
	<em>Advantages</em><br /> This is the best defense against a cloaked player. It is also a vast improvement over your usual
	crosshair iff. Friends will now appear as bright green, and enemies will now glow red. This makes it much easier to spot
	enemies at a distance, even if they are in shadows, and thus is great for spotting troublesome snipers. You can also see
	friends/enemies on the other side of walls at very close range.
</p>
<p>
	<em>Disadvantages</em><br /> There are 4 main problems with this aug. First, you can only see cloaked people at medium/short
	range. This makes the vision aug slightly less advantageous on a larger map. Second, the drain on the vision aug is greater
	than the cloak drain, which means they can stay cloaked longer than you can see them. Third, if you are facing any kind
	of explosion with this aug turned on, you will be temporarily blinded. The severity and duration of the blindness depend
	on the closeness/brightness of the explosion, and whether you were looking straight at it or caught it at an angle. Finally,
	the farther away an enemy player is, the less bright red he will glow.
</p>
<p>
	<em>Opposing</em><br /> The vision aug is directly opposed by the cloak. If you have the cloak, stay as far away from this
	person as possible and try to snipe them. The vision aug player is also very vulnerable to being blinded. Any kind of explosion
	or grenade stands a good chance of temporarily blinding them. The flamethrower and plasma are also bright enough to impede
	the vision aug player somewhat, although they do not cause the same type of blinding effect.
</p>
<h2>Slot 9</h2>
<h3>Spy Drone </h3>
<p>
	<img align="left" alt="Spy Drone" src="assets/images/img.php?f=kb/augs/drone.gif&w=52" width="52" /><em>Energy Drain: Moderate<br />
</em><em>Default button: F9</em><br /> Creates a small, remote-controlled drone. Pressing the firing key (or mouse button)
	while the drone is active delivers powerful EMP damage to any player or electronic device in the vicinity of the drone.
</p>
<p>
	<em>Advantages</em><br /> The spy drone lets you scout an area where you suspect an enemy to be at reduced risk to yourself.
	Once this is activated it moves very quickly across even the large maps, and is difficult for enemies to spot. The emp
	attack has been enhanced for multiplayer, and detonating this anywhere near a person will cause massive bioenergy loss.
	The drone is also useful to send ahead and disable a turret so you can then run past. The spy drone is nearly invulnerable
	while it is in flight. The drone is great to send alone up to the top of that likely sniper nest and flush someone out.
	A favorite close range tactic is to activate the spy drone and the emp shield at the same time, and detonate the drone
	immediately. This is very surprising to an enemy at close range and gives you an immediate energy advantage.
</p>
<p>
	<em>Disadvantages</em><br /> This aug does have a couple of drawbacks. First, while it is active, you cannot move. This
	means you better have a really secure place before you go flying around with the drone. Second, having this aug in a slot
	makes it very difficult to use the &#39;allaugs&#39; hotkey without special planning. Also note: while the spy drone can&#39;t
	be directly damaged by bullets, any type of nearby explosion has a good chance of blowing it up. This means an enemy can
	defend themselves with plasma or explosives, and you really don&#39;t want to get caught in your own emp blast.
</p>
<p>
	<em>Opposing</em><br /> There are a couple of ways to deal with an incoming drone. They make a distinctive humming sound
	so you can generally hear them coming. The simplest way to deal with one is to get a direct or near hit with some type
	of explosive or plasma. You can also emp a spy drone, knocking it out of the air. Also remember that while someone has
	a drone out, they are basically a sitting duck.
</p>
<h3>Aggressive Defense System</h3>
<p align="left">
	<em><img align="left" alt="ADS"   src="assets/images/img.php?f=kb/augs/ads.gif&w=52" width="52" /></em><em>Energy Drain: Low<br />
Default button: F9</em><br /> Enemy rockets detonate before they hit you, doing reduced damage. Large rockets (like the LAW)
	may detonate close enough to cause considerable damage to your character even if you activate the Aggressive Defense. Agressive
	Defense does not detonate thrown LAMs, Gas Grenades, or EMP Grenades.
</p>
<p>
	<em> Advantages</em><br /> This aug has a fairly low drain, and is quite effective at keeping away unwanted rockets. It
	is also useful as an umbrella for teammates, so if you are close together, only one of you needs to have this turned on.
	This is a great aug to turn on while crossing open areas. The offensive use of this aug is when you turn it on while very
	close to someone firing rockets or 20mm at you. The closer you are to them when they fire, the more likely they are to
	damage themselves. The other nice thing is that you can often hear incoming rockets and thus have time to turn this on
	quickly, thus negating or at least reducing the damage you take.
</p>
<p>
	<em> Disadvantages</em><br /> This is not a stealthy aug. Whenever you have this turned on you and nearby players will
	be able to hear a distinctive sound somewhat like a sonar pulse. This makes it much easier to find you if you are trying
	to hide. There have also been some major changes from the way this worked in single player. The only things aggressive
	defense will block in mp are rockets, wp rockets, 20mm, and the law rocket. It will not block placed or thrown grenades,
	darts, knives, or any of the other things it stopped in the singleplayer game. Also, depending on the skill of the opposing
	player and the weapon they use, you may still take some damage from incoming rockets even if you have this turned on. The
	best example is the law, which will still cause significant damage to you if you get caught in the open and try to defend
	yourself with aggressive defense.
</p>
<p>
	<em> Opposing</em><br /> Listen for the distinctive sound of this aug and be very careful before you start firing rockets
	around. When you hear this aug turned on, or you see a rocket detonate with a large blue explosion (much like an EMP explosion),
	it&#39;s time to switch weapons to something else. Since EMP grenades are not blocked by this augmentation, don&#39;t be
	afraid to toss one at your opponent.
</p>
<h2>Slot 10</h2>
<h3>Run Silent </h3>
<p>
	<img align="left" alt="Run Silent" src="assets/images/img.php?f=kb/augs/run-silent.gif&w=52" width="52" /><em>Energy Drain: Low <br />
</em><em>Default button: F10</em><br /> You move completely silently regardless of speed.
</p>
<p>
	<em>Advantages</em><br /> This is a nice low drain aug that is loads of fun for a stealth player. Experienced players will
	be listening for footsteps and it&#39;s great to be able to pop up without them hearing you. Using this with the vision
	aug to see your enemy through a wall and then walking (or running with the speed aug) up behind them is very satisfying.
</p>
<p>
	<em>Disadvantages</em><br /> No disadvantages worthy of note, except you can&#39;t have its opposing aug. This aug can
	cause a bit of overconfidence though. Just because you are being sneaky is no reason to let down your guard.
</p>
<p>
	<em>Opposing</em><br /> Again, paranoia is a great defense. If you can&#39;t hear their footsteps, sometimes you can hear
	them switching weapons or activating/deactivating augs. Look around a lot, watch for movement. The vision aug also helps
	a lot to defend against this: they think they are sneaking up the ladder, you are watching them through the floor and can
	mow them down before they pop their head up.
</p>
<h3>Microfibral Muscle </h3>
<p>
	<img align="left" alt="Microfibral Muscle" src="assets/images/img.php?f=kb/augs/muscle.gif&w=52" width="52" /><em>Energy Drain: Low<br />
</em><em>Default button: F10</em><br /> Allows you to pick up large crates.
</p>
<p>
	<em>Advantages</em><br /> While this aug doesn&#39;t have any direct damage applications, (at least in the premade maps),
	it does offer some interesting map control options. Few people take this aug, so if you are the only player who has it,
	you can move those large crates and no one else will be able to do anything about it. This doesn&#39;t sound terribly useful
	until you realize that you can use those large crates to strategically block off small passages or elevators, and thus
	funnel your opponents wherever you want them. Blocking doorways, air vents, and elevator exits can be extremely amusing.
</p>
<p>
	<em>Disadvantages</em><br /> The only real disadvantage is that the usefulness of this aug is directly tied to which map
	you are on, and if there are any large crates for you to move.
</p>
<p>
	<em>Opposing</em><br /> The simplest way to oppose this aug is to take it yourself. That or simply go way around and realize
	that you are being channeled to where your opponent wants you. The speed aug will often also allow you to jump over crates
	that your opponent has moved.
</p>
<h2>Slot 11</h2>
<h3>Aqualung</h3>
<p>
	<img align="left" alt="Aqualung" src="assets/images/img.php?f=kb/augs/aqualung.gif&w=52" width="52" /><em>Energy Drain: Low<br />
</em><em>Default button: F11</em><br /> Allows you to stay underwater 12 times longer than normal. This also doubles the
	player&#39;s swimming speed.
</p>
<p>
	<em> Advantages</em><br /> Using this aug will not only increase your air supply, but in multiplayer it also increases
	the speed at which you move underwater. If you arm yourself properly, you can get someone to follow you into the water
	and waste them when they try to keep up. This works particularly well if you have taken a weapon that works underwater
	(sword, knives, or crossbow).
</p>
<p>
	<em> Disadvantages</em><br /> No significant disadvantages unless you are on a map with no water, in which case this is
	just cluttering up your hud.
</p>
<p>
	<em> Opposing</em><br /> If you are on a map where water is a significant factor, make sure you have the aqualung as well,
	at least that way you are on an even footing. Also, while you can&#39;t fire most weapons underwater, that doesn&#39;t
	mean you can&#39;t fire into the water at your swimming opponent.
</p>

<h3>Skills overview</h3>

<p>
	<em>The information was taken from official Deus Ex readme file, written by Ion Storm.</em>
</p>
<p>
	<strong>1. Weapons: Heavy (costs 2000)</strong><br /> Upgrading this skill grants players greater accuracy, speed and damage
	with heavy weapons, just as in the single-player game. Affects plasma rifle, GEP gun, flamethrower.
</p>
<p>
	<strong>2. Weapons: Pistol </strong><strong> (costs 2000)</strong><br /> Upgrading this skill grants players greater accuracy
	and damage with pistol weapons, just as in the single-player game. Affects pistol, mini-crossbow.
</p>
<p>
	<strong>3. Weapons: Rifle</strong><strong> (costs 2000)</strong><br /> Upgrading this skill grants players greater accuracy
	and damage with rifle weapons, just as in the single-player game. Affects sniper rifle, assault rifle, sawed-off shotgun,
	assault shotgun.
</p>
<p>
	<strong>4. Weapons: Low-Tech </strong><strong> (costs 2000)</strong><br /> Upgrading this skill grants players greater
	accuracy and damage with low-tech weapons, just as in the single-player game. Affects combat knife, throwing knives, Dragon&#39;s
	Tooth sword, crowbar and etc.
</p>
<p>
	<strong>5. Weapons: Demolition</strong><strong> (costs 1000)</strong><br /> Upgrading this skill grants players greater
	accuracy and higher damage with demolitions (e.g., LAMs, gas grenades, EMP grenades). If your skill level is higher than
	the skill level of the player who placed one of these weapons as a proximity trap, you have more time to disarm it before
	it goes off.
</p>
<p>
	<strong>6. Environmental Training </strong><strong>(costs 1000)</strong><br /> This skill increases the duration and effectiveness
	of the Adaptive Armor, Ballistic Armor and Hazmat Suit. (Note: While this feature is enabled in DXMP, no such suits are
	placed on any of the levels included with the multiplayer version of the game. It is included here in support of users
	who wish to include these items in maps of their own creation).
</p>
<p>
	<strong>7. Lockpicking </strong><strong>(costs 1000)</strong><br /> Upgrading this skill reduces the number of picks required
	as well as the amount of time needed to pick a non-electronic lock.
</p>
<p>
	<strong>8. Multitooling</strong><strong> (costs 1000)</strong><br /> This skill reduces the number of multitools required
	and the amount of time needed to override a keypad lock or bypass a turret (returning it to a neutral state).
</p>
<p>
	<strong>9. Medicine</strong><strong> (costs 1000)</strong><br /> Upgrading the medicine skill makes Medkits more effective
	in restoring lost health points (HP). On the first upgrade level, medkits heal 30 points, on 2d &mdash; 60, on 3d &mdash;
	90.&nbsp;
</p>
<p>
	<strong>0. Computers</strong><strong> (costs 1000)</strong><br /> Upgrading the computer skill reduces the amount of time
	required to break into a computer security system and take control of cameras and turrets. Unlike single-player Deus Ex,
	all players can hack in multiplayer but your speed increases with skill level. However, you can only hack enemy-controlled
	or neutral computers; you can&#39;t hack a computer that has already been hacked by an ally.
</p>


<h3>Weapons overview</h3>
<p>
	<em>The information was taken from official Deus Ex readme file, written by Ion Storm.</em>
</p>
<h2>General</h2>
<p>
	There are 14 different weapons in Deus Ex multiplayer, not counting grenades. Most of them just deal damage, but a few have
	additional extra uses, and all of them have certain situations in which they are more effective than in others. Since you
	can only carry three weapons at a time, and since you often won&#39;t be equally skilled with all weapons, deciding what
	weapons to carry can be a tough choice. Generally you want to carry weapons that have different uses. Carrying two weapons
	that do almost exactly the same thing (such as carrying both shotguns) is a waste of valuable inventory space.
</p>
<h3>Accuracy </h3>
<p>
	Unlike singleplayer, most weapons in multiplayer are perfectly accurate. They shoot exactly where you point. That doesn&#39;t
	mean they always hit, since your opponents may be moving as well, but you can count on your shots to go where you aim.
	This is not true of some multiple shot weapons.
</p>
<h3>Ammo considerations </h3>
<p>
	With the exception of the nano sword and the combat knife, all weapons need ammo. Generally they carry about three clips
	worth. There are three ways to get more ammo for a weapon. The easiest is to use an ammo crate. This will replenish the
	ammo for the weapons you are carrying. Note that this will not replenish throwing knives if you have used all of them,
	since when you use your last throwing knife, you are no longer carrying that weapon. The next is to pick up another copy
	of the same weapon from a weapon rack. This will replenish your ammo with that weapon. Finally, if you search a corpse,
	and that corpse was carrying a weapon that you are carrying, your ammo will be replenished with that weapon. None of these
	methods restore alternate ammo (20 millimeter grenades or WP rockets). You must pick up more of that kind of ammo by finding
	the ammo itself. This ammo is usually stored in locked cabinets.
</p>
<h3>Hit Locations</h3>
<p>
	<img align="left" alt="Body" src="assets/images/img.php?f=kb/basics/body.jpg&w=86" width="86" /> There are three hit locations
	in Deus Ex Multiplayer. Legs, Torso, and Head. All of them have the same number of health points. The torso is the easiest
	to hit, and taking it out kills your opponent. Destroying your opponents legs slows him down greatly and leaves him crouched
	and unable to jump. Destroying your opponents head will kill him, and head shots count for double damage.
</p>
<h3>Reloading </h3>
<p>
	Reloading is generally faster in multiplayer than it was in the singleplayer game. In addition, if you put a weapon away,
	it automatically reloads itself. This is not faster than the automatic reload when you expend your current clip, but it
	means that if you equip a weapon and have ammo left, that ammo will be loaded.
</p>
<h3>Skills</h3>
<p>
	Weapons require different skills to use. In the basic team deathmatch game, all weapons skills are at maximum level. In other
	gametypes, weapon skills may start a lower levels and you may need to spend skill points to buy them up. The effect of
	a higher weapon skill varies from weapon to weapon, but in all cases, a higher skill means more damage.
</p>
<h2>Rifle Weapons</h2>
<p>
	The rifle skill affects the Sniper rifle, the Assault rifle, the Assault shotgun, and the Sawed off shotgun.
</p>
<h3>Sniper Rifle</h3>
<p>
	<em>Advantages<br />
</em>The sniper rifle is one of the most useful long range weapons. Bullets travel instantaneously to point of impact,
	and at master skill level, a head shot taken with a zoomed in sniper rifle will kill. Even torso shots will do a significant
	amount of damage. The vision augmentation is very handy with this weapon, since it helps you find enemies more easily.
</p>
<p>
	<em>Disadvantages<br />
</em>The sniper rifle does significantly less damage if the scope is not in use. It also has a fairly slow rate of fire,
	reloading after every shot. While zoomed in, you can&#39;t see a lot of the world around you, making you a prime target
	for being attacked from behind. Due to its slow reload time and need to be zoomed in, it is almost impossible to use this
	weapon effectively at close range.
</p>
<p>
	<em>Opposing<br />
</em>Ballistic defense protects somewhat against the sniper rifle. It is also very hard for someone to snipe at you if
	you have the speed augmentation on and are running. The cloak augmentation provides near perfect protection; since the
	distances involved in a sniper attack are generally much greater than the distance at which the vision augmentation perceives
	cloaked people, snipers will almost never be able to see cloaked people. If you don&#39;t have these augmentations, try
	dashing from cover to cover. Snipers have to be able to see you to shoot you. Closing very quickly with a sniper is often
	a good way to kill one, since his weapon is next to useless at close range.
</p>
<h3>Assault Rifle</h3>
<p>
	<em>Advantages<br />
</em>The assault rifle is a fairly versatile weapon. It works at both close and medium ranges, and does a fair amount of
	damage. Unlike most multiplayer weapons, it is not perfectly accurate. When unskilled, it is actually fairly inaccurate,
	although because it has burst fire, it tends to wound the opponent some anyway. Standing still or buying higher skill levels
	increases this accuracy, but not to perfect accuracy. This is both an advantage and a disadvantage. It makes it easier
	to hit a target with some of the bullets, but makes it harder to hit with all of them. The alternate ammo, 20 millimeter,
	is one of the most powerful ammo types in the game. The 20 millimeter grenades arc, and can therefore be used to shoot
	over obstacles with indirect fire. They are also highly explosive, and can be used as splash damage weapons.
</p>
<p>
	<em>Disadvantages<br />
</em>This gun is useless at long range when loaded with bullets. It is also not perfectly accurate, and when firing, can
	burn through a clip pretty quickly. The 20 mm ammo is very useful at longer ranges, but the arcing, although useful for
	indirect fire, can take a lot of getting used to. You must also be careful not to hit yourself with the 20 mm with a stray
	shot into a nearby wall.
</p>
<p>
	<em>Opposing</em><br /> Staying far away from your opponent helps, as the gun is useless at long ranges. If you can force
	your opponent to keep moving and firing, he will be less accurate and may run out of ammo quickly. Ballistic protection
	also protects well against this weapon, protecting you against both ammo types. The aggressive defense augmentation will
	stop the 20 mm, and, if you are close enough to your enemy, may even cause him to injure himself.
</p>
<h3>Assault Shotgun</h3>
<p>
	<em>Advantages<br />
</em>The assault shotgun has a high rate of fire and does decent damage. It works at short to moderate ranges. Since it
	fires five pellets, it is fairly easy to hit opponents with at least one of them. If you are right up next to your enemy,
	you can often hit with all five pellets. Unlike the singleplayer game, higher accuracy will not reduce the spread of the
	pellets. This is both an advantage and a disadvantage. It is an advantage in that it makes it easier to hit enemies, but
	a disadvantage in that those hits are less likely to be from all pellets.
</p>
<p>
	<em>Disadvantages<br />
</em>It doesn&#39;t work at longer ranges, and unless you are right next to your enemy, you&#39;re not going to get any
	one shot kills, since the pellets spread out.
</p>
<p>
	<em>Opposing<br />
</em>If you keep moving around, your opponent will find it very difficult to tag you with more than one or two pellets
	a shot.
</p>
<h3>Sawed-off Shotgun</h3>
<p>
	<em>Advantages<br />
</em>The sawed off shotgun does a lot of damage, almost twice as much as the assault shotgun. Like the assault shotgun,
	it works better at closer ranges, and the pellets always spread at least somewhat. Unlike the assault shotgun, it is much
	easier to get one shot kills. A full load of all five pellets, with skill level 3 and the targeting aug will kill someone
	if all pellets hit the torso.
</p>
<p>
	<em>Disadvantages<br />
</em>It has a slow refire rate, and doesn&#39;t hold much ammo in a clip. Although very dangerous at short ranges, this
	isn&#39;t a very dangerous weapon at longer ranges, even at ranges where the assault shotgun might still be effective.
</p>
<p>
	<em>Opposing<br />
</em>Much as with the assault shotgun, try to stay out of close range. If you must be in close range, take advantage of
	the slow refire rate to circle around your opponent with a much faster firing weapon.
</p>
<h2>Pistol Weapons</h2>
<p>
	The pistol skill affects the Pistol, the Stealth pistol, and the Mini-crossbow.
</p>
<h3>Pistol</h3>
<p>
	<em>Advantages<br />
</em>This weapon is a good middle-of-the-road weapon. It does a fair amount of damage, fires moderately quickly, and has
	a decent range. It lends itself well to a number of fast, aimed shots at a target.
</p>
<p>
	<em>Disadvantages<br />
</em>The pistol has no obvious disadvantages, but neither does it have any clear advantages. For any given purpose, there
	is probably another weapon that is more effective because of specialization.
</p>
<p>
	<em>Opposing<br />
</em>Escaping this weapon&#39;s most dangerous middle range is the most effect defense against it - either close quickly
	or get out of range.
</p>
<h3>Stealth Pistol</h3>
<p>
	<em>Advantages<br />
</em>This weapon features a very quick refire rate as its main strength. It is used best on unsuspecting targets, as the
	quiet nature of the weapon makes eliminates one of the main cues that players use to find their attacker. In addition,
	it works well on stationary targets where you can land a number of shots before they have time to react.
</p>
<p>
	<em>Disadvantages<br />
</em>The relatively short range of this weapon makes it useless for most sniping uses, and it&#39;s moderate damage and
	fast-but-not-rapid refire rate makes it both difficult to do snap shots and impossible to hose down an area.
</p>
<p>
	<em>Opposing<br />
</em>Escaping this weapon&#39;s most dangerous middle range is the most effect defense against it - either close quickly
	or get out of range.
</p>
<h3>Mini-Crossbow</h3>
<p>
	<em>Advantages<br />
</em>This weapon does a decent amount of damage, in addition to poisoning your target. Poisoned targets have blurred vision
	and continue to take damage for a short time. In fact, poison from crossbows kills more often than the actual dart impacts.
	This weapon also works underwater.
</p>
<p>
	<em>Disadvantages<br />
</em>The darts have limited range, and, since they are not instant hit weapons, often miss their targets.
</p>
<p>
	<em>Opposing<br />
</em>Stay a moderate distance away from your opponent and he can&#39;t hit you with the darts. If you have environmental
	resistance, the greatest threat (the poison) will be nullified.
</p>
<h2>Heavy Weapons</h2>
<p>
	The heavy weapons skill affects the GEP gun, the Plasma rifle, the Flamethrower, and the LAW.
</p>
<h3>GEP Gun</h3>
<p>
	<em>Advantages<br />
</em>This is a great long-range weapon. It is very useful for suppressing fire, forcing people to stay behind cover. Its
	locking capability is also very useful, and has been enhanced from the singleplayer version. At short to mid ranges, it
	is more useful than the sniper rifle is at similar ranges. It also has an alternate ammo type, the WP rocket. The WP rocket
	does less damage, but has a much larger blast radius, and anyone caught in the blast radius gets set on fire. The GEP comes
	with a sniper scope attached by default.
</p>
<p>
	<em>Disadvantages<br />
</em>There are a number of drawbacks to the GEP. First, more than any other weapon, this weapon relies on higher skill.
	With the GEP out, you cannot jump as high, run as fast, or turn as quickly. Skill reduces this somewhat, but does not completely
	eliminate it. The GEP can be almost completely stopped by the aggressive defense augmentation. It has a slow refire rate,
	and while you&#39;re waiting to reload, enemies can trace the trail of smoke back to figure out where you are. Also, because
	it causes explosions, this is not a good weapon to use at closer ranges if you have the vision aug on.
</p>
<p>
	<em>Locking<br />
</em>It is generally easier to get a lock than it was in the singleplayer game. To get a lock, try to hold your crosshair
	over the target. If it moves off a little bit, your lock will start slipping away, but won&#39;t go away instantly. If
	you generally keep it on the target, you should get a lock. Time to lock varies from 1.5 seconds to 0.25 seconds, depending
	on skill level. After the ammo counter indicates that you are locked, you will hear a tone. While you are getting the tone
	and the ammo counter indicates that you are locked, you are. If you have a lock and move your crosshairs off of the target,
	you have about a second to move them back on before the lock is lost.<br />
	<br /> For the curious, here is how a locked on GEP chases a target:
</p>
<ol>
	<li>
		If the GEP rocket has a line of sight to the center of the target, it aims for that point. If it does not:</li>
	<li>If the GEP rocket has a line of sight to the target&#39;s head, it aims for that point. If it does not:&nbsp;</li>
	<li>The rocket heads for the last place where it had a line of sight to one of those two points on the target. <br />
	</li>
</ol>
<p>
	The GEP rocket slows down a bit for turns, but it still has a significant turn radius, so it doesn&#39;t corner exceptionally
	well. It doesn&#39;t cheat, it only updates targeting information if it has a line of sight to the target.
</p>
<p>
	<em>Opposing<br />
</em>The cloak augmentation prevents locking. It is also very hard for someone to get a lock on you if you are moving around
	erratically. If a GEP round is incoming, moving out of the way when it gets close often causes it to miss, even if locked,
	as it has a minimum turn radius. Aggressive defense almost completely stops GEP rounds, and ballistic protection helps.
	Also, the rocket leaves a large smoke trail that indicates from where it was fired.
</p>
<h3>Plasma Rifle</h3>
<p>
	<em>Advantages<br />
</em>The plasma rifle is an excellent suppressive-fire weapon. Fires three plasma bolts that explode on impact. It has
	a fairly good rate of fire and good range. If you want to force someone to keep his head down, this works very well. It
	is generally best employed by shooting at the ground near your opponent&#39;s feet.
</p>
<p>
	<em>Disadvantages<br />
</em>The energy shield greatly reduces the effectiveness of this weapon. The splash damage can also hurt you if you are
	firing too close to yourself, and it can be dangerous to teammates. The energy shield helps reduce the penalties of self
	inflicted wounds.
</p>
<p>
	<em>Opposing<br />
</em>Jumping helps to avoid splash damage from bolts hitting the floor. The energy shield is very effective at stopping
	this weapon.
</p>
<h3>Flamethrower</h3>
<p>
	<em>Advantages<br />
</em>This weapon has a very high rate of fire, and, if you back someone into a corner, you can kill him with it very quickly.
	It also sets people on fire when it hits them. This doesn&#39;t do a lot of damage, but it makes them easy to spot, even
	if they are cloaked. The flamethrower can function as a sort of alternate vision augmentation. If you hear footsteps nearby
	but don&#39;t see anyone, spraying the area with the flamethrower may set your opponent on fire, making him easy to shoot.
</p>
<p>
	<em>Disadvantages<br />
</em>This weapon has very limited range, and the energy shield is very effective at blocking it.
</p>
<p>
	<em>Opposing<br />
</em>The energy shield is extremely effective at blocking the flamethrower. If you have the energy shield, you don&#39;t
	need to worry too much about the flamethrower. If you get set on fire, jump in the water or use a medkit to put it out.
</p>
<h3>LAW</h3>
<p>
	<em>Advantages<br />
</em>Does massive damage in a wide area. Will even do a significant amount of damage if the other person has aggressive
	defense up.
</p>
<p>
	<em>Disadvantages<br />
</em>Only one shot, but it takes up a whole weapon slot. It also requires lockpicks to get.
</p>
<p>
	<em>Opposing<br />
</em>There isn&#39;t a lot you can do when one is actually coming at you. Aggressive defense alone won&#39;t prevent you
	from taking a lot of damage. Aggressive defense combined with ballistic protection generally works fairly well. Ducking
	behind cover will also reduce the damage. All of these help, but if someone shoots a LAW at the ground near you, expect
	to take at least some damage.
</p>
<h2>Low-tech Weapons</h2>
<p>
	The Low-tech skill affects the Nano sword, the Combat knife, and the Throwing knives. All of the low-tech weapons are short
	range, all of them work underwater, and combat strength helps with all of them. The speed, cloak, and combat strength augmentations
	are all helpful when trying to use these.
</p>
<h3>Nano Sword</h3>
<p>
	<em>Advantages<br />
</em>The nano sword does a lot of damage and has a fairly high rate of fire. In addition, unlike the singleplayer game,
	it has a fairly high swing arc. The closer your opponents are to you and to the center of your screen, the more damage
	the sword does, but you can still hit people at the ends of the arc. This weapon also works under water. Combat strength
	greatly enhances the damage it does.
</p>
<p>
	<em>Disadvantages<br />
</em>The weapon is fairly short range. It is also very obvious when someone is using it. Equipping it makes a very distinct
	sound, and it emits a blue glow around you
</p>
<p>
	<em>Opposing<br />
</em>The best defense is to stay out of reach. This isn&#39;t very hard. If you have the speed aug on, your opponent will
	find it very difficult to hit you with the sword, even if he has the speed aug himself. If you hear the sound of the sword
	being drawn, move out of the way. It might be someone uncloaking behind you with the sword. Often someone attacking you
	with the sword is relying on the speed augmentation. Take that out and it is pretty easy to defeat him.
</p>
<h3>Combat Knife</h3>
<p>
	<em>Advantages<br />
</em>A decent amount of damage and a high rate of fire. Works underwater. Combat strength greatly enhances the damage it
	does. Unlike the nano sword, equipping it doesn&#39;t advertise your presence.
</p>
<p>
	<em>Disadvantages<br />
</em>Unlike the nano sword, it does not have an enhanced swing arc. Your opponent needs to be right in front of you at
	fairly short range.
</p>
<p>
	<em>Opposing<br />
</em>Stay out of range. If your opponent is relying on the speed aug, EMP him to eliminate that advantage.
</p>
<h3>Throwing Knife</h3>
<p>
	<em>Advantages<br />
</em>The throwing knife does a lot of damage and has a high rate of fire. It works at greater ranges than the other lowtech
	weapons. It works underwater, and combat strength makes it do more damage.
</p>
<p>
	<em>Disadvantages<br />
</em>Limited ammo. Unlike the other lowtech weapons, you can run out of ammo with this weapon. Once you run out of ammo,
	the weapon is gone, and using an ammo crate won&#39;t restore your ammo. It is also not instant-hit, and therefore it can
	be difficult to hit with it.
</p>
<p>
	<em>Opposing<br />
</em>Back up and dodge around. Your opponent will most likely run out of ammo quickly.
</p>
<h2>Grenades</h2>
<p>
	Grenades are affected by the demolitions skill. They include the EMP grenade, the Gas grenade, and the LAM.
</p>
<h3>General</h3>
<p>
	<em>Advantages<br />
</em>Grenades are fairly handy weapons. They don&#39;t take up slots that would be used by something else; each grenade
	has its own belt slot. They can be placed on walls as defense systems, or thrown at enemies as an attack. Each grenade
	has a very different effect on an enemy, making the demolitions skill fairly versatile. The screen of the player who planted
	or threw a grenade will flash an appropriate color (blue for EMP, green for Gas, white for LAM) when the grenade detonates.
	This is useful for knowing when grenades you have planted are being detonated.
</p>
<p>
	<em>Disadvantages<br />
</em>You can only carry three grenades of each type at any time, and many of the grenades are locked up. Also, thrown grenades
	will blow up if an explosion goes off nearby. The two most common ways this can happen are throwing a second LAM too soon
	after throwing the first, or by throwing a grenade when someone is shooting a plasma rifle at you.
</p>
<p>
	<em>Opposing<br />
</em>Placed grenades can be neutralized in several ways. Radar transparency allows you to walk past them without setting
	them off. You can then pick them up off of the wall and place them again. This leaves them in essentially the same place,
	but on your side. Many enemies will assume the grenade is still friendly. If you have a higher demolitions skill than the
	person placing the grenade, you have some time to locate and disarm it after you hear the beeping sound. EMP explosions
	will disable nearby grenades, and regular explosions will set them off. Since explosions penetrate a short distance through
	walls, one tactic when assaulting an enemy base is to blow up a rocket on the outside of the entrance, thereby exploding
	any grenades inside the entrance. The explosions from the grenades may injure the defending team. The best way to deal
	with thrown grenades is to dodge them. Thrown grenades make distinctive noises when they bounce along the ground. If you
	move quickly you can avoid most of the blast.
</p>
<p>
	<em>Placing</em><br /> When placing a grenade, remember that the targeting augmentation enhances your skill, and thus the
	damage done. It will make the grenade more effective when it actually goes off. Try not to place EMP grenades near other
	grenades, or else the explosion from your EMP grenade may disable the other grenades. The best place to place a grenade
	is in a location where, when your opponent comes into range to set them off, he can&#39;t quickly get away. One prime example
	is on the inside of a door. When he opens the door, he will often sit there for a second waiting for the door to open.
	During that time, the grenade can go off and kill him. On the other hand, if you place grenades where people expect them,
	they can blow them up or disable them and use them against you.
</p>
<h3>EMP Grenade</h3>
<p>
	<em>Advantages<br />
</em>EMP grenades are one of the only two ways in the game to do EMP damage. If you hit an enemy with one of these, he
	will most likely run out of energy and be at a significant disadvantage.
</p>
<p>
	<em>Disadvantages<br />
</em>If placed too near other grenades, an opponent may set one of these off before your other placed grenades, thus disabling
	your other grenades. Also, if your opponent was already out of bio energy, then this attack will do nothing.
</p>
<p>
	<em>Opposing<br />
</em>The EMP shield provides a lot of protection against these. When you do have the EMP shield, it often allows you to
	catch your opponents at a disadvantage. They expect you to have run out of bioenergy, but the shield has prevented you
	from running out. Carrying biocells around also helps lessen the negative effects.
</p>
<h3>Gas Grenade</h3>
<p>
	<em>Advantages<br />
</em>Gas grenades are a fairly safe way to slow down your opponents. They are unlikely to injure you or your opponent overmuch,
	but the vision blurring effect can help you run away. When combined with environmental resistance, they can be used much
	like flashbangs. You can toss one into a room and then charge in, immune to the gas. These grenades are also handy to place
	near friendly turrets. An enemy that sets off the grenade will be stumbling around while the turret fires.
</p>
<p>
	<em>Disadvantages<br />
</em>They don&#39;t do a lot of damage, and the gas clouds move unpredictably. Often you will hit yourself at least a little
	with these if you are not very careful.
</p>
<p>
	<em>Opposing</em><br /> Environmental resistance works well if turned on before you get hit by any poison gas. The gas
	also isn&#39;t that dangerous, if your opponent is badly wounded and you are not, it can be worth pursuing him through
	the gas to finish him off.
</p>
<h3>LAM</h3>
<p>
	<em>Advantages<br />
</em>Very dangerous as a hurled explosive. Unlike the other two grenades, the LAM deals a lot of direct damage. If a LAM
	explosion goes off near an enemy, either from a preplaced LAM or a well thrown one, it will most likely kill your opponent.
</p>
<p>
	<em>Disadvantages<br />
</em>They can be fairly dangerous as well. If you throw one and it blows up in midair (due to a nearby explosion) before
	it gets very far away from you, you are likely to kill yourself.
</p>
<p>
	<em>Opposing<br />
</em>Ballistic protection helps protect against the damage, dodging is best.
</p>


<h3>Weapons damage guide</h3>
<ul>
	<li>
		<a href="playing/weapon-damage-guide#WeaponAssaultGun">Assault Rifle</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponAssaultShotgun">Assault Shotgun</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponBaton">Baton</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponCombatKnife">Combat Knife</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponCrowbar">Crowbar</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponNanoSword">Dragon's Tooth Sword</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponEMPGrenade">Electromagnetic Pulse (EMP) Grenade</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponFlamethrower">Flamethrower</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponGasGrenade">Gas Grenade</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponGEPGun">Guided Explosive Projectile (GEP) Gun</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponLAW">Light Anti-Tank Weapon (LAW)</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponLAM">Lightweight Attack Munitions (LAM)</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponMiniCrossbow">Mini-Crossbow</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponPepperGun">Pepper Gun</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponPistol">Pistol</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponPlasmaRifle">Plasma Rifle</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponHideAGun">PS20</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponProd">Riot Prod</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponSawedOffShotgun">Sawed-off Shotgun</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponRifle">Sniper Rifle</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponStealthPistol">Stealth Pistol</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponSword">Sword</a>
	</li>
	<li>
		<a href="playing/weapon-damage-guide#WeaponShuriken">Throwing Knives</a>
	</li>
</ul>
<a name="WeaponAssaultGun"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Assault Rifle (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (1 hit)</td>
			<td>9</td>
			<td>13</td>
			<td>15</td>
			<td>18</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (1 hit)</td>
			<td>11</td>
			<td>15</td>
			<td>17</td>
			<td>20</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (1 hit)</td>
			<td>18</td>
			<td>26</td>
			<td>30</td>
			<td>36</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (1 hit)</td>
			<td>22</td>
			<td>30</td>
			<td>34</td>
			<td>40</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (5 hits)</td>
			<td>45</td>
			<td>65</td>
			<td>75</td>
			<td>90</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (5 hits)</td>
			<td>55</td>
			<td>75</td>
			<td>85</td>
			<td>100</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (5 hits)</td>
			<td>90</td>
			<td>130</td>
			<td>150</td>
			<td>180</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (5 hits)</td>
			<td>110</td>
			<td>150</td>
			<td>170</td>
			<td>200</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Assault Rifle vs. Ballistic Protection (60% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (1 hit)</td>
			<td>5</td>
			<td>7</td>
			<td>9</td>
			<td>10</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (1 hit)</td>
			<td>6</td>
			<td>9</td>
			<td>10</td>
			<td>12</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (1 hit)</td>
			<td>10</td>
			<td>14</td>
			<td>18</td>
			<td>20</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (1 hit)</td>
			<td>12</td>
			<td>18</td>
			<td>20</td>
			<td>24</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (5 hits)</td>
			<td>25</td>
			<td>35</td>
			<td>45</td>
			<td>50</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (5 hits)</td>
			<td>30</td>
			<td>45</td>
			<td>50</td>
			<td>60</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (5 hits)</td>
			<td>50</td>
			<td>70</td>
			<td>90</td>
			<td>100</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (5 hits)</td>
			<td>60</td>
			<td>90</td>
			<td>100</td>
			<td>120</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<a name="WeaponAssaultShotgun"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Assault Shotgun (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (1 hit)</td>
			<td>5</td>
			<td>7</td>
			<td>8</td>
			<td>10</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (1 hit)</td>
			<td>6</td>
			<td>8</td>
			<td>9</td>
			<td>11</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (1 hit)</td>
			<td>10</td>
			<td>14</td>
			<td>16</td>
			<td>20</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (1 hit)</td>
			<td>12</td>
			<td>16</td>
			<td>18</td>
			<td>22</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (5 hits)</td>
			<td>25</td>
			<td>35</td>
			<td>40</td>
			<td>50</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (5 hits)</td>
			<td>30</td>
			<td>40</td>
			<td>45</td>
			<td>55</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (5 hits)</td>
			<td>50</td>
			<td>70</td>
			<td>80</td>
			<td>100</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (5 hits)</td>
			<td>60</td>
			<td>80</td>
			<td>90</td>
			<td>110</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Assault Shotgun vs. Ballistic Protection (60% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (1 hit)</td>
			<td>3</td>
			<td>4</td>
			<td>4</td>
			<td>6</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (1 hit)</td>
			<td>3</td>
			<td>4</td>
			<td>5</td>
			<td>6</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (1 hit)</td>
			<td>6</td>
			<td>8</td>
			<td>8</td>
			<td>12</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (1 hit)</td>
			<td>6</td>
			<td>8</td>
			<td>10</td>
			<td>12</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (5 hits)</td>
			<td>15</td>
			<td>20</td>
			<td>20</td>
			<td>30</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (5 hits)</td>
			<td>15</td>
			<td>20</td>
			<td>25</td>
			<td>30</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (5 hits)</td>
			<td>30</td>
			<td>40</td>
			<td>40</td>
			<td>60</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (5 hits)</td>
			<td>30</td>
			<td>40</td>
			<td>50</td>
			<td>60</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponBaton"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Baton (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>7</td>
			<td>10</td>
			<td>12</td>
			<td>14</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>8</td>
			<td>12</td>
			<td>13</td>
			<td>15</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso)</td>
			<td>14</td>
			<td>17</td>
			<td>19</td>
			<td>21</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso)</td>
			<td>15</td>
			<td>19</td>
			<td>20</td>
			<td>22</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>14</td>
			<td>20</td>
			<td>24</td>
			<td>28</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>16</td>
			<td>24</td>
			<td>26</td>
			<td>30</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head)</td>
			<td>28</td>
			<td>34</td>
			<td>38</td>
			<td>42</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head)</td>
			<td>30</td>
			<td>38</td>
			<td>40</td>
			<td>44</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Baton vs. Ballistic Protection (60% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>4</td>
			<td>6</td>
			<td>7</td>
			<td>8</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>4</td>
			<td>7</td>
			<td>7</td>
			<td>9</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso)</td>
			<td>8</td>
			<td>10</td>
			<td>11</td>
			<td>12</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso)</td>
			<td>9</td>
			<td>11</td>
			<td>12</td>
			<td>13</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>8</td>
			<td>12</td>
			<td>14</td>
			<td>16</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>8</td>
			<td>14</td>
			<td>14</td>
			<td>18</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head)</td>
			<td>16</td>
			<td>20</td>
			<td>22</td>
			<td>24</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head)</td>
			<td>18</td>
			<td>22</td>
			<td>24</td>
			<td>26</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponCombatKnife"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Combat Knife (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>20</td>
			<td>30</td>
			<td>34</td>
			<td>40</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>25</td>
			<td>35</td>
			<td>39</td>
			<td>45</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso)</td>
			<td>40</td>
			<td>50</td>
			<td>54</td>
			<td>60</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso)</td>
			<td>45</td>
			<td>55</td>
			<td>59</td>
			<td>65</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>40</td>
			<td>60</td>
			<td>68</td>
			<td>80</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>50</td>
			<td>70</td>
			<td>78</td>
			<td>90</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head)</td>
			<td>80</td>
			<td>100</td>
			<td>108</td>
			<td>120</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head)</td>
			<td>90</td>
			<td>110</td>
			<td>118</td>
			<td>130</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Combat Knife vs. Ballistic Protection (60% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>12</td>
			<td>18</td>
			<td>20</td>
			<td>24</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>15</td>
			<td>21</td>
			<td>23</td>
			<td>27</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso)</td>
			<td>24</td>
			<td>30</td>
			<td>32</td>
			<td>36</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso)</td>
			<td>27</td>
			<td>33</td>
			<td>35</td>
			<td>39</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>24</td>
			<td>36</td>
			<td>40</td>
			<td>48</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>30</td>
			<td>42</td>
			<td>46</td>
			<td>54</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head)</td>
			<td>48</td>
			<td>60</td>
			<td>64</td>
			<td>72</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head)</td>
			<td>54</td>
			<td>66</td>
			<td>70</td>
			<td>78</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponCrowbar"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Crowbar (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>12</td>
			<td>18</td>
			<td>20</td>
			<td>24</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>15</td>
			<td>21</td>
			<td>23</td>
			<td>27</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso)</td>
			<td>24</td>
			<td>30</td>
			<td>32</td>
			<td>36</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso)</td>
			<td>27</td>
			<td>33</td>
			<td>35</td>
			<td>39</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>24</td>
			<td>36</td>
			<td>40</td>
			<td>48</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>30</td>
			<td>42</td>
			<td>46</td>
			<td>54</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head)</td>
			<td>48</td>
			<td>60</td>
			<td>64</td>
			<td>72</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head)</td>
			<td>54</td>
			<td>66</td>
			<td>70</td>
			<td>78</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Crowbar vs. Ballistic Protection (60% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>7</td>
			<td>10</td>
			<td>12</td>
			<td>14</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>9</td>
			<td>12</td>
			<td>13</td>
			<td>16</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso)</td>
			<td>14</td>
			<td>18</td>
			<td>19</td>
			<td>21</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso)</td>
			<td>16</td>
			<td>19</td>
			<td>21</td>
			<td>23</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>14</td>
			<td>20</td>
			<td>24</td>
			<td>28</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>18</td>
			<td>24</td>
			<td>26</td>
			<td>32</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head)</td>
			<td>28</td>
			<td>36</td>
			<td>38</td>
			<td>42</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head)</td>
			<td>32</td>
			<td>38</td>
			<td>42</td>
			<td>46</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponNanoSword"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Dragon's Tooth Sword (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (1 hit)</td>
			<td>10</td>
			<td>15</td>
			<td>17</td>
			<td>20</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (1 hit)</td>
			<td>12</td>
			<td>17</td>
			<td>19</td>
			<td>22</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso) (1 hit)</td>
			<td>20</td>
			<td>25</td>
			<td>27</td>
			<td>30</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso) (1 hit)</td>
			<td>22</td>
			<td>27</td>
			<td>29</td>
			<td>32</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (1 hit)</td>
			<td>20</td>
			<td>30</td>
			<td>34</td>
			<td>40</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (1 hit)</td>
			<td>24</td>
			<td>34</td>
			<td>38</td>
			<td>44</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head) (1 hit)</td>
			<td>40</td>
			<td>50</td>
			<td>54</td>
			<td>60</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head) (1 hit)</td>
			<td>44</td>
			<td>54</td>
			<td>58</td>
			<td>64</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (5 hits)</td>
			<td>50</td>
			<td>75</td>
			<td>85</td>
			<td>100</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (5 hits)</td>
			<td>60</td>
			<td>85</td>
			<td>95</td>
			<td>110</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso) (5 hits)</td>
			<td>100</td>
			<td>125</td>
			<td>135</td>
			<td>150</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso) (5 hits)</td>
			<td>110</td>
			<td>135</td>
			<td>145</td>
			<td>160</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (5 hits)</td>
			<td>100</td>
			<td>150</td>
			<td>170</td>
			<td>200</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (5 hits)</td>
			<td>120</td>
			<td>170</td>
			<td>190</td>
			<td>220</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head) (5 hits)</td>
			<td>200</td>
			<td>250</td>
			<td>270</td>
			<td>300</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head) (5 hits)</td>
			<td>220</td>
			<td>270</td>
			<td>290</td>
			<td>320</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Dragon's Tooth Sword vs. Ballistic Protection (60% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (1 hit)</td>
			<td>6</td>
			<td>9</td>
			<td>10</td>
			<td>12</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (1 hit)</td>
			<td>7</td>
			<td>10</td>
			<td>11</td>
			<td>13</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso) (1 hit)</td>
			<td>12</td>
			<td>15</td>
			<td>16</td>
			<td>18</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso) (1 hit)</td>
			<td>13</td>
			<td>16</td>
			<td>17</td>
			<td>19</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (1 hit)</td>
			<td>12</td>
			<td>18</td>
			<td>20</td>
			<td>24</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (1 hit)</td>
			<td>14</td>
			<td>20</td>
			<td>22</td>
			<td>26</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head) (1 hit)</td>
			<td>24</td>
			<td>30</td>
			<td>32</td>
			<td>36</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head) (1 hit)</td>
			<td>26</td>
			<td>32</td>
			<td>34</td>
			<td>38</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (5 hits)</td>
			<td>30</td>
			<td>45</td>
			<td>50</td>
			<td>60</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (5 hits)</td>
			<td>35</td>
			<td>50</td>
			<td>55</td>
			<td>65</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso) (5 hits)</td>
			<td>60</td>
			<td>75</td>
			<td>80</td>
			<td>90</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso) (5 hits)</td>
			<td>65</td>
			<td>80</td>
			<td>85</td>
			<td>95</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (5 hits)</td>
			<td>60</td>
			<td>90</td>
			<td>100</td>
			<td>120</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (5 hits)</td>
			<td>70</td>
			<td>100</td>
			<td>110</td>
			<td>130</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head) (5 hits)</td>
			<td>120</td>
			<td>150</td>
			<td>160</td>
			<td>180</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head) (5 hits)</td>
			<td>130</td>
			<td>160</td>
			<td>170</td>
			<td>190</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponEMPGrenade"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Electromagnetic Pulse (EMP) Grenade (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage</td>
			<td>200</td>
			<td>240</td>
			<td>320</td>
			<td>400</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting</td>
			<td>250</td>
			<td>290</td>
			<td>370</td>
			<td>450</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength</td>
			<td>400</td>
			<td>440</td>
			<td>520</td>
			<td>600</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat</td>
			<td>450</td>
			<td>490</td>
			<td>570</td>
			<td>650</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Electromagnetic Pulse (EMP) Grenade vs. EMP Shield (5% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage</td>
			<td>10</td>
			<td>12</td>
			<td>16</td>
			<td>20</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting</td>
			<td>12</td>
			<td>14</td>
			<td>18</td>
			<td>22</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength</td>
			<td>20</td>
			<td>22</td>
			<td>26</td>
			<td>30</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat</td>
			<td>22</td>
			<td>24</td>
			<td>28</td>
			<td>32</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponFlamethrower"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Flamethrower (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (1 hit)</td>
			<td>5</td>
			<td>7</td>
			<td>8</td>
			<td>10</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (1 hit)</td>
			<td>6</td>
			<td>8</td>
			<td>9</td>
			<td>11</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (1 hit)</td>
			<td>10</td>
			<td>14</td>
			<td>16</td>
			<td>20</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (1 hit)</td>
			<td>12</td>
			<td>16</td>
			<td>18</td>
			<td>22</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (7 hits)</td>
			<td>35</td>
			<td>49</td>
			<td>56</td>
			<td>70</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (7 hits)</td>
			<td>42</td>
			<td>56</td>
			<td>63</td>
			<td>77</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (7 hits)</td>
			<td>70</td>
			<td>98</td>
			<td>112</td>
			<td>140</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (7 hits)</td>
			<td>84</td>
			<td>112</td>
			<td>126</td>
			<td>154</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Flamethrower vs. Energy Shield (50% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (1 hit)</td>
			<td>2</td>
			<td>3</td>
			<td>4</td>
			<td>5</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (1 hit)</td>
			<td>3</td>
			<td>4</td>
			<td>4</td>
			<td>5</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (1 hit)</td>
			<td>4</td>
			<td>6</td>
			<td>8</td>
			<td>10</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (1 hit)</td>
			<td>6</td>
			<td>8</td>
			<td>8</td>
			<td>10</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (7 hits)</td>
			<td>14</td>
			<td>21</td>
			<td>28</td>
			<td>35</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (7 hits)</td>
			<td>21</td>
			<td>28</td>
			<td>28</td>
			<td>35</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (7 hits)</td>
			<td>28</td>
			<td>42</td>
			<td>56</td>
			<td>70</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (7 hits)</td>
			<td>42</td>
			<td>56</td>
			<td>56</td>
			<td>70</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponGasGrenade"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Gas Grenade (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>20</td>
			<td>24</td>
			<td>32</td>
			<td>40</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>25</td>
			<td>29</td>
			<td>37</td>
			<td>45</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso)</td>
			<td>40</td>
			<td>44</td>
			<td>52</td>
			<td>60</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso)</td>
			<td>45</td>
			<td>49</td>
			<td>57</td>
			<td>65</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>40</td>
			<td>48</td>
			<td>64</td>
			<td>80</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>50</td>
			<td>58</td>
			<td>74</td>
			<td>90</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head)</td>
			<td>80</td>
			<td>88</td>
			<td>104</td>
			<td>120</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head)</td>
			<td>90</td>
			<td>98</td>
			<td>114</td>
			<td>130</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Gas Grenade vs. Environmental Resistance (10% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>2</td>
			<td>2</td>
			<td>3</td>
			<td>4</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>2</td>
			<td>2</td>
			<td>3</td>
			<td>4</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso)</td>
			<td>4</td>
			<td>4</td>
			<td>5</td>
			<td>6</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso)</td>
			<td>4</td>
			<td>4</td>
			<td>5</td>
			<td>6</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>4</td>
			<td>4</td>
			<td>6</td>
			<td>8</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>4</td>
			<td>4</td>
			<td>6</td>
			<td>8</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head)</td>
			<td>8</td>
			<td>8</td>
			<td>10</td>
			<td>12</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head)</td>
			<td>8</td>
			<td>8</td>
			<td>10</td>
			<td>12</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponGEPGun"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Guided Explosive Projectile (GEP) Gun (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>300</td>
			<td>450</td>
			<td>522</td>
			<td>600</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>375</td>
			<td>525</td>
			<td>597</td>
			<td>675</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>600</td>
			<td>900</td>
			<td>1044</td>
			<td>1200</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>750</td>
			<td>1050</td>
			<td>1194</td>
			<td>1350</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Guided Explosive Projectile (GEP) Gun vs. Energy Shield (50% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>150</td>
			<td>225</td>
			<td>261</td>
			<td>300</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>187</td>
			<td>262</td>
			<td>298</td>
			<td>337</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>300</td>
			<td>450</td>
			<td>522</td>
			<td>600</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>374</td>
			<td>524</td>
			<td>596</td>
			<td>674</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponLAW"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Light Anti-Tank Weapon (LAW) (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>1000</td>
			<td>1500</td>
			<td>1740</td>
			<td>2000</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>1250</td>
			<td>1750</td>
			<td>1990</td>
			<td>2250</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>2000</td>
			<td>3000</td>
			<td>3480</td>
			<td>4000</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>2500</td>
			<td>3500</td>
			<td>3980</td>
			<td>4500</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Light Anti-Tank Weapon (LAW) vs. Energy Shield (50% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>500</td>
			<td>750</td>
			<td>870</td>
			<td>1000</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>625</td>
			<td>875</td>
			<td>995</td>
			<td>1125</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>1000</td>
			<td>1500</td>
			<td>1740</td>
			<td>2000</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>1250</td>
			<td>1750</td>
			<td>1990</td>
			<td>2250</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponLAM"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Lightweight Attack Munitions (LAM) (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>500</td>
			<td>600</td>
			<td>800</td>
			<td>1000</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>625</td>
			<td>725</td>
			<td>925</td>
			<td>1125</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso)</td>
			<td>1000</td>
			<td>1100</td>
			<td>1300</td>
			<td>1500</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso)</td>
			<td>1125</td>
			<td>1225</td>
			<td>1425</td>
			<td>1625</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>1000</td>
			<td>1200</td>
			<td>1600</td>
			<td>2000</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>1250</td>
			<td>1450</td>
			<td>1850</td>
			<td>2250</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head)</td>
			<td>2000</td>
			<td>2200</td>
			<td>2600</td>
			<td>3000</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head)</td>
			<td>2250</td>
			<td>2450</td>
			<td>2850</td>
			<td>3250</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Lightweight Attack Munitions (LAM) vs. Energy Shield (50% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>250</td>
			<td>300</td>
			<td>400</td>
			<td>500</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>312</td>
			<td>362</td>
			<td>462</td>
			<td>562</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso)</td>
			<td>500</td>
			<td>550</td>
			<td>650</td>
			<td>750</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso)</td>
			<td>562</td>
			<td>612</td>
			<td>712</td>
			<td>812</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>500</td>
			<td>600</td>
			<td>800</td>
			<td>1000</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>624</td>
			<td>724</td>
			<td>924</td>
			<td>1124</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head)</td>
			<td>1000</td>
			<td>1100</td>
			<td>1300</td>
			<td>1500</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head)</td>
			<td>1124</td>
			<td>1224</td>
			<td>1424</td>
			<td>1624</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponMiniCrossbow"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Mini-Crossbow (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>10</td>
			<td>15</td>
			<td>17</td>
			<td>20</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>12</td>
			<td>17</td>
			<td>19</td>
			<td>22</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>20</td>
			<td>30</td>
			<td>34</td>
			<td>40</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>24</td>
			<td>34</td>
			<td>38</td>
			<td>44</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Mini-Crossbow vs. Environmental Resistance (10% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>1</td>
			<td>1</td>
			<td>1</td>
			<td>2</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>1</td>
			<td>1</td>
			<td>1</td>
			<td>2</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>2</td>
			<td>2</td>
			<td>2</td>
			<td>4</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>2</td>
			<td>2</td>
			<td>2</td>
			<td>4</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponPepperGun"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Pepper Gun (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (1 hit)</td>
			<td>1</td>
			<td>1</td>
			<td>1</td>
			<td>2</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (1 hit)</td>
			<td>1</td>
			<td>1</td>
			<td>1</td>
			<td>2</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (1 hit)</td>
			<td>2</td>
			<td>2</td>
			<td>2</td>
			<td>4</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (1 hit)</td>
			<td>2</td>
			<td>2</td>
			<td>2</td>
			<td>4</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (7 hits)</td>
			<td>7</td>
			<td>7</td>
			<td>7</td>
			<td>14</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (7 hits)</td>
			<td>7</td>
			<td>7</td>
			<td>7</td>
			<td>14</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (7 hits)</td>
			<td>14</td>
			<td>14</td>
			<td>14</td>
			<td>28</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (7 hits)</td>
			<td>14</td>
			<td>14</td>
			<td>14</td>
			<td>28</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Pepper Gun vs. Environmental Resistance (10% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (1 hit)</td>
			<td>0</td>
			<td>0</td>
			<td>0</td>
			<td>0</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (1 hit)</td>
			<td>0</td>
			<td>0</td>
			<td>0</td>
			<td>0</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (1 hit)</td>
			<td>0</td>
			<td>0</td>
			<td>0</td>
			<td>0</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (1 hit)</td>
			<td>0</td>
			<td>0</td>
			<td>0</td>
			<td>0</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (7 hits)</td>
			<td>0</td>
			<td>0</td>
			<td>0</td>
			<td>0</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (7 hits)</td>
			<td>0</td>
			<td>0</td>
			<td>0</td>
			<td>0</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (7 hits)</td>
			<td>0</td>
			<td>0</td>
			<td>0</td>
			<td>0</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (7 hits)</td>
			<td>0</td>
			<td>0</td>
			<td>0</td>
			<td>0</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponPistol"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Pistol (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>20</td>
			<td>30</td>
			<td>34</td>
			<td>40</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>25</td>
			<td>35</td>
			<td>39</td>
			<td>45</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>40</td>
			<td>60</td>
			<td>68</td>
			<td>80</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>50</td>
			<td>70</td>
			<td>78</td>
			<td>90</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Pistol vs. Ballistic Protection (60% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>12</td>
			<td>18</td>
			<td>20</td>
			<td>24</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>15</td>
			<td>21</td>
			<td>23</td>
			<td>27</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>24</td>
			<td>36</td>
			<td>40</td>
			<td>48</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>30</td>
			<td>42</td>
			<td>46</td>
			<td>54</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponPlasmaRifle"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Plasma Rifle (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (1 hit)</td>
			<td>8</td>
			<td>12</td>
			<td>13</td>
			<td>16</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (1 hit)</td>
			<td>10</td>
			<td>14</td>
			<td>15</td>
			<td>18</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (1 hit)</td>
			<td>16</td>
			<td>24</td>
			<td>26</td>
			<td>32</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (1 hit)</td>
			<td>20</td>
			<td>28</td>
			<td>30</td>
			<td>36</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (3 hits)</td>
			<td>24</td>
			<td>36</td>
			<td>39</td>
			<td>48</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (3 hits)</td>
			<td>30</td>
			<td>42</td>
			<td>45</td>
			<td>54</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (3 hits)</td>
			<td>48</td>
			<td>72</td>
			<td>78</td>
			<td>96</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (3 hits)</td>
			<td>60</td>
			<td>84</td>
			<td>90</td>
			<td>108</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Plasma Rifle vs. Energy Shield (50% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (1 hit)</td>
			<td>4</td>
			<td>6</td>
			<td>6</td>
			<td>8</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (1 hit)</td>
			<td>5</td>
			<td>7</td>
			<td>7</td>
			<td>9</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (1 hit)</td>
			<td>8</td>
			<td>12</td>
			<td>12</td>
			<td>16</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (1 hit)</td>
			<td>10</td>
			<td>14</td>
			<td>14</td>
			<td>18</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (3 hits)</td>
			<td>12</td>
			<td>18</td>
			<td>18</td>
			<td>24</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (3 hits)</td>
			<td>15</td>
			<td>21</td>
			<td>21</td>
			<td>27</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (3 hits)</td>
			<td>24</td>
			<td>36</td>
			<td>36</td>
			<td>48</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (3 hits)</td>
			<td>30</td>
			<td>42</td>
			<td>42</td>
			<td>54</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponHideAGun"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">PS20 (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>8</td>
			<td>12</td>
			<td>13</td>
			<td>16</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>10</td>
			<td>14</td>
			<td>15</td>
			<td>18</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>16</td>
			<td>24</td>
			<td>26</td>
			<td>32</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>20</td>
			<td>28</td>
			<td>30</td>
			<td>36</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">PS20 vs. Energy Shield (50% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>4</td>
			<td>6</td>
			<td>6</td>
			<td>8</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>5</td>
			<td>7</td>
			<td>7</td>
			<td>9</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>8</td>
			<td>12</td>
			<td>12</td>
			<td>16</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>10</td>
			<td>14</td>
			<td>14</td>
			<td>18</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponProd"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Riot Prod (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>15</td>
			<td>22</td>
			<td>26</td>
			<td>30</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>18</td>
			<td>26</td>
			<td>29</td>
			<td>33</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>30</td>
			<td>44</td>
			<td>52</td>
			<td>60</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>36</td>
			<td>52</td>
			<td>58</td>
			<td>66</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponSawedOffShotgun"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Sawed-off Shotgun (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (1 hit)</td>
			<td>9</td>
			<td>13</td>
			<td>15</td>
			<td>18</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (1 hit)</td>
			<td>11</td>
			<td>15</td>
			<td>17</td>
			<td>20</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (1 hit)</td>
			<td>18</td>
			<td>26</td>
			<td>30</td>
			<td>36</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (1 hit)</td>
			<td>22</td>
			<td>30</td>
			<td>34</td>
			<td>40</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (5 hits)</td>
			<td>45</td>
			<td>65</td>
			<td>75</td>
			<td>90</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (5 hits)</td>
			<td>55</td>
			<td>75</td>
			<td>85</td>
			<td>100</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (5 hits)</td>
			<td>90</td>
			<td>130</td>
			<td>150</td>
			<td>180</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (5 hits)</td>
			<td>110</td>
			<td>150</td>
			<td>170</td>
			<td>200</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Sawed-off Shotgun vs. Ballistic Protection (60% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (1 hit)</td>
			<td>5</td>
			<td>7</td>
			<td>9</td>
			<td>10</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (1 hit)</td>
			<td>6</td>
			<td>9</td>
			<td>10</td>
			<td>12</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (1 hit)</td>
			<td>10</td>
			<td>14</td>
			<td>18</td>
			<td>20</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (1 hit)</td>
			<td>12</td>
			<td>18</td>
			<td>20</td>
			<td>24</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso) (5 hits)</td>
			<td>25</td>
			<td>35</td>
			<td>45</td>
			<td>50</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso) (5 hits)</td>
			<td>30</td>
			<td>45</td>
			<td>50</td>
			<td>60</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head) (5 hits)</td>
			<td>50</td>
			<td>70</td>
			<td>90</td>
			<td>100</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head) (5 hits)</td>
			<td>60</td>
			<td>90</td>
			<td>100</td>
			<td>120</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponRifle"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Sniper Rifle (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>8</td>
			<td>12</td>
			<td>15</td>
			<td>17</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>10</td>
			<td>15</td>
			<td>17</td>
			<td>19</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>16</td>
			<td>24</td>
			<td>30</td>
			<td>34</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>20</td>
			<td>30</td>
			<td>34</td>
			<td>38</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Scope) (Torso)</td>
			<td>25</td>
			<td>37</td>
			<td>43</td>
			<td>50</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Scope) (Torso)</td>
			<td>31</td>
			<td>43</td>
			<td>49</td>
			<td>56</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Scope) (Head)</td>
			<td>50</td>
			<td>74</td>
			<td>86</td>
			<td>100</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Scope) (Head)</td>
			<td>62</td>
			<td>86</td>
			<td>98</td>
			<td>112</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Sniper Rifle vs. Ballistic Protection (60% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>5</td>
			<td>7</td>
			<td>8</td>
			<td>10</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>6</td>
			<td>8</td>
			<td>10</td>
			<td>11</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>10</td>
			<td>14</td>
			<td>16</td>
			<td>20</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>12</td>
			<td>16</td>
			<td>20</td>
			<td>22</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Scope) (Torso)</td>
			<td>15</td>
			<td>22</td>
			<td>25</td>
			<td>30</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Scope) (Torso)</td>
			<td>18</td>
			<td>25</td>
			<td>29</td>
			<td>33</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Scope) (Head)</td>
			<td>30</td>
			<td>44</td>
			<td>50</td>
			<td>60</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Scope) (Head)</td>
			<td>36</td>
			<td>50</td>
			<td>58</td>
			<td>66</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponStealthPistol"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Stealth Pistol (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>12</td>
			<td>18</td>
			<td>20</td>
			<td>24</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>15</td>
			<td>21</td>
			<td>23</td>
			<td>27</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>24</td>
			<td>36</td>
			<td>40</td>
			<td>48</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>30</td>
			<td>42</td>
			<td>46</td>
			<td>54</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Stealth Pistol vs. Ballistic Protection (60% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>7</td>
			<td>10</td>
			<td>12</td>
			<td>14</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>9</td>
			<td>12</td>
			<td>13</td>
			<td>16</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>14</td>
			<td>20</td>
			<td>24</td>
			<td>28</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>18</td>
			<td>24</td>
			<td>26</td>
			<td>32</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponSword"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Sword (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>20</td>
			<td>30</td>
			<td>34</td>
			<td>40</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>25</td>
			<td>35</td>
			<td>39</td>
			<td>45</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso)</td>
			<td>40</td>
			<td>50</td>
			<td>54</td>
			<td>60</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso)</td>
			<td>45</td>
			<td>55</td>
			<td>59</td>
			<td>65</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>40</td>
			<td>60</td>
			<td>68</td>
			<td>80</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>50</td>
			<td>70</td>
			<td>78</td>
			<td>90</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head)</td>
			<td>80</td>
			<td>100</td>
			<td>108</td>
			<td>120</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head)</td>
			<td>90</td>
			<td>110</td>
			<td>118</td>
			<td>130</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Sword vs. Ballistic Protection (60% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>12</td>
			<td>18</td>
			<td>20</td>
			<td>24</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>15</td>
			<td>21</td>
			<td>23</td>
			<td>27</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso)</td>
			<td>24</td>
			<td>30</td>
			<td>32</td>
			<td>36</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso)</td>
			<td>27</td>
			<td>33</td>
			<td>35</td>
			<td>39</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>24</td>
			<td>36</td>
			<td>40</td>
			<td>48</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>30</td>
			<td>42</td>
			<td>46</td>
			<td>54</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head)</td>
			<td>48</td>
			<td>60</td>
			<td>64</td>
			<td>72</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head)</td>
			<td>54</td>
			<td>66</td>
			<td>70</td>
			<td>78</td>
		</tr>
	</tbody>
</table>
<br />
<a name="WeaponShuriken"></a>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Throwing Knives (100% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>17</td>
			<td>25</td>
			<td>29</td>
			<td>34</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>21</td>
			<td>29</td>
			<td>33</td>
			<td>38</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso)</td>
			<td>34</td>
			<td>42</td>
			<td>46</td>
			<td>51</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso)</td>
			<td>38</td>
			<td>46</td>
			<td>50</td>
			<td>55</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>34</td>
			<td>50</td>
			<td>58</td>
			<td>68</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>42</td>
			<td>58</td>
			<td>66</td>
			<td>76</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head)</td>
			<td>68</td>
			<td>84</td>
			<td>92</td>
			<td>102</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head)</td>
			<td>76</td>
			<td>92</td>
			<td>100</td>
			<td>110</td>
		</tr>
	</tbody>
</table>
<p>&nbsp;</p>
<table cellpadding="4" cellspacing="0" class="smallcw">
	<tbody>
		<tr align="center">
			<th colspan="5" nowrap="nowrap">Throwing Knives vs. Ballistic Protection (60% damage)</th>
		</tr>
		<tr align="center">
			<td>&nbsp;</td>
			<td>Base Damage</td>
			<td>Level 1</td>
			<td>Level 2</td>
			<td>Level 3</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Torso)</td>
			<td>10</td>
			<td>15</td>
			<td>17</td>
			<td>20</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Torso)</td>
			<td>12</td>
			<td>17</td>
			<td>19</td>
			<td>22</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Torso)</td>
			<td>20</td>
			<td>25</td>
			<td>27</td>
			<td>30</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Torso)</td>
			<td>22</td>
			<td>27</td>
			<td>30</td>
			<td>33</td>
		</tr>
		<tr align="center">
			<td align="right">Base Damage (Head)</td>
			<td>20</td>
			<td>30</td>
			<td>34</td>
			<td>40</td>
		</tr>
		<tr align="center">
			<td align="right">Targeting (Head)</td>
			<td>24</td>
			<td>34</td>
			<td>38</td>
			<td>44</td>
		</tr>
		<tr align="center">
			<td align="right">Combat Strength (Head)</td>
			<td>40</td>
			<td>50</td>
			<td>54</td>
			<td>60</td>
		</tr>
		<tr align="center">
			<td align="right">Target + Combat (Head)</td>
			<td>44</td>
			<td>54</td>
			<td>60</td>
			<td>66</td>
		</tr>
	</tbody>
</table>
