---
id: asset-bundle
title: Asset Bundles
sidebar_label: Models and Assets
---

Some mods requires custom models, that's no problem! You can use Asset Bundles to load custom models and other assets (everything except code). See the Unity tutorial on how to create/use Asset Bundles, [click](http://docs.unity3d.com/500/Documentation/Manual/BuildingAssetBundles5x.html).

When you've made your asset bundles you can include them in your mod. Create a subfolder in your mod 'Asset Bundles'. Now head over to your mod.json and configure it, set AssetBundleDir to 'Asset Bundles' and AssetBundlePrefix to a prefix of your liking. Now when you restart the game, the client will copy all your asset bundles to `(Parkitect folder)/Parkitect_Data/StreamingAssets/mods/(your asset bundle prefix)`. You can reach your asset bundles with the following piece on the following path:

    Application.streamingAssetsPath + '/mods/your-prefix/your-asset-bundle-file'

An example to load a custom model:

``` c#
    using UnityEngine;

    namespace PandaEntertainer
    {
        public class AssetBundleManager
        {
            public readonly GameObject One;
            public readonly GameObject Two;

            public AssetBundleManager(Main main)
            {
                var dsc = System.IO.Path.DirectorySeparatorChar;
                var assetBundle = AssetBundle.LoadFromFile(main.Path + dsc + "assetbundle" + dsc + "assetpack");

                One = assetBundle.LoadAsset<GameObject>("1");
                Two = assetBundle.LoadAsset<GameObject>("2");
                assetBundle.Unload(false);
            }
        }
    }
```