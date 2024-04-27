# PDF PII Redaction

This repository contains the code for redacting PII (Personal Identifiable Information) from Resume PDFs. 

The name, email and phone number of the user needs to be redacted automatically from the resume before sharing it with clients. 

## Requirements
- `nltk` and `spacy` for NER of user's name
- `regex` for indentifying phone numbers and emails
- `fitz` from PyMuPDF to extract text and redact PDFs

## Challenges 
1. Finding the names from the PDFs is challenging. 
- We could probably leverage OpenAI's model to help with that
- Or we could use the existing database to give the resume and the name of the person who the resume belongs to

2. Redaction is not limited to the name but anything that looks like the name in the rest of the resume document as well
- We can limit the redaction to the top 50% of the resume or lesser 

3. Not enough actual (real world) samples to test
