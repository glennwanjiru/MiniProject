# CCTV Feed Description App

![App Banner](banner.png)

## MiniProject

### Members
- **Kennedy Ngugi** - CS/MG/2134/09/20
- **Shedrack Wambua** - CS/MG/2043/09/21
- **Glenn Wanjiru Njoroge** - CS/MG/2418/09/20

---

This application helps blind users by describing their surroundings using images captured from their CCTV feed or webcam. The app leverages the BLIP (Bootstrapping Language-Image Pre-training) model to generate detailed captions for the images and converts the captions to speech for auditory notification.

## Features

- **Open Image**: Select an image file from your computer to generate a caption.
- **Capture Photo**: Use your webcam to capture an image and generate a caption.
- **Text-to-Speech**: Captions are read aloud for auditory notifications.
- **Progress Bar**: Visual feedback during image processing.

## Prerequisites

- Python 3.6 or higher
- [PyTorch](https://pytorch.org/)
- [Transformers](https://huggingface.co/transformers/)
- [Pillow](https://python-pillow.org/)
- [OpenCV](https://opencv.org/)
- [pyttsx3](https://pyttsx3.readthedocs.io/)
- [ttkthemes](https://ttkthemes.readthedocs.io/)

## Installation

1. **Clone the repository**
    ```sh
    git clone https://github.com/glennwanjiru/cctv-feed-description-app.git
    cd cctv-feed-description-app
    ```

2. **Create and activate a virtual environment**
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install required packages**
    ```sh
    pip install -r requirements.txt
    ```

4. **Download BLIP model and processor**
    ```python
    from transformers import BlipProcessor, BlipForConditionalGeneration
    processor = BlipProcessor.from_pretrained("Salesforce/blip-image-captioning-large")
    model = BlipForConditionalGeneration.from_pretrained("Salesforce/blip-image-captioning-large")
    ```

## Running the App

1. **Activate the virtual environment**
    ```sh
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

2. **Run the application**
    ```sh
    python app.py
    ```

## Usage

- **Open Image**: Click on the 'Open Image' button to select an image from your computer. The app will generate and display a caption, and read it aloud.
- **Capture Photo**: Click on the 'Capture Photo' button to take a photo using your webcam. The app will generate and display a caption, and read it aloud.

## Contributing

Contributions are welcome! Please fork this repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

**Note**: This app is designed to aid blind users by providing auditory descriptions of their surroundings using image captions. Please ensure your webcam is properly connected and functional for capturing photos.




