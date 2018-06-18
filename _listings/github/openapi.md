---
swagger: "2.0"
x-collection-name: GitHub
x-complete: 1
info:
  title: GitHub
  description: github-is-the-best-place-to-share-code-with-friends-coworkers-classmates-and-complete-strangers--over-24-million-people-use-github-to-build-amazing-things-together-across-67-million-repositories--with-the-collaborative-features-of-github-com-and-github-business-it-has-never-been-easier-for-individuals-and-teams-to-write-faster-better-code-
  termsOfService: https://help.github.com/articles/github-terms-of-service/#b-api-terms
  version: 1.0.0
host: api.github.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /repos/{owner}/{repo}/commits:
    get:
      summary: Get Repos Owner Repo Commits
      description: List commits on a repository.
      operationId: list-commits-on-a-repository
      x-api-path-slug: reposownerrepocommits-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: author
        description: GitHub login, name, or email by which to filter by commit author
      - in: path
        name: owner
        description: Name of repository owner
      - in: query
        name: path
        description: Only commits containing this file path will be returned
      - in: path
        name: repo
        description: Name of repository
      - in: query
        name: sha
        description: Sha or branch to start listing commits from
      - in: query
        name: since
        description: 'The time should be passed in as UTC in the ISO 8601 format:
          YYYY-MM-DDTHH:MM:SSZ'
      - in: query
        name: until
        description: ISO 8601 Date - Only commits before this date will be returned
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Commits
  /repos/{owner}/{repo}/commits/{ref}/status:
    get:
      summary: Get Repos Owner Repo Commits Ref Status
      description: |-
        Get the combined Status for a specific Ref
        The Combined status endpoint is currently available for developers to preview. During the preview period, the API may change without advance notice. Please see the blog post for full details.
        To access this endpoint during the preview period, you must provide a custom media type in the Accept header:
        application/vnd.github.she-hulk-preview+json
      operationId: get-the-combined-status-for-a-specific-refthe-combined-status-endpoint-is-currently-available-for-de
      x-api-path-slug: reposownerrepocommitsrefstatus-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: ref
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Commits
      - Ref
      - Status
  /repos/{owner}/{repo}/commits/{shaCode}:
    get:
      summary: Get Repos Owner Repo Commits Shacode
      description: Get a single commit.
      operationId: get-a-single-commit
      x-api-path-slug: reposownerrepocommitsshacode-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      - in: path
        name: shaCode
        description: SHA-1 code of the commit
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Commits
      - Shacode
  /repos/{owner}/{repo}/commits/{shaCode}/comments:
    get:
      summary: Get Repos Owner Repo Commits Shacode Comments
      description: List comments for a single commitList comments for a single commit.
      operationId: list-comments-for-a-single-commitlist-comments-for-a-single-commit
      x-api-path-slug: reposownerrepocommitsshacodecomments-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      - in: path
        name: shaCode
        description: SHA-1 code of the commit
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Commits
      - Shacode
      - Comments
    post:
      summary: Add Repos Owner Repo Commits Shacode Comments
      description: Create a commit comment.
      operationId: create-a-commit-comment
      x-api-path-slug: reposownerrepocommitsshacodecomments-post
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      - in: path
        name: shaCode
        description: SHA-1 code of the commit
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Commits
      - Shacode
      - Comments
  /repos/{owner}/{repo}/git/commits:
    post:
      summary: Add Repos Owner Repo Git Commits
      description: Create a Commit.
      operationId: create-a-commit
      x-api-path-slug: reposownerrepogitcommits-post
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Git
      - Commits
  /repos/{owner}/{repo}/git/commits/{shaCode}:
    get:
      summary: Get Repos Owner Repo Git Commits Shacode
      description: Get a Commit.
      operationId: get-a-commit
      x-api-path-slug: reposownerrepogitcommitsshacode-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      - in: path
        name: shaCode
        description: SHA-1 code
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Git
      - Commits
      - Shacode
  /repos/{owner}/{repo}/pulls/{number}/commits:
    get:
      summary: Get Repos Owner Repo Pulls Number Commits
      description: List commits on a pull request.
      operationId: list-commits-on-a-pull-request
      x-api-path-slug: reposownerrepopullsnumbercommits-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Id of pull
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
      - Number
      - Commits
---