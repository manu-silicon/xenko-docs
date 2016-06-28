# Asset Manager

# Assets

After creating your assets in GameStudio, @'SiliconStudio.Core.Serialization.Assets.AssetManager' is the class responsible for loading, unloading and saving assets.

## Creating

You usually create assets directly in the GameStudio.

Their URL will match the name (including folder) in the GameStudio.

Examples of URLs:

- knight (user imports knight.fbx directly in main asset folder)
- level1/room1 (user creates level1 and import room1.fbx inside)

Please check [HOWTO: Create or import asset data](../../getting-started/howto-create-or-import-asset-data.md) for more details.

## Loading

Loading an asset should be done with the help of @'SiliconStudio.Core.Serialization.Assets.AssetManager' class:

```cs
// Load an asset directly from a file:
var texture = Asset.Load<Texture>("texture1");

// Load a Scene asset
var scene = Asset.Load<Scene>("scenes/scene1");
 
// Load an Entity asset
var entity = Asset.Load<Entity>("entity1");
```


Note that loading an asset that has already been loaded only increment the reference counter and do not reload the asset.

## Unloading

Unloading is also done using the AssetManager class:

```cs
 Asset.Unload(asset);
```


## Asset life time

Asset load and unload are working in pairs. For each call to 'load', a corresponding call to 'unload' is expected. 

An asset is actually loaded only during the first call to 'load'. All subsequent calls only result to an asset reference increment.

An asset is actually unload only when the number of call to unload match the number of call the load.

The @'SiliconStudio.Core.Serialization.Assets.AssetManager.Get' method returns the reference to a loaded asset but does not increment the asset reference counter.

```cs
 var firstReference = Asset.Load<Texture>("MyTexture"); // load the asset and increase the reference counter (ref count = 1)
 
// the texture can be used here
 
var secondReference = Asset.Load<Texture>("MyTexture"); // only increase the reference counter (ref count = 2)
 
// the texture can still be used here
 
Asset.Unload(firstReference); // decrease the reference counter (ref count = 1)
 
// the texture can still be used here
 
Asset.Get<Texture>("MyTexture"); // return the loaded asset without increasing the reference counter (ref count = 1)
 
// the texture can still be used here
Asset.Unload(secondReference); // decrease the reference counter and unload the asset (ref count = 0)
 
// The texture has been unloaded, it cannot be used here anymore.
```


