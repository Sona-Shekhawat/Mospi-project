# Optimizing Survey Data Processes: Extraction and Classification

This project aims to optimize the survey data processes by automating the extraction and classification of financial statements from factories. The process involves extracting balance sheet and profit and loss (P&L) data from PDF or Excel documents, cleaning and structuring the data, and finally classifying each item into their respective categories using machine learning techniques.

## Prerequisites

Before running the project, ensure the following prerequisites are met:

1. Financial statements of factories in PDF or Excel format containing balance sheet and P&L data.
2. Python interpreter or IDE (e.g., Jupyter Notebook) installed.
3. Necessary modules installed and imported, including:
   - `regex` for NLP tasks
   - `pytesseract` for OCR
   - `pdf2image` for converting PDF pages to images for OCR
   - `pillow` for image processing and saving
   - `pandas` for data manipulation
   - `fuzzywuzzy` for approximate string matching
   - `pyenchant` for dictionary
   - `sklearn` for machine learning tasks

## Methodology

### 1. Data Collection

The data collection process involves utilizing advanced techniques such as Optical Character Recognition (OCR) to extract information from scanned PDF documents. These PDFs contain crucial data related to balance sheets and profit and loss statements.

### 2. Data Cleaning

Extracted data is often unstructured and needs to be converted into a structured format suitable for analysis. This involves using techniques like regular expressions (regex) and data scraping to identify numerical accounting data patterns. The cleaned data is stored in tabular format using the pandas library.

### 3. Model Building

After cleaning and storing the data, each "Item Name" is categorized into respective blocks using supervised classification techniques like random forests. Features such as "Item Name" and "Reference Account" are used for training the model. There is a reference data set named "ready references" used for some items for training, limited to blocks C through J.

### 4. Handling Block C

Block C contains fixed assets, often supplied in a separate page within the PDF. A separate function is created to scan this page directly. Since the page is usually in landscape orientation, it needs to be converted and rotated before processing. Techniques involving OpenCV and image processing modules are employed for this purpose.

## Usage

To use the project, follow these steps:
1. Ensure all prerequisites are met.
2. Clone the repository to your local machine.
3. Run the provided scripts or notebooks in a Python environment.
4. Follow the instructions provided within the scripts/notebooks for data extraction, cleaning, and classification.

