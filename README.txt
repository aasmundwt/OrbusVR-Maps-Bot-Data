# OrbusVR-Maps-Bot-Data
This contains a collection of maps that show the location of most, if not all objects in OrbusVR:Reborn and is primarilly used by the OrbusVR Maps discord bot.
There are also full detailed maps, and some config files.

Config Files
SearchItems.json contains a complete directory of the location maps;
 SearchTerm, is what I use to search ond sort the objects in the maps bot.
 Description, is a full description for displaying
 Zone, is the zone the object is in
 Type, is whatever category the object falls under on the interactive map
 NearestTeleport, is the closest teleport to the object
 Emoji, is the Discord Emoji ID for the objects icon, these are in private servers
 Path, is the local repository path to the map of that object

StaticMaps.json is a directory of the static maps;
  Name, is the name of the map
  Emoji, is the Discord Emoji ID for the maps icon, this is in a private server
  Link, is the local repository path to the map
 
BountyMaps.json is a directory for the bounty maps
  MapZones, is a collection of the different zones and contains all the bounty maps
    Zone, is the name of the zone
    Emoji, is the discord emoji ID for that zone
    PathGameMaps, is the local repo path to an overview map of all the in-game bounty maps of the zone
    Maps, contains all the maps separately, the order is the same as in the PathGameMaps image
      NearestTeleport, is the closest teleport pillar to the bounty map
      PathMap, is the local repo path to the larger map that clearly shows the location of the map
      PathGameMap, is the local repo path to the smaller in-game map
  Emoji, is the discord emoji id for the bounty map icon

FishTimes.json contains all collected pond and time info on legendary fish
  StartReferenceTime, is the start time for the flounder rotations
  PondMapPath, is the local repo path to an overview image of the different fishing ponds
  AllFishTimes, contains all the different times that fish spawn in the different ponds
    Fish, is the "ID" of the fish, 0 is blimp, 1 is kylakin, 2 is frosted perch, 3 is jelmiry and 4 is flounder, honestly not sure why i have this.
    Lure, is the lure required to catch the fish
      Name, is the name of the lure component
      Emoji, is the discord emoji id of that lure component
    Emoji, is the discord emoji id for the fish
    Times, is a collection of spawn times for the fish
      SpawnTimes, is a 2d array that contains all info on when they spawn. each sub-array is a day and each number is a 5/4 hour period where every 15 min is represented by a bit where true means the fish is active and false means it's not active. If you want more details, message @aasmundwt on discord
      Zones, is all the zones the ponds the fish will appear in during this spawn
      Requirements, is the weather requirements for this spawn time
        Name, is just a description of the requirements
        Emoji, is the discord emoji id for the requirement graphic
      ReqAND, specifies wether all the requirements must be met, or just one of them
