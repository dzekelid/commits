{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Commits",
    "_postman_id": "a1a10c95-26fe-4d95-8be8-0ee4af3e2b5d",
    "description": "These are the repository's commits. They are paginated and returned\nin reverse chronological order, similar to the output of `git log` and\n`hg log`. Like these tools, the DAG can be filtered.\n\n## GET /repositories/{username}/{repo_slug}/commits/\n\nReturns all commits in the repo in topological order (newest commit\nfirst). All branches and tags are included (similar to\n`git log --all` and `hg log`).\n\n## GET /repositories/{username}/{repo_slug}/commits/master\n\nReturns all commits on rev `master` (similar to `git log master`,\n`hg log master`).\n\n## GET /repositories/{username}/{repo_slug}/commits/dev?exclude=master\n\nReturns all commits on ref `dev`, except those that are reachable on\n`master` (similar to `git log dev ^master`).\n\n## GET /repositories/{username}/{repo_slug}/commits/?exclude=master\n\nReturns all commits in the repo that are not on master\n(similar to `git log --all ^master`).\n\n## GET /repositories/{username}/{repo_slug}/commits/?include=foo&include=bar&exclude=fu&exclude=fubar\n\nReturns all commits that are on refs `foo` or `bar`, but not on `fu` or\n`fubar` (similar to `git log foo bar ^fu ^fubar`).\n\nBecause the response could include a very large number of commits, it\nis paginated. Follow the 'next' link in the response to navigate to the\nnext page of commits. As with other paginated resources, do not\nconstruct your own links.\n\nWhen the include and exclude parameters are more than can fit in a\nquery string, clients can use a `x-www-form-urlencoded` POST instead.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "f0f0d642-9301-4307-a06f-c6fb37339474",
          "name": "getRepositoriesUsernameRepoSlugCommits",
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "These are the repository's commits"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b858fa08-a96d-4dcc-9e63-381c97b71c9f"
            }
          ]
        }
      ]
    }
  ]
}