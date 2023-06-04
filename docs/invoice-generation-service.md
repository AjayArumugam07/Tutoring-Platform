# Invoice Generation Service
***
## Requirements
***
### Functional Requirements
* Accept input such as tutorID, student ID, number of billable hours, and description of what was done during the session.
* Retrieve tutor and student details like personal info, negotiated hourly cost, etc. from database using student ID.
* Generate unique invoice numbers for each invoice to ensure proper identification and tracking.
* Handle invoices in different currencies to accommodate international transactions and currency conversions.
* Generate invoice in PDF format using a common template for all invoices.
* Email and text invoice PDF to tutor and student.
* Charge customer through their preferred mode of payment.
* Store invoice in Cloud Storage.

### Non Functional Requirements
* System should be highly scalable.
* System does not need to be highly performant and only needs to generate invoice within 10 minutes.

## Design
***
### Tech Stack
* Go: capable of executing resource intensive tasks such as PDF generation concurrently.
* gRPC: communication between Invoice Generation Service and other microservices.
* pdfcpu: go library to generate PDF documents.
* Docker: containerization of microservice.
