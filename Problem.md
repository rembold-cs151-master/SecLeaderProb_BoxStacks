# Box Stacking

You are presented a situation wherein you have a snapshot of a side view of a collection of rectangular boxes which are in free fall. The boxes are magical, and are thus perfectly aligned to a grid. You have a file with data on the current position of the boxes, that might look something like:
```
1,2-2,2:#ffffff
4,6-5,7:#00ff00
```
Here, the first pair of coordinates represents the upper left grid point of the box, while the second pair of coordinates represents the lower right grid point of the box. The value following the `:` represents the color of the box. So for example, the first line would indicate a 2x1 white box, while the second would represent a 2x2 green box.

Your initial challenge here is to visualize all of the boxes using PGL.
