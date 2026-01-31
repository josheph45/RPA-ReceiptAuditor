# RPA-ReceiptAuditor

A modular UiPath automation designed to replace manual data entry in expense auditing. This solution digitizes physical receipts through OCR, validates contents against business rules, and generates financial reports.

## Features

- **Automated Digitization**: Converts image-based receipts into structured data using OCR and Regular Expressions.
- **Layered Architecture**: Decoupled design separating the controller, service, and business logic layers for easy maintenance.
- **Custom Utility Library**: Includes `ReceiptAuditorUtils` for specialized currency normalization and data cleaning.
- **Consolidated Reporting**: Automatically generates an Excel-based audit report of all processed expenses.

## Architecture Overview



The project is structured to maximize modularity and error handling:

* **Main.xaml**: The master controller responsible for the robot's lifecycle and global exception handling.
* **Process.xaml**: The core engine where business logic orchestration and data validation occur.
* **Extract_Receipt_Data.xaml**: A specialized service layer focused on OCR processing and Regex data extraction.
* **ReceiptAuditorUtils**: A custom library developed for normalizing financial data across different locales.

## Technical Workflow

1.  **Initialization**: Load configuration files and initialize OCR engines.
2.  **Data Extraction**: Process receipt images to extract Merchant Name, Date, and Amount.
3.  **Validation**: Apply business logic to flag suspicious or non-compliant expenses.
4.  **Reporting**: Export all validated data into a master Excel file for final review.

---
*Developed with UiPath Studio*
