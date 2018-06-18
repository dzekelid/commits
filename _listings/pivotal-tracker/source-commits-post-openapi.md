---
swagger: "2.0"
x-collection-name: Pivotal Tracker
x-complete: 0
info:
  title: Pivotal Tracker Post Source Commits
  description: Allows integration with post-commit hooks of Source Control Management
    (SCM) systems such as Subversion, Git, etc.
  version: 1.0.0
host: www.pivotaltracker.com
basePath: /services/v3/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /source_commits:
    post:
      summary: Post Source Commits
      description: Allows integration with post-commit hooks of Source Control Management
        (SCM) systems such as Subversion, Git, etc.
      operationId: postSourceCommits
      x-api-path-slug: source-commits-post
      responses:
        200:
          description: OK
      tags:
      - Source
      - Commits
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