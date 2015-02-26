## Website Performance Optimization portfolio project

Please see below the list of changes made to the portfolio in order to improve performance.

### Pagespeed

1. I moved the scripts to the bottom of the body to stop render blocking.

2. I moved the style.css inline and changed the google fonts call to an @font-face query which drastically improved load times.

3. I created a second pizzeria image and scaled it down to 100px wide using GIMP (after optimsing the image with a windows tool), then I put this in the img directory and removed the style tag to set it to 100px, because its always 100px.

4. These changes gave me a page speed score of 95 when hosted on github.io. #### Stangg187.github.io.

I also minified all css and js files to improve load times as well as minifying the inline css code.  All minified code was added to the repo for readability.

### Pizza FPS and Resizing

1. I have commented the areas of code that I have changed, an overview is given below:

2. Moved some calculations out of "for" loops when they only needed to be calculated once.  This was particularly important for the changePizzaSizes function.

3. For both changePizzaSizes and updatePositions I moved the querySelectorAll variables out of the local scope so that they are only calculated once and when needed.

4. For updatePositions I moved a calculation out of the for loop and changed the method for moving the background pizzas to a trasfnorm using translate 3d to make use of the gpu.  This drastically improved paint times and fps.

