{
  "info": {
    "name": "Bitbucket Add Repositories Username Repo Slug Commits",
    "_postman_id": "8f27abc3-27a5-4546-93ef-1a743750893a",
    "description": "Identical to `GET /repositories/{username}/{repo_slug}/commits`,\nexcept that POST allows clients to place the include and exclude\nparameters in the request body to avoid URL length issues.\n\n**Note that this resource does NOT support new commit creation.**",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "0740b7d8-0136-48e4-a1b8-4f0284b14d41",
          "name": "postRepositoriesUsernameRepoSlugCommits",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/commits"
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
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Identical to `GET /repositories/{username}/{repo_slug}/commits`,\nexcept that POST allows clients to place the include and exclude\nparameters in the request body to avoid URL length issues"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dfae0e8f-cbf4-4e81-9080-2c9313b09dec"
            }
          ]
        }
      ]
    }
  ]
}