# OCR BASED MEDICAL DATA EXTRACTION

### Problem Statement
---
Health insurance companies are required to process a massive volume of images sent by hospitals to extract relevant data.They often outsource the work to analytics firms,which manually extract information from images.However,this manual method is prone to errors, and the volume of images becomes unmanageable, especially during high-demand periods like pandemics.This led to the requirement of building a software to improve efficiency and accuracy by reducing manual work.

### Approach to the problem
---
We propose building a program to automate data extraction from images, which would then be verified by a person before submission. This project uses Python programming language and the Pytesseract library to extract text from images. Regular expressions are employed to derive the necessary fields of interest.

### Workflow
---
![This is a workflow image](https://github.com/Nivi107/Medical_Data_Extraction_Project/blob/main/Workflow.jpg?raw=true)

### Technolgies and Libraries used
---
- Python
- Pdf2image for conversion of pdf to jpg
- Opencv for computer vision
- pytesseract for OCR
- Regular expression for pattern matching
- pytest for unit testing
- Postman for API testing
- FastApi for building APIs

### Image Processing
---
The initial step is converting prescription and patient detail PDFs to image format for text extraction. Pdf2image is used for this conversion. Since the images are often unclear, resulting in poor text extraction, we preprocess the images using adaptive thresholding, a computer vision technique. This technique subdivides the image into regions and applies corresponding thresholds to each region, resulting in a clearer image.

[OpenCv notebook](https://github.com/Nivi107/Medical_Data_Extraction_Project/blob/main/backend/notebooks/cv_concepts.ipynb)

### Extraction of data fields
---
Text is extracted from the preprocessed images using the Pytesseract module. Regular expressions are then used to match patterns and extract only the necessary data. You can practice regular expressions before implementing them in your code here:
[Practice regular expressions](https://regex101.com/)

### Jupyter Notebook
---
To develop the functionality for the above processes, a trial-and-error approach in Jupyter notebooks is used to iteratively create and test smaller blocks of functionality. These smaller blocks were then refined and organized into classes and methods following object-oriented programming principles to build the final codebase.

[Notebooks](https://github.com/Nivi107/Medical_Data_Extraction_Project/blob/main/backend/notebooks)

### Test driven development
---
Adopting a test-driven development approach ensures that our code is reliable and maintainable. By writing tests with Pytest, we can catch bugs early and ensure that our extraction logic remains accurate as we refine the software.

### Postman
---
As this project is focused on the backend, there is no frontend development involved. Therefore, I utilized Postman to create and test HTTP requests for the API endpoints. Postman facilitated the creation, testing, and debugging of these requests, ensuring that the APIs functioned correctly before any integration with a frontend interface.

### Result
---
The backend developed in this project can be integrated with a frontend interface where users can upload images and extract the data using OCR technolgy.
To ensure accuracy, the extracted data can be reviewed and verified by a person before final submission. This two-step process allows for efficient data extraction while maintaining high accuracy levels.




