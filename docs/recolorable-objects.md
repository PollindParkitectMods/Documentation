---
id: recolorable-objects
title: Recolorable Objects
sidebar_label: Recolorable Objects
---

Introduction
------------
Scenery that you made can be recolored just like the in-game items that are recolorable.

Requirements
------------
- Modeling
- [This](https://github.com/ParkitectNexus/CustomSceneryModTemplate/raw/master/256palette.tga) texture
- UV Mapping skills

Texuring
--------
When you've made your model, use the texture you just downloaded to map the colors to your model. The texure to use is the 256palette.tga in the mod template, it looks like this: 

![3200 zoomed in](http://i.imgur.com/Q1SSCiJ.png)

It's best for the performance that you use these colors ingame, as the engine can batch draw the textures. In the bottom right of the texture you see 4 special colors. Those are the pixels you can map that are recolored in-game. The pixels are in the following order:

    Indigo, Blue,
    Green, Red

    Color 4 Color 3
    Color 2 Color 1

For example, the slanted wooden support will be fully recolorable. Thus we will set all UVs to the red pixel on the bottom right corner like in the following image. Yes, UVs will be very compressed, but because of Parkitect's art design, it won't matter.

![UVsExample](http://i.imgur.com/BhTducf.png)

If you don't know how to map UV's, please search tutorials for your own modeling program. Thanks to Kenney, there is now an easy way to map UV's in Sketchup, read [this tutorial](Recoloring-in-sketchup).

Next we have to configure the [scenery.json](configuring-scenery.json) file to add in the custom colors. Because we used the red pixel, we need to use "color 1" on the json file. For the model, it ended up like the following

    {
      "Diagonal Support": {
        "model": "SM_SlantedSupport",
        "type": "deco",
        "price": 5.0,
        "recolorable": true,
        "recolorableOptions": {
          "color1": "#471f00"
        }
      }
    }

The hexadecimal number is the default color for the game when you open the color picker. In my case '#471f00' is brown, **the # in front of it is required**. You can see the hexadecimal code using the in-game color picker. Then edit the json file and hot-reload it using CTRL - R.

Finished
--------
Now you have custom colors for your models! Congratulations!
![Done!](http://i.imgur.com/A0OGysD.png)
