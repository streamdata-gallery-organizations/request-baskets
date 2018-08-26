{
  "info": {
    "name": "Request Baskets Get basket settings",
    "_postman_id": "4429039b-ba3e-478e-b67c-65a8665596ce",
    "description": "Retrieves configuration settings of this basket.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "id": "87d0af98-3306-45a9-abad-ba5758e4e9b2",
      "name": "baskets.get",
      "request": {
        "url": "http://rbaskets.in/baskets?max=%7B%7D&q=%7B%7D&skip=%7B%7D",
        "method": "GET",
        "header": [
          {
            "key": "Accept",
            "value": "*/*",
            "disabled": false
          }
        ],
        "body": {
          "mode": "raw"
        },
        "description": "Fetches a list of basket names managed by service. Require master token."
      },
      "response": [
        {
          "status": "OK",
          "code": 200,
          "name": "Response_200",
          "id": "c18f6f2f-56ea-4045-bb75-818ed131cf6d"
        }
      ]
    },
    {
      "id": "2d9e3002-85c3-45f0-a1ce-1a63fdae9718",
      "name": "baskets.name.get",
      "request": {
        "url": {
          "protocol": "http",
          "host": "rbaskets.in",
          "path": [
            "baskets/:name"
          ],
          "variable": [
            {
              "id": "name",
              "value": "{}",
              "type": "string"
            }
          ]
        },
        "method": "GET",
        "header": [
          {
            "key": "Accept",
            "value": "*/*",
            "disabled": false
          }
        ],
        "body": {
          "mode": "raw"
        },
        "description": "Retrieves configuration settings of this basket."
      },
      "response": [
        {
          "status": "OK",
          "code": 200,
          "name": "Response_200",
          "id": "1c9a6746-2384-460a-ac80-103f1baefce3"
        }
      ]
    },
    {
      "id": "453dfef5-c0d1-44bc-a8d9-2f854378de95",
      "name": "baskets.name.delete",
      "request": {
        "url": {
          "protocol": "http",
          "host": "rbaskets.in",
          "path": [
            "baskets/:name"
          ],
          "variable": [
            {
              "id": "name",
              "value": "{}",
              "type": "string"
            }
          ]
        },
        "method": "DELETE",
        "header": [
          {
            "key": "Accept",
            "value": "*/*",
            "disabled": false
          }
        ],
        "body": {
          "mode": "raw"
        },
        "description": "Permanently deletes this basket and all collected requests."
      },
      "response": [
        {
          "status": "OK",
          "code": 200,
          "name": "Response_200",
          "id": "118923af-daef-430a-9c00-80bdabfd684f"
        }
      ]
    }
  ]
}