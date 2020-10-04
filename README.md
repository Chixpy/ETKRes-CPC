# ETKRes-CPC
Resources for Emuteca: Amstrad CPC (Plus)

Icons, images, texts, videos, etc. for use with [Emuteca](https://github.com/Chixpy/Emuteca).

## About Images

### Screenshot, Titles

Rule #1: No filters to screenshots.

All images in .png format at original resolution... CPC has 3 official resolutions without hacking:

* Mode 0: 160×200 pixels with 16 colors (4 bpp) (192×272 with borders)
* Mode 1: 320×200 pixels with 4 colors (2 bpp) (384×272 with borders)
* Mode 2: 640×200 pixels with 2 colors (1 bpp) (768×272 with borders)

A "Mode 3" exists with a trick, wich is a Mode 0 with 4 colors

There a Full Screen Trick that allow to write pixels in border area. So we will stick with *384x272* and
show full border. MODE 0 original pixels will be 2 pixels wide in images.

After all, 384×272 is not 4:3... BUT Amstrad CPC monitor was 286mmx208mm (not 4:3 true)

*TO DO*: ¿MODE 2 images? May be 768x544, but top and bottom border will be doubled and image will be cropped to 768x472 to keep border size.

### Front, Back, Spine, Ads, Reviews, Media, Other

Escaned .jpg; with a maximum of 2048x2048, don't enlarge artificially (if larger, we can resize it to 2048 the larger side, keeping aspect ratio and a quality of 90%). Trying not to do transformations and resave it. Lossless rotation or cropping allowed.

### Icons, Logos

Rule #1: Only 1 image for group or game. No folders with multiple images.

Icons are mainly extracted from game screenshots at original resolution. Usually they are protagonist frames, lives icons or recognizable icon.

Logos are usually extracted from Title or Main Menu screens.

All images are .png format. Width and Height are variable, using it's original size without resizing to a fixed size or adding more border to make it square. Emuteca handle they automatically.

The only time that the image will be scaled is when all 'icon pixels' are 2x2, 3x3, etc. pixels.

After extracting the icon image with transparent background, a border is added: Middle grey, half transparency (128, 128, 128, 128). 

[Emuteca](https://github.com/chixpy/emuteca) has [ETKIconBorder](https://github.com/Chixpy/Emuteca/blob/master/bin/Tools/ETKIconBorder.exe) tool in its distribution. A simple image editor to cut, extract, make transparency in images and apply filters to original image.

Altenatively, there is a GIMP's script too, that can add the border automatically after transparent background is created. But it's slooooow.

Download
--------

Use GIT to clone the repository or download it in zip:

https://github.com/Chixpy/ETKRes-CPC/archive/master.zip