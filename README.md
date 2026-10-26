# EXP.1-IMAGE-HANDLIND-AND-PIXEL-TRANSFORMATION-USING-OPENCV
## AIM:
Write a Python program using OpenCV that performs the following tasks:

Read and Display an Image.
Adjust the brightness of an image.
Modify the image contrast.
Generate a third image using bitwise operations.
## Software Required:
Anaconda - Python 3.7
Jupyter Notebook (for interactive development and execution)
## Algorithm:
Step 1:
Load an image from your local directory and display it.

Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.
Display the original, brighter, and darker images.

Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).
Display the original, lower contrast, and higher contrast images.

Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels

## Program Developed By:
Name: N.KANISHKA

Register Number: 212225230127

## Program:
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('kanish1.jpg', cv2.IMREAD_COLOR)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("KANISHKA")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
image = cv2.imread('kanish1.jpg')
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
line_img = cv2.line(img_rgb, (0, 0), (522, 672), (0, 0, 255), 2) # cv2.line(image, start_point, end_point, color, thickness)
plt.imshow(line_img, cmap='viridis')  
plt.title("KANISHKA")
plt.axis('off')  
plt.show()
image = cv2.imread('kanish1.jpg')
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
circle_img = cv2.circle(img_rgb,(261,336),180,(255,0,255),10) # cv2.circle(image, center, radius, color, thickness)
plt.imshow(circle_img, cmap='viridis')  
plt.title("KANISHKA")
plt.axis('off')  
plt.show()
image = cv2.imread('kanish1.jpg')
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (521, 671), (0, 0, 255), 20)  # cv2.rectangle(image, start_point, end_point, color, thickness)
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("KANISHKA")
plt.axis('off')  
plt.show()
image = cv2.imread('kanish1.jpg')
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
text_img = cv2.putText(img_rgb, "OpenCV Drawing", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (0, 255, 255), 2)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)
plt.imshow(text_img, cmap='viridis')  
plt.title("KANISHKA")
plt.axis('off')  
plt.show()
image = cv2.imread('kanish1.jpg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
image[186:486, 111:411] = [255, 0, 255]  # Rows: 200-499, Columns: 200-499
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
image = cv2.imread('kanish1.jpg')
image.shape
resized_image = cv2.resize(image, (522 // 2, 672 // 2))  # (new_width, new_height)
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
resized_image_rgb.shape
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
image = cv2.imread('kanish1.jpg')
image.shape
roi = image[50:350, 50:350]  # Rows: 50-349, Columns: 50-349
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
image = cv2.imread('kanish1.jpg')
flipped_horizontally = cv2.flip(image, 1)
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
flipped_vertically = cv2.flip(image, 0)
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```

## OUTPUT:
<img width="357" height="492" alt="image" src="https://github.com/user-attachments/assets/1eb0ece4-c9d4-4e6e-9e1a-9dec39872dc9" />
<img width="357" height="497" alt="image" src="https://github.com/user-attachments/assets/2824defc-15c5-4ca9-9b48-a62304442d66" />
<img width="361" height="502" alt="image" src="https://github.com/user-attachments/assets/ea83dd8d-3071-4682-8d9c-7fda8729795d" />
<img width="357" height="487" alt="image" src="https://github.com/user-attachments/assets/e8f48c5c-9b11-4748-a32c-513a6ffe96e6" />
<img width="357" height="487" alt="image" src="https://github.com/user-attachments/assets/ed7857cf-fff2-4a5a-83c4-604ac8988c0c" />
<img width="342" height="487" alt="image" src="https://github.com/user-attachments/assets/1b98ba6c-d918-4b6c-9f4e-a0e692cdf402" />
<img width="362" height="487" alt="image" src="https://github.com/user-attachments/assets/fcf0aa55-0596-4613-8b33-815bc0fd32a7" />
<img width="362" height="492" alt="image" src="https://github.com/user-attachments/assets/cba97fb6-78ee-4ea8-a51a-ef6f42b19a53" />
<img width="357" height="495" alt="image" src="https://github.com/user-attachments/assets/a3aca13b-3406-4aea-aa12-beeb0d6d0162" />
<img width="357" height="500" alt="image" src="https://github.com/user-attachments/assets/80a0feec-3876-4c0b-a442-d7e99f31306b" />
<img width="361" height="496" alt="image" src="https://github.com/user-attachments/assets/0b3487b4-98f7-43b2-8cd5-0c03244783e9" />
<img width="352" height="487" alt="image" src="https://github.com/user-attachments/assets/44d2fc0f-03dc-410d-be84-58842b2334c1" />
<img width="402" height="482" alt="image" src="https://github.com/user-attachments/assets/1b8d77f3-daf4-4086-8d54-855040a52708" />
<img width="356" height="490" alt="image" src="https://github.com/user-attachments/assets/d6cb707e-73de-4aff-a77e-e615e6e4bef2" />
<img width="362" height="500" alt="image" src="https://github.com/user-attachments/assets/52381087-82a3-46c4-af9f-f5d83ec085ab" />

## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.



