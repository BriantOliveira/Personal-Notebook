**Edge Detection** - Identifying sharp changes in intensity in adjacent pixels.

**The canny edge detection technique**

The goal of edge detection is to identify the boundaries of objects within images.

In essence we'll be using a detection to try and find regions in an image where there is a sharp change in intensity a sharp change in color before diving into this.

It's important to recognize that an image can mirror it as a matrix an array of pixels a pixel contains

the light intensity at some location in the image.Each pixels intensity denoted by a numeric value that ranges from 0 to 255 and intensity value of zero

indicates no intensity.

```
[0 0 255 255]
[0 0 255 255]
[0 0 255 255]
[0 0 255 255]
```

If something is completely black Where s 255 represents maximum intensity something being completely. What's that being said gradient is that the change in brightness over a series of pixels. A strong gradient indicates a steep change whereas a small gradient represents a shallow change on the right hand side and you're looking at the gradient of the soccerball the outline of white pixels corresponds to the discontinuity in brightness at the points the strengthen gradient.

This helps us identify edges in our image since an edge is defined by the difference in intensity values in adjacent pixels.And wherever there is a sharp change in intensity a rapid change in brightness wherever there is a strong gradient there is a corresponding bright pixel in the gradient image by tracing out all of these pixels we obtain the edges.

We're going to use this intuition to detect the edges in our road image.This is a multi-step process.

**Step one** being to convert our image to grayscale. Why convert it to grayscale. Well as we discussed earlier images are made up of pixels. A three channel color image would have red green and blue channels each pixel a combination of three intensity values whereas a greyscale image only has one channel each pixel with only one intensity value ranging from 0 to 255.

The point being by using a grayscale image processing a single channel is faster than processing a three channel color image and less computational intensive. Let's start implementing this inside of them. We've already loaded and read our image into an array. Now what we'll do is import numb pie as the alias and P We're going to work with a copy of this array by setting a link image is equal to pie dog copy image.

Thus copying our array into a new variable it's imperative that you actually make a copy of the array instead of just setting lane image is equal to image. If we do this any changes we make to Lane image will also be reflected in the original viewable array.

Always ensure that you make a copy whenever working with a race instead of just setting them equal directly. So what we'll do now is we'll create a grayscale from the color image. We'll do that by setting a variable. Gray is equal to see to and from our open CV library will call the function CVT color which converts an image from one color space to another. We'll be converting lane image. And the second argument for an R G B to grayscale conversion. We can use the flag C-v to dot color underscore R G B to gray. Very intuitive.And now instead of showing the color image will show the gray image. If we go to our terminal Python Layne's that p y everything works out accordingly. This was step number one. Step number two of edge detection will be two.

**Gaussian Blur**

**Step two** is to now reduce noise and smooth in our image when detecting edges while it's important to accurately catch as many edges in the image as possible. We must filter out any image noise image noise can create false edges and ultimately affect edge detection. That's why it's imperative to filter it out and thus smoothen the image filtering out image noise and smoothing will be done with a Gaussian filter to understand the concept of a Gaussian filter. Recall that an image is stored as a collection of discrete pixels. Each of the pixels for a greyscale image is represented by a single number that describes the brightness of the pixel. For the sake of example how do we smooth in the following image.

_**The typical answer would be to modify the value of a pixel with the average value of the pixel intensities around it. Averaging out the pixels in the image to reduce noise will be done with the kernel. Essentially this kernel of normally distributed numbers is run across our entire image and sets each pixel about equal to the weighted average of its neighboring pixels thus smoothing our image**_. We're not going to go over kernel convolution and how it does it just know that when we write this line of code inside of our editor blur is equal to C-v to dog Gosden blur what we're doing is applying a gaussian blur on a greyscale image with a 5 by 5 kernel the size of the kernel is dependent on specific situations a 5 by 5 kernel is a good size for most cases.

But ultimately what that will do is returning a new image that we simply called blur. Applying the gaussian blur by involving our image with a kernel of Gaussian values reduces noise in our image back to our project set. Blur is equal to C-v to the gaussian blur. **We'll apply this blur in our gray scale image with our 5 by 5 kernel and we'll just leave the deviation is zero.**

The main thing you should take away from this is that we're using a gaussian blur to reduce noise in our greyscale scale image and now will simply show the blurred image. If we run this code Python Laine's dot p why there is our blurred greyscale image later on when we apply the Kenni method. It should be noted that this step was actually optional since the kidney function is going to internally apply a 5 by 5 Gaussian when we call it regardless. Now we know the theory with a 10 hour grayscale with smoothen data and reduced noise with a gaussian blur.

```
Strong Gradient        Small Gradient 
[0 0 255 255]            [0 0 20 20]
[0 0 255 255]            [0 0 20 20]
[0 0 255 255]            [0 0 20 20]
[0 0 255 255]            [0 0 20 20]
```



