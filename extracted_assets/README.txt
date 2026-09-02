PPTX ASSET EXTRACTION OUTPUT

Source:
C:\Users\Mushfiq\Downloads\Shebar_Janala_BCOLBD_2026_Claymorphic_Final_31_Slides.pptx

Key files:
- manifest.json: global inventory, hashes, reuse data, summary, and limitations
- validation_report.json: second-pass validation results
- contact_sheet.png: visual index of extracted visual occurrences
- reconstructed_contact_sheet.png: focused index of cards, icons, illustrations, and UI blocks cropped from flattened slides
- slide_XX/manifest.json: slide-specific inventory and transformations
- slide_XX/slide_preview.png: full rendered slide reference
- asset_XX_original.*: unmodified source bytes or native OOXML shape fragment
- asset_XX_rendered.png: rendered occurrence as it appeared on the slide
- asset_XX_reconstructed_*.png: user-authorized crop from a flattened slide; not an independently embedded original

Reusable extractor:
C:\Personal_Endeavours\AccessAI\extract_pptx_assets.py
C:\Personal_Endeavours\AccessAI\segment_flattened_assets.py

Example rerun (use a new or empty output directory):
python extract_pptx_assets.py input.pptx extracted_assets_new --render-script path\to\render_slides.py --render-width 1920 --render-height 1080

Notes:
- Slides 1-20 are flattened raster slides. By explicit user override, their visible cards, icons, illustrations, and UI blocks were extracted as clearly labelled reconstructed crops. Missing/occluded pixels were not invented.
- Slides 21-31 contain native PowerPoint drawing objects. All native objects, including text-bearing shapes, are preserved as OOXML fragments and, where they have a non-zero bounding box, as rendered PNG crops.
- Rendered crops are visual references; original files/fragments remain untouched.
