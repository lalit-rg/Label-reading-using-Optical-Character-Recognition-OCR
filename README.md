# Label-reading-using-Optical-Character-Recognition-OCR
This project focuses on using the OpenCV library and Tesseract OCR (Optical Character Recognition) to perform text recognition on live video feed from a camera.

Here's an explanation of the code:

1. Importing Libraries:
   - `cv2`: It is the OpenCV library for computer vision and image processing.
   - `pytesseract`: It is a Python wrapper for Tesseract OCR.

2. Setting Tesseract OCR Path:
   - `pytesseract.pytesseract.tesseract_cmd`: It sets the path to the Tesseract OCR executable file.

3. Defining Text Recognition Function:
   - `recText(img)`: It takes an image as input and uses Tesseract OCR to extract text from the image.

4. Initializing Variables:
   - `cam = cv2.VideoCapture(0)`: It initializes the video capture object to read frames from the camera (device index 0).

5. Text Recognition Loop:
   - The code enters a loop to continuously read frames from the camera, convert them to grayscale, and perform text recognition.
   - `cam.read()`: It reads a frame from the camera.
   - `cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)`: It converts the frame to grayscale.
   - `recText(img)`: It calls the text recognition function to extract text from the grayscale image.
   - The extracted text is assigned to the variable `info`.
   - The frame is displayed using `cv2.imshow()`.
   - The loop continues until the 'Esc' key is pressed.

6. Exiting the Program:
   - `cam.release()`: It releases the camera.
   - `cv2.destroyAllWindows()`: It closes all windows.

This project demonstrates a basic implementation of text recognition using Tesseract OCR and OpenCV. It allows real-time extraction of text from the camera feed, which can be useful for various applications such as document scanning, text extraction from images, or real-time text processing.
