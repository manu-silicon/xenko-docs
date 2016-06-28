# SpriteBatch

A sprite batch is a collection of sprites (2D textured planes).

# Creating a sprite batch

Xenko offers a easy way to deal will batches of sprites through the @'SiliconStudio.Xenko.Graphics.SpriteBatch' class. The user can use this class to regroup all of his sprites, update them and display them efficiently.

**Code:** Creating a sprite batch

```cs
var spriteBatch = new SpriteBatch(GraphicsDevice);
```


The user can specify the size of his batch size. It is not the maximum number of sprites the SpriteBatch is able to display, but simply the maximum number of sprites it can store before drawing.

**Code:** Setting the batch size

```cs
var spriteBatch = new SpriteBatch(GraphicsDevice, 2000);
```


It is also possible to set various states like the ones discussed in the [pipeline state](pipeline-state.md) documentation page.

# Drawing a sprite batch

The @'SiliconStudio.Xenko.Graphics.SpriteBatch' class has multiple draw methods to set various parameters. For a comprehensive list of all the features, please refer to the @'SiliconStudio.Xenko.Graphics.SpriteBatch' class reference documentation.

**Code:** Drawing a sprite batch

```cs
// begin the sprite batch operations
spriteBatch.Begin(GraphicsContext, SpriteSortMode.Immediate);
 
// draw the sprite immediately
spriteBatch.Draw(myTexture, new Vector2(10, 20));
 
// end the sprite batch operations
spriteBatch.End();
```


There are five modes to draw a sprite batch. They are enumerated in the @'SiliconStudio.Xenko.Graphics.SpriteSortMode' enum:

- Deferred (default mode): the sprites are drawn at the same time at the end to reduce the drawcall overhead
- Immediate: the sprites are draw after each each @'SiliconStudio.Xenko.Graphics.SpriteBatch.Draw' call
- Texture: Deferred mode but sprites are sorted based on their texture to reduce effect parameters update
- BackToFront: Deferred mode with a sort based on the z-order of the sprites
- FrontToBack: Deferred mode with a sort based on the z-order of the sprites

To set the mode, the user should specify it in the @'SiliconStudio.Xenko.Graphics.SpriteBatch.Begin' method.

**Code:** Deferred drawing of the sprite batch

```cs
// begin the sprite batch operations
spriteBatch.Begin(GraphicsContext); // same as spriteBatch.Begin(GraphicsContext, SpriteSortMode.Deferred);

// store the modification of the sprite
spriteBatch.Draw(myTexture, new Vector2(10, 20));

// end the sprite batch operations, draw all the sprites
spriteBatch.End();
```


It is possible to set several parameters on the sprite, for example:

- position
- rotation
- scale
- depth
- center offset
- color tint

For a comprehensive list, please refer to the @'SiliconStudio.Xenko.Graphics.SpriteBatch' class reference documentation, especially the @'SiliconStudio.Xenko.Graphics.SpriteBatch.Draw' methods.

**Code:** More complex sprite batch drawing

```cs
// begin the sprite batch operations
spriteBatch.Begin(GraphicsContext);
const int gridCount = 10;
var textureOffset = new Vector2((float)graphicsDevice.BackBuffer.Width/gridCount, (float)graphicsDevice.BackBuffer.Height/gridCount);
var textureOrigin = new Vector2(myTexture.Width/2.0f, myTexture.Height/2.0f);

// draw 100 sprites on a 10x10 grid with a rotation of 1.2 rad and a scale of 0.5 for each of them
for (int y = 0; y < gridCount; y++)
{
    for (int x = 0; x < gridCount; x++)
    {
        spriteBatch.Draw(UVTexture, new Vector2(x * textureOffset.X + textureOffset.X / 2.0f, y * textureOffset.Y + textureOffset.Y / 2.0f), Color.White, 1.2f, textureOrigin, 0.5f);
    }
}
 
// end the sprite batch operations, draw all the sprites
spriteBatch.End();
```


