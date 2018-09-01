{
  "info": {
    "name": "Request Baskets Get baskets",
    "_postman_id": "b9fcf27f-9028-4bb1-8af1-cc5e1ced873c",
    "description": "Fetches a list of basket names managed by service. Require master token.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "id": "fb246c77-fe54-4d80-8afd-883c7b47d5b3",
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
          "id": "c5762779-aebb-459f-8c76-b90a4b011351"
        }
      ]
    }
  ]
}