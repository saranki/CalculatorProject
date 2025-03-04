This is a simple project to convert SOAP request to JSON, get the response in JSON and convert to SOAP.

**Sample Request:**
```
curl --location 'https://localhost:8253/calculator/add' \
--header 'Content-Type: text/xml; charset=utf-8' \
--header 'SOAP_ACTION: http://tempuri.org/Add' \
--data '<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <Add xmlns="http://tempuri.org/">
      <param1>10</param1>
      <param2>5</param2>
    </Add>
  </soap:Body>
</soap:Envelope>'
```

**Sample Response:**

```
<AddResponse xmlns="http://tempuri.org/">
    <response>success</response>
</AddResponse>
```
