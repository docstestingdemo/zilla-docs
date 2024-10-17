

  # **generateHouseAsset Function**

High Level

This function is part of our Node.js SDK, which you can install from NPM and import from the `sprite` object as follows:

```javascript
import { sprite } from 'sprite';
```

## Why should I use this function?

The `generateHouseAsset` function allows you to create 2D assets for use in Phaser JS games, specifically depicting houses or building-like structures. It leverages the DALL-E 3 model to generate these assets based on your description, making it easier to quickly produce game assets without manual design work.

## What parameters or arguments are required?

1. `description` (string): A description of the house or building you want to generate.
2. `options` (object): An optional object containing additional parameters:
   - `iterations` (number): The number of assets to generate.
   - `size` (string): The size of the generated image (default: "1024x1024").

## Prerequisites

- You must have the sprite SDK installed and properly configured.
- An active OpenAI API key with access to the DALL-E 3 model.

## How do I use this function?

Here's an example of how to use the `generateHouseAsset` function:

```javascript
const sprite = require('sprite');

async function generateGameAsset() {
  const description = "medieval stone tower with a thatched roof";
  const options = { iterations: 3, size: "512x512" };

  try {
    const assets = await sprite.generateHouseAsset(description, options);
    console.log("Generated assets:", assets);
  } catch (error) {
    console.error("Error generating assets:", error);
  }
}

generateGameAsset();
```

This function will generate three different 512x512 images of a medieval stone tower with a thatched roof. The function returns an array of responses from the DALL-E 3 API, each containing the generated image data.

If you don't specify the `iterations` option, the function will generate a single image and return the API response directly.

Note that the generated assets are optimized for use in 2D Phaser JS games, so they should be ready to integrate into your game project with minimal additional processing.

  