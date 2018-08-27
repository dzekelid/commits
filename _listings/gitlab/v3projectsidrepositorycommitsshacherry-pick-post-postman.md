{
  "info": {
    "name": "GitLab Post Projects Repository Commits Sha Cherry Pick",
    "_postman_id": "04c648ec-f521-4b29-bcf6-3aa434a54618",
    "description": "Post projects repository commits sha cherry pick.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Projects",
      "item": [
        {
          "id": "1b780fca-2a34-4db7-b83b-817b8060913d",
          "name": "getV3ProjectsIdRepositoryCommitsShaBuilds",
          "request": {
            "url": {
              "protocol": "http",
              "host": "localhost",
              "path": [
                "api",
                "v3/projects/:id/repository/commits/:sha/builds"
              ],
              "port": "3000",
              "query": [
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "per_page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "scope",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sha",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get builds for a specific commit of a project"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c8b93d10-b7f7-4a5a-84e1-8a843206c8d8"
            }
          ]
        },
        {
          "id": "813fb509-fd3f-424d-b406-3f8ea74298fe",
          "name": "getV3ProjectsIdRepositoryCommits",
          "request": {
            "url": {
              "protocol": "http",
              "host": "localhost",
              "path": [
                "api",
                "v3/projects/:id/repository/commits"
              ],
              "port": "3000",
              "query": [
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "path",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "per_page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "ref_name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "since",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "until",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a project repository commits"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a43a33d0-4577-4cb8-bdf0-caaf354ed41f"
            }
          ]
        },
        {
          "id": "11f01c67-5dd4-4fb4-aa72-2f53307781df",
          "name": "postV3ProjectsIdRepositoryCommits",
          "request": {
            "url": {
              "protocol": "http",
              "host": "localhost",
              "path": [
                "api",
                "v3/projects/:id/repository/commits"
              ],
              "port": "3000",
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "actions",
                  "value": "{}",
                  "disabled": false,
                  "description": "Actions to perform in commit"
                },
                {
                  "key": "author_email",
                  "value": "{}",
                  "disabled": false,
                  "description": "Author email for commit"
                },
                {
                  "key": "author_name",
                  "value": "{}",
                  "disabled": false,
                  "description": "Author name for commit"
                },
                {
                  "key": "branch_name",
                  "value": "{}",
                  "disabled": false,
                  "description": "The name of branch"
                },
                {
                  "key": "commit_message",
                  "value": "{}",
                  "disabled": false,
                  "description": "Commit message"
                }
              ]
            },
            "description": "This feature was introduced in GitLab 8.13"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a068a15e-2770-47ef-849a-9ffe6d901f2d"
            }
          ]
        },
        {
          "id": "8ecbaefe-1b6a-46b7-97bf-168476219b29",
          "name": "getV3ProjectsIdRepositoryCommitsSha",
          "request": {
            "url": {
              "protocol": "http",
              "host": "localhost",
              "path": [
                "api",
                "v3/projects/:id/repository/commits/:sha"
              ],
              "port": "3000",
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sha",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get projects repository commits sha."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "36844555-7793-481d-8225-7938fe2268ab"
            }
          ]
        },
        {
          "id": "b81a850f-ff70-413a-8f91-6a08a7830e06",
          "name": "getV3ProjectsIdRepositoryCommitsShaDiff",
          "request": {
            "url": {
              "protocol": "http",
              "host": "localhost",
              "path": [
                "api",
                "v3/projects/:id/repository/commits/:sha/diff"
              ],
              "port": "3000",
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sha",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get the diff for a specific commit of a project"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c58c98c9-71d3-47a1-a3bf-a685836e498a"
            }
          ]
        },
        {
          "id": "ebeb83d4-c0a9-4de2-8189-05b264c3b7e3",
          "name": "getV3ProjectsIdRepositoryCommitsShaComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "localhost",
              "path": [
                "api",
                "v3/projects/:id/repository/commits/:sha/comments"
              ],
              "port": "3000",
              "query": [
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "per_page",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sha",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get projects repository commits sha comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b8d45d49-5090-4842-979c-612aa79c31f8"
            }
          ]
        },
        {
          "id": "b500d1bf-7d37-4fb3-8d2b-5ce0e2753aa3",
          "name": "postV3ProjectsIdRepositoryCommitsShaComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "localhost",
              "path": [
                "api",
                "v3/projects/:id/repository/commits/:sha/comments"
              ],
              "port": "3000",
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sha",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "line",
                  "value": "{}",
                  "disabled": false,
                  "description": "The line number"
                },
                {
                  "key": "line_type",
                  "value": "{}",
                  "disabled": false,
                  "description": "The type of the line"
                },
                {
                  "key": "note",
                  "value": "{}",
                  "disabled": false,
                  "description": "The text of the comment"
                },
                {
                  "key": "path",
                  "value": "{}",
                  "disabled": false,
                  "description": "The file path"
                }
              ]
            },
            "description": "Post projects repository commits sha comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d29b9483-7e74-487e-be98-aebcd555ea9c"
            }
          ]
        },
        {
          "id": "7e75b99d-d588-4ba9-8b03-7a56a28608f6",
          "name": "postV3ProjectsIdRepositoryCommitsShaCherryPick",
          "request": {
            "url": {
              "protocol": "http",
              "host": "localhost",
              "path": [
                "api",
                "v3/projects/:id/repository/commits/:sha/cherry_pick"
              ],
              "port": "3000",
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sha",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "branch",
                  "value": "{}",
                  "disabled": false,
                  "description": "The name of the branch"
                }
              ]
            },
            "description": "Post projects repository commits sha cherry pick."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7198ee43-1a4d-4fcf-ab72-ce640be4a12f"
            }
          ]
        }
      ]
    }
  ]
}