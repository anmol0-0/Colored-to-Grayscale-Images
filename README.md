import cv2
import numpy as np
import gradio as gr
from PIL import Image

def read_image(impath: str) -> np.ndarray:
    raw_image = cv2.imread(impath)
    return raw_image

def convert_to_grayscale(color_img: np.ndarray) -> np.ndarray:
    gray_img = cv2.cvtColor(color_img, cv2.COLOR_RGB2GRAY)
    return gray_img

def convert_image_to_grayscale(input_image):
    # Convert Gradio Image to numpy array
    input_np = np.array(input_image)

    # Perform grayscale conversion using your function
    grayscale_img = convert_to_grayscale(input_np)

    # Convert the result back to Gradio-compatible format (PIL Image)
    result_pil = Image.fromarray(grayscale_img)

    return result_pil

# Create Gradio Interface
iface = gr.Interface(
    fn=convert_image_to_grayscale,
    inputs=gr.Image(),
    outputs=gr.Image(),
    live=True,
    title="Colored to Grayscale Conversion",
    description="Click image icon, select colored image, AI converts to grayscale, download result.",
    theme="gradio/monochrome"
)

# Deploy the Gradio interface as a web app
iface.launch(share=True)

