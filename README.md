# UnityGOTiles
After reading countless reddit and stackoverflow posts about how using gameobjects as tiles is a bad idea because instantiation causes performance issues
and after trying and failing to implement gameobjects as tiles for a procedurally generated system, i've finally came up with a solution that is
kind of decent. And as much a big part of me wants to horde this sacred knowledge, i thought i'd go ahead and share my work in the hopes that it will
help someone else who is stuck in a similar situation that i have been in FOR MONTHS!!!

The system uses perlin noise to generate the terrain/floor as chunks of separate Tiles.
Each tile has flags that indicate if that particular tile is being rendered etc. 
the terrain system currently supports Grass, Dirt, "Water", rocks, and trees.

This is the first release of this system, i will be updating this repository with any updates i make to the system such as supporting more procedurally
generated objects.

You can adjust the amount of regions that are loaded, the chunks that are loaded, and the distance from a tile you have to be to make the tile "reset" itself
and add itself to a pool to be reused, if the unload distance is too low the chunks you're moving towards won't load (as the unloader unloads them before they
have chance to spawn).

I was originally using cubes for the "floor" but decided to generate just the top plain of a cube for performance reasons.
The system can load a pretty insane amount of tiles before it starts slowing down. i've found 1000-2000 GameObjects is the limit for this system at the moment.

I need to clean up the MapManager and break a lot of the code out into separate classes, so if you fancy doing that before i have chance to feel free to help out.

This project is mainly for my own personal entertainment so updates will be irregular, when i fancy working on it really. 

I hope this helps you out, because i know the struggle of trying to get a tiled gameobject system working FAR too well... and i've spent WAY too much time figuring it out.

Enjoy!
