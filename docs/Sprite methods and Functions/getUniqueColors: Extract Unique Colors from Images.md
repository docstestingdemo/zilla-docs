

  # **getUniqueColors Function**

High Level

This function is part of our Node.js SDK, which you can install from NPM and import from the `sprite` object as follows:

```javascript
import { sprite } from 'sprite'
```

## Why should I use this function?

The `getUniqueColors` function is useful when you need to extract all unique colors from an image. This can be particularly helpful in various image processing tasks, such as color analysis, palette generation, or sprite optimization.

## What parameters or arguments are required?

The function requires the following parameters:

1. `imagePath` (string): The path to the image file you want to analyze.
2. `options` (object, optional): An optional parameter for additional configuration (currently not used in the provided code).

## Prerequisites

Before using this function, ensure you have:

1. Installed the Sprite SDK in your project.
2. Imported the necessary modules, including Jimp for image processing.

## How do I use this function?

To use the `getUniqueColors` function, follow these steps:

1. Import the function from the Sprite SDK:

```javascript
import { sprite } from 'sprite'
```

2. Call the function with the path to your image:

```javascript
const uniqueColors = await sprite.getUniqueColors('path/to/your/image.png')
```

3. The function returns a Promise that resolves to an array of unique color integers. You can then use these color values as needed in your application.

Example usage:

```javascript
try {
  const uniqueColors = await sprite.getUniqueColors('mySprite.png')
  console.log(`Number of unique colors: ${uniqueColors.length}`)
  // Process the unique colors as needed
} catch (error) {
  console.error('Error processing image:', error)
}
```

Note that this function ignores fully transparent pixels and only considers pixels with some level of opacity when determining unique colors.

  