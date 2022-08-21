# Doc-Scanner
This is a project for document scanner which scans a document and gives appropriate output.
You might have used cam scanner or something similar somewhen.
We can make it by ourself using openCV and visual studio.


For that we need to know about openCV a little.
I'll brief you about the commands i used in the code.
>GAUSSIAN BLUR: Gaussian blur is the most commonly used smoothing technique to eliminate noises in images and videos.
Ex gaussianblur(inputimg,outputimg, size(3,3),0).  size(3,3) is size of kernel which refers to strength of blur.

>cvtcolor: This command changes the colour of thr image. 
Ex. cvtcolor(inputimg, outputimg, COLOR_BGR2GRAY). It will output a gray image.

>Canny: It baically detects the edges in the image.
Ex. canny(imgblur, imgcanny, 25, 75). We are taking blur image as our input because there will be less noise in it. 25 and 75 are lower thresold and upper thresold respectively.
If a pixel gradient is higher than the upper threshold, the pixel is accepted as an edge. If a pixel gradient value is below the lower threshold, then it is rejected.

>Erode: It is widely used to remove noises from image. It increases white background thus decreases the area of the object.
Ex. erode(imgDil, imgErode, kernel);

>Dilation: It increases the area of object . It is mostly used when we want to remove noise which will be done be erode, since erode decreases the area, we use dilation first then 
erode.
Ex. dilate(imgCanny, imgDil, kernel);
