# roomulon_1.1.5
text-based roguelike adventure


This is a working version of roomulon, playable at agbwebdesigns.com/roomulon_1.1.5/index.html

It has a few bugs:
-Some of the direction tiles display a black screen or display the wrong tile.  The directions being shown in the text when clicking "look" are always correct
-Occassionally if you play long enough a baddie might wander away in the middle of combat, possibly trapping you in combat without a baddie and breaking the game
-Sometimes the first room will load only one door and the connecting room also only creates one door back to the previous room.  Try resetting the game until you get a getter map.
-The game is also limited in what you can do.  There is a knife you can pick up and equip in the first room and medpacks throughout the game that you can use to heal yourself.  You can run around revealing rooms and killing the baddies that pop up in each room.  You will collect gold by killing them.  The hero will level up based on attacking and defending and you might reach a point where the baddies can no longer kill you.  This is effectively the end of the game.

I'm working on the next version and refactoring this into a more manageable game so I'm not going to work on this version anymore.

Key:
  //- to do
  //  complete
  
//-future upgrades to the room creator
//-different sized rooms
//-there can be an object for each sized room as well
//-multiple floors
//-a different floor array for each floor
//-which floor array you are accessing will determine which floor you are on
//-different sized maps
//-a journal for keeping notes about different rooms
//-finding a staircase that leads to another floor
//-there can be an object for the overall game that creates the first floor
//-each game and each floor and each room can all be their own objects
//-the game object will hold all of the directions and commands as well as the objects for everything else
//baddies that randomly are created and show up in the room that you are in
//an object for each different kind of baddie
//-a way to keep notes on different rooms to remember which is which
//a way to travel between rooms
//-or at least a way to see the path that needs to be travelled on the map
//create an object for the hero
//must include: hit points, giving damage unarmed, the ability to take damaged
//-addons for later: armor worn on the body, rings to buff, damage armed, the ability to equip weapons, each weapon should be its own object, the ability to lvl up
//need a display for hero stats and equipment
//-baddies
//-large scorpion - if you get stung by a large scorpion the venom will poison you and drain your health by 1hp per minute
//-small scorpion - these are more dangerous than the large ones, if you get stung by a large scorpion the venom will poison you and drain your health by 10hp per minute, also you don't get hit for as much during the attach but, the venom is more poisonous.
//-reset game button
//-stop combat button
//if a baddie is created and you are not in the room then it should start to wander around the map and you will be notified when you enter a room with a baddie or if a baddie enters a room that you are in
//if a baddie walks into a room that you are in then combat needs to be started
//-as you level up, the baddies get tougher, they level up too, or higher level baddies are created
//-does the player need to lvl up or will the baddie spawn at higher lvls based on player skill?
//-as your lvl of skill increases baddies will spawn based on those lvl increases
//-have different baddies spawn based on which skills are leveling up
//-if you make a lot of noise while walking around the different rooms and killing the baddies then then baddies in the other rooms will hear you and walk towards you and come into the room you are in and attack you
//-sneaking skill
//-baddies need the ability to hear you
//tracking all of the baddies running around and knowing where they are doesn't matter
//-there needs to be a check when in combat and trying to click the direcion buttons to see if an escape is possible
//-as you walk into a new room the next text message after, ex. ('you travel north'), should be, ("you have entered a new room") or ("you enter a new area"), if you are entering a new room but, not if you enter a room that already exists
//-create a new combat engine
//-this governs combat between the hero and the baddie
//-right now this is part of the player object

//-stats at the end of the game
//how many rooms created
//-how many baddies created/defeated
//-how long the game lasted

//-add doors to the game
//-as each new room is created the directions available can also randomly have a door or not and it can be locked or not
//-having a locked door could indicate that there is something of value behind the door, weapon, armor, etc.
//-lockpicking skill
//-booby traps
//-disarm skill
//-chests with things to use throughout the game
//-need an inventory
//-weapons
//-potions
//-locked chests
//-lockpicking skill
//-boobie traps that destroy contents inside if a fail to disarm happens
//-disarm skill
//-the ability to smash the lock and open it with force
//-merchants that travel throughout the game that you can run into and trade with

