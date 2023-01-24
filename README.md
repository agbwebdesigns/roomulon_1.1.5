# roomulon_1.1.5
text-based roguelike adventure


This is a working version of roomulon, playable at agbwebdesigns.com/roomulon_1.1.5/index.html

It has a few bugs:
-Some of the direction tiles display a black screen or display the wrong tile.  The directions being shown in the text when clicking "look" are always correct
-Occassionally if you play long enough a baddie might wander away in the middle of combat, possibly trapping you in combat without a baddie and breaking the game
-Sometimes the first room will load only one door and the connecting room also only creates one door back to the previous room.  Try resetting the game until you get a getter map.
-The game is also limited in what you can do.  There is a knife you can pick up and equip in the first room and medpacks throughout the game that you can use to heal yourself.  You can run around revealing rooms and killing the baddies that pop up in each room.  You will collect gold by killing them.  The hero will level up based on attacking and defending and you might reach a point where the baddies can no longer kill you.  This is effectively the end of the game.

I'm working on the next version and refactoring this into a more manageable game so I'm not going to work on this version anymore.
