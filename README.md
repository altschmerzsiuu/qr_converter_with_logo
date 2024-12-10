# QR Code Generator with Optional Logo
This project is a Python-based tool for generating QR codes with or without a logo. It includes features for creating QR codes for any type of data, such as text or URLs, and optionally embedding a centered logo with customizable padding.

## Features
- Generate QR codes for text or URLs.
- Add a logo in the center of the QR code.
- Automatic resizing of logos to fit within the QR code.
- Configurable padding around the logo for enhanced visibility.
- High error correction ensures QR code readability even with embedded logos.

## Installation
### Prerequisites
Ensure you have Python installed (Python 3.6 or later is recommended). Install the required libraries:
- ```bash
  pip install qrcode[pil] pillow

## Usage
### Running the Script
1. Clone or download the repository.
2. Open a terminal and navigate to the directory containing the script.
3. Run the script using:
   - ```bash
     python qr_code_generator.py

### Inputs
- Data: Enter the text or URL to encode in the QR code.
- Logo Path (Optional): Enter the file path of the logo to embed in the QR code. Leave blank to skip adding a logo.
- Encode as URL: If the data is a URL, the script can specifically encode it as a URL-friendly QR code.

## Code Features
### Functions
1. generate_qr_code_with_logo
    - Generates a QR code and embeds a logo at the center if a path is provided.
    - Parameters:
        - `data`: The data to encode in the QR code.
        - `filename`: Filename to save the QR code image (default: qrCode.png).
        - `box_size`: Size of each box in the QR code grid (default: 10).
        - `border`: Size of the QR code border (default: 2).
        - `logo_path`: Path to the logo image.

2. generate_qr_for_url
      - Encodes a URL into a QR code.
      - Parameters:
        - `url`: The URL to encode.
        - `filename`: Filename to save the QR code image (default: qrCodeForURL.png).
 
### Examples
1. Generate a Simple QR Code
      - Input:
        ```bash
        Enter the data to be encoded in the QR code: Hello, World!
        Enter the path to the logo image file (optional):
        
      - Output:
        Generates a QR code saved as `qrCode.png`.

2. Generate a QR Code with Logo
      - Input:
        ```bash
        Enter the data to be encoded in the QR code: Welcome to GitHub!
        Enter the path to the logo image file (optional): path/to/logo.png
        
      - Output:
        Generates a QR code with the specified logo saved as `qrCode.png`.

3. Generate a QR Code with Logo
      - Input:
        ```bash
        Enter the data to be encoded in the QR code: https://github.com
        Enter the path to the logo image file (optional): 
        Do you want to encode a URL (y/n)? y
        
      - Output:
        Generates a QR code for the URL saved as `qrCodeForURL.png`.

## Output Files
- The QR codes are saved as PNG images in the current directory.
- Default filenames are:
    - `qrCode.png` (simple QR codes or with logos).
    - `qrCodeForURL.png` (URL-specific QR codes).
 
## Notes
- Ensure the logo image file is in PNG format for optimal results.
- The script adjusts the logo size dynamically to ensure the QR code remains scannable.

## Acknowledgments
This project uses the following libraries:
- qrcode: For generating QR codes.
- Pillow: For image manipulation and logo embedding.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
