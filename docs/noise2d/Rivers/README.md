# Rivers noise2d

![Hero Image](./screenshot.jpg)

**Contributors:** Nevir

The rivers heightmap allows you to mix rivers into your biome's terrain.

Also see the [Rivers - Standard](../RiversStandard) noise for a version of this 2d noise function configured with common values.

## Configuration

**Function**: The underlying function used to generate rivers. Simplex is used for "Rivers - Standard".

**River Thickness**: Controls how wide the generated rivers are.

**River Distortion**: Controls how much distortion is applied to the rivers (e.g. snakiness).

**River Depth**: Controls the riverbed's y-height.  Positive values lower the riverbed _beyond_ the `minY` of your heightmap.  A river depth of 0.0 means the riverbed should be at exactly your `minY`.  A river depth of 1.0 means the riverbed should be as deep as the biome's heightmap is tall.

**Edge Smoothing**: Controls how smooth/sharp the transition between river and your terrain is.

**Terrain**: This is a heightmap that is used where there are no rivers; your main terrain.

**Riverbed**: A heightmap used for the riverbed.

**Riverbed Scale**: Scales the riverbed heightmap vertically.
