# CoWTracker

CoWTracker is a high-quality dense point tracker. It tracks all image points jointly without computing feature correlations, but by means of a warping module.

## Reference frame

Let `W` and `H` be, respectively, the width and height of an image in pixels. CoWTracker assumes that (0,0) is the coordinate of the top-left corner of the top-left pixel, and (W,H) the coordinate of the bottom-right corner of the bottom-right pixel. This means that the coordinates of the center of the top-left pixels are (0.5,0.5).

Many trackers use different a convention where (0,0) is the coordinate of the center of the top-left pixel. Our choice makes it easier to handle scaling (if the image is scaled by a factor `s`, then the same factor applies to the point coordinates).
