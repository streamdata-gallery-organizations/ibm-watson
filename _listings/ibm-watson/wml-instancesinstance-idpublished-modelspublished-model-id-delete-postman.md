{
  "info": {
    "name": "IBM Watson Machine Learning Delete Wml Instances Instance Published Models Published Model",
    "_postman_id": "2f5883ad-7754-4d0c-9d0e-66831f8adfc8",
    "description": "Delete wml instances instance published models published model.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Machine Learning",
      "item": [
        {
          "id": "cf2e395c-9209-4078-ad04-70e02da3dd67",
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
              "id": "21889334-82c9-4ae1-ab4e-5a66b3e157d3"
            }
          ]
        },
        {
          "id": "7ab73071-8b92-43cb-803d-bb1f08208ed0",
          "name": "details-about-specific-published-model",
          "request": {
            "url": {
              "protocol": "http",
              "host": "ibm-watson-ml.mybluemix.net",
              "path": [
                "v3",
                "wml_instances/:instance_id/published_models/:published_model_id"
              ],
              "variable": [
                {
                  "id": "instance_id",
                  "value": "instance_id",
                  "type": "string"
                },
                {
                  "id": "published_model_id",
                  "value": "published_model_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get wml instances instance published models published model."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6576f470-8924-45e4-afdc-95df06a0b5b0"
            }
          ]
        },
        {
          "id": "1e74ccd5-ed82-4dce-93bc-2cb06d7a71ad",
          "name": "deletes-the-published-model-and-all-its-deployments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "ibm-watson-ml.mybluemix.net",
              "path": [
                "v3",
                "wml_instances/:instance_id/published_models/:published_model_id"
              ],
              "query": [
                {
                  "key": "ignore_spark_errors",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "instance_id",
                  "value": "instance_id",
                  "type": "string"
                },
                {
                  "id": "published_model_id",
                  "value": "published_model_id",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete wml instances instance published models published model."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fb17a8ee-6c7e-40d1-bcce-5947bb06581e"
            }
          ]
        }
      ]
    }
  ]
}