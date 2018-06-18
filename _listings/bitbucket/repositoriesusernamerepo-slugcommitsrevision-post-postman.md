{
  "info": {
    "name": "Bitbucket Add Repositories Username Repo Slug Commits Revision",
    "_postman_id": "f1cccfea-fb0d-41eb-8193-dd41502ba1cd",
    "description": "Identical to `GET /repositories/{username}/{repo_slug}/commits`,\nexcept that POST allows clients to place the include and exclude\nparameters in the request body to avoid URL length issues.\n\n**Note that this resource does NOT support new commit creation.**",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "403f9f48-ece7-4dcf-8692-0598e6540348",
          "name": "postRepositoriesUsernameRepoSlugCommitsRevision",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/commits/:revision"
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
                  "id": "revision",
                  "value": "revision",
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
              "id": "fcd76a75-cab8-4dc0-93cd-88f62bf5c652"
            }
          ]
        }
      ]
    }
  ]
}