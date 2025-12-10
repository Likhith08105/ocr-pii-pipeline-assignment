# ocr-pipeline-assignment

This is a small project where I built a basic OCR + PII extraction pipeline for handwritten JPEG images.  
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
Since these documents include a lot of handwriting (especially medical notes), the OCR output is not always perfect.  
Handwritten text is naturally difficult for OCR, especially when:

- The writing is fast or messy
- The document has signatures or shorthand
- The scan is tilted or low quality

Still, the pipeline is able to run end-to-end on all sample images and extract some useful text.  
The structure is in place, so the OCR accuracy can be improved easily by adding stronger preprocessing or by trying better handwriting OCR models in the future.

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
