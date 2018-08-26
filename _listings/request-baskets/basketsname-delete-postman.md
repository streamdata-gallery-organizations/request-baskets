{
  "info": {
    "name": "Request Baskets Delete basket",
    "_postman_id": "b8102da9-1a27-4a68-8058-81c4f293a8bc",
    "description": "Permanently deletes this basket and all collected requests.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "id": "4e538b49-f99e-4567-a32f-44476e75c880",
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
          "id": "0417ed46-df0b-49ce-b24e-021cf5980839"
        }
      ]
    },
    {
      "id": "66b6cf60-3f65-4913-948b-477c256c70da",
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
          "id": "cd6e457e-672e-4191-b496-a38128d693ea"
        }
      ]
    }
  ]
}