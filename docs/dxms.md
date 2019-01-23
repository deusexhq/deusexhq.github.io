<div class="tcalert">
<b>The following steps can also be performed automatically!</b><br>
<a href="https://cdn.discordapp.com/attachments/421285829818974209/535045916185460757/dxmsfix.exe"><img src="https://cdn.discordapp.com/emojis/456853254748504097.png" alt="MS Fix" width="15" height="15" border="0" />Click here to download the automatic fix.</a><br />
<small>This executable does the exact same as described below, but makes the process easier by finding the DeusEx.ini by itself and applying the fix.<br>
Credits to Elliot/Machete for the patcher.</small>
</div>

## What happened to the servers?
<p>
All servers in the game rely on something called a Masterserver to be displayed to players in-game.
Originally, the servers were hosted by Gamespy, but at some point Gamespy shut down their service, and since then, the new host has been 333networks. 
Everything works as before, but in order to use the new masterserver, you need to change to it manually.
</p>

## How do I use the new masterserver?
<p>
Configuring the masterservers is done in the DeusEx.ini file.

### Finding the DeusEx.ini

The DeusEx.ini is usually in a directory named System in your DeusEx game directory. The DeusEx game directory can be in
different locations:
```
C:\Deus Ex\
C:\GOG Games\Deus Ex
C:\Program Files\DeusEx\
C:\Program Files (x86)\DeusEx\
C:\Program Files\Steam\SteamApps\common\Deus Ex
C:\Program Files (x86)\Steam\SteamApps\common\Deus Ex
..\Somewhere in MyDocuments (If using Kenties Launcher)
```

If you only play Deus Ex and never host a gameserver, this is the only step that is
required. 
Open DeusEx.ini and find the following:

```
[DeusEx.MenuScreenJoinGame]
```

Beneath this line, there will be something in the sorts of MasterServerAddress= with a value behind it. This value will most likely be similar to: <strong>master0.gamespy.com</strong>
Replace this value with the following: <strong>master.deusexnetwork.com</strong>		or <strong>master.333networks.com</strong> Save the file and you're done! Everything should work without any problems but should you run into any issues or have further questions, feel free to leave a message via the <a href="http://discord.gg/KUA8acb">Discord</a><br>
</p>

### Configuring the gameserver
<p>
If you're also hosting a gameserver it's important to add the alternative masterserver to your server's uplink as well. This way players can also find your server on the new masterserver. Open DeusEx.ini and find the following:
`[DeusEx.DeusExGameEngine]`
Beneath this line, there will be one or multiple lines looking like the following:
`ServerActors=IpServer.UdpServerUplink MasterServerAddress=`
or
`ServerActors=Nephthys.NptServerUplink MasterServerAddress=`
You will have the first line if you don't use Nephthys (which you should, it adds vital protection to your server!), and second if you do use Nephthys.
Change the value after <strong>MasterServerAddress=</strong> with either of the following: 
<strong>master.deusexnetwork.com</strong> 
or
<strong>master.333networks.com</strong>

The value MasterServerPort does not need to be modified.
In the end, it should look something like this:
```
ServerActors=IpServer.UdpServerUplink MasterServerAddress=master.333networks.com MasterServerPort=27900
ServerActors=IpServer.UdpServerUplink MasterServerAddress=master.epicgames.com MasterServerPort=27900
ServerActors=IpServer.UdpServerUplink MasterServerAddress=master.fragaholic.com MasterServerPort=27900
```

As long as one line contains either <strong>master.deusexnetwork.com</strong> or <strong>master.333networks.com</strong>, the server will connect.
Save the file and you're done! Everything should work without any problems but should you run into any issues or have further
questions, feel free to leave a message via the <a href="http://discord.gg/KUA8acb">Discord</a>.

<em>Page originally from DXAlpha, modified and updated by Kaiser. Patcher by Machete.</em>
</p> 
