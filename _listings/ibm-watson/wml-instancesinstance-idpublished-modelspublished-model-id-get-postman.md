{
  "info": {
    "name": "IBM Watson Machine Learning Get Wml Instances Instance Published Models Published Model",
    "_postman_id": "b615c55d-1066-4229-adb7-21789b80bda8",
    "description": "Get wml instances instance published models published model.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Machine Learning",
      "item": [
        {
          "id": "c3b763b3-c526-4520-bae3-4ea8510520cb",
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
              "id": "5f9dabd7-dbc6-4829-89fb-8f79b2c73499"
            }
          ]
        },
        {
          "id": "d719467f-201d-415b-ada7-f170f1d96b37",
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
              "id": "99a69be2-6bcd-4fbf-b05d-0124b717e6f4"
            }
          ]
        }
      ]
    }
  ]
}