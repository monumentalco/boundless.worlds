# World Colors

The WorldColor Nodes define recipes for the a world to select its block colours. The block colours are indexed into a set of universal BlockColor Palettes. The world hence picks an index per block type.

World Level is indexed from 1 to 8 in game.
The configuration files are indexed from 0 to 7.

All the WorldColor configs follow a similar strategy of defining a shared hierarchy of colours based on a top level collection of base colours.

* Base Seed - the base hue for the world.
  * Veg-Solid Root - a variation for saturation and luminance.
    * Vegetation Root - a variation for all soft vegetation: Foliage, Grass, Growth, Tangle, Thorns, Plants, Flowers.
    * Solid Root - a variation for all solid vegetation: Wood, Ash.
      * The following are a combination of Vegetation and Solid: Soil, Mould, Mud, Fungus.
  * Min-Liq Root - a variation for saturation and luminance.
    * Liquid Root - a variation for liquid derived materials: Ice, Glacier, Sponge.
    * Mineral Root - a variation for mineral derived materials: Rock, Gravel.
      * Gleam - a variation for: Gleam
* Sand Base - a root for sand and a combination with rock: Sand, Alt Planets.


There is a recipe per world configuration:

Lush Worlds:

* lush-0 - Lush Level 1
* lush-1 - Lush Level 2
* lush-2 - Lush Level 3
* lush-3 - Lush Level 4

### Coal Worlds:

Reducing Luminance
SVML = Solid [-50,-40,-30,-20], Vegetation, Mineral [50,40,30,20], Liquid [100,80,60,40] 

* coal-2 - Coal Level 3 :: 0#Base[], 2#veg[lum+15], 3#solid[hue-50,lum+15], 5#liquid[hue+100,lum+15], 6#mineral[hue+50,lum-15]
* coal-3 - Coal Level 4 :: 0#Base[], 2#veg[lum+15], 3#solid[hue-40,lum-15], 5#liquid[hue+80, lum+15], 6#mineral[hue+40,lum-15]
* coal-4 - Coal Level 5 :: 0#Base[], 2#veg[lum-15], 3#solid[hue-30,lum-15], 5#liquid[hue+60, lum+15], 6#mineral[hue+30,lum-15]
* coal-5 - Coal Level 6 :: 0#Base[], 2#veg[lum-15], 3#solid[hue-20,lum-15], 5#liquid[hue+40, lum-15], 6#mineral[hue+20,lum-15]

### Metal Worlds:

Reduced Saturation
VSxLM = Vegetation, Solid [50,40,30,20], Liquid [180], Minerals[180-50,180-40,180-30,180-20]

* metal-2 - Metal Level 3 :: 0#Base[sat-20], 2#veg[], 3#solid[hue+50], 4#MinLiq[hue+180], 5#liquid[], 6#mineral[hue-50]
* metal-3 - Metal Level 4 :: 0#Base[sat-20], 2#veg[], 3#solid[hue+40], 4#MinLiq[hue+180], 5#liquid[], 6#mineral[hue-40]
* metal-4 - Metal Level 5 :: 0#Base[sat-20], 2#veg[], 3#solid[hue+30], 4#MinLiq[hue+180], 5#liquid[], 6#mineral[hue-30]
* metal-5 - Metal Level 6 :: 0#Base[sat-20], 2#veg[], 3#solid[hue+20], 4#MinLiq[hue+180], 5#liquid[], 6#mineral[hue-20]

### Gem Element Worlds:

Reduced Luminance
LMVS = Liquid[-20], Mineral[-10], Vegetation, Solid[10]

* gem-4 - Gem Element Level 5 :: 0#Base[lum-10], 2#veg[], 3#solid[hue+10], 5#liquid[hue-20], 6#mineral[hue-10]

Increased Luminance
SVML = Solid[-10], Vegetation, Mineral[10], Liquid[10]

* gem-5 - Gem Element Level 6 :: 0#Base[lum+10], 2#veg[], 3#solid[hue-10], 5#liquid[hue+20], 6#mineral[hue+10]

#### Special Element Worlds:

Umbris - Reduced Luminance, Warm Vegetation, Hue [Orange-Red]
Blink - Increased Luminance, Cold Vegetation, Hue [Green-Yellow]
Rift - Split Hue [Pink-Purple] 

* special-6 - Special Element Level 7
* special-7 - Special Element Level 8