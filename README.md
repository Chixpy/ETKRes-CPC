# ETKRes-CPC

Resources for Emuteca: **Amstrad CPC (Plus)**

Icons, images, texts, videos, etc. for use with [Emuteca](https://github.com/Chixpy/Emuteca).

## Download

Use GIT to clone the repository or download it in zip:

https://github.com/Chixpy/ETKRes-CPC/archive/master.zip

## About Emuteca's Media search.

You can read more about media files in [Emuteca's Web Page](https://chixpy.github.io/Emuteca/pages/Media-Files.html) (but it's in Spanish...)

Emuteca will search media of games and groups in the next order in selected folder. But only de first hit:

  1. All suported files inside a subfolder named as SortTitle of the game. `MediaFolder\SoftSortTitle\*.ext` (`.ext` can be any supported media extension)
  2. All suported files inside a compresed archive named as SortTitle of the game. `MediaFolder\SoftSortTitle.zip\*.ext` (`.zip` can be any supported compressed extension and all files will be extracted in a temporal folder.)
  3. Single file with named as SortTitle of the game and a supported media extensión.    `MediaFolder\*.ext`
  4. Step 1 to 3 with SortTitle of the game's group.
  
Note: Maybe be, some day, support for compressed file (Point 2) will be removed...

## About Images

### Screenshot, Titles

  - **Rule #1**: No filters to screenshots.
  - **Rule #2**: There is not need to make a ZIP, 7Z or CBX with groups of images.

All images in .png format at original resolution: CPC has 3 official resolutions without hacking:

* Mode 0: 160×200 pixels with 16 colors (4 bpp) (192×272 with borders)
* Mode 1: 320×200 pixels with 4 colors (2 bpp) (384×272 with borders)
* Mode 2: 640×200 pixels with 2 colors (1 bpp) (768×272 with borders)
A "Mode 3" exists with a trick, wich is a Mode 0 with 4 colors
There is a Full Screen Trick that allow to write pixels in border area. So we will stick with *384x272* and show full border.
* MODE 0: 384×272. Original pixels will be 2 pixels wide in images.
* Mode 1: 384×272.
* MODE 2: It's needed to use *768x544* to keep pixel accuracy. Original pixels will be 2 pixels height in images.


### Front, Back, Spine, Manual, Media, Maps, Reviews, Ads, Other

Emuteca have ETKMagCut and ETKPDF2CBX to help cutting magazine texts 

Generally (except digital maps):

  - `.jpg` images
  - Maximum of 2048px in its largest side, if its smaller don't scale it up.
  - If it's larger than 2048px, it's best to crop (see below) before scaling it down to 2048. 
  - Keeping aspect ratio.
  - Trying not to resave it many times. There are some transformations that can be done without lossing quality...

For game's media (Front, Back, Spine, Manual and Media):

  - Box Front, Back and Spine in separated images and cropped without any border. 
  - Media: Whole cart, CD, etc. scanned and cropped without any border (if possible)

For Magazine texts:

  - Crop original page image to article text, game images and box arts, with a little border.
  - Ignore background or another kind pictures.
  - If in the cropped image there are parts of text from another game can be *deleted*. (ETKMagCut have a button to clear a delection, ideally must be transparent...)
  - One page each image, unless some text or a images is cut.

For Maps (or magazine game guides):

  - If it's a magazine game guide: Same as Magazine texts.
  - If it's a digital map (made with screenshots or similar): Better in .png format and **keep as is** (do not remove author, or other info; and if it's bigger than 2048px keep the size too).

### Icons, Logos

  - **Rule #1**: Only 1 image for group or game. No folders with multiple images.

Icons are mainly extracted from game screenshots at original resolution and usually they are protagonist frames, lives icons or recognizable icon.

Logos are usually extracted from Title or Main Menu screens.

All images are .png format. Width and Height are variable, using it's original size without resizing to a fixed size or adding more border to make it square. Emuteca handle they automatically.

The only time that the image will be scaled is when all 'icon pixels' are 2x2, 3x3, etc. pixels.

After extracting the icon image with transparent background, a border is added: Middle grey, half transparency (128, 128, 128, 128). 

[Emuteca](https://github.com/chixpy/emuteca) has [ETKIconBorder](https://github.com/Chixpy/Emuteca/blob/master/bin/Tools/ETKIconBorder.exe) tool in its distribution. A simple image editor to cut, extract, make transparency in images and apply filters to original image.



## About Texts

Texts must be raw UTF8 text: .txt

Better if:

  - No UTF8 Bit Order Mask (BOM)
  - Empty line between paragraphs.
  - No new line inside paragraphs (Textbox has wordwrap activated).
  - Maybe Markdown fortmat is good, too.
  
