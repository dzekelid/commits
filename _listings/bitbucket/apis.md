---
name: Bitbucket
x-slug: bitbucket
description: Collaborate on code with inline comments and pull requests. Manage and
  share your Git repositories to build and ship software, as a team.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
x-kinRank: "8"
x-alexaRank: "901"
tags: Commits
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/apis.md
specificationVersion: "0.14"
apis:
- name: Bitbucket Get Repositories Username Repo Slug Commits
  x-api-slug: bitbucket
  description: |-
    These are the repository's commits. They are paginated and returned
    in reverse chronological order, similar to the output of `git log` and
    `hg log`. Like these tools, the DAG can be filtered.

    ## GET /repositories/{username}/{repo_slug}/commits/

    Returns all commits in the repo in topological order (newest commit
    first). All branches and tags are included (similar to
    `git log --all` and `hg log`).

    ## GET /repositories/{username}/{repo_slug}/commits/master

    Returns all commits on rev `master` (similar to `git log master`,
    `hg log master`).

    ## GET /repositories/{username}/{repo_slug}/commits/dev?exclude=master

    Returns all commits on ref `dev`, except those that are reachable on
    `master` (similar to `git log dev ^master`).

    ## GET /repositories/{username}/{repo_slug}/commits/?exclude=master

    Returns all commits in the repo that are not on master
    (similar to `git log --all ^master`).

    ## GET /repositories/{username}/{repo_slug}/commits/?include=foo&include=bar&exclude=fu&exclude=fubar

    Returns all commits that are on refs `foo` or `bar`, but not on `fu` or
    `fubar` (similar to `git log foo bar ^fu ^fubar`).

    Because the response could include a very large number of commits, it
    is paginated. Follow the 'next' link in the response to navigate to the
    next page of commits. As with other paginated resources, do not
    construct your own links.

    When the include and exclude parameters are more than can fit in a
    query string, clients can use a `x-www-form-urlencoded` POST instead.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commits
  tags: Repositories, Username, Repo, Slug, Commits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/repositoriesusernamerepo-slugcommits-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/repositoriesusernamerepo-slugcommits-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Commits
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug commits
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commits
  tags: Repositories, Username, Repo, Slug, Commits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/repositoriesusernamerepo-slugcommits-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/repositoriesusernamerepo-slugcommits-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Commits
  x-api-slug: bitbucket
  description: |-
    Identical to `GET /repositories/{username}/{repo_slug}/commits`,
    except that POST allows clients to place the include and exclude
    parameters in the request body to avoid URL length issues.

    **Note that this resource does NOT support new commit creation.**
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commits
  tags: Repositories, Username, Repo, Slug, Commits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/repositoriesusernamerepo-slugcommits-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/repositoriesusernamerepo-slugcommits-post-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Commits Revision
  x-api-slug: bitbucket
  description: |-
    These are the repository's commits. They are paginated and returned
    in reverse chronological order, similar to the output of `git log` and
    `hg log`. Like these tools, the DAG can be filtered.

    ## GET /repositories/{username}/{repo_slug}/commits/

    Returns all commits in the repo in topological order (newest commit
    first). All branches and tags are included (similar to
    `git log --all` and `hg log`).

    ## GET /repositories/{username}/{repo_slug}/commits/master

    Returns all commits on rev `master` (similar to `git log master`,
    `hg log master`).

    ## GET /repositories/{username}/{repo_slug}/commits/dev?exclude=master

    Returns all commits on ref `dev`, except those that are reachable on
    `master` (similar to `git log dev ^master`).

    ## GET /repositories/{username}/{repo_slug}/commits/?exclude=master

    Returns all commits in the repo that are not on master
    (similar to `git log --all ^master`).

    ## GET /repositories/{username}/{repo_slug}/commits/?include=foo&include=bar&exclude=fu&exclude=fubar

    Returns all commits that are on refs `foo` or `bar`, but not on `fu` or
    `fubar` (similar to `git log foo bar ^fu ^fubar`).

    Because the response could include a very large number of commits, it
    is paginated. Follow the 'next' link in the response to navigate to the
    next page of commits. As with other paginated resources, do not
    construct your own links.

    When the include and exclude parameters are more than can fit in a
    query string, clients can use a `x-www-form-urlencoded` POST instead.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commits/{revision}
  tags: Repositories, Username, Repo, Slug, Commits, Revision
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitsrevision-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitsrevision-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Commits Revision
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug commits revision
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commits/{revision}
  tags: Repositories, Username, Repo, Slug, Commits, Revision
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitsrevision-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitsrevision-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Commits Revision
  x-api-slug: bitbucket
  description: |-
    Identical to `GET /repositories/{username}/{repo_slug}/commits`,
    except that POST allows clients to place the include and exclude
    parameters in the request body to avoid URL length issues.

    **Note that this resource does NOT support new commit creation.**
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commits/{revision}
  tags: Repositories, Username, Repo, Slug, Commits, Revision
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitsrevision-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitsrevision-post-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pullrequests Pull Request  Commits
  x-api-slug: bitbucket
  description: |-
    Returns a paginated list of the pull request's commits.

    These are the commits that are being merged into the destination
    branch when the pull requests gets accepted.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/commits
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Commits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idcommits-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idcommits-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Pullrequests Pull Request  Commits
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug pullrequests pull request  commits
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/commits
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Commits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idcommits-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idcommits-parameters-openapi.md
- name: Bitbucket Get Snippets Username Encoded  Commits
  x-api-slug: bitbucket
  description: Returns the changes (commits) made on this snippet.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/commits
  tags: Snippets, Username, Encoded, , Commits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/snippetsusernameencoded-idcommits-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/snippetsusernameencoded-idcommits-get-openapi.md
