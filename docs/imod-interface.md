---
id: imod-interface
title: The IMod Interface
sidebar_label: IMod Interface
---


IMod Interface
--------------
The IMod interface can be found in`(Game Directory)/Parkitect_Data/Managed/Assembly-CSharp.dll` and looks roughly like this:


``` cs
/// <summary>
///     An interface for user made mods.
/// </summary>
public interface IMod
{
    /// <summary>
    ///     Called to indicate this instance should load its logic.
    ///     This method is called during the loading routine of a savegame or a fresh game.
    /// </summary>
    void onEnabled();

    /// <summary>
    ///     Called to indicate this instance should unload its logic.
    ///     This method is called before the game quits.
    /// </summary>
    void onDisabled();

    /// <summary>
    ///     Gets the name of this instance.
    /// </summary>
    string Name { get; }

    /// <summary>
    ///     Gets the description of this instance.
    /// </summary>
    string Description { get; }

    /// <summary>
    ///     Gets an unique identifier of this mod.
    /// <summary>
    string Identifier{ get; }
}
```
