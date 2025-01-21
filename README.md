

# Face Detection  
Basic face detection program  

Using the libraries of `cv2` and `pathlib`, I was able to figure out a program that simply detects a face.  
Now I'll explain the code by grouping it.  

First, part of the code is importing the libraries themselves.  
Second is creating a variable called `cascade_path` that equals `pathlib.Path`, which looks for a file to give you the exact location of the file you are looking for. In this case, it is `data/haarcascade_frontalface_default.xml`.  

Next, I created the `clf` that contains the `CascadeClassifier` and converts it into a string.  
Then I created a `while` loop that contains the code to open and convert the color into gray (the program runs better with gray than color), and created the actual `faces` variable that detects faces and puts a square around them.  

Along with that, I've added a name box to go with the square detecting the face, using the `for` loop and the x, y measurements in the `faces` variable. It also detects the face but labels the box as "Face".  

Using the x and y, which create the top-left corner of the rectangle, we simply copied that for the length and width of the square.  

Finally, `cv2.imshow("Faces", frame)` allows for updates to happen in real time.  
The `if` statement says if `waitKey(1)` is equal to the key bind "q", then break.  

