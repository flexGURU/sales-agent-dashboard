# sales-agent-dashboard
a comprehensive Angular web application designed to efficiently manage schools, invoices, and collections through intuitive dashboards, data visualizations, and seamless CRUD operations.

## Features

### Dashboard

1. **Summary**: The dashboard displays summaries of collections, signups, total revenue, bounced checks, and upcoming invoices.
2. **Product Distribution**: Pie charts illustrate the actual and target distributions of three products: Zeraki Analytics, Zeraki Finance, and Zeraki Timetable. The target distribution for each product is set to 15%.
3. **School Type Distribution**: Bar charts show the distribution of schools (Primary, Secondary, and IGCSE) for each product: Zeraki Analytics, Zeraki Finance, and Zeraki Timetable.

### Schools

The Schools section allows you to manage schools, invoices, and collections. You can perform CRUD (Create, Read, Update, Delete) operations against the `db.json` file using an HTTP client.

## Data Schema

The application uses a `db.json` file to store data. Here is the data schema:

### Schools

{
 "id": number,
 "name": string,
 "type": string,
 "products": string[],
 "county": string,
 "registrationDate": string,
 "contactInfo": {
   "email": string,
   "phone": string
 },
 "balance": number
}

### Invoices
{
  "id": number,
  "schoolId": number,
  "invoiceNumber": string,
  "invoiceItem": string,
  "creationDate": string,
  "dueDate": string,
  "amount": number,
  "paidAmount": number,
  "balance": number,
  "status": string
}

### Collections
{
  "id": number,
  "schoolId": number,
  "invoiceNumber": string,
  "invoiceItem": string,
  "creationDate": string,
  "dueDate": string,
  "amount": number,
  "paidAmount": number,
  "balance": number,
  "status": string
}


## Services
The application utilizes three services:

1. data-add service: This service contains functions responsible for adding data and is injected into components that add collections, invoices, or schools.
2. edit service: This service handles data editing operations.
3. school service: This service manages school-related operations.

## Deployment
To run the project locally, follow these steps:

## Clone the repository.
<b>PREREQUISITES: </b> must have Node 18 and above, angular/cli and Typescript installed
Install the required dependencies by running npm install.
Start the development server with ng serve.
Navigate to http://localhost:4200/ in your web browser.

# Note: The application uses Angular CLI 17.3.7 and Node.js 20.13.1, and it employs standalone components.
