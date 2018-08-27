{
  "info": {
    "name": "HitBTC Commit Withdraw Crypro",
    "_postman_id": "2eb21077-e159-483d-b6b7-e55da34b166a",
    "description": "Commit withdraw crypro.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Commit",
      "item": [
        {
          "id": "61357b0d-a476-4a9d-a81e-c3b957522eea",
          "name": "putAccountCryptoWithdraw",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "account/crypto/withdraw/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
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
            "description": "Commit withdraw crypro."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4203e727-c8c3-4e5f-bab7-7073f763f60b"
            }
          ]
        }
      ]
    }
  ],
  "variable": [
    {
      "key": "default",
      "value": "http://www.example.com/api/2"
    }
  ]
}