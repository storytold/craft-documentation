---
title: Adjust the colors of an image
description: Colorize grayscale images with a fill color, adjust images with live Color Adjustments and Color Effects, make the changes permanent, and recolor images with Edit Colors.
sidebar:
  order: 19.6
type: guide
category: Images and data
subcategory: Images
cover: /assets/uploads/vectorcraft/adjust-image-colors-colorize.webp
summary: Colorize, adjust and recolor placed and embedded images.
parent: workflows
---

This guide covers changing the colors of images in a document: colorizing a grayscale or black-and-white image with its fill color, adjusting an image with live Color Adjustments and Color Effects, editing or removing those adjustments in the Appearance panel, making them permanent, and recoloring an image with the **Edit → Edit Colors** commands. To place, link or embed an image, see [Work with placed images](/apps/vectorcraft/work-with-placed-images/).

Linked and embedded images take these changes differently:

| Change | Embedded image | Linked image |
|---|---|---|
| Colorize with the fill color | Grayscale and 1-bit images | Grayscale and 1-bit images |
| Color Adjustments and Color Effects | VectorCraft draws the image with the adjustment | VectorCraft shows the original pixels |
| **Apply as Filter**, **Expand Appearance**, **Edit → Edit Colors** | The pixels change | The pixels do not change |

A colorized image is the exception: these changes recolor its colorize color, whether the image is linked or embedded, and its gray pixels stay as they are.

To adjust the pixels of a linked image, embed it first: select it and click **Embed** in the Properties panel, or choose **Embed Image(s)** from the Links panel menu.

## Colorize a grayscale or black-and-white image

A grayscale or 1-bit image takes the color of its fill. VectorCraft draws each pixel in that color and makes the pixel as opaque as it is dark, so black pixels take the full color and white pixels become transparent.

1. Select the image with the Selection tool. The Properties panel shows its **Embedded Image** or **Linked File** section, with the color mode **Grayscale**.
2. Make the fill active and pick a solid color: click a swatch in the Swatches panel, or set the color in the Color panel. The image redraws in that color, and the **Fill** box in the Properties panel's **Appearance** section shows it.
3. To take the color off, set the fill to **None**.

![The harbor-zine.vectorcraft document with lighthouse-gray.png selected, its lighthouse and rock shown in deep violet tints over a cream frame. The Properties panel shows the Embedded Image section with Grayscale and a violet Fill, and the Swatches panel shows the same violet in its fill box.](/assets/uploads/vectorcraft/adjust-image-colors-colorize.webp)

Only a solid color colorizes an image. An RGB or CMYK image keeps its pixels when you set its fill. A grayscale image that has transparency takes only a spot color, black or white. With a process color, VectorCraft shows the error "a process color can't colorize a grayscale image with transparency: use a spot color, black or white".

When you recolor a colorized image with an adjustment or an **Edit Colors** command, VectorCraft changes its colorize color and leaves the gray pixels as they are.

## Adjust tones and color with a live effect

The commands in **Effect → Color Adjustments** add a live effect to the selected objects. The effect recolors fills, strokes, type, gradient meshes and embedded images, and the original colors and pixels stay in the document until you make the change permanent.

1. Select one or more images.
2. Choose **Effect → Color Adjustments** and one of **Brightness/Contrast…**, **Curves…**, **Hue/Saturation…**, **Levels…**, **Shift to Color…** or **Temperature/Tint…**.
3. Set the values. **Preview** is on when the dialog opens, so the canvas shows the result as you change it.
4. Click **OK**. The adjustment appears as a row in the Appearance panel.

![The Levels dialog beside the selected dusk-pier.png image, with Input Black 24, Input White 230, Output Black 0, Output White 255, Channel RGB, Gamma 1.2 and Preview on. The pier image shows a coral sky with a setting sun over navy water.](/assets/uploads/vectorcraft/adjust-image-colors-levels.webp)

### Brightness/Contrast

| Option | Range | Default | What it does |
|---|---|---|---|
| **Brightness** | -100 to 100 | 0 | Lightens or darkens the tones. Black and white stay as they are. |
| **Contrast** | -100 to 100 | 0 | Spreads the tones apart or draws them together. |

### Curves

| Option | Range | Default | What it does |
|---|---|---|---|
| Curve graph and **Points** | Input and output 0 to 255 | `0,0 128,128 255,255` | Maps each input level to an output level along a smooth curve through the points. The curve is flat past the first and last points. |
| **Channel** | RGB, Red, Green, Blue | RGB | Applies the curve to all three channels or to one. |

### Hue/Saturation

