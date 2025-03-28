Invoice Generator API
============

Invoice Generator is a simple tool for generating invoices. It returns a PDF of the generated invoice.

![Build Status](https://img.shields.io/badge/build-passing-green)
![Code Climate](https://img.shields.io/badge/maintainability-B-purple)
![Prod Ready](https://img.shields.io/badge/production-ready-blue)

This is a Python API Wrapper for the [Invoice Generator API](https://apiverve.com/marketplace/api/invoicegenerator)

---

## Installation
	pip install apiverve-invoicegenerator

---

## Configuration

Before using the invoicegenerator API client, you have to setup your account and obtain your API Key.  
You can get it by signing up at [https://apiverve.com](https://apiverve.com)

---

## Usage

The Invoice Generator API documentation is found here: [https://docs.apiverve.com/api/invoicegenerator](https://docs.apiverve.com/api/invoicegenerator).  
You can find parameters, example responses, and status codes documented here.

### Setup

```
# Import the client module
from apiverve_invoicegenerator.apiClient import InvoicegeneratorAPIClient

# Initialize the client with your APIVerve API key
api = InvoicegeneratorAPIClient("[YOUR_API_KEY]")
```

---


### Perform Request
Using the API client, you can perform requests to the API.

###### Define Query

```
query = {  "invoiceNumber": "INV000001",  "date": "2025-02-01",  "dueDate": "2025-11-30",  "from": {   "from_name": "John Doe",   "from_street": "123 Elm St",   "from_city": "Springfield",   "from_state": "IL",   "from_zip": "62701"  },  "to": {   "to_name": "Jane Smith",   "to_street": "456 Oak St",   "to_city": "Springfield",   "to_state": "IL",   "to_zip": "62702"  },  "job": "Web Development",  "paymentTerms": "Net 30",  "discount": 10,  "salesTax": 37.07,  "currency": "USD",  "items": [   {    "qty": 2,    "description": "Web Design Services",    "unit_price": 500.00   },   {    "qty": 1,    "description": "Domain Registration",    "unit_price": 100.00   }  ] }
```

###### Simple Request

```
# Make a request to the API
result = api.execute(query)

# Print the result
print(result)
```

###### Example Response

```
{
  "status": "ok",
  "error": null,
  "data": {
    "pdfName": "f9210db5-8be3-4de4-8b20-d58019b0600a.pdf",
    "expires": 1740259902629,
    "downloadURL": "https://storage.googleapis.com/apiverve-helpers.appspot.com/htmltopdf/f9210db5-8be3-4de4-8b20-d58019b0600a.pdf?GoogleAccessId=1089020767582-compute%40developer.gserviceaccount.com&Expires=1740259902&Signature=PVHHoAfVg%2BUOXCC1kt3m3ttRAns6UTrYPm8%2BVS19hEFAH27VG%2FnZHgUl75iUYpZozqycZw7etohyekZIBPeqozfFWkkodkMvi487x2onk%2B3S9nQN5J0gmPxhcfWVjT4jPxk7ggQMhG2rl7QCxjAhG9OGo1U9OuhSYdJXaQqEmOMhTDkhW%2BB3RFMHqXmgYZHBLo8kh1aLLK%2FdKbGOF5ofR33W0w%2F5ywdykG%2BAnk0Rv3oxTIppAR%2F4NsDeqhYBgq3yXyRubOgcZGBEEtAj2bpYPuzNtqKgF7aENTQe4MkghWct8P4qs%2F8MDSSMCZCN1B24Xz8TxGGem814qThfv3DLOw%3D%3D"
  },
  "code": 200
}
```

---

## Customer Support

Need any assistance? [Get in touch with Customer Support](https://apiverve.com/contact).

---

## Updates
Stay up to date by following [@apiverveHQ](https://twitter.com/apiverveHQ) on Twitter.

---

## Legal

All usage of the APIVerve website, API, and services is subject to the [APIVerve Terms of Service](https://apiverve.com/terms) and all legal documents and agreements.

---

## License
Licensed under the The MIT License (MIT)

Copyright (&copy;) 2025 APIVerve, and EvlarSoft LLC

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.