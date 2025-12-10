# ocr-pipeline-assignment

In this assignment I built a basic OCR + PII extraction pipeline for handwritten JPEG images.  
The main idea is to take a handwritten document, clean it up a bit, extract whatever text is readable, and then try to detect simple PII items like names, phone numbers, emails, etc.

## What the pipeline does
- Reads the image
- Preprocesses it (grayscale, blur, threshold)
- Runs OCR using Tesseract
- Cleans the text
- Detects basic PII using regex + spaCy
- Can also blackout (redact) the detected PII on the image

I kept the code simple and modular so each part can be improved later if needed.

## About the accuracy
The pipeline runs properly on all the sample images, but the text accuracy depends a lot on the handwriting. 
Since the documents have different writing styles and some parts are hard to read, the extracted text is not always perfect.
Even then, the overall flow (preprocessing → OCR → PII detection → redaction) works correctly.

If needed, the accuracy can be improved later by adding more preprocessing or trying a better handwriting OCR model.


## What’s included
- The Colab notebook with the full pipeline
- A simple dependencies file
- Screenshots of the output for the test images
- Redacted results saved from the notebook

## How to run it
1. Open the notebook in Google Colab  
2. Install the dependencies (first cell)  
3. Upload a JPG handwritten document  
4. Call:  