| Option | Range | Default | What it does |
|---|---|---|---|
| **Hue** | -180 to 180 degrees | 0 | Turns every color around the color wheel. |
| **Saturation** | -100 to 100 | 0 | Makes colors more or less vivid. |
| **Lightness** | -100 to 100 | 0 | Lightens or darkens every color. |
| **Colorize** | On or off | Off | Gives every color the same hue. With Colorize on, the Hue slider still runs from -180 to 180 and sets that hue directly. A negative value wraps around the color wheel, so -20 gives a hue of 340 degrees. The saturation is (100 + Saturation) / 2 percent. |

![The Hue/Saturation dialog beside the selected dusk-pier.png image, with Hue -20, Saturation 30, Lightness 0, Colorize off and Preview on. The sky of the pier image previews in magenta and pink.](/assets/uploads/vectorcraft/adjust-image-colors-hue-saturation.webp)

### Levels

| Option | Range | Default | What it does |
|---|---|---|---|
| **Input Black** | 0 to 255 | 0 | Input levels at or below this value become the output black. |
| **Input White** | 0 to 255 | 255 | Input levels at or above this value become the output white. |
| **Output Black** | 0 to 255 | 0 | The darkest level in the result. |
| **Output White** | 0 to 255 | 255 | The lightest level in the result. |
| **Channel** | RGB, Red, Green, Blue | RGB | Applies the levels to all three channels or to one. |
| **Gamma** | 0.1 to 10 | 1 | A value above 1 lightens the midtones, and a value below 1 darkens them. |

### Shift to Color

| Option | Range | Default | What it does |
|---|---|---|---|
| **Color** | Any color | `#ff8000` | The color the image shifts toward. |
| **Amount** | 0 to 100% | 50% | How far the colors shift. |
| **Preserve Lightness** | On or off | On | On: the colors take the hue and saturation of the target color and keep their own lightness. Off: the colors mix with the target color. |

### Temperature/Tint

| Option | Range | Default | What it does |
|---|---|---|---|
| **Temperature** | -100 to 100 | 0 | Negative values make the image cooler, and positive values make it warmer. |
| **Tint** | -100 to 100 | 0 | Negative values make the image greener, and positive values make it more magenta. |

## Apply a color effect

**Effect → Color Effects** has four more live adjustments. They work like the Color Adjustments and stack with them in the order they appear in the Appearance panel. The **Object → Plug-ins → Color Effects** submenu also holds **Exposure…**, **Desaturate**, **Duotone…** and **Invert Colors**, along with a **Color Effects Panel** item that opens the Color Effects panel.

| Effect | What it does |
|---|---|
| **Desaturate** | Turns every color to the gray of its lightness. It has no options. |
| **Duotone…** | Draws the image with one to four inks, set in the Duotone dialog. |
| **Exposure…** | Brightens or darkens in stops of light, in linear light. **Exposure** runs from -20 to 20 stops (default 0), **Offset** from -0.5 to 0.5 (default 0) and **Gamma** from 0.1 to 10 (default 1). Each stop of exposure doubles or halves the light. |
| **Invert Colors** | Turns every color to its RGB inverse. It has no options. |

The **Duotone** dialog has these settings:

| Setting | What it does |
|---|---|
| **Tone 1** to **Tone 4** | Turns each tone on or off. Each tone is a swatch or a **Process Color** with a hex value. A new Duotone effect has one black tone. |
| **Curve** | Picks the tone whose curve the graph shows. Drag the points on the graph, or type them as `x,y` pairs from 0 to 100 in **Points**. |
| **Reset to Linear** and **Reset to Inverse** | Set the shown tone's curve to a straight line or to its inverse. |
| **Skip Objects with Spot Colors** | Leaves objects painted with spot colors unchanged. |
| **Preview** | Shows the effect on the canvas before you click **OK**. It is on when the dialog opens. |

The inks overprint, so where two tones overlap their tints multiply. A single tone of a swatch gives a tint of that swatch.

![The Duotone dialog beside the selected dusk-pier.png image, with Tone 1 a navy process color 1e2a5a, Tone 2 an amber process color f59e0b and the Tone 2 curve set to 0,0 40,62 100,100. The pier image previews in brown and sepia tones.](/assets/uploads/vectorcraft/adjust-image-colors-duotone.webp)

## Change or remove an adjustment in the Appearance panel

1. Select the image and choose **Window → Appearance** (**Shift+F6**). The panel lists the image's rows, with one row for each adjustment.
2. Click the eye next to an adjustment to hide it. VectorCraft does not draw a hidden adjustment. Click the eye again to show it.
3. Click the adjustment's name to open its dialog with the current values, change them, and click **OK**.
4. To remove an adjustment, select its row and click **Delete Selected Item** at the bottom of the panel.

