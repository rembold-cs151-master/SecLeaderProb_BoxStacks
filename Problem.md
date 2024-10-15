# Box Stacking

You are presented a situation wherein you have a snapshot of a side view of a collection of rectangular boxes which are in free fall. The boxes are magical, which gives them two particularly special properties:

- They are perfectly aligned to a grid, with sizes and shapes all multiples of the grid size.
- They will not tip. If any part of the box is supported by something beneath, then it is stable in that position.

You have a file with data on the current state of the boxes, including position, size, and color, that looks like:
```
1,2,2,2:#ffffff
4,6,5,7:#00ff00
```
Here, the first two coordinates represent the upper left corner of the box, while the second two coordinates represent the width and height of the box, respectively. Both are in "grid units". The value following the `:` represents the color of the box. So for example, the first line would indicate a 2x2 white box, while the second would represent a 5x7 green box.

Your overall goal here is to determine the area of the minimal bounding box enclosing all the rectangles once they have dropped. To add to the visual though, you want this to be a bit interactive. Thus, your series of task looks like:

- [ ] Visualize the boxes all in a PGL window
- [ ] Whenever the mouse is clicked, the lowest unstabilized box is "dropped", moving download until it contacts either the bottom of the window or a box beneath it. This should be animated.
- [ ] Once all the boxes have been dropped, clicking the mouse one more draws the bounding box to the GWindow and prints the area (in grid units) to the console.


Some things to keep in mind:
- The bricks were all generated in a window 12 grid units wide and 25 grid units tall.
- All the values in the text file are in grid coordinates. You'll likely want to scale that to your PGL window, unless you want to work with the tiniest visualization.
- What parts of the gridded shape will you need to check for collisions for? While it is generally more than a single point, it isn't a huge number.
- As you are dropping your boxes and looking for collisions, you might be a pixel or two off at times depending on how fast you are dropping the boxes. That should be ok, you'll just need to round your eventual grid unit area
- The repo has a screenshot of what the starting and ending state of the clicking should look like for the `bricks1.txt` file.
