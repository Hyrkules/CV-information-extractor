# CV Information Extractor

## Project Overview

This project is focused on splitting a curriculum vitae (CV) into important sections, extracting the text from each part using OCR (Optical Character Recognition), and leveraging the extracted text to perform **Retrieval-Augmented Generation (RAG)** for answering questions about the CV. It provides a step-by-step approach to processing scanned or image-based CVs and enables answering natural language questions by using the extracted information.

By splitting the CV into manageable parts, converting the visual data to text, and applying modern techniques like RAG, this project makes it easy to interact with and query large CV documents.

### Key Features:
1. **Splitting the CV**: Break the CV into logical parts to ensure easy extraction and analysis.
2. **OCR Text Extraction**: Extract text from each CV section using the powerful `Tesseract OCR` library.
3. **RAG-based Question Answering**: Apply Retrieval-Augmented Generation to allow questions to be answered based on the extracted CV content.

---

## Workflow

### 1. Splitting the CV into Important Parts
The project starts by breaking down a large CV into smaller, important sections (e.g., Education, Work Experience, Skills). This step ensures that the document is processed more efficiently, especially when dealing with long or complex CVs.

**Example:**
![CV Split Example](utils/cv_split_example.png)

### 2. Using OCR to Convert CV Image to Text
Once the CV is split, we use the `pdf2image` library to convert the CV from PDF format into images. Then, `pytesseract` extracts the text from each image. The extracted text for each part is saved in individual text files for further use.

**Example:**
![OCR Text Extraction](utils/ocr_extraction_example.png)

### 3. Answering Questions with RAG
After extracting the text from all parts of the CV, we apply **Retrieval-Augmented Generation (RAG)** to enable the system to answer specific questions. The text serves as the source of knowledge, and the model retrieves relevant sections from the CV to provide accurate answers to user queries.

**Example:**
![RAG Question Answering](utils/rag_example.png)

---
