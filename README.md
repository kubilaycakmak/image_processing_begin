# Starting with PGM file to image Processing which file type has no ide to open in Windows.
  Pgm files first 2 or 3 lines has information about file.
  # • The Portable Pixmap Format (PPM)
    This format is for colored images. The image data is specified using red, green and
      blue color values.
  # • The Portable Graymap Format (PGM)
    This format is for grayscale images. It is very similar to PPM with the exception of
      only using one color value to specify the gray intensity.
  # • The Portable Bitmap Format (PBM)
    This format is for monochrome (black and white) images. It contains a
      1's which specify if the color is white(1) or black (0).
      
    These image file formats all share the same syntax and simplicity. The 3 file formats are
practically the same. The only section that will differ between them is the image data
section.
PPM, PGN and PBM can themselves be broken down into 2 variations, they are text
format and binary format. This gives a total of 6 different variations. Each of these file
formats follow the same rules and general syntax. The different file formats are
distinguishable by the first entry in the header. No line in a PPM should exceed 70
characters. Programs should be as accepting as possible when interpreting the 6 file
formats.
The PPM, PGN and PBM header contain the following fields:
• Magic number identifier
• Width
• Height
• Maximum color value (Not present in the PBM file format)
Following the image header is an image data section.
Each entry mentioned above in the header can contain comments and whitespace
intertwined. Each entry must be separated by at least one whitespace. If a character with
a # is encountered anywhere in the file header, the rest of the line (following the #) is
considered to be a comment. A comment can appear anywhere in the file header.
Magic number identifier
This field always contains 2 characters (16 bits) and can have 6 possible values
# • 'P1': PBM raster data following the header is interpreted as ASCII text
# • 'P2': PGM raster data following the header is interpreted as ASCII text
# • 'P3': PPM raster data following the header is interpreted as ASCII text
# • 'P4': PBM raster data following the header is interpreted as binary
# • 'P5': PGM raster data following the header is interpreted as binary
# • 'P6': PPM raster data following the header is interpreted as binary

Example of a small PBM in P1 (ASCII text) format
P1
# This image is a 4 x 2 image in text mode
4 2
0 1 1 0
1 1 1 1Example of a small PGM in P2 (ASCII text) format
P2
# This image is a 4 x 2 image in text mode
4 2
255
0
255 128 16
255 127 16 0
Example of a small PPM in P3 (ASCII text) format
P3
# This image is a 4 x 2 image in text mode
4 2
255
255 255 255
0 0
0
255 255 255
0 0
0
0
0
0
255 255 255 0 0
0
255 255 255
Example of a small PBM in P4 (binary) format
P4
# This image is a 2 x 2 image in binary mode
2 2
<binary data>
Example of a small PGM in P5 (binary) format
P5
# This image is a 2x2 image in binary mode
2 2
255
<binary data>
Example of a small PPM in P6 (binary) format
P6
# This image is a 2x2 image in binary mode
2 2
255
<binary data>
  
# source: web
