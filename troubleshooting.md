## Procedure Entry Point error
<p>
It&#39;s <em>most likely</em> caused by improperly installed renderer&#39;s driver. The majority of people get this error when they try to change to OpenGL renderer &mdash; because they download a wrong driver for Unreal Tournament from <a href="http://cwdohnal.home.mindspring.com/utglr/">Chris Dohnal&#39;s website</a>. To solve the problem, re-download the driver which is meant to be used with Deus Ex, not Unreal Tournament. The section with Deus Ex drivers is below section with UT drivers. Unreal Tournament drivers don&#39;t work with the game and cause this error.
</p>
	
## Mismatching
<p>
So, you see a server with your favourite map on, or your fellow clan mate playing on it. You swiftly attempt to join the
server when *SMASH*, you're stopped in your tracks by a large "*Filename*_MisMatch error", or a similar message.
I&rsquo;ve had enough of these in the past, and although not life-threatening, they can be a hefty nuisance. I'm going
to briefly go over the simplest way to fix this problem, let's look at probably the most common example:
</p>

### Fixing MisMatch Errors
<p>
You see a popular server, 8/10 slots full, 80 ping, playing on DXMP_Cathedral. You attempt to join and you get the old MisMatch
error (I'll explain why later). Now the best way to fix this is:
</p>
<ol start="1">
<li>Close down all instances of Deus Ex. </li>
<li>Locate your Maps folder, generally in MyComputer&gt;C:&gt;DeusEx&gt;Maps. </li>
<li>Locate DXMP_Cathedral, most likely near the bottom. </li>
<li>Either Drag this onto your desktop or some other place, or delete it. </li>
<li>Now attempt to re-join the server. You should be able to join without error. </li>
</ol>
<p>
If you still get the MisMatch error, and you have definitely taken DXMP_Cathedral away from your Deus Ex folder, it may be
required that you purge your cache. The cache, in brief, stores all of the Downloads you have taken from servers, so Gun
Mods, Maps, Anti-Cheating Mods, etc. Either delete all of that or take about 3-5 out at a time, then try to re-join the
server.
</p>
### Why do MisMatch Errors occur?
<p>
If we take DXMP_Cathedral for example, several versions of the same map were released under the name DXMP_Cathedral. That
means that it attempts to fetch the DXMP_Cathedral in your /Maps folder, because it sees you are joining a map with the
name DXMP_Cathedral. If the server is running a different version however, Deus Ex tends to just get confused and give
up, leaving you to mop up the pieces and sort it out!
</p>
<p>
Another typical example is CaroneElevatorSet.u, a clever mod used to help make lift-making simpler in Deus Ex Editor/SDK.
The maker, Carone I believe, released several versions under the same name. The map DXMP_RPGCity apparently uses it, must
be in the crane or something - but I will usually get a MisMatch Error if I have been using CaroneElevator in a map I was
making, and forgotten to remove it from /System.
</p>
<p>
So to re-cap, if you get MisMatch errors, look at what the filename/map it is, then close Deus Ex and take that map/file
out of your /DeusEx Folder!
</p>

## Bad Name error and/or New/None Actor Channel
<p>
This problem appears when one of the system files of Deus Ex is corrupted, usually it&#39;s "DeusEx.u" or "Engine.u". Other issues may also be involved.
There are various ways to solve this:
<ul>
<li>Insert your Deus Ex CD, open it for browsing. Find System/ folder and copy "DeusEx.u" to your DeusEx/System/ folder. If it doesn&#39;t work, try copying all the files with .u extension to your DeusEx/System/ folder. </li>
<li>Ask someone to give you the file(s). </li>
<li>The easiest way is to reinstall Deus Ex. If you don&#39;t want to lose the settings, move/copy User.ini, Defuser.ini, DeusEx.ini and Default.ini from DeusEx/System to a safe place during installation and when it&#39;s finished, move them back.</li>
</ul>

<strong>Other things to try</strong>:
Try turning off GUI fix/other fixes in Kenteis.
Either change renderer, then change back to original, 
or ingame type `debug gpf` then restart.

<em>Thanks to Clix for the solution.</em>
</p>

## Clientdeath
### What is it?
This is a bug of the game, called "client death". "Client death" is when you hear your own death scream, your user interface disappears, but you can still move (from a technical point of view, the player dies on <em>your</em> computer, but it doesn't die on the server, so the server doesn't clean your inventory, respawn and fine a death point on the scoreboard).

### Fixing
When happened, just press "Esc" button on your keyboard, it will show the main menu, then return to the game.
Your interface should appear again. Don't pay attention to your "dead" body &mdash; the bug will go as soon as you're injured.

### Causes
The glitch occurs when the multiplayer replication code de-syncs between the client and server, which can happen for many reasons, including server lag, bad coding or other rare glitches.
Basically, the server didn't expect the death to occur, but something on the client forced the death, which causes the desync.
	
## Bad Name Index
This problem appears when one of the system files of Deus Ex is corrupted, usually it's "DeusEx.u" or "Engine.u". Other issues may also be involved.
There are various ways to solve this:
<ul>
	<li>Insert your Deus Ex CD, open it for browsing. Find System/ folder and copy "DeusEx.u" to your DeusEx/System/
		folder. If it doesn't work, try copying all the files with .u extension to your DeusEx/System/ folder. </li>
	<li>Ask someone to give you the file(s). </li>
	<li>The easiest way is to reinstall Deus Ex. If you don't want to lose the settings, move/copy User.ini, Defuser.ini, DeusEx.ini
		and Default.ini from DeusEx/System to a safe place during installation and when it's finished, move them back.</li>
</ul>

<strong>Other things to try</strong>:
Try turning off GUI fix/other fixes in Kenteis.
New/None actor channel: Either change renderer, then change back to original, or ingame type `debug gpf` then restart.
<p>
	<em>Thanks to Clix for the solution.</em>
</p>
