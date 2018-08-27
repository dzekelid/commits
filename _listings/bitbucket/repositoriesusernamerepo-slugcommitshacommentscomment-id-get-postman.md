{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Commit Sha Comments Comment",
    "_postman_id": "319f92ed-0c59-40ba-a87b-5dfbc90012dc",
    "description": "Get repositories username repo slug commit sha comments comment",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "243797de-8371-4cdc-b3f7-4d885676d4b7",
          "name": "getRepositoriesUsernameRepoSlugCommitShaCommentsComment",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/commit/:sha/comments/:comment_id"
              ],
              "variable": [
                {
                  "id": "username",
                  "value": "username",
                  "type": "string"
                },
                {
                  "id": "repo_slug",
                  "value": "repo_slug",
                  "type": "string"
                },
                {
                  "id": "sha",
                  "value": "sha",
                  "type": "string"
                },
                {
                  "id": "comment_id",
                  "value": "comment_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get repositories username repo slug commit sha comments comment"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "71d96b2a-442f-49f9-a0e7-0ce7c77b4061"
            }
          ]
        }
      ]
    }
  ]
}