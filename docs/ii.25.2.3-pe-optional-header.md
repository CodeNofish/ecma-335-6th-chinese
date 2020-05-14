## II.25.2.3 PE optional header

Immediately after the PE Header is the PE Optional Header. This header contains the following information:

 Offset | Size | Header part | Description
 ---- | ---- | ---- | ----
 0 | 28 | Standard fields | These define general properties of the PE file, see §[II.25.2.3.1](ii.25.2.3.1-pe-header-standard-fields.md).
 28 | 68 | NT-specific fields | These include additional fields to support specific features of Windows, see §[II.25.2.3.2](ii.25.2.3.2-pe-header-windows-nt-specific-fields.md).
 96 | 128 | Data directories | These fields are address/size pairs for special tables, found in the image file (for example, Import Table and Export Table).
