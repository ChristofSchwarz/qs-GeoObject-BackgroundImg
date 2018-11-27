# qs-GeoObject-BackgroundImg
Using Qlik Sense's native GeoObject together with any office/shop/plant plan image

__New: 27-Nov-2018__, now possible up to zoom level 4 (4096x4096 pixels)

The steps are explained here in this video https://youtu.be/4uWlmNm95n8

The approach in a nutshell:
 * you have a background image of a floor/shop/office/whatever plan (a yacht ;-) which you want to use as a background to visualize data on (e.g. sensor positions)
 * your plan image will be sliced into pieces of 256x256 pixels in such a manner as if it was a new geo-tile-server
 * the tiles will be loaded into Qlik Sense own content library and with the help of the code snippets attached here, you can use the Point Layer of the native Geo Object to show data as if it was geographic data
 * the Geo Object needs to be properly configured to work with "meter" data instead of a Mercato projection
 * to create the slices I am using a freeware portable version of ImageMagick available here https://imagemagick.org/script/download.php
 * to compute the right commands (it is a command-line operated tool) I am attaching an Excel, which does that job
 
 Follow the 11 - 13 minutes video above. Enjoy
 
 ![alt text](https://github.com/ChristofSchwarz/qs-GeoObject-BackgroundImg/raw/master/projection.png "Screenshot")
