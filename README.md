# Image Steganography with Python

This project demonstrates basic image steganography techniques using Python and the OpenCV library. It allows you to embed and extract text messages within image files.

## Prerequisites

* Python 3.x
* OpenCV (cv2) library: `pip install opencv-python`

## Usage

1.  **Clone the repository (optional):**
    ```bash
    git clone [repository_url]
    cd [repository_directory]
    ```
2.  **Place your image:**
    * Place the image you want to use for steganography in the same directory as `stego.py`.
    * Modify the `img = cv2.imread("mypic.jpg")` line in `stego.py` to reflect your image's filename.
3.  **Run the script:**
    ```bash
    python stego.py
    ```
4.  **Embedding:**
    * You will be prompted to enter a secret message and a password.
    * The script will embed the message into the image and create a new image named `encryptedImage.jpg`.
5.  **Extraction:**
    * Run the script again.
    * When prompted for the password, enter the same password used during embedding.
    * The script will extract and display the hidden message.
6. **Platform specific image opening:**
    * The script uses `os.system("start encryptedImage.jpg")` to open the image. This command is for windows. If you are on linux, or MacOS, you must change this command to the appropriate command for your OS. For example on linux, you can use `os.system("xdg-open encryptedImage.jpg")`.

## Code Explanation

* The script uses Least Significant Bit (LSB) steganography, where the message characters are encoded into the least significant bits of the image's pixel values.
* A password is used for basic authentication.
* OpenCV is used for image reading and writing.
* Dictionaries are used to map characters to their ASCII values and vice-versa.

## Improvements

* **Error Handling:** The code could be improved with more robust error handling (e.g., handling file not found, invalid input).
* **More Robust Steganography:** More advanced techniques like DCT-based steganography could be implemented.
* **Encryption:** Adding a stronger encryption algorithm before embedding the message would greatly increase security.
* **GUI:** A graphical user interface could be added for easier use.
* **Robustness:** The current implementation is very fragile. Adding error correction would increase resilience.
* **Platform Independence:** Making the image opening command platform independent.

## Disclaimer

This project is for educational purposes only. Steganography should be used responsibly and ethically.
