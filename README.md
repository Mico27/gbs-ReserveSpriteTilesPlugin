# gbs-ReserveSpriteTilesPlugin
GBStudio plugin that allows reserving tiles for actors

In gbstudio, when you change a sprite sheet on an actor using the set sprite sheet event, it will mark the actor to have reserved tile space in the tileset VRAM, that reserved tile space will take the amount of tile equals to the bigger sprite sheet that can be swapped on that actor. 
<img width="693" height="93" alt="image" src="https://github.com/user-attachments/assets/be24621b-3f54-44e6-9cd8-ed41f32e0386" />

However, if you were to use GBVM instead of the event and use VM_ACTOR_SET_SPRITESHEET, GBStudio cannot detect that you are changing the sprite of a specific actor as it only looks for the specific set sprite sheet events to mark an actor to have reserved tiles.
This is a problem as upon changing the spritesheet of an actor that doesnt reserve tiles to fit the changed spritesheet, it will potentialy overwrite other actors tiles.

This plugin allows to reserve tiles for actors without having to use the set sprite sheet event, allowing to then be able to use GBVM or any other method to replace the sprite sheet safely.
The length value of this plugins new event "Reserve sprite tiles" will correspond to the amount of sprites of the bigger spritesheet, just check which in the sprite tab the amount of unique tiles spritesheet have to see what value to use.
<img width="372" height="458" alt="image" src="https://github.com/user-attachments/assets/b3cc04db-5637-4fd8-8258-e503144cace8" />

<img width="684" height="989" alt="image" src="https://github.com/user-attachments/assets/9e42128e-547e-460a-bbec-1aa89e522e55" />

