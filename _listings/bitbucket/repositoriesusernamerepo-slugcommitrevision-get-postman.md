{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Commit Revision",
    "_postman_id": "76a01187-a1d0-4baa-8efe-1067a56ce6f1",
    "description": "Get repositories username repo slug commit revision",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "bb733fae-0703-4db6-8f42-30698daa7b6d",
          "name": "getRepositoriesUsernameRepoSlugCommitRevision",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/commit/:revision"
              ],
              "variable": [
                {
                  "id": "revision",
                  "value": "{}",
                  "type": "string"
                },
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get repositories username repo slug commit revision"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0a5f5213-b068-47cd-87f9-98ab8b39cbfa"
            }
          ]
        }
      ]
    }
  ]
}