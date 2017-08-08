# Imagemagick
ImageMagick is a free and open-source software suite for displaying, converting, and editing raster image and vector image files. 

## Resizing images

#### Resize to 640×480 (maximum width and height), keep the aspect ratio
shell mogrify -resize 640x480 *.jpg`

#### Resize to fixed width of 640, keep the aspect ratio
`mogrify -resize 640 *.jpg`

#### Resize to fixed height of 480, keep the aspect ratio
`mogrify -resize x480 *.jpg`

#### Resize to exact 640×480, change aspect ratio if necessary
`mogrify -resize 640x480! *.jpg`

#### Resize to 50% of original size, keep the aspect ratio
`mogrify -resize 50% *.jpg`

#### Resize images that are less than 640 pixel wide to 640px wide (image wider will be ignored)
`mogrify -resize 640"<" *.jpg`

#### Resize images that are more than 480 pixel height to 480px height (image image shorter will be ignored)
`mogrify -resize x480">" *.jpg`

#### Resize images to no larger than 640×480 (images with width and height less than 640 or 480 will be ignored)
`mogrify -resize 640x480">" *.jpg`

#### Resize images to 100K pixels
`mogrify -resize 100000 *.jpg`

## Converting images

#### Convert all .png to .jpg
`mogrify -format jpg *.png`

#### Convert multiple pages pdf to single png images
convert file.pdf file-%0d.png
