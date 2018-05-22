{
  "info": {
    "name": "IBM Watson Machine Learning Get Wml Instances Instance Published Models",
    "_postman_id": "658fc1ed-ba62-4cce-aa44-7f4ecf7f8639",
    "description": "Get wml instances instance published models.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Machine Learning",
      "item": [
        {
          "id": "beb0804a-93c2-4517-b8cd-4a39c9aa894a",
          "name": "listModelDeployments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "ibm-watson-ml.mybluemix.net",
              "path": [
                "v3",
                "wml_instances/:instance_id/published_models"
              ],
              "query": [
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "instance_id",
                  "value": "instance_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get wml instances instance published models."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a28a8ead-4e7e-4079-9b1b-6761f570bf5f"
            }
          ]
        }
      ]
    }
  ]
}