# Grist Image Preview Widget

Custom Grist widget that previews images from a column on the **active record**. The column can hold a URL, several URLs, or Grist attachments.

## Using the widget in Grist

1. Host this folder (GitHub Pages or any HTTPS URL).
2. Add a **Custom widget** and paste that URL.
3. Point the widget at the table.
4. Hover the widget, open the gear, and choose the image column.

The preview updates when you change row. Double-click the image to open the URL from the **Link column** (if configured).

## Settings

- **Image column** — URL text, or Attachment.
- **Link column** — URL text or HyperLink. Double-click the image to open it in a new tab.
- **Fit** — `contain` keeps the whole image visible; `cover` fills the widget.
- **Alignment** — where the image sits in the pane (9 positions; default top-left).
- **Background** — color behind the image.

The gear is hidden until the pointer is over the widget. It stays visible while settings are open.

## Small pane clip (Grist iframe limit)

Grist embeds custom widgets in `iframe.custom_view` without `width: 100%` / `min-width: 0`, so the iframe may stay near ~300×150px and the section clips it. Paste `grist-host.css` into the Grist host stylesheet (`/home/fede/grist-style/custom.css` on this install) to let the iframe shrink.
