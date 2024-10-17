

  # **Remove Background Color**

High Level

This function is part of our Node.js SDK, which you can install from NPM and import from the `sprite` object as follows:

```javascript
import { sprite } from 'sprite'
```

## Why should I use this function?

The `removeBackgroundColor` function is useful when you need to remove a specific background color from an image, creating transparency where that color was present. This is particularly helpful for:

- Creating sprites with transparent backgrounds
- Cleaning up images for use in graphic design
- Preparing images for overlays in digital media

## What parameters are required?

The function takes the following parameters:

1. `inputPath` (string): The path to the input image file.
2. `outputPath` (string): The path where the processed image will be saved.
3. `targetColor` (string): The color to be removed, specified as a CSS color string (e.g., '#FFFFFF' for white).
4. `colorThreshold` (number, optional): The tolerance for color matching. Default is 0.
5. `options` (object, optional): Additional options (currently unused in the provided code).

## Prerequisites

Before using this function, ensure you have:

- Installed the Sprite SDK via NPM
- Imported the necessary modules (Jimp is used internally)
- Node.js environment set up

## How do I use this function?

Here's an example of how to use the `removeBackgroundColor` function:

```javascript
import { sprite } from 'sprite'

async function processImage() {
  try {
    await sprite.removeBackgroundColor(
      'input/image.png',
      'output/transparent_image.png',
      '#FFFFFF',
      10
    )
    console.log('Background removed successfully!')
  } catch (error) {
    console.error('Error processing image:', error)
  }
}

processImage()
```

This function processes the image pixel by pixel, comparing each pixel's color to the target color. If the color difference is within the specified threshold, it sets the pixel to transparent. The resulting image is then saved to the specified output path.

Remember to handle the returned promise appropriately, as the function is asynchronous.

  