# Translate & Fit for Illustrator

Export the text of an Adobe Illustrator document to XLIFF for your translation tool, import the translation into the same document with the formatting inside each paragraph, and fit the text that no longer fits its frame, within limits you set.

This page is the help and trial page for the Adobe Exchange version (a panel). The source code is not published here.

## Free trial

Download `TranslateFit_Trial_v1.0.0.zip` from [Releases](https://github.com/linguist-coder/translate-fit/releases/latest).

- Export, Check overset and pseudo-translation are unlimited.
- Import writes up to 20 paragraphs per document, and Fit fits up to 10 frames per document, counted across runs.
- The sample document in the zip is not limited, so you can try the whole round trip on it.
- The trial is a script: choose **File > Scripts > Other Script...** and select `TranslateFit_Trial.jsx`. Instructions are in `QUICK-START-TRIAL.md` inside the zip.

The full version is a panel on Adobe Exchange (**Window > Extensions > Translate & Fit** after installing).

## How it works

1. Save the document. In the panel, click **Export XLIFF** and enter the language codes. Send the `.xliff` to the translator and keep the `.tfmap` file.
2. When the translation comes back, click **Import translated XLIFF**. Every paragraph is checked first (tags, line breaks, missing or edited paragraphs, fonts). If a problem is found, it is listed and nothing is imported.
3. Click **Check overset** to list the frames whose text does not fit. **Select frame** takes you to each one.
4. Click **Fit overset text**. Tracking, then horizontal scale, then font size go down within the limits you set, and stop as soon as the text fits. A frame that cannot fit is put back exactly as it was and listed.
5. Review every page, then use **File > Save As**. The extension does not save the document.

**Pseudo-translation** makes a longer test XLIFF from your export, so you can check how the layout responds before the real translation arrives.

## Formatting tags

Each paragraph is one translation unit. Bold, italic, color and size changes inside a paragraph become tags such as `<g id="1">two years</g>`. The translator keeps each tag around the matching words. Threaded text frames are exported as one story.

## Requirements

- Adobe Illustrator 2026
- Windows (macOS has not been tested)
- The document must be saved before you export. The files are written next to it.
- The fonts for the translated text must be installed.

## Notes

- To discard an import or Fit run, close the document without saving or choose File > Revert. Illustrator cannot undo the whole run in one step.
- Point text is not checked for overflow.
- Text converted to outlines and text inside images are not exported.
- Right-to-left and vertical text have not been tested.

## Support

hi@linguist-coder.com

## Legal

- [License (full version)](LICENSE.md)
- [Privacy](PRIVACY.md)

Adobe and Illustrator are trademarks of Adobe Inc. This product is not made or endorsed by Adobe.
