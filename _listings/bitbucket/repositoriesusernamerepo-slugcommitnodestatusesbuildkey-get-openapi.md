---
swagger: "2.0"
x-collection-name: Bitbucket
x-complete: 0
info:
  title: Bitbucket Get Repositories Username Repo Slug Commit Node Statuses Build
    Key
  description: Get repositories username repo slug commit node statuses build key
  termsOfService: https://www.atlassian.com/legal/customer-agreement
  contact:
    name: Bitbucket Support
    url: https://support.atlassian.com/bitbucket
    email: support@bitbucket.org
  version: 1.0.0
host: api.bitbucket.org
basePath: /2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /repositories/{username}/{repo_slug}/commits:
    get:
      summary: Get Repositories Username Repo Slug Commits
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
      operationId: getRepositoriesUsernameRepoSlugCommits
      x-api-path-slug: repositoriesusernamerepo-slugcommits-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commits
    parameters:
      summary: Parameters Repositories Username Repo Slug Commits
      description: Parameters repositories username repo slug commits
      operationId: parametersRepositoriesUsernameRepoSlugCommits
      x-api-path-slug: repositoriesusernamerepo-slugcommits-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commits
    post:
      summary: Add Repositories Username Repo Slug Commits
      description: |-
        Identical to `GET /repositories/{username}/{repo_slug}/commits`,
        except that POST allows clients to place the include and exclude
        parameters in the request body to avoid URL length issues.

        **Note that this resource does NOT support new commit creation.**
      operationId: postRepositoriesUsernameRepoSlugCommits
      x-api-path-slug: repositoriesusernamerepo-slugcommits-post
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commits
  /repositories/{username}/{repo_slug}/commits/{revision}:
    get:
      summary: Get Repositories Username Repo Slug Commits Revision
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
      operationId: getRepositoriesUsernameRepoSlugCommitsRevision
      x-api-path-slug: repositoriesusernamerepo-slugcommitsrevision-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commits
      - Revision
    parameters:
      summary: Parameters Repositories Username Repo Slug Commits Revision
      description: Parameters repositories username repo slug commits revision
      operationId: parametersRepositoriesUsernameRepoSlugCommitsRevision
      x-api-path-slug: repositoriesusernamerepo-slugcommitsrevision-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commits
      - Revision
    post:
      summary: Add Repositories Username Repo Slug Commits Revision
      description: |-
        Identical to `GET /repositories/{username}/{repo_slug}/commits`,
        except that POST allows clients to place the include and exclude
        parameters in the request body to avoid URL length issues.

        **Note that this resource does NOT support new commit creation.**
      operationId: postRepositoriesUsernameRepoSlugCommitsRevision
      x-api-path-slug: repositoriesusernamerepo-slugcommitsrevision-post
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commits
      - Revision
  /repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/commits:
    get:
      summary: Get Repositories Username Repo Slug Pullrequests Pull Request  Commits
      description: |-
        Returns a paginated list of the pull request's commits.

        These are the commits that are being merged into the destination
        branch when the pull requests gets accepted.
      operationId: getRepositoriesUsernameRepoSlugPullrequestsPullRequestCommits
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idcommits-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Commits
    parameters:
      summary: Parameters Repositories Username Repo Slug Pullrequests Pull Request  Commits
      description: Parameters repositories username repo slug pullrequests pull request  commits
      operationId: parametersRepositoriesUsernameRepoSlugPullrequestsPullRequestCommits
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idcommits-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Commits
  /snippets/{username}/{encoded_id}/commits:
    get:
      summary: Get Snippets Username Encoded  Commits
      description: Returns the changes (commits) made on this snippet.
      operationId: getSnippetsUsernameEncodedCommits
      x-api-path-slug: snippetsusernameencoded-idcommits-get
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Commits
    parameters:
      summary: Parameters Snippets Username Encoded  Commits
      description: Parameters snippets username encoded  commits
      operationId: parametersSnippetsUsernameEncodedCommits
      x-api-path-slug: snippetsusernameencoded-idcommits-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Commits
  /snippets/{username}/{encoded_id}/commits/{revision}:
    get:
      summary: Get Snippets Username Encoded  Commits Revision
      description: Get snippets username encoded  commits revision
      operationId: getSnippetsUsernameEncodedCommitsRevision
      x-api-path-slug: snippetsusernameencoded-idcommitsrevision-get
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Commits
      - Revision
    parameters:
      summary: Parameters Snippets Username Encoded  Commits Revision
      description: Parameters snippets username encoded  commits revision
      operationId: parametersSnippetsUsernameEncodedCommitsRevision
      x-api-path-slug: snippetsusernameencoded-idcommitsrevision-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Commits
      - Revision
  /repositories/{username}/{repo_slug}/commit/{node}/approve:
    delete:
      summary: Delete Repositories Username Repo Slug Commit Node Approve
      description: |-
        Redact the authenticated user's approval of the specified commit.

        This operation is only available to users that have explicit access to
        the repository. In contrast, just the fact that a repository is
        publicly accessible to users does not give them the ability to approve
        commits.
      operationId: deleteRepositoriesUsernameRepoSlugCommitNodeApprove
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodeapprove-delete
      parameters:
      - in: path
        name: node
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Approve
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Node Approve
      description: Parameters repositories username repo slug commit node approve
      operationId: parametersRepositoriesUsernameRepoSlugCommitNodeApprove
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodeapprove-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Approve
    post:
      summary: Add Repositories Username Repo Slug Commit Node Approve
      description: |-
        Approve the specified commit as the authenticated user.

        This operation is only available to users that have explicit access to
        the repository. In contrast, just the fact that a repository is
        publicly accessible to users does not give them the ability to approve
        commits.
      operationId: postRepositoriesUsernameRepoSlugCommitNodeApprove
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodeapprove-post
      parameters:
      - in: path
        name: node
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Approve
  /repositories/{username}/{repo_slug}/commit/{node}/statuses:
    get:
      summary: Get Repositories Username Repo Slug Commit Node Statuses
      description: Returns all statuses (e.g. build results) for a specific commit.
      operationId: getRepositoriesUsernameRepoSlugCommitNodeStatuses
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatuses-get
      parameters:
      - in: path
        name: node
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Node Statuses
      description: Parameters repositories username repo slug commit node statuses
      operationId: parametersRepositoriesUsernameRepoSlugCommitNodeStatuses
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatuses-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
  /repositories/{username}/{repo_slug}/commit/{node}/statuses/build:
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Node Statuses Build
      description: Parameters repositories username repo slug commit node statuses
        build
      operationId: parametersRepositoriesUsernameRepoSlugCommitNodeStatusesBuild
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatusesbuild-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
      - Build
    post:
      summary: Add Repositories Username Repo Slug Commit Node Statuses Build
      description: |-
        Creates a new build status against the specified commit.

        If the specified key already exists, the existing status object will
        be overwritten.

        When creating a new commit status, you can use a URI template for the URL.
        Templates are URLs that contain variable names that Bitbucket will
        evaluate at runtime whenever the URL is displayed anywhere similar to
        parameter substitution in
        [Bitbucket Connect](https://developer.atlassian.com/bitbucket/concepts/context-parameters.html).
        For example, one could use `https://foo.com/builds/{repository.full_name}`
        which Bitbucket will turn into `https://foo.com/builds/foo/bar` at render time.
        The context variables available are `repository` and `commit`.
      operationId: postRepositoriesUsernameRepoSlugCommitNodeStatusesBuild
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatusesbuild-post
      parameters:
      - in: path
        name: node
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
      - Build
  /repositories/{username}/{repo_slug}/commit/{node}/statuses/build/{key}:
    get:
      summary: Get Repositories Username Repo Slug Commit Node Statuses Build Key
      description: Get repositories username repo slug commit node statuses build
        key
      operationId: getRepositoriesUsernameRepoSlugCommitNodeStatusesBuildKey
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatusesbuildkey-get
      parameters:
      - in: path
        name: key
        description: The build status unique key
      - in: path
        name: node
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
      - Build
      - Key
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Node Statuses Build
        Key
      description: Parameters repositories username repo slug commit node statuses
        build key
      operationId: parametersRepositoriesUsernameRepoSlugCommitNodeStatusesBuildKey
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatusesbuildkey-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
      - Build
      - Key
    put:
      summary: Update Repositories Username Repo Slug Commit Node Statuses Build Key
      description: |-
        Used to update the current status of a build status object on the
        specific commit.

        This operation can also be used to change other properties of the
        build status:

        * `state`
        * `name`
        * `description`
        * `url`
        * `refname`

        The `key` cannot be changed.
      operationId: putRepositoriesUsernameRepoSlugCommitNodeStatusesBuildKey
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatusesbuildkey-put
      parameters:
      - in: path
        name: key
        description: The commit status unique key
      - in: path
        name: node
        description: The commits SHA1
      - in: body
        name: _body
        description: The updated build status object
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
      - Build
      - Key
  /repositories/{username}/{repo_slug}/commit/{revision}:
    get:
      summary: Get Repositories Username Repo Slug Commit Revision
      description: Get repositories username repo slug commit revision
      operationId: getRepositoriesUsernameRepoSlugCommitRevision
      x-api-path-slug: repositoriesusernamerepo-slugcommitrevision-get
      parameters:
      - in: path
        name: revision
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Revision
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Revision
      description: Parameters repositories username repo slug commit revision
      operationId: parametersRepositoriesUsernameRepoSlugCommitRevision
      x-api-path-slug: repositoriesusernamerepo-slugcommitrevision-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Revision
  /repositories/{username}/{repo_slug}/commit/{sha}/comments:
    get:
      summary: Get Repositories Username Repo Slug Commit Sha Comments
      description: |-
        Returns the commit's comments.

        This includes both global and inline comments.

        The default sorting is oldest to newest and can be overridden with
        the `sort` query parameter.
      operationId: getRepositoriesUsernameRepoSlugCommitShaComments
      x-api-path-slug: repositoriesusernamerepo-slugcommitshacomments-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Sha
      - Comments
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Sha Comments
      description: Parameters repositories username repo slug commit sha comments
      operationId: parametersRepositoriesUsernameRepoSlugCommitShaComments
      x-api-path-slug: repositoriesusernamerepo-slugcommitshacomments-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Sha
      - Comments
  /repositories/{username}/{repo_slug}/commit/{sha}/comments/{comment_id}:
    get:
      summary: Get Repositories Username Repo Slug Commit Sha Comments Comment
      description: Get repositories username repo slug commit sha comments comment
      operationId: getRepositoriesUsernameRepoSlugCommitShaCommentsComment
      x-api-path-slug: repositoriesusernamerepo-slugcommitshacommentscomment-id-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Sha
      - Comments
      - Comment
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Sha Comments Comment
      description: Parameters repositories username repo slug commit sha comments
        comment
      operationId: parametersRepositoriesUsernameRepoSlugCommitShaCommentsComment
      x-api-path-slug: repositoriesusernamerepo-slugcommitshacommentscomment-id-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Sha
      - Comments
      - Comment
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