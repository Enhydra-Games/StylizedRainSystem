# A configurable rain system for Unreal Engine 

Stylized Rain System is an Unreal Engine plugin that provides a system for efficiently implementing rain into a scene. 
With the rain system, rain is only activated around the player, saving on performance - especially when using rain with enabled collision, as it can become quite expensive when covering too large of an area.

## BP_RainZone
<img width="1260" height="740" alt="grafik" src="https://github.com/user-attachments/assets/a1b69431-2c9c-4f80-8136-b956780406f3" />

Make sure the inner boxes of neighboring Rain Zones touch each other, or gaps in the rain will appear.

<img width="1919" height="1136" alt="Screenshot 2026-05-07 150210" src="https://github.com/user-attachments/assets/2df46177-5b2e-42ac-b14e-ec95029a66c7" />

### Variables
- RainSizeX and RainSizeY: Control the size
- ShowBounds: Show bounds in game
- The other public variables are set automatically, but public for easier debugging.

<img width="273" height="221" alt="grafik" src="https://github.com/user-attachments/assets/6de32a49-c570-49e0-b272-e90eb1d6bd30" />

See the in engine tooltips for more detailed info.

### Tipps
- You can add a custom collision layer for the outher boxes in the Rain Zones, but make sure they are set to overlap with only the new layer you created.


## BP_RainManager

### Variables

RainTime, RainProbability, RainAmount, RainIntensity and RainVFX configure the values and visuals for all Rain Zones.

<img width="273" height="221" alt="grafik" src="https://github.com/user-attachments/assets/abaea2ff-cc70-4163-ad3f-b40078aaad9e" />

See the in engine tooltips for more detailed info.

### Tipps
- The rain probability is checked every time the player enters a Rain Zone.
- You can check the RainZones array to see, if all Rain Zones are registered correctly.

## Usage Notes

- Make sure the scene includes a Rain Manager.
- Add as many Rain Zones as needed, the inner, thicker boxes should be right next to each other, the outher boxes should overlap.
- Adjust the Rain Zone size by adjusting the RainSizeX and RainSizeY variables.
- Bigger Rain Zones have smoother transitions, but cost more performance since more particles are on screen at once.
- The rain system is only intended to be used with a single player.
