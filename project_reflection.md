## Project Reflection

The pipeline that I have built is based on learning of previous classes. We are given a set of 
predefined and commonly used funtions that we separately used in previous quizze to understand
process of detectin lane lines.

In my pipeline, I have applied these concepts together to have lane detection available in 
videos. 

### Step 1
Read images - This process reads the input image object into memory. By reading it into 
memory, we can manipulate images like a matrix since a image is basically a large matrix of pixels. 

### Step 2
Grayscale - This process converts a colored image to grayscale. By doing this, we can narrow our
search for detecting edges to fewer colors and apply a more focused approach. 

### Step 3
Gaussian blur - We blur out the image so that we can remove the noise and have a smoother image
with lesser contrasts to work with. I have used a kernel size of 7 which in retrospective
and based on project feedback is a bit high since it adds more noise. Because a larger Kernel 
covers more space I wanted to test how that would affect the line detecting. I will change 
the kernel size to 3 so that we can remove more noise. 

### Step 4
Applying Canny edge detection algorithm. This steps helps us detect edges in the image. 
Since lines are also edges of a surface, this step helps us futher focus on things that are
important in our image. By detection edges and removing curved edges, we can keep only 
straight line edges in our image.

### Step 5
Hough Lines. This steps takes as input the image with edges detected and gives us a set of lines.
We then plot these lines over the image to highlight the detected lines. We give as input
several parameters that determine what kinds of edges will make into our output of set of lines.

### Step 6
We draw our detected lines over the original image. This gives us an output image as the original 
image with our detected lane lines superimposed over the original image.

I am not an expert python programmer (but I am a hacker). I have tried to keep things simple and get
them to work. I did not focus much on keeping code clean and refactored as I am more interested
in understanding how the process of lane detection works. I am good at OOP and can refactor my 
solution to be much better and cleaner but for the purpose of this submission I did not spend 
too much time on it. 

### What could be better?

Once a step worked well, I did not go back and change those params. Because kernel size worked well 
for a lot of the test images, I did not try and change it. I could have spent more time on this but
I prefer getting quicker feedback from project reviewer. I will apply recommendations and try
and clean up the code to be more "pythonic".

I will also find some better ways of extrapolation and see if that helps build a more robus pipeline.


Thanks!
