# Optical Character Recognition (OCR) Solution

## Summary

### Issue
We want a solution which could convert pdfs/images to searchable text.

### Decision
Use Tesseract OCR

### Status
Decided

### Group
Integration, data

### Assumptions
- We only need to support images and pdfs
- We don't need to use an specific tool
- We can use a tool that is not a Saas

# Constraints
There's no constraint

### Positions
- Use tools as GOCR, Ocrad, Dynamsoft OCR SDK.
- Use third-party managed services Asprise OCR SDK and consume their api.

### Argument
Use Tesseract managed in an own instance in EC2 behind an API in charge of managing and recognizing the test in the files. Teserract allows us to recognize text in different languages and has a vast set of SDKs

### Implications
- We need to create an extra service to manage the text from the files.
- Extra effort to manage in service. This requires DevOps effort.