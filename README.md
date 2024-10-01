# Perception Challenge
2024 Wisconsin Autonomous Perception Challenge
![answer](https://github.com/user-attachments/assets/c00f6921-976a-4bad-a666-fa063ede227f)

# Methodology
I first converted the image into HSV because it separates image intensity from color information.
I then defined color thresholds and used a 5x5 kernel and blur to remove noise from the image.
Next I used Canny to detect edges in the image and found contours using those edges.
I then used the Ramer-Douglas-Pecker algorithm to simplify the contours.
Next, I found convex hulls and checked that the hulls that were found had 3-to-10 points.
After that, I got rid of hulls that were facing the wrong way.
I used least squares regression to get parameters for the best fit line for the lanes and generated them.

# What Did I try and Why I Think it Didn't Work.
I tried using grayscale instead of HSV but there were no contours found. If I had spent more time tweaking the parameters I could have made it work.

# What Libraries I Used
I used the following Python libraries:
OpenCV, NumPy, Matplotlib, SciPy
