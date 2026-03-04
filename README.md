# Invoice-Automation-AI-Agent
An automation tool using Google AI Studio and n8n to perform OCR(Optical Character Recognition) on invoices and manage data via Google Sheets
## System Architecture:
The project consists of three primary components interacting in real-time:
### **1. Frontend (Google AI Studio)**
A multi-tab dashboard providing a user-friendly interface:
* **Dashboard Tab:** Provides a high-level overview of processed data.
* **Invoices Tab:** Displays a detailed list of all records retrieved from storage.
* **Upload Tab:** A dedicated portal for users to submit raw invoice files (PDF/Images).
### **2. Automation Engine (n8n Workflows)**
Two distinct workflows handle the data pipeline logic:
* **Data Retrieval Workflow:** Triggered upon loading the Dashboard/Invoices tabs. It fetches all existing records from the database and pushes them to the UI.
* **OCR & Processing Workflow:** Triggered via a Webhook when a file is uploaded. It utilizes AI/OCR to parse text, identify key-value pairs (Invoice #, Date, Total), and execute the storage command.
### **3. Database (Google Sheets)**
Serves as the persistent data store for all processed invoice information.

## Technical Details:
* **Automation:** n8n (Webhooks, HTTP Request, Google Sheets Node)
* **Interface:** Google AI Studio
* **Logic:** JSON Parsing, OCR Data Extraction, Data Processing and Storage
* **Database:** Google Sheets API
NOTE : Original dataflow files have been lost, the files uploaded here are older versions.
