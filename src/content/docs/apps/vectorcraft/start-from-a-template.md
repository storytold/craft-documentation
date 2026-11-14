---
title: Start documents from a template
description: Save a document as a template, start new documents from it, change it later, and choose the folder where templates are kept.
sidebar:
  order: 10.2
type: guide
category: Documents and artboards
subcategory: Documents
cover: /assets/uploads/vectorcraft/start-from-a-template-new-untitled.webp
summary: Save a document as a template and start new documents from it.
parent: workflows
---

This page shows how to save a document as a template, start new documents from it, change it, and choose where templates are kept.

A template is a saved document that you start new work from. Its artboards, layers, art, swatches and guides open as a new untitled document, and the template file itself stays as it was.

## Save a document as a template

1. Set up the document the way every new copy should start: its artboards, layers, guides, swatches, styles and placeholder art and type.
2. Choose **File → Save as Template…**. The save dialog opens in the Templates folder and suggests the document's name followed by "template", for example `Postcard set template.vctemplate`.
3. In **Save as type**, pick the kind of template. The following table describes both kinds.
4. Type a name if you want a different one, and click **Save**.

| Save as type | Extension | What it holds |
|---|---|---|
| **VectorCraft Template** | `.vctemplate` | The whole document, as a `.vectorcraft` file holds it, marked as a template. This is the default |
| **PDF-compatible .ait template** | `.ait` | A PDF page for each artboard, plus the whole document, written the way VectorCraft writes a `.ai` file. VectorCraft opens the whole document from it. Apps that read PDF files show the artboards as pages |

VectorCraft does not show an options dialog for either kind of template. The document you saved from keeps its own file, name and unsaved changes.

![The Save As dialog open in the VectorCraft Templates folder, with the file name Postcard set template.vctemplate and the type VectorCraft Template (*.vctemplate). Behind it are the dusk postcards, with a sun over teal hills on the front, Your message here on the back, and the address side below](/assets/uploads/vectorcraft/start-from-a-template-save-dialog.webp)

If you type a name that ends in another format's extension, such as `card.png`, VectorCraft replaces that extension with the template's. A name without an extension gets one.

## Start a document from a template

1. Choose **File → New from Template…** (**Ctrl+Shift+N**, or **Cmd+Shift+N** on macOS). The open dialog starts in the Templates folder.
2. Pick a template and click **Open**.

The template opens as a new document named Untitled and a number, for example Untitled-1. It has the template's artboards, layers, art, swatches and guides. Because the document has no file yet, **File → Save** asks for a name and a folder.

![A new Untitled-1 tab beside the Postcard set.vectorcraft tab shows the Front, Back and Address postcards with their margin guides and placeholder text. The Layers panel lists Guides, Type, Art and Background, and the Swatches panel below it shows a group of dusk violets, corals, ambers and teals](/assets/uploads/vectorcraft/start-from-a-template-new-untitled.webp)

The open dialog's **Templates** file type lists `.vctemplate`, `.ait`, `.vectorcraft` and `.drawcraft` files. The other file types list every format VectorCraft opens. **New from Template…** opens any of these files as a new untitled document, an ordinary `.vectorcraft` document included.

:::note
**File → Open…** also opens a `.vctemplate` or `.ait` file as a new untitled document. **File → Save** then asks for a new file name instead of writing over the template.
:::

## Change a template

1. Open the template with **File → New from Template…** or **File → Open…**. It opens as an untitled document.
2. Make your changes.
3. Choose **File → Save as Template…**.
4. Pick the template's existing file in the Templates folder, with the same **Save as type**, and click **Save**.
5. When the save dialog asks whether to replace the existing file, confirm that you want to replace it.

Documents you already started from the template do not change.

## Choose where templates are kept

**File → Save as Template…** and **File → New from Template…** start in the Templates folder. By default this is the `VectorCraft Templates` folder in your `Documents` folder. On Linux and the BSDs, VectorCraft uses the documents folder set in your desktop's user folder settings (`XDG_DOCUMENTS_DIR`).

To use another folder:

1. Choose **Edit → Preferences…** (**Ctrl+K**). On macOS, choose **VectorCraft → Settings → General…** (**Cmd+K**).
2. Click the **File Handling** page.
3. In **Templates Folder**, type the full path of the folder. The field has no **Choose…** button.
4. Click **OK**.

Clear the field to go back to the default folder. When the Templates folder does not exist, VectorCraft makes it the next time one of the two dialogs opens. If VectorCraft cannot make it, the dialog starts in the nearest folder above it that exists. If no folder above it exists, the dialog starts in your home folder.

A preferences file made with **Export Preferences…** in the Preferences dialog does not include **Templates Folder**. Set the folder on each computer.

## Related

- [Workflows](/apps/vectorcraft/workflows/)
- [Set up a document and artboards](/apps/vectorcraft/set-up-documents-and-artboards/)
- [Manage artboards](/apps/vectorcraft/manage-artboards/)
- [Lay out pages with guides](/apps/vectorcraft/lay-out-pages-with-guides/)
- [Open and save files](/apps/vectorcraft/open-and-save-files/)
- [Preferences](/apps/vectorcraft/preferences/)
