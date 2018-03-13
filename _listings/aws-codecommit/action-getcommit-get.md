---
swagger: "2.0"
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
  /?Action=GetCommit&k=1:
    get:
      summary: ' Get Commit '
      description: Returns information about a commit, including commit message and
        committer information
      operationId: getCommit
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
      - commits
definitions: []
x-collection-name: AWS CodeCommit
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---