---
title: Place documents and PDF pages
description: Place another VectorCraft document, or a page of a PDF or .ai file, as one linked object, pick the page and its crop box, edit the original in its own tab, and update, relink or embed it from the Links panel.
sidebar:
  order: 19.8
type: guide
category: Images and data
subcategory: Images
cover: /assets/uploads/vectorcraft/place-linked-documents-placed-badge.webp
summary: Place a document or PDF page as one linked object and keep it updated.
parent: workflows
---

This guide shows how to place another VectorCraft document, or a page of a PDF or `.ai` file, as one linked, locked object, how to pick the page and the box it is cropped to, how to edit the original in its own tab, and how to update, relink and embed the placed object.

## Place a VectorCraft document

1. Open the document you want to place the other document in.
2. Choose **File → Place…** (**Ctrl+Shift+P**, or **Cmd+Shift+P** on macOS) and pick a `.vectorcraft` file.
3. In the Place dialog, leave **Link** turned on. Link is on by default, and the dialog keeps your last choice.
4. Press **Place**. The document is placed in the center of the view as one object.
5. Move, scale or rotate the object with the Selection tool, or drag its handles.

The placed object shows the first artboard of the document, clipped to the artboard. Guides and the art on hidden and template layers do not show. The art inside the object is locked: you cannot select or edit its paths in this document. To change the art, edit the original file (see [Edit the placed document](#edit-the-placed-document)).

With **Link** turned off, the document's art is placed as an editable group instead, with no link to the file.

The placed object keeps a copy of the file and a preview of up to 1024 pixels on its longer side. By default, a save writes only the preview in place of the file, and the object shows that preview when its file is missing. To keep the file itself in the saved document, turn on **Include Linked Files** in the **VectorCraft Options** dialog that follows **File → Save As…**. The object stays linked either way. The art is read from the file again for printing, for exporting and when you zoom in past the preview, and it is output as vectors. A file larger than 256 MiB cannot be placed.

When the object is selected, the Properties panel reads **Placed Document**, and the Links panel lists the file. Its Link Info shows **Format** VectorCraft, **Dimensions** in points, **Scale** as a percentage of the artboard's size, the **Page** (the artboard number) and the **Status**.

![The festival-program document with the placed lantern-badge.vectorcraft, a teal disc with an amber lantern, selected in its violet to coral header. The Properties panel reads Placed Document, and the Links panel lists the file with Link Info showing Format VectorCraft, Location C:\Art\lantern-festival, Dimensions 240 pt × 240 pt, Scale H: 70.0% V: 70.0%, Page 1 and Status Linked](/assets/uploads/vectorcraft/place-linked-documents-placed-badge.webp)

To place several files at once, see [Place a file instead of opening it](/apps/vectorcraft/open-and-save-files/#place-a-file-instead-of-opening-it).

## Place a page of a PDF or .ai file

1. Choose **File → Place…** and pick a PDF, `.ai` or `.ait` file.
2. Leave **Link** turned on and press **Place**.
3. If the file has more than one page, the Place PDF dialog opens. Pick the page with the arrows under the preview, or type its number in the box. The arrows go to the first, previous, next and last page.
4. Choose a box in **Crop To**. The preview shows the page cropped to that box.
5. Click **OK**.

A file with one page and no password is placed at once, cropped to its Crop box. The placed page is a linked object like a placed VectorCraft document, and its Link Info shows the page number.

| Crop To | What the placed page shows |
|---|---|
| **Bounding Box** | The bounds of the art on the page |
| **Art** | The page's art box |
| **Crop** | The visible page area that PDF viewers show. This is the default |
| **Trim** | The finished page size |
| **Bleed** | The page with its bleed area |
| **Media** | The whole sheet |

A page with no Art, Trim or Bleed box uses its Crop box instead. Every box is clipped to the Media box.

![The Place PDF dialog over the festival-program document, showing page 2 of a three-page PDF: a navy map titled Lantern routes with a teal river and amber and coral routes. The page box reads 2 of 3 between the page arrows, and the Crop To list is open with Bounding Box, Art, Crop, Trim, Bleed and Media, Trim highlighted](/assets/uploads/vectorcraft/place-linked-documents-place-pdf.webp)

### Place a password-protected PDF

When the PDF has a password, the dialog first says that the file needs a password and shows a **Password** box.

1. Type the password and click **OK**.
2. If the file has more than one page, pick the page and the **Crop To** box, then click **OK**.

A page placed with a password is placed as an editable group, not as a linked object.

## Edit the placed document

1. Select the placed document.
2. Click **Edit Original** at the bottom of the Links panel, or choose **Edit → Edit Original**.
3. Edit the document in the new tab that opens.
4. Choose **File → Save** (**Ctrl+S**, or **Cmd+S** on macOS).

![The lantern-badge.vectorcraft tab open beside the festival-program tab after Edit Original, with the Direct Selection tool active and the lantern body selected. The Properties panel shows the path with its Fill set to coral, and the lantern on the canvas is now coral on the teal disc](/assets/uploads/vectorcraft/place-linked-documents-edit-original.webp)

When you save the original in VectorCraft, every open document that places it shows the change at once, and each update is one undo step in that document.

![Back in the festival-program document after the badge was saved, the placed lantern-badge.vectorcraft now shows a coral lantern. It is selected, and the Links panel shows its Link Info with Status Linked](/assets/uploads/vectorcraft/place-linked-documents-updated.webp)

VectorCraft checks the linked files every two seconds for changes made by another app. What happens when a file changed depends on **Update Links** in **Edit → Preferences… → File Handling** on Windows and Linux, or **VectorCraft → Settings → File Handling…** on macOS:

| Update Links | What happens when the file changes |
|---|---|
| **Automatically** | The placed object is read again |
| **Manually** | The status bar reports the change. Use **Update Link** in the Links panel |
| **Ask When Modified** | The **Update Modified Links** dialog asks whether to show the new version. This is the default |

If the file is missing, Edit Original reports that it cannot be found. Relink it first.

## Update, relink and embed a placed document

Select the placed document, or its row in the Links panel, and choose a command from the panel menu. **Relink…**, **Go To Link**, **Update Link**, **Edit Original** and **Break Link** are also buttons at the bottom of the panel.

| Command | What it does to a placed document |
|---|---|
| **Relink…** | Links the object to another file. The object shows the same artboard or page of the new file and keeps its bounds |
| **Relink to Folder…** | Links the object to the file with the same name in a folder you pick |
| **Find in Folder…** | Searches a folder and its subfolders for the file |
| **Go To Link** | Selects the object and scrolls the view to it |
| **Update Link** | Reads a modified file again. It is available only when the file changed |
| **Edit Original** | Opens the file in a new tab |
| **Embed Image(s)** | Replaces the object with an editable copy of its art, the same copy that placing the file without Link gives. The art's symbols, patterns, swatches and images are added to the document. The **Break Link** button does the same |
| **Placement Options…** | Sets how the file takes the object's place when it is updated or relinked |
| **Show in Folder** | Shows the file in the system's file manager |

**Object → Expand…** also turns a placed document into an editable copy of its art. Each update, relink and embed is one undo step. A placed document stays linked when you embed it if its file cannot be read or has changed since it was read. Relink or update it first.

![The Links panel menu open beside the festival-program document with the coral badge selected. The menu lists Relink…, Relink to Folder…, Find in Folder…, Go To Link, Update Link (unavailable), Edit Original, Embed Image(s) (highlighted), Unembed… (unavailable), Placement Options… and Show in Folder, then Select Linked and the other select choices, and Show All (checked), Show Missing, Show Modified and Show Embedded](/assets/uploads/vectorcraft/place-linked-documents-links-menu.webp)

When you open a document, VectorCraft looks for each placed file at its saved path, then at its path relative to the document and by name in the document's folder. A placed document whose file VectorCraft cannot find shows its saved preview, or its full art when the document was saved with **Include Linked Files**. See [Fix missing links when a document opens](/apps/vectorcraft/work-with-placed-images/#fix-missing-links-when-a-document-opens).

## Placed documents inside placed documents

A placed document can hold placed documents of its own, and VectorCraft reads them the same way, up to 8 levels deep. A document placed deeper than that shows its saved preview. When two documents place each other, VectorCraft stops reading them at the same limit.

## Related

- [Open and save files](/apps/vectorcraft/open-and-save-files/#place-a-file-instead-of-opening-it)
- [Work with placed images](/apps/vectorcraft/work-with-placed-images/)
- [Fix missing links when a document opens](/apps/vectorcraft/work-with-placed-images/#fix-missing-links-when-a-document-opens)
- [Manage artboards](/apps/vectorcraft/manage-artboards/)
- [All VectorCraft workflows](/apps/vectorcraft/workflows/)