//- baddies have a main baddie that spawn the rest of the baddies
//-rats have a rat king, spiders have a spider queen, slimes have a great slime, snakes have a cobra king, zombies have a necromancer, etc.
//-you have to fight each one differently
//-there are only rats in the rat quest, spiders in the spider quest etc, ending in the boss

//the ability to pick up weapons, a knife or a pipe
//maybe don't change the chance of a baddie being spawned but, add a weapon to see how this changes the balance
//the weapon will need to be added to inventory
//need the ability to equip the weapon from the inventory
//the weapon gives an extra die roll
//a look button to see if and how many baddies there are in a room
//a search room ability to see what is in the room

//-weapon
//the weapon needs to be an object with only one attribute, how many dice rolls to add to the weapon bonus
//then i need a way to read how many dice rolls and add that to augment the player
//need a way to equip the weapon
//the weapon should move from inventory to equiped, or show that it is equiped in inventory

//-container
//the weapon needs to be spawned by a container, which is spawned by the room
//it should be kept in a container until retrieved by the hero
//the hero needs to see the container
//open the container
//look into the container
//take items out of the container
//transfer the items to the players inventory
//put them into inventory of the player
//-possibly equip items from the container
//a container object needs an array to keep its objects in
//it also needs a function to create its contents, randomly or otherwise
//the container needs to only be created in the first room and the first room shouldn't create a baddie
//need the container to create healthpacks too
//one use item
//needs to disappear when used / counter decrements upon use
//need a way to use the healthpack
//the heal button should have an indicator for how many uses the player has depending on how many health packs have been picked up
//pick up the health pack
//it gets added to inventory
//-the health pack use indicator increments by 1 and allows you to use the heal button
//otherwise you get a message saying that you have no health packs
//-when you use the health pack the indicator decrements by 1
//the health pack is removed from inventory

//-when combat starts a new window opens that is the combat window
//-maybe an overlay window
//-combat can commence from there
//-a picture/image of the baddie being faught
//-take turns doing combat, heal, run or whathaveyou
//-the baddie could have a chance at running too
//-if they are successful they run off but, their health doesn't heal and they get a nickname
//-if they run into other baddies they embolden them and the other baddies get a buff too
//-if the named baddie gets killed later on their death further emboldens the other baddies and they get another buff
//-there could also be a chance that their death demoralizes the other baddies and they get a negative buff / "lose the will to fight"

//-need to change the text of the hero attack from punch to slice or bash or smash or whatever the case is depending on if attacking unarmed or with a weapon

//-info upon death
//-how many rooms created
//-how many baddies created/killed

//increase the size of the text box and add all text above it to the text box

//the look button
//directions/how many doors
//how many baddies
//any chests

//-change the player cursor to a dot at the center of the screen so the player can see the directions available on the map in the current room
//-right now it is a class that is being applied to the current room that turns the entire room square on the map white
//-it should be a div that is being moved around so that the css only applies to that div

//change the text when fighting baddies and leveling up to only display this information when the player stats are being increased.

//-spawn uber-baddies
//-maybe when you reach a certain level they begin to spawn
//-or maybe random
//-maybe a random baddie generator that creates baddies and randomly increases the badness of the baddie

//-have the baddies drop gold when they are killed that the hero can collect
//-create a shopkeeper that gets randomly created that you can spend the gold with
//-he will have health packs, maps of the area, weapons, armor, etc.

//-fix the map creating rooms past the boundaries of the map, it should not do this

//-there needs to be a counter for how many available direction of travel there are on the map at one time
//-when a new room is created, the counter needs to increment by the number of available directions in the new room
//-the counter needs to decrement by 1 whenever a new room is entered
//-there should be a 10% chance that a staircase can be created in a new room
//-if the counter drops to 0, you are in the final room that can be created and no new rooms can be made
//-in this last room, if the staircase hasn't been created, it needs to be created here

//-stairs to another level
//-get the staircase working in the first room again like the chest
//-the staircase is really just a way to create a new map
//-then get it to randmonly appear in a room

//-need the ability to level up the health, attack and defense power
//-mobile first