![The harbor-zine.vectorcraft document with dusk-pier.png selected and the Appearance panel listing its Levels and Hue/Saturation rows, each with an eye icon. The Color Effects panel below shows the Adjustment menu, the Add as Effect, Apply as Filter and Reset buttons, and the Duotone… button under Inks.](/assets/uploads/vectorcraft/adjust-image-colors-appearance.webp)

For more on the Appearance panel, see [Apply effects and appearance](/apps/vectorcraft/apply-effects-and-appearance/).

## Make the change permanent

A live adjustment keeps the original pixels. Two commands write the adjustment into the image instead.

**Apply as Filter** recolors the selected objects once, in their own colors and pixels, and adds no effect:

1. Select the image and choose **Object → Plug-ins → Color Effects → Color Effects Panel**.
2. Pick an adjustment in the **Adjustment** menu: **Brightness/Contrast**, **Hue/Saturation**, **Levels**, **Temperature/Tint**, **Exposure**, **Desaturate** or **Invert Colors**.
3. Set its values.
4. Click **Apply as Filter**. The change is one undo step, and effects the image already has stay as they are.

In the same panel, **Add as Effect** adds the adjustment as a live effect, and **Reset** sets the values back to their defaults. **Duotone…** opens the Duotone dialog.

**Expand Appearance** turns the image's live adjustments into pixels:

1. Select an image that has live adjustments.
2. Choose **Object → Expand Appearance**. VectorCraft writes the adjusted pixels into a new embedded image and removes the live effects. The image looks the same as before. For a colorized image, VectorCraft changes the colorize color instead of the pixels.

**Expand Appearance** stops with an error, and the image keeps its live adjustments, when the image is a colorized grayscale image with transparency and the adjusted color would be a process color.

## Recolor an image with Edit → Edit Colors

Most commands in **Edit → Edit Colors** recolor the selected objects, embedded images included, without adding an effect. VectorCraft makes a recolored copy of each image, and the original image stays for any other object that uses it. Each command is one undo step.

![The Edit menu open over the harbor-zine.vectorcraft document with market-stall.png selected. The Edit Colors submenu lists its twelve commands, with Convert to Grayscale highlighted.](/assets/uploads/vectorcraft/adjust-image-colors-edit-colors.webp)

| Command | What it does to an embedded image |
|---|---|
| **Convert to Grayscale** | Converts the pixels to gray and stores the image with one gray channel. |
| **Convert to CMYK** and **Convert to RGB** | Converts the pixels to that color model. |
| **Invert Colors** | Turns every pixel to its RGB inverse. |
| **Saturate…** | Makes colors more or less vivid. **Intensity** runs from -100% to 100% (default 0%), and the canvas previews the change while **Preview** is on. |
| **Adjust Color Balance…** | Opens the **Adjust Colors** dialog, which shifts each color channel by a percentage. |
| **Recolor Artwork…** and **Recolor with Preset** | Open the **Recolor Artwork** dialog. When a row replaces a color, the image pixels of exactly that color change to the row's new color. The dialog lists a colorized image's colorize color as a row. |

For the options of the Recolor Artwork dialog, see [Change the colors of finished art](/apps/vectorcraft/fill-stroke-and-color/#change-the-colors-of-finished-art).

The **Blend Front to Back**, **Blend Horizontally** and **Blend Vertically** commands recolor vector objects and leave images unchanged. **Overprint Black…** sets black fills and strokes to overprint, and it leaves image pixels as they are.

The **Adjust Colors** dialog has these settings:

| Setting | Default | What it does |
|---|---|---|
| **Color Mode** | **RGB** | **Grayscale**, **RGB**, **CMYK** or **Global**. The dialog shows a slider for each channel of the mode. **Global** has one slider, **Tint**, which shifts the tints of global and spot colors and leaves other colors and images unchanged. |
| Channel sliders | 0% | Add -100% to 100% to each channel. |
| **Convert** | Off | On: the adjusted colors stay in the chosen color mode. Off: each color keeps its own color model. The checkbox is unavailable in **Global** mode. |
| **Adjust Options** | **Fill** and **Stroke** on | **Fill** and **Stroke** choose which paints change. |
| **Preview** | On | Shows the change on the canvas before you click **OK**. |

## Related

- [Work with placed images](/apps/vectorcraft/work-with-placed-images/)
- [Apply effects and appearance](/apps/vectorcraft/apply-effects-and-appearance/)
- [Built-in plug-ins: Adjust colors](/apps/vectorcraft/built-in-plug-ins/#adjust-colors)
- [Fill, stroke and color](/apps/vectorcraft/fill-stroke-and-color/)
- [Trace an image](/apps/vectorcraft/trace-an-image/)
- [All VectorCraft workflows](/apps/vectorcraft/workflows/)
