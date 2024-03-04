# Terrarum

The project is hosted on [This repository](https://github.com/curioustorvald/Terrarum), this repo is just a loose recording of the development progress.

____

### 2015-12-31

The project, Terrarum (or Terrarum-renewed) started. (yes, there exists the even older version. In fact, this is 3rd iteration)

### 2016-02-05

First git commit.

### 2016-02-06

Tiles look connected when they are rendered.

____

*there's too much old commits, I won't put them here. Ah, one important commit:*

### 2016-10-23

![201671023 — Cylindrical world.](roundworld_tapestry.png)

A feature called Roundworld has implemented. The world is now topologicaly cylindrical, where eastern end of the world meets the western end, creating a loop along the X-axis.

____

### 2017-03-01

I'm on GPL bandwagon now!

### 2017-03-03

I'm on Git LFS bandwagon now!

### 2017-04-18

First implementation of the pickaxe.

### 2017-04-19

Large textures are getting GZipped.

### 2017-04-28

Quickslot re-implemented. This gets broken again in the future, when I moved from Slick2D to LibGDX, and not getting fixed because of its low prority.

### 2017-06-02

Blocks that are exposed to the light are drawn brighter than their actual light level, this improves aesthetics and playability. (looks prettier and ground more recognisable)

### 2017-06-22

I'm on LibGDX bandwagon now!

### 2017-07-05

![20170705 — Smooth lighting is achieved by a shader. Torch casts realistic orange colour, which is based on colourimeter measurement. You'll be seeing more things with accurate colours like this one in the future.](screenshot_01.png)

Smooth lighting is achieved by a shader. Torch (it's not a candle!) casts realistic orange colour, which is based on my own colourimeter measurement. You'll be seeing more things with life-like colours such as this one in the future.

In the actual game, the torch flickers (gets brighter and darker) randomly, which mimics real-life fire.

### 2017-07-16

Skybox is dithered by the shader to remove banding artefacts.

### 2017-07-20

Vertical parallax scrolling (sky looks bluer as you go up)

### 2017-07-26

![20170726 — The titlescreen.](titlescreen_koKR.png)

The titlescreen. This shows the main principal of the design — the minimalism. Fraps was open while taking the screenshot.

### 2017-11-07

![20171107 — The inventory.](inventory_peek2.png)

One of the proposed inventory screen. May undergo some changes. 

### 2018-05-09

The inventory UI now scrolls.

### 2018-06-21

In-game features are now modularised: The base code (engine) and Module BaseGame. More modules will come.

### 2018-06-30

New set of renderers I call IngameRenderer is finally built and it's working.

### 2018-07-03

Postprocessor on the rendering engine.

### 2018-08-15

Experiments of parametric skybox model according to the paper *A Practical Analytic Model for Daylight*. Actual implementation has not been conducted.

### 2018-08-30

The titlescreen menus (called RemoCon) reworked, they're now more easily expandable.

### 2018-09-16

RNG is now serialisable (for saving/loading world). In-game font got its update

### 2018-10-09

Been testing with the world save/load and got them partially working.

### 2018-10-27

Xoroshiro RNG for everything, including the game's custom build Joise noise library.

### 2018-11-06

Established solid in-game calendar, 4 season-months, 120 days total, influenced from The World Calendar.

### 2018-11-10

Tile breakage now properly displays with the tiling shader.

### 2018-12-02

I'm on Gradle bandwagon now!

### 2018-12-08

Long-dreaded memory leak bug was caught. It's me not disposing 'temporary' GDX textures.

### 2018-12-29

Water now flows, thanks to [this article](https://w-shadow.com/blog/2009/09/01/simple-fluid-simulation/). Added the fluid layer. Removed water marker block.

### 2018-12-31

Platforms are implemented. (if you don't know what platform is, go play some Terraria, it's a great game)

### 2019-01-03

CSV editor was made

### 2019-01-04

Rudimentary sprite walk cycle

### 2019-01-07

![20190107 — The sprite assembler.](sprite_assembler.png)

The first output of Sprite Assembling: sprites can be assembled from bodyparts and Animation Description Language, using Skeletons and Transforms.

Still have more features to be implemented, but the most crucial parts are working as intended.

### 2019-01-15

Semitransparent-texture-on-semitransparent now renders correctly (e.g. Crude Glass will no longer render "cloudy with sky blue"), thanks to the new GDX version and my improved understanding on alpha; This game now strictly uses "Premultiplied Alpha", and PSD-to-TGA conversion script is also included (dependency: ImageMagick, Windows)

### 2019-02-18

More work on the ingame BuildingMaker

### 2019-03-03

Pre-built tile atlas no longer needed: just make sheet for individual blocks and the game will stitch them together. Blocks can now have all available connecting variations. 47 distinct tiles to cover all 256 possible cases.

### 2019-03-10

First working minimap. Colour is pulled from the tile atlas. Updates every 0.5 seconds

### 2019-05-04

New world system to "actually" support wires. World renderer now draws wires on top of the blocks. You can select which kind of wire to draw.

### 2019-05-30

First working implementation of Fixtures (they spawn and emit lights). Actors won't disappear when the camera wraps around.

### 2019-06-25

Major improvements over the world accessing (pretty much most of the code depend on it) using ```sun.misc.Unsafe```, formely a 60 fps game now runs 100 fps.

### 2019-06-25

Fallable blocks (e.g. sands) now falls, scaffoldings doesn't get "supports" as the feature is TODO.

### 2019-08-13

The camera will zoom-in/out when you hit the 'Z' key

### 2019-08-15

Implementation of the "air jumping"

### 2019-11-27

World generation now runs multithreaded

### 2020-02-24

[![.](https://img.youtube.com/vi/k1y3cRy7feU/0.jpg)](https://www.youtube.com/watch?v=k1y3cRy7feU)

Torches now flicker randomly

### 2020-11-10

Faster light simulation

### 2020-11-21

Finally fixing the long-existing bug where certain window size may crash the game

### 2021-02-25

Block/Item/etc. IDs are now strings instead of integers

### 2021-07-27

LibGDX upgraded to 1.10/LWJGL 3

### 2021-07-28

![.](Screenshot_20210728_215435.png)

Layer between wall and terrain now has a shadow

### 2021-08-18

![.](Screenshot_20210813_142413.png)

Signal wires

### 2021-08-20

[![.](https://img.youtube.com/vi/ouabzMAeXJU/0.jpg)](https://www.youtube.com/watch?v=ouabzMAeXJU)

Actors will climb gradual slope as a staircase if they are tall enough

### 2021-10-14

Save and load using the proprietary archival format

### 2021-10-23

![.](FCWaCLdUUAMMBXz.jpg)

Multilingual input IME

### 2021-11-17

Added various keyboard layouts/IMEs

### 2021-12-22

Player/Actor head is added to the minimap to indicate where they are

### 2022-01-24

Terrarum 0.3 is released

### 2022-02-03

![.](light_withblur.png)

Dual Kawase blur for lightmap

### 2022-02-10

Terrarum 0.3.1 is released

### 2022-02-24

![.](FMWX3ubVQAEOnU4.jpg)

Actors can block the light

### 2022-03-10

![.](Screenshot_20231222_172106.png)

Crafting system is added

### 2022-06-13

Press 'Z' to zoom in/out added

### 2022-06-29

![.](FWaFLq7akAEZU42.jpg)

The reworked crafting UI

### 2022-07-13

![.](FXjAcTYaIAAE1sW.jpg)

Player can direct the wire connection whereever they want

### 2022-07-28

![.](FYwoFMcacAAoBE0.jpg)

Doors are added

### 2022-09-11

![.](https://video.twimg.com/tweet_video/FcXlUwtaMAAOgoP.mp4)

Doors now block lights when closed

### 2022-10-15

Rudimentary FPS benchmarking is added

### 2022-12-29

LibGDX upgraded to 1.11

### 2023-02-28

Updated the shaders to meet OpenGL 3.2 standard

### 2023-04-12

BlockStats is upgraded to TileSurvey

### 2023-05-28

A world portal that allows the player to venture into the multiverse

### 2023-06-06

A new format for item spritesheet

### 2023-06-22

A headless bootstrapper now handles the launching of the game, with user-defineable max JVM heap size and JVM arguments

### 2023-07-05

completely rewritten avatar and world loading UI with rename and delete

### 2023-07-21

![.](Screenshot_20230721_202145.png)

Bilinear and Hq2x filtering mode

### 2023-08-02

![.](Screenshot-1690970042656.png)

First stars on the night sky

### 2023-08-05

Terrarum 0.3.2 is released

### 2023-08-21

![.](Screenshot-1692629666414.png)

First clouds on the sky

### 2023-08-30

True weather system is added

### 2023-09-06

![.](Screenshot-1693927747990.png)

Sledgehammers are added

### 2023-09-07

![.](Screenshot_20230907_121013.png)

Six ecological seasons are implemented for grass textures

### 2023-09-16

![.](Screenshot-1694836434217.png)

Fast random grass spreading simulation

### 2023-09-20

A workbench, the first fixture with a Crafting Station attribute, is added

### 2023-10-03

![.](Screenshot-1696329852358_2.png)

Can throw an holding item

### 2023-10-05

LibGDX upgraded to 1.12

### 2023-10-06

![.](terrarum_0.3.3_day_night_cycle.jpg)

Terrarum 0.3.3 is released with a completely re-worked skybox model

### 2023-10-10

![.](Screenshot-1696936085940.png)

The ore layer is added

### 2023-10-14

![.](Screenshot-1697288319601.png)

Particle effects are added

### 2023-10-23

![.](Screenshot_20231023_225722.png)

A POI editor is added

### 2023-11-04

![.](Screenshot-1699086647328.png)

Tiles are randomly rotated and flipped

### 2023-11-06

![.](Screenshot-1699278280447.png)

More ores are added

### 2023-11-13

Trees are spawned on worldgen

### 2023-11-25

![.](Screenshot-1700048111114.png)

Marble veins are added

### 2023-11-29

![.](Screenshot-1701184076673.png)

The custom audio engine is fully implemented

### 2023-12-01

Footstep and block breaking sound effects are added

### 2023-12-14

Audio resampler is added

### 2023-12-12

![.](Screenshot-1702057524717.png)

Snapshot 23w49a is released

### 2023-12-22

![.](Screenshot_20231222_001039_2.png)

Compression methods for chunks in the savegame can be chosen by the user, Zstd and Snappy is available, deprecating Gzip

### 2024-01-11

Dynamic Source of the audio now tracks the player that changes panning and the lowpass.

### 2024-01-16

Audio engine has reworked so that changing buffer size would not require the game restart

### 2024-01-18

Chunks are only generated near the player

### 2024-01-23

Ambient sounds and codes to playing them has been added

### 2024-01-27

![.](Screenshot-1706293178179.png)

Emissive layer on the sprites. They will glow regardless of the ambient lighting.

### 2024-02-02

![.](Screenshot-1706800998033.png)

New smelter UI is finally working

### 2024-02-14

![.](Screenshot-1707932669060.png)

Explosives!

### 2024-02-19

Terrarum 0.4.0 is released

### 2024-03-03

Terrarum 0.4.1 is released

### 2024-03-04

![.](circuits_1.png)
![.](circuits_2.png)

[Verum-Nimply Logic](https://curioustorvald.github.io/techtales/?a=general_202312190308_verum_nimply_logic) and construction of logic gates
