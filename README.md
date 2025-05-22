BillBuster - Smart Receipt & Bill Tracker

Project Description

BillBuster is a Python tool that uses Optical Character Recognition (OCR) to extract data from scanned bills and receipts. It categorizes spending based on predefined rules and saves the data to a CSV file for easy tracking and analysis, ideal for budgeting or tax purposes.

Key Features





Extracts text from receipt images using Tesseract OCR



Parses the text to identify date and total amount



Categorizes spending based on keywords in the receipt text



Saves extracted data to a CSV file for expense tracking

Real-world Use Cases





Budgeting: Track personal expenses by category (e.g., Food, Transportation) to manage finances.



Tax Preparation: Organize receipt data for deductible expenses, simplifying tax filing.



Automation: Reduce manual data entry by extracting information from physical receipts.

Installation Steps





Install Tesseract OCR





Windows:





Download Tesseract from GitHub



Install it and add the installation directory to your PATH (e.g., C:\Program Files\Tesseract-OCR)



Verify installation: tesseract --version



Linux (Ubuntu):





Run sudo apt-get install tesseract-ocr



macOS:





Install using Homebrew: brew install tesseract



Install Python dependencies





Create a virtual environment (optional): python -m venv venv



Activate the virtual environment:





Linux/macOS: source venv/bin/activate



Windows: venv\Scripts\activate



Install requirements: pip install -r requirements.txt



Clone this repository





git clone https://github.com/yourusername/BillBuster.git



Replace yourusername with your GitHub username



Set up the project





Navigate to the project directory: cd BillBuster



Edit config.py to add or modify categories and keywords as needed

How to Run





Run the main script with the path to a receipt image:

python main.py --image path/to/receipt.jpg



The extracted data (date, total, category, filename) will be appended to expenses.csv in the project directory.

Sample Output

After running the script, expenses.csv will contain rows like:

Date,Total,Category,Filename
2025-05-20,$54.99,Food,receipt1.jpg
2025-05-21,$29.95,Transportation,receipt2.jpg

Notes





Tesseract Setup: Ensure Tesseract is installed and accessible in your system's PATH. Test with tesseract --version.



Image Quality: OCR accuracy depends on clear, high-quality images. Preprocessing (e.g., with OpenCV) could improve results but is not included in this starter project.



Customization: Modify config.py to add categories or keywords for better categorization accuracy.



Limitations: The project uses simple regex for parsing and keyword matching for categorization, which may not handle all receipt formats perfectly. For advanced use, consider enhancing parsing logic or using NLP.

Future Enhancements





Add image preprocessing with OpenCV to improve OCR accuracy.



Support multiple currencies and more date formats.



Include a Streamlit interface for uploading images and viewing results interactively.
