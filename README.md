<h1 align="center">Digital-Image-Recording-via-Web-Camera</h1>

## Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
<br>Use cv2.VideoCapture(0) to access web camera.

### Step 2:
<br>Use cv2.imread to read the video or image.

### Step 3:
<br>Use cv2.imwrite to save the image.

### Step 4:
<br>Use cv2.imshow to show the video.

### Step 5:
<br>End the program and close the output video window.

## Program:
```
### Developed By: Pradeep kumar G
### Register No: 212223230150
```
## i) Write the frame as JPG file
```py
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_frame.jpg", frame)
cap.release()

captured_image = cv2.imread('captured_frame.jpg')
plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()
```



## ii) Display the video
```py
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```



## iii) Display the video by resizing the window
```py
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```



## iv) Rotate and display the video
```py
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```
## Output

### i) Write the frame as JPG image
</br>
<img width="629" height="510" alt="image" src="https://github.com/user-attachments/assets/18da6bd3-1e33-4c6e-bb45-c17873ce952a" />
</br>

### ii) Display the video
</br>
<img width="622" height="469" alt="image" src="https://github.com/user-attachments/assets/e4c7d1a1-4eb7-4f08-a18a-d91f83d08289" />
</br>

### iii) Display the video by resizing the window
</br>
<img width="309" height="465" alt="image" src="https://github.com/user-attachments/assets/9539a6ef-fe10-4a01-b5a0-900bfd5af908" />
</br>

### iv) Rotate and display the video
</br>
<img width="349" height="463" alt="image" src="https://github.com/user-attachments/assets/e3106f00-e48c-4734-b4e3-a9d52f736195" />
</br>

## Result:
Thus the image is accessed from webcamera and displayed using openCV.
