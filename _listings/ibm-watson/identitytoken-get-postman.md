{
  "info": {
    "name": "IBM Watson Machine Learning Get Entity Token",
    "_postman_id": "1cb64387-01ca-4746-b344-f263f1366ffa",
    "description": "Tokens are required for the ML REST API authentication. They are generated using ML service credentials",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Machine Learning",
      "item": [
        {
          "id": "d0523c5a-6c8a-4151-8b37-ae9ccbef380d",
          "name": "generateToken",
          "request": {
            "url": "http://ibm-watson-ml.mybluemix.net/v3/identity/token",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Tokens are required for the ML REST API authentication. They are generated using ML service credentials"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4fed1641-d10f-430c-9267-f7d157552644"
            }
          ]
        }
      ]
    }
  ]
}