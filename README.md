# CleanChat
Turtle WoW Chat Addon

# Functions
* Removes [Guild], [Party], [Raid] and [Officer] prefix from chat.
* Abbreviates [Raid Leader] and [Raid Warning].
* Removes channel names 'General', 'Trade', 'LookingForGroup', 'XXXDefense' or replaces with a short prefix.
* Removes custom channel names.
* Colorize chat names.
* Option to activate cursor keys while typing a message (instead of ALT+Cursor keys).
* Option to hide scroll buttons.
* Option to use the mouse wheel to scroll. Hold Shift while scroll up or down and it scrolls immediately to the top or bottom of the chat.
* Option to collect class, level and faction information from random chat people (people not in party / raid / guild / friend list)
* Option to save this information between sessions.
* Option to popup message if it contains your name.
* Clickable URLs. You can click a URL or bind a key to toggle the URL window. The window shows last five URLs and allows you to copy a URL to the clipboard.
* Highlight custom text in chat message (requires to edit a textfile, advanced users only). 

# Turtle WoW stuff
* Option to show players faction in chat

# Commands
Enter <code>/cleanchat</code> or bind a key to show the configuration window. There you can enable/disable the addon functions.

If you choose to enable the option "Show level" and/or "Show faction" and/or "Use class colors" there a few things to note:
* The level and class of your party, raid and guild members as well as friends is always known.
* To show levels, factions and apply class colors to random chat people, you have to allow the addon to use the /who command. If the random is first seen by the addon then it will initiate a /who query, so the second time the random types a message the information can be applied. If a lot of chitchat is going on, the addon can not keep up because a /who command is only allowed every three seconds. But sooner or later the information is gathered. Keep in mind that the level information afterwards will not be updated as long as the random is known by the addon.
* If you save the collected information about randoms and you don't see a name for three days all information about the name will be deleted. The collected information are stored per character.
* If you disable the save option, the name information will be lost after a hour or on logout. 

# Colorize details
Here is a list how the addon decides what color a name gets (read to fully understand colorize options, but not required):
1. If 'classcolors' enabled and the class is known then it uses the Blizzard class colors.
2. Otherwise, it uses the guild color if a guild member and guild color is set.
3. Otherwise, it uses the friend color if a friend and friend color is set.
4. Otherwise, it uses the party color if party member and party color is set.
5. Otherwise, it uses the the raid color if raid member and raid color is set.
6. Otherwise, it uses unknownclass color if 'classcolors' enabled, class is NOT known and unknownclass color is set.
7. Otherwise, it uses grey color if 'classcolors' enabled, class is NOT known and unknownclass color is NOT set.
8. Otherwise, it uses 'others' color if that color is set.
9. Otherwise, it generates a color for that name if enabled.
10. Otherwise, use Blizzard default color.

# Notes / Tips / More details
* If you want just random colors, only enable 'Use colorize names...'.
* If you want one color for all people then set only 'color for others'.
* If a name needs a 'random' color, the addon generates a color based on the hashvalue of the name. This means that a name has always the same 'random' color.
* To highlight custom text in chat messages open 'HighlightConfig.lua'. I prepared a few examples there to get you started. 

