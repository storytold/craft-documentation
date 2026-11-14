---
title: Expand objects into paths
description: Use Object → Expand… to turn live shapes, type, fills and strokes into plain art, use Expand Appearance for art with effects, and find the expand command for each kind of live object.
sidebar:
  order: 12.8
type: guide
category: Draw and edit
subcategory: Paths
cover: /assets/uploads/vectorcraft/expand-objects-into-paths-result.webp
summary: Turn live objects, fills and strokes into plain art you can edit.
parent: workflows
---

This guide covers **Object → Expand…**, **Object → Expand Appearance** for art with effects, and the expand commands of other kinds of live objects. **Object → Expand…** turns live art into plain art: live shapes and type become paths, gradient and pattern fills become separate objects, and strokes become filled shapes.

## Expand fills, strokes and live objects

1. With the Selection tool, select the objects to expand.
2. Choose **Object → Expand…**. The Expand dialog opens with **Object**, **Fill** and **Stroke** turned on. An option that has nothing to expand in the selection is dimmed.
3. Turn off any of **Object**, **Fill** and **Stroke** that you want to keep as they are.
4. If the selection has a gradient fill, choose what it becomes under **Expand Gradient To**: **Gradient Mesh**, or **Specify** and the number of objects.
5. Click **OK**.

Expand is one undo step, so **Edit → Undo** (**Ctrl+Z**, or **Cmd+Z** on macOS) brings the objects back as they were. The expanded objects stay selected.

![The Expand dialog over the desert poster, with Object, Fill and Stroke checked and Specify set to 12 objects under Expand Gradient To](/assets/uploads/vectorcraft/expand-objects-into-paths-dialog.webp)

In the following image, the sky rectangle had a violet-to-coral linear gradient and the sun had an amber fill with a thick coral stroke. With Specify set to 12 objects, the sky became 12 bands of solid color inside a clip group shaped like the rectangle. The sun's stroke became a filled ring, a compound path, grouped with the sun's fill path. In the Layers panel, the **Sky** clip group lists its 12 band paths and its clipping path, which is the underlined row at the bottom.

