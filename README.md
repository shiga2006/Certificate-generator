
Certificate Generation Script
This repository contains a Python script that generates personalized workshop certificates with candidate names and photos, and saves them directly into a PDF file. This project is designed for automating certificate creation for participants of workshops or similar events, saving time and ensuring consistency.

Features
- Automatically generates certificates with personalized details.
- Supports adding candidate photos to certificates.
- Saves all certificates directly into a single PDF file.
- Error handling for missing photos.

Requirements
- Python 3.x
- Required Libraries:
  - `Pillow` (For image processing)
  - `reportlab` (For generating PDF files)
  - `pandas` (For handling the CSV files with candidate data)

You can install these libraries using the following command:

```bash
pip install pillow reportlab pandas
```

 How It Works
1. CSV Input: The script reads candidate details (name, institute, and image file path) from a CSV file.
2. Certificate Template: A base certificate image is used as the template. Candidate details and their photo are added to this template.
3. PDF Output: Certificates are saved directly to a single PDF file without saving individual image files separately.

Input Files
1. CSV File: Contains the candidate names, institute details, and paths to the photo files.
2. Photos: Candidate photos stored locally in the specified file paths.
3. Certificate Template: A predefined template image (JPEG/PNG) used for generating certificates.

Output
The script generates a PDF file containing all the certificates for the candidates listed in the CSV file.

Usage

1. Clone this repository:

```bash
git clone https://github.com/yourusername/certificate-generator.git
```

2. Navigate to the project directory:

```bash
cd certificate-generator
```

3. Ensure that you have a CSV file with the following columns:
   - `Name` (Candidate's Name)
   - `Institute` (Candidate's Institute Name)
   - `Photo` (Path to Candidate's Photo)

   Example CSV structure:

   | Name           | Institute                            | Photo                                         |
   |----------------|--------------------------------------|-----------------------------------------------|
   | PRASANNA E     | GRT INSTITUTE OF ENGINEERING AND TECHNOLOGY | C:/path/to/photo/1.jpg                         |
   | ROHITH K N     | GRT INSTITUTE OF ENGINEERING AND TECHNOLOGY | C:/path/to/photo/2.jpg                         |

4. Run the script:

```bash
python certificate_generator.py
```

5. After execution, the generated PDF file containing all certificates will be saved to the specified output folder.
Error Handling:
If a photo is missing or the path is incorrect, the script will display a message but continue processing other certificates.

Contribution:
Feel free to contribute to this project by submitting pull requests, opening issues, or suggesting improvements.


 Acknowledgements
Thanks to the creators of the `Pillow`, `reportlab`, and `pandas` libraries for making this project possible.

