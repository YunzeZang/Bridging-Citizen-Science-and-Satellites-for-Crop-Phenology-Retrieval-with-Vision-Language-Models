# Labeled Validation Test Set

This workbook (`test_set_labeled_validation.xlsx`) contains the manually visually interpreted reference annotations for a 500-photo validation test set. These annotations are the ground truth used to assess crop identification and rapeseed phenology predictions.

## Ground-truth annotations

Each image was visually interpreted to determine its crop identity and, for rapeseed images, its principal BBCH growth stage.

- **`label`** is the manually assigned crop label, including rapeseed and non-rapeseed.
- **`bbch_principal`** is the manually assigned principal BBCH stage for rapeseed. The available stage groups are `1`, `2`, `3`, `5`, `6`, `7-8`, and `9`. 
- **`pod_stage`** refines the BBCH `7-8` group only. It is empty for all other BBCH stages. Within BBCH `7-8`, `0` indicates **green pods (GP)** and `1` indicates **non-green pods (NP)**.

## Image files

The image files are included in this directory and are organized by the manually assigned binary crop class:

- `Rapeseed/` contains photos annotated as rapeseed.
- `Non-rapeseed/` contains all other photos.

The value in **`photo_filename`** is the exact image filename. It can be joined with the appropriate directory above to locate the corresponding image. **`photo_link`** is a clickable link to the original GBIF image record in spreadsheet applications that preserve hyperlinks.

## Other columns

| Column | Description |
| --- | --- |
| `gbifID` | Identifier of the associated GBIF occurrence record. |
| `photo_filename` | Filename of the local image file. |
| `photo_link` | Hyperlink to the original image/record source. |
| `label` | Visually interpreted crop type (rapeseed vs non-rapeseed). |
| `bbch_principal` | Manually visually interpreted principal BBCH stage for rapeseed; see above. |
| `pod_stage` | Green-pod/non-green-pod subdivision for BBCH `7-8`; see above. |
| `yearParsed` | Year parsed from the source record metadata. |
| `eventDate` | Observation or event date and time from the source record metadata. |
| `decimalLatitude` | Geographic latitude in decimal degrees from the source record metadata. |
| `decimalLongitude` | Geographic longitude in decimal degrees from the source record metadata. 