![The desert poster after Expand, with the sky drawn as horizontal violet and magenta bands and anchor points along the inner and outer edges of the sun's coral ring. The Layers panel shows the Sun group holding a compound path and a path, and the Sky group holding 12 paths above an underlined path](/assets/uploads/vectorcraft/expand-objects-into-paths-result.webp)

## Expand options

| Option | What it expands |
|---|---|
| **Object** | Live shapes become paths and type becomes outlines. Blends become groups of their steps, repeats become groups of their copies, Intertwine groups become groups of their objects, and envelopes become their distorted content. Placed documents become editable copies of the art they show. Symbol instances without effects and not in perspective become the art of their symbol. |
| **Fill** | Gradient fills become the objects that **Expand Gradient To** sets. Pattern fills become the pattern's tiles inside a clip group shaped like the object. A solid fill has nothing to expand. |
| **Stroke** | Strokes become filled shapes the size of the stroke, the same result as **Object → Path → Outline Stroke**. |
| **Expand Gradient To: Gradient Mesh** | Each linear, radial or conic gradient fill becomes a gradient mesh inside a clip group shaped like the object. |
| **Expand Gradient To: Specify … Objects** | Each gradient fill becomes that many objects of solid color inside a clip group shaped like the object: strips for a linear gradient, concentric ellipses for a radial gradient, and wedges around the center for a conic gradient. The default is 255, and the box takes 1 to 1000. |

An option is dimmed when the selection has nothing for it to expand. A rectangle is a live shape, so for a rectangle with a solid fill and a stroke, **Object** and **Stroke** are available and **Fill** is dimmed.

**Expand Gradient To** is dimmed unless **Fill** is on and the selection has a gradient fill. A freeform gradient always becomes a gradient mesh shaped like the object, whichever choice is set.

When the fill or stroke is in the art of a symbol instance, and nowhere else in the selection, **Fill** or **Stroke** is available only while **Object** is on.

## Expand art with effects and several fills or strokes

**Object → Expand…** is dimmed while the selection has appearance attributes:

- an effect, such as Zig Zag or a drop shadow;
- more than one fill or stroke;
- a fill or stroke with its own opacity, blend mode or effects;
- a brush on a path;
- a group or layer with fills, strokes or effects of its own;
- a type object with a fill or stroke added to the type object itself, even a single fill.

When you point at the dimmed item, a tooltip reads **Expand Appearance first (Object › Expand Appearance)**. The same message shows in the status bar if you run Expand from the command palette or a shortcut, and the art is left as it was.

To expand such art:

1. Select it and choose **Object → Expand Appearance**. Each fill and stroke becomes an object of its own, grouped in paint order. Shape effects are applied to the paths, and raster effects become embedded images.
2. To turn the remaining strokes into filled shapes, choose **Object → Expand…** with **Stroke** on, or choose **Object → Path → Outline Stroke**.

After Expand Appearance, a stroke is still a stroke, with its weight, dashes and arrowheads, on its own copy of the path. Expand Appearance is available when the selection has any of the appearance attributes listed above. [Apply effects and appearance](/apps/vectorcraft/apply-effects-and-appearance/#make-the-appearance-permanent) describes what Expand Appearance makes of each effect.

## Other expand commands

Several kinds of live object have an expand command of their own.

| Command | Where to find it | Result | More |
|---|---|---|---|
| **Outline Stroke** | **Object → Path → Outline Stroke** | Replaces each stroked path with a filled shape the size of the stroke | [Draw and edit paths](/apps/vectorcraft/draw-and-edit-paths/) |
| **Expand Shape** | **Object → Shape → Expand Shape** | Turns live shapes into plain paths without their corner widgets | [Draw and transform shapes](/apps/vectorcraft/draw-and-transform-shapes/#turn-a-path-into-a-live-shape) |
| **Expand Compound Shape** | The **Expand** button in the Pathfinder panel, **Object → Plug-ins → Compound Shapes → Expand Compound Shape**, or the Pathfinder panel menu | Turns a compound shape into one path or compound path of the area it shows, painted as it looks | [Combine and cut shapes](/apps/vectorcraft/combine-and-cut-shapes/#use-the-pathfinder-panel-menu) |
| **Blend → Expand** | **Object → Blend → Expand**, or the **Expand** button in the Blend panel | Replaces the blend with a group of its objects and steps | [Make patterns, blends and repeats](/apps/vectorcraft/make-patterns-blends-and-repeats/#set-blend-options-and-change-the-spine) |
| **Envelope Distort → Expand** | **Object → Envelope Distort → Expand** | Replaces the envelope with a group of the distorted art, with type turned into outlines | [Reshape with the warp tools](/apps/vectorcraft/reshape-with-warp-tools/#edit-reset-or-remove-an-envelope) |
| **Live Paint → Expand** | **Object → Live Paint → Expand** | Turns a Live Paint group into a plain group of its painted faces and edges | [Combine and cut shapes](/apps/vectorcraft/combine-and-cut-shapes/#color-regions-with-live-paint) |
| **Image Trace → Expand** | **Object → Image Trace → Expand**, or **Expand** in the Image Trace panel | Keeps the traced paths and removes the source image | [Trace an image](/apps/vectorcraft/trace-an-image/#finish-the-tracing) |
| **Objects on Path → Expand** | **Object → Objects on Path → Expand** | Makes the objects and the path an ordinary group, with the objects where they are | [Make patterns, blends and repeats](/apps/vectorcraft/make-patterns-blends-and-repeats/#place-objects-along-a-path) |
| **Expand Brush Strokes** | The button at the bottom of the Brushes panel, or the Brushes panel menu | Replaces each brushed path with a group of the brush art | [Paint with brushes and variable widths](/apps/vectorcraft/paint-with-brushes/#turn-brush-strokes-into-paths) |
| **Bake** | The Contour bar, while the Contour tool is active | Turns the live contour into plain paths | [Cut, join and refine paths](/apps/vectorcraft/cut-join-and-refine-paths/#outline-areas-with-the-contour-tool) |

**Object → Expand…** with **Object** on also expands blends, envelopes and live shapes, along with everything else in the selection.

## Related

- [Workflows](/apps/vectorcraft/workflows/)
- [Draw and edit paths](/apps/vectorcraft/draw-and-edit-paths/)
- [Cut, join and refine paths](/apps/vectorcraft/cut-join-and-refine-paths/)
- [Draw and transform shapes](/apps/vectorcraft/draw-and-transform-shapes/)
- [Fill, stroke and color](/apps/vectorcraft/fill-stroke-and-color/)
- [Apply effects and appearance](/apps/vectorcraft/apply-effects-and-appearance/)
- [Combine and cut shapes](/apps/vectorcraft/combine-and-cut-shapes/)
- [Make patterns, blends and repeats](/apps/vectorcraft/make-patterns-blends-and-repeats/)
- [Reshape with the warp tools](/apps/vectorcraft/reshape-with-warp-tools/)
- [Paint with brushes and variable widths](/apps/vectorcraft/paint-with-brushes/)
- [Trace an image](/apps/vectorcraft/trace-an-image/)
