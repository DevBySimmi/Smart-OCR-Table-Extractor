📄 Smart OCR Table Extractor

A powerful Python-based GUI application for extracting text and structured tables from PDF files and images.

The project combines Tesseract OCR for text recognition with Microsoft Table Transformer for automatic table detection and structure recognition.

Extracted data can be exported into Excel, TXT, or DOCX formats.

✨ Features

- 📄 Extract text from PDF files
- 🖼️ Extract text from JPG, JPEG, and PNG images
- 📊 Automatically detect tables
- 🔍 Recognize table rows and columns
- 🧠 Uses Microsoft Table Transformer for table detection
- 🔤 Uses Tesseract OCR for text extraction
- 📑 Process selected PDF page ranges
- 📊 Export tables and text to Excel
- 📝 Export extracted content to TXT
- 📘 Export extracted content and tables to DOCX
- 🖥️ Simple Tkinter graphical interface
- ⚡ Image preprocessing with OpenCV
- 📚 Supports multiple tables from a document

🛠️ Technologies Used

- Python 3.12
- Tkinter — GUI
- Tesseract OCR — Optical Character Recognition
- PyTesseract — Python interface for Tesseract
- OpenCV — Image preprocessing
- Pillow — Image processing
- PyPDF2 — PDF page handling
- pdf2image — PDF-to-image conversion
- Pandas — Data processing
- OpenPyXL — Excel export
- python-docx — DOCX export
- PyTorch — Deep learning framework
- Transformers — Table Transformer models

🤖 AI Models

This project uses Microsoft's Table Transformer models:

Table Detection

microsoft/table-transformer-detection

Table Structure Recognition

microsoft/table-transformer-structure-recognition

These models help identify tables and determine their rows and columns before OCR is performed on individual cells.

📂 Supported Input

Input| Supported
PDF| ✅
JPG| ✅
JPEG| ✅
PNG| ✅

📤 Export Formats

Format| Output
Excel| ".xlsx"
Text| ".txt"
Word| ".docx"

⚙️ Installation

Clone the repository:

git clone https://github.com/your-username/Smart-OCR-Table-Extractor.git
cd Smart-OCR-Table-Extractor

Install the required Python packages:

py -3.12 -m pip install pytesseract pdf2image PyPDF2 pillow pandas numpy opencv-python python-docx openpyxl torch transformers

🔧 External Requirements

1. Tesseract OCR

Install Tesseract OCR separately on Windows and make sure its executable is available to your system.

If Tesseract is installed but not added to PATH, you can configure its location in Python:

pytesseract.pytesseract.tesseract_cmd = r"C:\Path\To\tesseract.exe"

Replace the path with the actual location on your computer.

2. Poppler

"pdf2image" requires Poppler on Windows for converting PDF pages into images.

After installing Poppler, add its "bin" folder to your system PATH or provide its path when calling "convert_from_path()".

🚀 How to Use

Step 1

Run the Python application:

python IMGPDF_OCR.py

Step 2

Click:

Select File

Choose a PDF or image.

Step 3

For PDFs, select the required page range:

All
1-5
6-10
11-15
...

Step 4

Choose the output format:

Excel
TXT
DOC

Step 5

Click:

Process

The application will:

PDF/Image
    ↓
Image Preprocessing
    ↓
Table Detection
    ↓
Table Structure Recognition
    ↓
Cell Extraction
    ↓
Tesseract OCR
    ↓
Structured Data
    ↓
Excel / TXT / DOCX

📊 Example Workflow

For a PDF containing an invoice:

Invoice PDF
     ↓
Convert PDF pages to images
     ↓
Detect invoice table
     ↓
Detect rows and columns
     ↓
OCR each cell
     ↓
Create Pandas DataFrame
     ↓
Export to Excel

📁 Project Structure

Smart-OCR-Table-Extractor/
│
├── IMGPDF_OCR.py
├── README.md
├── requirements.txt
└── LICENSE

📦 requirements.txt

You can create a "requirements.txt" file containing:

pytesseract
pdf2image
PyPDF2
Pillow
pandas
numpy
opencv-python
python-docx
openpyxl
torch
transformers

Then install everything using:

pip install -r requirements.txt

⚠️ Important Notes

- Tesseract OCR must be installed separately.
- Poppler is required for PDF-to-image conversion on Windows.
- The first run may take longer because the Table Transformer models may need to be downloaded.
- Large PDFs and high-resolution scans may require significant RAM and processing time.
- OCR accuracy depends on the quality and clarity of the input document.
- Complex or irregular tables may not be detected perfectly.

🔮 Future Improvements

Possible future upgrades include:

- [ ] Drag-and-drop file support
- [ ] Batch processing of multiple files
- [ ] Progress bar
- [ ] Dark mode GUI
- [ ] Better OCR preprocessing
- [ ] Automatic column-name correction
- [ ] Multiple-language OCR
- [ ] CSV export
- [ ] Searchable PDF output
- [ ] Preview extracted tables before export
- [ ] Improved handling of merged cells
- [ ] GPU acceleration
- [ ] Modern GUI using CustomTkinter

🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new branch
3. Make your changes
4. Commit your changes
5. Push the branch
6. Open a Pull Request

📜 License

This project can be released under the MIT License.

⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.

---

👨‍💻 Built With

Python • Tesseract OCR • OpenCV • PyTorch • Hugging Face Transformers • Pandas • Tkinter

«Turn unstructured PDFs and images into structured, usable data. 🚀»
