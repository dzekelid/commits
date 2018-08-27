swagger: "2.0"
x-collection-name: AWS CodeCommit
x-complete: 1
info:
  title: AWS CodeCommit API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=GetCommit:
    get:
      summary: Get Commit
      description: Returns information about a commit, including commit message and
        committer information.
      operationId: getCommit
      x-api-path-slug: actiongetcommit-get
      parameters:
      - in: query
        name: commitId
        description: The commit ID
        type: string
      - in: query
        name: repositoryName
        description: The name of the repository to which the commit was made
        type: string
      responses:
        200:
          description: OK
      tags:
      - Commits