- name: Bitbucket Parameters Snippets Username Encoded  Commits
  x-api-slug: bitbucket
  description: Parameters snippets username encoded  commits
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/commits
  tags: Snippets, Username, Encoded, , Commits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/snippetsusernameencoded-idcommits-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/snippetsusernameencoded-idcommits-parameters-openapi.md
- name: Bitbucket Get Snippets Username Encoded  Commits Revision
  x-api-slug: bitbucket
  description: Get snippets username encoded  commits revision
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/commits/{revision}
  tags: Snippets, Username, Encoded, , Commits, Revision
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/snippetsusernameencoded-idcommitsrevision-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/snippetsusernameencoded-idcommitsrevision-get-openapi.md
- name: Bitbucket Parameters Snippets Username Encoded  Commits Revision
  x-api-slug: bitbucket
  description: Parameters snippets username encoded  commits revision
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/commits/{revision}
  tags: Snippets, Username, Encoded, , Commits, Revision
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/snippetsusernameencoded-idcommitsrevision-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/snippetsusernameencoded-idcommitsrevision-parameters-openapi.md
- name: Bitbucket
  x-api-slug: bitbucket
  description: Collaborate on code with inline comments and pull requests. Manage
    and share your Git repositories to build and ship software, as a team.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Commits
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/commits/master/_listings/bitbucket/openapi.md
x-common:
- type: x-crunchbase
  url: https://crunchbase.com/organization/bitbucket
- type: x-developer
  url: https://developer.atlassian.com/cloud/bitbucket/
- type: x-documentation
  url: https://confluence.atlassian.com/bitbucket/bitbucket-cloud-documentation-221448814.html?_ga=2.77295890.629375793.1519179030-1077111323.1516485126
- type: x-status
  url: https://status.bitbucket.org/?_ga=2.76365714.629375793.1519179030-1077111323.1516485126
- type: x-support
  url: https://support.atlassian.com/bitbucket-cloud/
- type: x-terms-of-service
  url: https://www.atlassian.com/legal/customer-agreement?_ga=2.76365714.629375793.1519179030-1077111323.1516485126
- type: x-twitter
  url: https://twitter.com/bitbucket
- type: x-website
  url: http://bitbucket.org
- type: x-website
  url: https://bitbucket.org/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---