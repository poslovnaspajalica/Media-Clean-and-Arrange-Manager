# Media-Clean-and-Arrange-Manager
Tools for cleaning, syncing, and bulk managing images in the WordPress Media Library.
=== Media Clean and Arrange Manager ===
Contributors: businessclipltd
Tags: media, uploads, images, cleanup, gallery, bulk, attachments, migration
Requires at least: 6.0
Tested up to: 6.8
Requires PHP: 7.4
Stable tag: 1.0.0
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

Manage and clean WordPress Media Library with a gallery UI, bulk actions, sync missing upload files into attachments, and safely remove orphan resized images.

== Description ==

**Media Clean and Arrange Manager** is a practical toolbox for real-world WordPress sites where the Media Library is messy:

- Gallery view (grid) for quick selection.
- Bulk actions: Trash, Restore, Detach, Permanent delete (images only).
- Filter by upload date **or** by folder range (YYYY/MM) based on uploads path.
- Sync tool: scan `wp-content/uploads` and import missing originals into the Media Library.
- Cleanup tool: delete orphan resized `-WxH` files **only if** no original exists (supports `-scaled` / `-rotated` originals too).

This plugin focuses on **images only** and does not touch PDFs/documents.

== Installation ==

1. Upload the plugin folder to `/wp-content/plugins/media-clean-and-arrange-manager/`
2. Activate the plugin through the "Plugins" menu in WordPress.
3. Go to **Media Clean & Arrange** in the WordPress admin menu.

== Frequently Asked Questions ==

= Will this delete PDFs or documents? =

No. All operations are limited to attachments with MIME type `image/*`.

= Why are images missing from the gallery even though files exist in uploads? =

WordPress only shows files registered in the database as Media Library attachments. If files were copied to `uploads` without importing, they will not appear until you use the **Sync from uploads** tool.

= What does "Cleanup resized" remove? =

It removes resized variants like `photo-150x150.jpg` **only when** there is no corresponding original (including `photo.jpg`, `photo-scaled.jpg`, `photo-rotated.jpg`, etc.).

= Is it safe to run on production? =

Always take a full backup first. Use scan steps and review samples before running destructive actions.

== Screenshots ==

1. Gallery view with bulk actions
2. Sync from uploads (scan + batch import)
3. Cleanup orphan resized images

== Changelog ==

= 0.1.0 =
* Initial release.


