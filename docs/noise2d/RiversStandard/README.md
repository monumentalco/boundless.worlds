# Rivers noise2d

![Hero Image](../Rivers/screenshot.jpg)

**Contributors:** Nevir

The rivers heightmap allows you to mix rivers into your biome's terrain.

Also see the [Rivers](../RiversStandard) noise for the advanced version of this noise function that exposes more configuration options.

## Configuration

**Terrain**: This is a heightmap that is used where there are no rivers; your main terrain.

**River Depth**: Controls the riverbed's y-height.  Positive values lower the riverbed _beyond_ the `minY` of your heightmap.  A river depth of 0.0 means the riverbed should be at exactly your `minY`.  A river depth of 1.0 means the riverbed should be as deep as the biome's heightmap is tall.

**River Thickness**: Controls how wide the generated rivers are.

**Edge Smoothing**: Controls how smooth/sharp the transition between river and your terrain is.
