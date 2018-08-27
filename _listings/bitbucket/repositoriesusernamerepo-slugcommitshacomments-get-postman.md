{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Commit Sha Comments",
    "_postman_id": "31c13a26-ff6a-4921-896e-fdad28dbe86c",
    "description": "Returns the commit's comments.\n\nThis includes both global and inline comments.\n\nThe default sorting is oldest to newest and can be overridden with\nthe `sort` query parameter.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "cd9c376b-10a7-4890-a567-ccc397046738",
          "name": "getRepositoriesUsernameRepoSlugCommitShaComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/commit/:sha/comments"
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
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the commit's comments"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "56cbc016-f976-43fd-b616-c5050e2a0b3c"
            }
          ]
        }
      ]
    }
  ]
}