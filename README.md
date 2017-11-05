## General

[![Poggit Release](https://poggit.pmmp.io/shield.approved/CustomAlerts)](https://poggit.pmmp.io/p/CustomAlerts)


Customize or hide alerts (join/leave messages, whitelist messages, outdated server/client messages, etc...) plugin for PocketMine-MP

## Overview


With CustomAlerts you can customize or hide whitelist kick messages, outdated server/client messages, join/leave messages, first join messages, death messages, world change messages...

## Features

- Customize or hide join, quit and death messages
- Add first join and world change messages
- Customize Motd
- Customize Outdated Server/Client kick messages
- Customize Whitelist kick messages
- Customize Full Server kick messages

## Colours

**Colours:**

Black ("&0");<br>
Dark Blue ("&1");<br>
Dark Green ("&2");<br>
Dark Aqua ("&3");<br>
Dark Red ("&4");<br>
Dark Purple ("&5");<br>
Gold ("&6");<br>
Gray ("&7");<br>
Dark Gray ("&8");<br>
Blue ("&9");<br>
Green ("&a");<br>
Aqua ("&b");<br>
Red ("&c");<br>
Light Purple ("&d");<br>
Yellow ("&e");<br>
White ("&f");<br>

## Formatting

Obfuscated ("&k");<br>
Bold ("&l");<br>
Strikethrough ("&m");<br>
Underline ("&n");<br>
Italic ("&o");<br>
Reset ("&r");<br>

## Configuration

```
---
#REMEMBER THAT IF YOU USE CustomAlerts EXTENSIONS, MESSAGES MAY NOT FOLLOW THE DEFAULT CONFIG
#Date/Time format (replaced in {TIME}). For format codes read http://php.net/manual/en/datetime.formats.php
datetime-format: "H:i:s"
#Server Motd message settings (available from MCPE 0.11.0 and later)
Motd:
  #Motd update timeout
  update-timeout: 1
  #Show custom Motd
  custom: true
  #Motd message
  #Available Tags:
  # - {MAXPLAYERS}: Show the maximum number of players supported by the server
  # - {TIME}: Show current time
  # - {TOTALPLAYERS}: Show the number of all online players
  message: "&e[{TIME}] &aWelcome to your server! &n&b[{MAXPLAYERS}/{TOTALPLAYERS}]"
#Outdated Client message (available from MCPE 0.11.0 BUILD 11 and later)
OutdatedClient:
  #Show custom Outdated Client message
  custom: true
  #Outdated Client message
  #Available Tags:
  # - {MAXPLAYERS}: Show the maximum number of players supported by the server
  # - {PLAYER}: Show player name
  # - {TIME}: Show current time
  # - {TOTALPLAYERS}: Show the number of all online players
  message: "&cYour MCPE client is outdated!"
#Outdated Server message (available from MCPE 0.11.0 BUILD 11 and later)
OutdatedServer:
  #Show custom Outdated Server message
  custom: true
  #Outdated Server message
  #Available Tags:
  # - {MAXPLAYERS}: Show the maximum number of players supported by the server
  # - {PLAYER}: Show player name
  # - {TIME}: Show current time
  # - {TOTALPLAYERS}: Show the number of all online players
  message: "&cOops! Server outdated!"
#Whitelisted Server message (available from MCPE 0.11.0 BUILD 11 and later)
WhitelistedServer:
  #Show custom Whitelisted Server message
  custom: true
  #Whitelisted Server message
  #Available Tags:
  # - {MAXPLAYERS}: Show the maximum number of players supported by the server
  # - {PLAYER}: Show player name
  # - {TIME}: Show current time
  # - {TOTALPLAYERS}: Show the number of all online players
  message: "&c&oThis Server is whitelisted!"
#Full Server message (available from MCPE 0.11.0 BUILD 11 and later)
FullServer:
  #Show custom Full Server message
  custom: true
  #Available Tags:
  # - {MAXPLAYERS}: Show the maximum number of players supported by the server
  # - {PLAYER}: Show player name
  # - {TIME}: Show current time
  # - {TOTALPLAYERS}: Show the number of all online players
  message: "&e{PLAYER}&b, The Server is full &c[{TOTALPLAYERS}/{MAXPLAYERS}]&b!\n&l&dTry to join later :)"
#First Join message settings
FirstJoin:
  #Enable First Join message
  enable: true
  #First Join message
  #Available Tags:
  # - {MAXPLAYERS}: Show the maximum number of players supported by the server
  # - {PLAYER}: Show player name
  # - {TIME}: Show current time
  # - {TOTALPLAYERS}: Show the number of all online players
  message: "&2[{TIME}] &a{PLAYER}&d joined the game for the first time."
#Join message settings
Join:
  #Hide Join message
  hide: false
  #Show custom Join message 
  custom: true
  #Join message
  #Available Tags:
  # - {MAXPLAYERS}: Show the maximum number of players supported by the server
  # - {PLAYER}: Show player name
  # - {TIME}: Show current time
  # - {TOTALPLAYERS}: Show the number of all online players
  message: "&2[{TIME}] &a{PLAYER}&e joined the game."
#Quit message settings
Quit:
  #Hide Quit message
  hide: true
  #Show custom Quit message 
  custom: false
  #Quit message
  #Available Tags:
  # - {MAXPLAYERS}: Show the maximum number of players supported by the server
  # - {PLAYER}: Show player name
  # - {TIME}: Show current time
  # - {TOTALPLAYERS}: Show the number of all online players
  message: "&4[{TIME}] &c{PLAYER}&e has left the game"
#World Change message settings
WorldChange:
  #Enable World Change message
  enable: true
  #World Change message
  #Available Tags:
  # - {MAXPLAYERS}: Show the maximum number of players supported by the server
  # - {ORIGIN}: Show origin world name
  # - {PLAYER}: Show player name
  # - {TARGET}: Show target world name
  # - {TIME}: Show current time
  # - {TOTALPLAYERS}: Show the number of all online players
  message: "&2[{TIME}] &a{PLAYER}&e moved from &c{ORIGIN}&e to &a{TARGET}"
#Death message settings
Death:
  #Hide deafult Death message
  hide: false
  #Show custom default Death message
  custom: true
  #Default Death message
  #Available Tags:
  # - {MAXPLAYERS}: Show the maximum number of players supported by the server
  # - {PLAYER}: Show player name
  # - {TIME}: Show current time
  # - {TOTALPLAYERS}: Show the number of all online players
  message: "&c{PLAYER} died"
  #Death by contact message
  death-contact-message:
    #Hide Death by contact message
    hide: false
    #Show custom Death by contact message
    custom: true
    #Death by contact message
    #Available Tags:
    # - {BLOCK}: The name of the block which killed the player
    # - {MAXPLAYERS}: Show the maximum number of players supported by the server
    # - {PLAYER}: Show player name
    # - {TIME}: Show current time
    # - {TOTALPLAYERS}: Show the number of all online players
    message: "&cOops! {PLAYER} was killed by {BLOCK}"
  #Death by entity message (players and mobs)
  kill-message:
    #Hide Death by entity message
    hide: false
    #Show custom Death by entity message
    custom: true
    #Death by entity message
    # - {KILLER}: The name of the killer entity
    # - {MAXPLAYERS}: Show the maximum number of players supported by the server
    # - {PLAYER}: Show player name
    # - {TIME}: Show current time
    # - {TOTALPLAYERS}: Show the number of all online players
    message: "&9{PLAYER} &ewas killed by &c{KILLER}"
  #Death by projectile message
  death-projectile-message:
    #Hide Death by projectile message
    hide: false
    #Show custom Death by projectile message
    custom: true
    #Death by projectile message
    # - {KILLER}: The name of the killer entity
    # - {MAXPLAYERS}: Show the maximum number of players supported by the server
    # - {PLAYER}: Show player name
    # - {TIME}: Show current time
    # - {TOTALPLAYERS}: Show the number of all online players
    message: "&c{PLAYER} was killed by {KILLER} by arrow"
  #Death by suffocation message
  death-suffocation-message:
    #Hide Death by suffocation message
    hide: false
    #Show custom Death by suffocation message
    custom: true
    #Death by suffocation message
    # - {MAXPLAYERS}: Show the maximum number of players supported by the server
    # - {PLAYER}: Show player name
    # - {TIME}: Show current time
    # - {TOTALPLAYERS}: Show the number of all online players
    message: "&c{PLAYER} suffocated"
  #Death by fall message
  death-fall-message:
    #Hide Death by fall message
    hide: false
    #Show custom Death by fall message
    custom: true
    #Death by fall message
    # - {MAXPLAYERS}: Show the maximum number of players supported by the server
    # - {PLAYER}: Show player name
    # - {TIME}: Show current time
    # - {TOTALPLAYERS}: Show the number of all online players
    message: "&c{PLAYER} fell from a high place"
  #Death by fire message
  death-fire-message:
    #Hide Death by fire message
    hide: false
    #Show custom Death by fire message
    custom: true
    #Death by fire message
    # - {MAXPLAYERS}: Show the maximum number of players supported by the server
    # - {PLAYER}: Show player name
    # - {TIME}: Show current time
    # - {TOTALPLAYERS}: Show the number of all online players
    message: "&c{PLAYER} went up in flames"
  #Death on fire message
  death-on-fire-message:
    #Hide Death on fire message
    hide: false
    #Show custom Death on fire message
    custom: true
    #Death on fire message
    # - {MAXPLAYERS}: Show the maximum number of players supported by the server
    # - {PLAYER}: Show player name
    # - {TIME}: Show current time
    # - {TOTALPLAYERS}: Show the number of all online players
    message: "&c{PLAYER} burned"
  #Death by lava message
  death-lava-message:
    #Hide Death by lava message
    hide: false
    #Show custom Death by lava message
    custom: true
    #Death by lava message
    # - {MAXPLAYERS}: Show the maximum number of players supported by the server
    # - {PLAYER}: Show player name
    # - {TIME}: Show current time
    # - {TOTALPLAYERS}: Show the number of all online players
    message: "&c{PLAYER} tried to swim in lava"
  #Death by drowning message
  death-drowning-message:
    #Hide Death by drowning message
    hide: false
    #Show custom Death by drowning message
    custom: true
    #Death by drowning message
    # - {MAXPLAYERS}: Show the maximum number of players supported by the server
    # - {PLAYER}: Show player name
    # - {TIME}: Show current time
    # - {TOTALPLAYERS}: Show the number of all online players
    message: "&c{PLAYER} drowned"
  #Death by explosion message
  death-explosion-message:
    #Hide Death by explosion message
    hide: false
    #Show custom Death by explosion message
    custom: true
    #Death by explosion message
    # - {MAXPLAYERS}: Show the maximum number of players supported by the server
    # - {PLAYER}: Show player name
    # - {TIME}: Show current time
    # - {TOTALPLAYERS}: Show the number of all online players
    message: "&c{PLAYER} exploded"
  #Death by void message
  death-void-message:
    #Hide Death by void message
    hide: false
    #Show custom Death by void message
    custom: true
    #Death by void message
    # - {MAXPLAYERS}: Show the maximum number of players supported by the server
    # - {PLAYER}: Show player name
    # - {TIME}: Show current time
    # - {TOTALPLAYERS}: Show the number of all online players
    message: "&c{PLAYER} fell into the void"
  #Death by suicide message
  death-suicide-message:
    #Hide Death by suicide message
    hide: false
    #Show custom Death by suicide message
    custom: true
    #Death by suicide message
    # - {MAXPLAYERS}: Show the maximum number of players supported by the server
    # - {PLAYER}: Show player name
    # - {TIME}: Show current time
    # - {TOTALPLAYERS}: Show the number of all online players
    message: "&c{PLAYER} committed suicide"
  #Death magic message
  death-magic-message:
    #Hide Death magic message
    hide: false
    #Show custom Death magic message
    custom: true
    #Death magic message
    # - {MAXPLAYERS}: Show the maximum number of players supported by the server
    # - {PLAYER}: Show player name
    # - {TIME}: Show current time
    # - {TOTALPLAYERS}: Show the number of all online players
    message: "&c{PLAYER} was killed by a spell"
```
## Permissions

`customalerts.help` - CustomAlerts command Help permission

`customalerts.info` - CustomAlerts command Info permission

`customalerts.reload`- CustomAlerts command Reload permission

## Developers

**Basic Tutorial:**

*1. Define the plugin dependency in plugin.yml (you can check if CustomAlerts is installed in different ways):*
```
depend: [CustomAlerts]
```
*2. Include CustomAlerts API and CustomAlerts Events in your php code:*
```
//PocketMine Event Listener
use pocketmine\event\Listener;
//CustomAlerts API
use CustomAlerts\CustomAlerts;
//CustomAlerts Events
use CustomAlerts\Events\CustomAlertsJoinEvent;
```
*3. Create the class:*
```
class Example extends PluginBase implements Listener {
}
```
*4. Check if CustomAlerts API is compatible (insert this code in onEnable() function)*
```
if(CustomAlerts::getAPI()->getAPIVersion() == "(used API version)"){
            //API compatible
            //Register Events
            $this->getServer()->getPluginManager()->registerEvents($this, $this);
        }else{
            //API not compatible
            $this->getPluginLoader()->disablePlugin($this);
        }
  }
```
*5. Handle a CustomAlerts event (in this tutorial we will handle the CustomAlertsJoinEvent):*
```
public function onCAJoinEvent(CustomAlertsJoinEvent $event){
  CustomAlerts::getAPI()->setJoinMessage("Example Join message: " . $event->getPlayer()->getName());
}
```
*6. Call the API function:*
```
CustomAlerts::getAPI()->api_function();
```
###### CustomAlertsDeathEvent:

This event is handled when a player dies.

Event functions are:

###### Get Player:

```
Player getPlayer()
```
**Description:**<br>
Get death event player.<br>
**Return:**<br>
The death event player

###### Get Cause:

```
EntityDamageEvent|null getCause()
```
**Description:**<br>
Get death event cause.<br>
**Return:**<br>
The death event cause

###### CustomAlertsFullServerKickEvent:

This event is handled when a player is kicked due to full server.

Event functions are:

###### Get Player:

```
Player getPlayer()
```
**Description:**<br>
Get event player.<br>
**Return:**<br>
The event player (instance of pocketmine\Player)

###### CustomAlertsJoinEvent:

This event is handled when a player joins.

Event functions are:

###### Get Player:

```
Player getPlayer()
```
**Description:**<br>
Get join event player.<br>
**Return:**<br>
The join event player (instance of pocketmine\Player)

###### Get default PocketMine join message:

```
string getPocketMineJoinMessage()
```
**Description:**<br>
Get default PocketMine join message.<br>
**Return:**<br>
The default PocketMine join message

###### CustomAlertsMotdUpdateEvent:

This event is handled when the motd is updated

Event functions are:

###### Get default PocketMine Motd:

```
string getPocketMineMotd()
```
**Description:**<br>
Get default PocketMine Motd.<br>
**Return:**<br>
The default PocketMine Motd

###### CustomAlertsOutdatedClientKickEvent:

This event is handled when a player is kicked due to outdated client.

Event functions are:

###### Get Player:

```
Player getPlayer()
```
**Description:**<br>
Get event player.<br>
**Return:**<br>
The event player (instance of pocketmine\Player)

###### CustomAlertsOutdatedServerKickEvent:

This event is handled when a player is kicked due to outdated server.

Event functions are:

###### Get Player:

```
Player getPlayer()
```
**Description:**<br>
Get event player.<br>
**Return:**<br>
The event player (instance of pocketmine\Player)

###### CustomAlertsQuitEvent:

This event is handled when a player quits. It must be declared:

Event functions are:

###### Get Player:

```
Player getPlayer()
```
**Description:**<br>
Get quit event player.<br>
**Return:**<br>
The quit event player (instance of pocketmine\Player)

###### Get default PocketMine quit message:

```
string getPocketMineQuitMessage()
```
**Description:**<br>
Get default PocketMine quit message.<br>
**Return:**<br>
The default PocketMine quit message

###### CustomAlertsWhitelistKickEvent:

This event is handled when a player is kicked due to whitelisted server.

Event functions are:

###### Get Player:

```
Player getPlayer()
```
**Description:**<br>
Get event player.<br>
**Return:**<br>
The event player (instance of pocketmine\Player)

###### CustomAlertsWorldChangeEvent:

This event is handled when a player changes world. It must be declared:

Event functions are:

###### Get Player:

```
Player getPlayer()
```
**Description:**<br>
Get world change event player.<br>
**Return:**<br>
The world change event player (instance of pocketmine\Player)

###### Get Origin Level:

```
Level getOrigin()
```
**Description:**<br>
Get origin level.<br>
**Return:**<br>
The origin level (instance of pocketmine\Level)

###### Get Target Level:

```
Level getTarget()
```
**Description:**<br>
Get target level.<br>
**Return:**<br>
The target level (instance of pocketmine\Level)

**CustomAlerts API Functions:**

###### Get Version:
```
string getVersion()
```
**Description:**<br>
Get CustomAlerts plugin version<br>
**Return:**<br>
plugin version

###### Get API Version:
```
string getAPIVersion()
```
**Description:**<br>
Get the CustomAlerts API version.<br>
**Return:**<br>
plugin API version

###### Check if motd message is custom:
```
boolean isMotdCustom()
```
**Description:**<br>
Check if motd message is custom.<br>
**Return:**<br>
*boolean*

###### Get default motd message:
```
string getDefaultMotdMessage()
```
**Description:**<br>
Get default motd message.<br>
**Return:**<br>
*string* the default motd message

###### Get current motd message:
```
string getMotdMessage()
```
**Description:**<br>
Get current motd message.<br>
**Return:**<br>
*string* the current motd message

###### Set current motd message:
```
function setMotdMessage($message)
```
**Description:**<br>
Set current motd message.<br>
**Parameters:**<br>
*$message*

###### Check if outdated client message is custom:
```
boolean isOutdatedClientMessageCustom()
```
**Description:**<br>
Check if outdated client message is custom.<br>
**Return:**<br>
*boolean*

###### Get default outdated client message:
```
string getDefaultOutdatedClientMessage(Player $player)
```
**Description:**<br>
Get default outdated client message.<br>
**Parameters:**<br>
*$player* the current player<br>
**Return:**<br>
*string* the default outdated client message

###### Get current outdated client message:
```
string getOutdatedClientMessage()
```
**Description:**<br>
Get current outdated client message.<br>
**Return:**<br>
*string* the current outdated client message

###### Set current outdated client message:
```
function setOutdatedClientMessage($message)
```
**Description:**<br>
Set current outdated client message.<br>
**Parameters:**<br>
*$message*

###### Check if outdated server message is custom:
```
boolean isOutdatedServerMessageCustom()
```
**Description:**<br>
Check if outdated server message is custom.<br>
**Return:**<br>
*boolean*

###### Get default outdated server message:
```
string getDefaultOutdatedServerMessage(Player $player)
```
**Description:**<br>
Get default outdated server message.<br>
**Parameters:**<br>
*$player* the current player<br>
**Return:**<br>
*string* the default outdated server message

###### Get current outdated server message:
```
string getOutdatedServerMessage()
```
**Description:**<br>
Get current outdated server message.<br>
**Return:**<br>
*string* the current outdated server message

###### Set current outdated server message:
```
function setOutdatedServerMessage($message)
```
**Description:**<br>
Set current outdated server message.<br>
**Parameters:**<br>
*$message*

###### Check if whitelist message is custom:
```
boolean isWhitelistMessageCustom()
```
**Description:**<br>
Check if whitelist message is custom.<br>
**Return:**<br>
*boolean*

###### Get default whitelist message:
```
string getDefaultWhitelistMessage(Player $player)
```
**Description:**<br>
Get default whitelist message.<br>
**Parameters:**<br>
*$player* the current player<br>
**Return:**<br>
*string* the default whitelist message

###### Get current whitelist message:
```
string getWhitelistMessage()
```
**Description:**<br>
Get current whitelist message.<br>
**Return:**<br>
*string* the current whitelist message

###### Set current whitelist message:
```
function setWhitelistMessage($message)
```
**Description:**<br>
Set current whitelist message.<br>
**Parameters:**<br>
*$message*

###### Check if full server message is custom:
```
boolean isFullServerMessageCustom()
```
**Description:**<br>
Check if full server message is custom.<br>
**Return:**<br>
*boolean*

###### Get default full server message:
```
string getDefaultFullServerMessage(Player $player)
```
**Description:**<br>
Get default full server message.<br>
**Parameters:**<br>
*$player* the current player<br>
**Return:**<br>
*string* the default full server message

###### Get current full server message:
```
string getFullServerMessage()
```
**Description:**<br>
Get current full server message.<br>
**Return:**<br>
*string* the current full server message

###### Set current full server message:
```
function setFullServerMessage($message)
```
**Description:**<br>
Set current full server message.<br>
**Parameters:**<br>
*$message*

###### Check if default first join message is enabled:
```
boolean isDefaultFirstJoinMessageEnabled()
```
**Description:**<br>
Check if default first join message is enabled.<br>
**Return:**<br>
*boolean*

###### Get default first join message:
```
string getDefaultFirstJoinMessage(Player $player)
```
**Description:**<br>
Get default first join message.<br>
**Parameters:**<br>
*$player* the current player<br>
**Return:**<br>
*string* the default first join message

###### Check if a player has joined for the first time:
```
boolean hasJoinedFirstTime(Player $player)
```
**Description:**<br>
Check if a player has joined for the first time.<br>
**Parameters:**<br>
*$player*<br>
**Return:**<br>
*boolean*

###### Check if default join message is custom:
```
boolean isDefaultJoinMessageCustom()
```
**Description:**<br>
Check if default join message is custom.<br>
**Return:**<br>
*boolean*

###### Check if default join message is hidden:
```
boolean isDefaultJoinMessageHidden()
```
**Description:**<br>
Check if default join message is hidden.<br>
**Return:**<br>
*boolean*

###### Get default join message:
```
string getDefaultJoinMessage(Player $player)
```
**Description:**<br>
Get default join message.<br>
**Parameters:**<br>
*$player* the current player<br>
**Return:**<br>
*string* the default join message

###### Get current join message:
```
string getJoinMessage()
```
**Description:**<br>
Get current join message.<br>
**Return:**<br>
*string* the current join message

###### Set current join message:
```
function setJoinMessage($message)
```
**Description:**<br>
Set current join message.<br>
**Parameters:**<br>
*$message*

###### Check if default quit message is custom:
```
boolean isDefaultQuitMessageCustom()
```
**Description:**<br>
Check if default quit message is custom.<br>
**Return:**<br>
*boolean*

###### Check if default quit message is hidden:
```
boolean isDefaultQuitMessageHidden()
```
**Description:**<br>
Check if default quit message is hidden.<br>
**Return:**<br>
*boolean*

###### Get default quit message:
```
string getDefaultQuitMessage(Player $player)
```
**Description:**<br>
Get default quit message.<br>
**Parameters:**<br>
*$player* the current player<br>
**Return:**<br>
*string* the default quit message

###### Get current quit message:
```
string getQuitMessage()
```
**Description:**<br>
Get current quit message.<br>
**Return:**<br>
*string* the current quit message

###### Set current quit message:
```
function setQuitMessage($message)
```
**Description:**<br>
Set current quit message.<br>
**Parameters:**<br>
*$message*

###### Check if default world change message is enabled:
```
boolean isDefaultWorldChangeMessageEnabled()
```
**Description:**<br>
Check if default world change message is enabled.<br>
**Return:**<br>
*boolean*

###### Get default world change message:
```
string getDefaultWorldChangeMessage(Player $player, Level $origin, Level $target)
```
**Description:**<br>
Get default world change message.<br>
**Parameters:**<br>
*$player* the current player<br>
*$origin* the origin level<br>
*$target* the target level<br>
**Return:**<br>
*string* the default world change message

###### Get current world change message:
```
string getWorldChangeMessage()
```
**Description:**<br>
Get current world change message.<br>
**Return:**<br>
*string* the current world change message

###### Set current world change message:
```
function setWorldChangeMessage($message)
```
**Description:**<br>
Set current world change message.<br>
**Parameters:**<br>
*$message*

###### Check if default death messages are custom:
```
boolean isDefaultDeathMessageCustom($cause = null)
```
**Description:**<br>
Check if default death messages are custom.<br>
**Parameters:**<br>
*$cause* Check message by cause<br>
**Return:**<br>
*boolean*

###### Check if default death messages are hidden:
```
boolean isDefaultDeathMessageHidden($cause = null)
```
**Description:**<br>
Check if default death messages are hidden<br>
**Parameters:**<br>
*$cause* Check message by cause<br>
**Return:**<br>
*boolean*

###### Get default death message related to the specified cause:
```
string getDefaultDeathMessage(Player $player, $cause = null)
```
**Description:**<br>
Get default death message related to the specified cause.<br>
**Parameters:**<br>
*$player* the current player<br>
*$cause* the cause of death (instanceof EntityDamageEvent). If it's null, the function will return the default death message
**Return:**<br>
*string* the default death message related to the specified cause

###### Get current death message:
```
string getDeathMessage()
```
**Description:**<br>
Get current death message.<br>
**Return:**<br>
*string* the current death message

###### Set current death message:
```
function setDeathMessage($message)
```
**Description:**<br>
Set current death message.<br>
**Parameters:**<br>
*$message*
