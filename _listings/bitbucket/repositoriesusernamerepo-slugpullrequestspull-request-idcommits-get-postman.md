{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Pullrequests Pull Request  Commits",
    "_postman_id": "6bf79fa7-12f3-4fdb-aec3-da3ac64b80f7",
    "description": "Returns a paginated list of the pull request's commits.\n\nThese are the commits that are being merged into the destination\nbranch when the pull requests gets accepted.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "7051c95a-3643-416d-843d-a174d48a67ae",
          "name": "getRepositoriesUsernameRepoSlugPullrequestsPullRequestCommits",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/pullrequests/:pull_request_id/commits"
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
                  "id": "pull_request_id",
                  "value": "pull_request_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a paginated list of the pull request's commits"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d3319171-9802-4608-901e-e0c95d169107"
            }
          ]
        }
      ]
    }
  ]
}