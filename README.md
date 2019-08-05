# Creating a searchable database with text extracted from scanned Pdfs or images

In this short tutorial I show how to extract text from images and scanned PDFs and store the results in a database to make the document searchable.

PDF documents and images with text are difficult to work with. Most business people manually read through multiple pages to retrieve the information they are looking for.  We want to use a python program that will take a pdf, whether scanned or not as well as any image that contains text and extract the text by page and index each page in a DataFrame which can be stored in any database of your choice and be made available for users to write a search query against the table.

The example we will use is a pdf document with a mini course  on Weka by machine learning mastery. The pdf has 23 pages. We will use python packages wand, pillow and pytesseract to convert it to image and then extract each page text , all in one program.

For the package pytesseract to work, download and install tesseract-ocr from this link https://github.com/UB-Mannheim/tesseract/wiki and then run this line pytesseract.pytesseract.tesseract_cmd = r"C:\Program Files (x86)\Tesseract-OCR\tesseract.exe" in python. I want to give credit to Ratul Doley.
