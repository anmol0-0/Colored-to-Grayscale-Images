# Colored to Grayscale Conversion
This Python script provides functionality for converting colored images to grayscale using a web-based interface created with Gradio. It utilizes popular image processing libraries such as OpenCV (cv2) and PIL (Pillow) for image manipulation.

# Functionality
The script performs the following tasks:

1. Reads an input image from the file path provided.
2. Converts the input image from colored to grayscale using OpenCV.
3. Converts the grayscale image to a Gradio-compatible format (PIL Image).
4. Displays the original colored image and the grayscale converted image in a web interface.
5. Allows users to upload a colored image, view the grayscale conversion in real-time, and download the resulting image.

# Libraries Used
- OpenCV (cv2): Used for reading and processing images.
- NumPy: Utilized for numerical operations on arrays.
- Gradio: Provides tools for creating web-based interfaces for machine learning models and image processing tasks.
- PIL (Pillow): Used for converting images between different formats and manipulating images.

# Usage
To use the script:
1. Ensure you have Python installed on your system.
2. Install the required libraries by running: pip install opencv-python numpy gradio pillow
3. Run the Python script.
4. Once the script is running, access the provided web interface by navigating to the URL displayed in the terminal.
5. Click the image icon, select a colored image from your device, and observe the grayscale conversion in real-time.
6. Download the resulting grayscale image using the provided download button.

# Note
- The script is configured to use the "gradio/monochrome" theme for the interface, providing a clean and minimalistic design.
- The interface is set to enable live updates, allowing users to see the grayscale conversion as they upload the image.
