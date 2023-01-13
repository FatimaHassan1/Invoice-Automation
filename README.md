# Invoice-Automation

Why

Every month, I have to amend a Google Sheet, export it as a PDF,
and give it to Kristin. Every month, this process took about 3 minutes.
I made the decision to spend some time automating it.
Perhaps other employees in the company will also find it useful.


Package ----------------------
In Node.js and the browser, we can create PDF documents thanks to PDFKit. 
It works best for things like creating PDF invoices for your web server on the go. 
The aforementioned example taught you about PDFKit and demonstrated how to use it to dynamically create a PDF invoice from a straightforward object-based data model.
npm i pdfkit


Model-------------------------
A shipment key that contains all the shipping details to print on the invoice is present in the aforementioned object.
All of the items you wish to print on the invoice are in an array under the items key (the amount is the sum for all pieces of this item in cents). 
The paid field allows you to define how much has already been paid for this invoice, and the subtotal key includes the total of all items in cents.
The invoice is identified by its invoice nr.

Generate Invoice---------------
Now that you have this data model, you may create a PDF file. 
Create a function called createInvoice(invoice, path) that utilises the invoice object to generate a legitimate PDF invoice and saves it to the file at path.


Adding Data to PDF------------
It's time to add extra information to the PDF page that is now empty. 
Header and Footer are the two static elements to start with.
