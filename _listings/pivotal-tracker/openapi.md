---
swagger: "2.0"
x-collection-name: Pivotal Tracker
x-complete: 1
info:
  title: Pivotal Tracker
  description: access-and-manipulate-agile-project-management-data-including-projects-stories-and-tasks-
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
---