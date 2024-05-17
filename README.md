# Haar Virtual Glasses Try On

This Python script uses OpenCV to detect faces and eyes in an image, and overlays a pair of sunglasses on the detected face. The sunglasses are automatically scaled and positioned based on the distance between the detected eyes, allowing users to virtually try on glasses.

## Requirements

- Python 3.x
- OpenCV (cv2) library
- Haar cascade classifiers for face and eye detection (`haarcascade_frontalface_default.xml` and `haarcascade_eye.xml`)
- Input image (`Male.jpg`)
- Sunglasses image with an alpha channel (`glasses.png`)

## Usage

1. Install the required libraries (OpenCV) if not already installed.
2. Place the input image (`Male.jpg`) and the sunglasses image (`glasses.png`) in the same directory as the script.
3. Ensure that the Haar cascade classifiers (`haarcascade_frontalface_default.xml` and `haarcascade_eye.xml`) are also in the same directory or update the file paths accordingly.
4. Run the script.
5. The script will display the input image with the overlaid sunglasses on the detected face.
6. Press any key to close the window.

## How it Works

1. The script loads the Haar cascade classifiers for face and eye detection.
2. It reads the input image (`Male.jpg`) and the sunglasses image (`glasses.png`) with an alpha channel.
3. The face detection algorithm is applied to the input image, and for each detected face:
  - The face region is extracted from the grayscale and color images.
  - Eye detection is performed within the face region.
  - The centers of the detected eyes are calculated and stored.
4. If two eyes are detected, the script calculates the average position of the eyes and determines the dimensions of a rectangle around the eyes.
5. The sunglasses image is scaled based on the dimensions of the rectangle, while maintaining the aspect ratio. The scaling factor is limited to a range of 0.5 to 2.
6. The scaled sunglasses image is positioned between the detected eyes, centered horizontally and vertically.
7. If the sunglasses dimensions are larger than the face region, the sunglasses are resized to fit the face region.
8. The sunglasses image is blended onto the input image using alpha blending, preserving the transparency of the sunglasses image.
9. The resulting image with the overlaid sunglasses is displayed using OpenCV.

## Note

The script assumes that the input image (`Male.jpg`) and the sunglasses image (`glasses.png`) are present in the same directory as the script. If the file paths or names are different, update them accordingly in the script.
