

  # **Generate Sprite**

High Level

This function is part of our Node.js SDK, which you can install from NPM and import from the `sprite` object as follows:

```javascript
import { sprite } from 'sprite'
```

## Why should I use this function?

The `generateSprite` function is a powerful tool for creating game assets, particularly sprite sheets for walking animations. It leverages AI technology to generate pixel art-style character sprites based on a text description. This function is especially useful for:

1. Rapid prototyping of game characters
2. Creating consistent sprite sheets for walking animations
3. Generating SNES-style graphics without the need for manual pixel art creation

## What parameters or arguments are required?

The `generateSprite` function accepts two parameters:

1. `description` (required): A string describing the character you want to generate.
2. `options` (optional): An object that can include the following properties:
   - `iterations`: Number of sprite variations to generate
   - `size`: Image size (default is "1024x1024")
   - `save`: Boolean to determine if the generated image should be saved locally

## Prerequisites

To use this function, you need:

1. An OpenAI API key with access to DALL-E 3 and GPT-4 Vision Preview
2. Node.js installed on your system
3. The `sprite` package installed in your project
4. Necessary dependencies: `axios`, `sharp`, and `openai`

## How do I use this function?

Here's a step-by-step guide to using the `generateSprite` function:

1. Import the function from the sprite package:
   ```javascript
   import { sprite } from 'sprite'
   ```

2. Call the function with a description and optional parameters:
   ```javascript
   const result = await sprite.generateSprite("a cute robot", { iterations: 3, save: true });
   ```

3. The function will return an object (or an array of objects if iterations > 1) containing:
   - `messages`: JSON object with recommended frameWidth and frameHeight for use in Phaser.js
   - `image`: Base64 encoded image data URL

4. You can then use this data to load the sprite in your game engine. For example, in Phaser.js:
   ```javascript
   this.load.spritesheet('robot', result.image, { 
     frameWidth: result.messages.content.frameWidth, 
     frameHeight: result.messages.content.frameHeight 
   });
   ```

This function streamlines the process of creating game-ready sprite sheets, allowing you to focus on game design and mechanics rather than asset creation.

  