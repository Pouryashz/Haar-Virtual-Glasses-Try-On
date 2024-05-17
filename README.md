Haar Virtual Glasses Try-On

Overview:
Haar Virtual Glasses Try-On is a Python project that allows users to try on virtual glasses on their faces in photos. The project utilizes Haar cascades for face and eye detection to accurately place virtual glasses on detected faces.

This version of the project focuses on implementing the virtual glasses try-on functionality for photos. Future versions will extend this functionality to videos, enabling real-time virtual glasses overlay.

Features:
- Detects faces and eyes in photos using Haar cascades.
- Places virtual glasses on detected faces, adjusting size and position based on eye locations.
- Support for transparent glasses images with an alpha channel.

Installation:
1. Clone the repository:
   git clone https://github.com/your_username/Haar-virtual-glasses-tryon.git
2. Install the required dependencies:
   pip install opencv-python

Usage:
1. Ensure you have Python installed on your system.
2. Navigate to the project directory.
3. Place your input image (with a face) in the same directory.
4. Run the script:
   python virtual_glasses_tryon.py
5. The output image with virtual glasses overlaid on the face will be displayed.

Contributing:
Contributions are welcome! Feel free to open issues or pull requests for any improvements or additional features you'd like to see in the project.

License:
This project is licensed under the MIT License.
