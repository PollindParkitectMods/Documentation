---
id: asset-bundle-for-beginner
title: Asset Bundle For Beginners
sidebar_label: Asset Bundle For Beginners
---

Introduction
--------------
Asset bundles are unity's way of providing game assets to the game after a game has been released. It's meant for DLC or expansion packs. But that can be used for modding also!

Requirements
------------
- 3D Models
- Unity 5+
- Default unity layout is recommended for this tutorial.

How To
------
Create (or open) a new default 3d project in Unity. Drag your models into the asset folder (found in the project tab, bottom left). Right click on the asset folder > create > C# Script and call it AssetBundleExporter. Double click that file, now monodevelop or visual studio will open.

Replace the contents with the following script:

``` cs
using UnityEditor;

public class AssetBundleExporter
{
    [MenuItem("Assets/Build AssetBundles")]
    static void BuildAllAssetBundles()
    {
        BuildPipeline.BuildAssetBundles("./");
    }
}
```

Save the file and close MonoDevelop or Visual Studio.

Now select **all** the models that you want to include in an asset bundle. In the inspector on the bottom right side of your screen there is an Asset Labels section. Open the dropdown and click on new, enter your assetbundle name. **If you're following this tutorial for the custom scenery, the name must be 'scenery'.**

Now go in the top menu to Assets > Build AssetBundles. This can take from a few seconds to minutes, depending on how much models you have included.

When it's done building, the asset bundles can be found in the root of your unity project folder. If you follow this tutorial for the custom scenery, make sure you copy scenery and scenery.manifest.