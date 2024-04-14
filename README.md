# Renovate depTypes Reproduction

The depTypes is a variable that holds a list all depTypes identified during the Renovate execution.

The PR addressed this issue https://github.com/renovatebot/renovate/pull/27939
Sure @rarkins .

**The issue**

* I ran a renovate execution from the branch of this PR https://github.com/renovatebot/renovate/pull/28148 so I can use the `includes` for templating. 
* This execution raised this PR https://github.com/juancarlosjr97/renovate-test-27939/pull/4
* The expected PR title and commit should have been `production Update all dependencies`

<details><summary>Logs</summary>

```
> renovate@0.0.0-semantic-release prestart /Users/juancarlosjr97/Developer/Personal/renovate
> run-s 'generate:*'


> renovate@0.0.0-semantic-release generate:imports /Users/juancarlosjr97/Developer/Personal/renovate
> node tools/generate-imports.mjs

generating imports
> data/debian-distro-info.json
> data/kubernetes-api.json5
> data/node-js-schedule.json
> data/ubuntu-distro-info.json
> node_modules/emojibase-data/en/shortcodes/github.json
generating hashes

> renovate@0.0.0-semantic-release start /Users/juancarlosjr97/Developer/Personal/renovate
> ts-node lib/renovate.ts "juancarlosjr97/renovate-test-27939"

DEBUG: Using RE2 regex engine
DEBUG: Parsing configs
DEBUG: Checking for config file in config.js
DEBUG: No config file found on disk - skipping
DEBUG: File config
       "config": {}
DEBUG: CLI config
       "config": {"repositories": ["juancarlosjr97/renovate-test-27939"]}
DEBUG: Env config
       "config": {"hostRules": [], "token": "***********"}
DEBUG: Combined config
       "config": {
         "hostRules": [],
         "token": "***********",
         "repositories": ["juancarlosjr97/renovate-test-27939"]
       }
DEBUG: Enabling forkProcessing while in non-autodiscover mode
DEBUG: Found valid git version: 2.40.0
DEBUG: Setting global hostRules
DEBUG: Using default github endpoint: https://api.github.com/
DEBUG: hostRules: authentication already set for api.github.com
DEBUG: Platform config
       "platformConfig": {
         "hostType": "github",
         "endpoint": "https://api.github.com/",
         "isGHApp": false,
         "isGhe": false,
         "userDetails": {
           "username": "juancarlosjr97",
           "name": "Juan Carlos Blanco Delgado",
           "id": 36451129
         },
         "userEmail": "***"
       },
       "renovateUsername": "juancarlosjr97"
DEBUG: Using platform gitAuthor: Juan Carlos Blanco Delgado <juancarlosjr97@gmail.com>
DEBUG: Adding token authentication for api.github.com (hostType=github) to hostRules
DEBUG: Using baseDir: /var/folders/73/ykcrrqpd6rjd96sptqy1cx480000gn/T/renovate
DEBUG: Using cacheDir: /var/folders/73/ykcrrqpd6rjd96sptqy1cx480000gn/T/renovate/cache
DEBUG: Using containerbaseDir: /var/folders/73/ykcrrqpd6rjd96sptqy1cx480000gn/T/renovate/cache/containerbase
DEBUG: Initializing Renovate internal cache into /var/folders/73/ykcrrqpd6rjd96sptqy1cx480000gn/T/renovate/cache/renovate/renovate-cache-v1
DEBUG: Commits limit = null
DEBUG: Setting global hostRules
DEBUG: Adding token authentication for api.github.com (hostType=github) to hostRules
DEBUG: validatePresets()
DEBUG: Reinitializing hostRules for repo
DEBUG: Clearing hostRules
DEBUG: Adding token authentication for api.github.com (hostType=github) to hostRules
 INFO: Repository started (repository=juancarlosjr97/renovate-test-27939)
       "renovateVersion": "0.0.0-semantic-release"
DEBUG: Using localDir: /var/folders/73/ykcrrqpd6rjd96sptqy1cx480000gn/T/renovate/repos/github/juancarlosjr97/renovate-test-27939 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: PackageFiles.clear() - Package files deleted (repository=juancarlosjr97/renovate-test-27939)
DEBUG: initRepo("juancarlosjr97/renovate-test-27939") (repository=juancarlosjr97/renovate-test-27939)
DEBUG: hostRules: authentication already set for api.github.com (repository=juancarlosjr97/renovate-test-27939)
DEBUG: juancarlosjr97/renovate-test-27939 default branch = main (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using personal access token for git init (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Resetting npmrc (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Resetting npmrc (repository=juancarlosjr97/renovate-test-27939)
DEBUG: checkOnboarding() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: isOnboarded() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: findPr(renovate/configure, Configure Renovate, !open) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: http cache: saving https://api.github.com/repos/juancarlosjr97/renovate-test-27939/pulls?per_page=100&state=all&sort=updated&direction=desc&page=1 (etag=W/"79945a9c67d615a1d67c45f8dab8fc1d73f77c81d8f9ce099d49f66e607f90d1", lastModified=undefined) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: getPrList success (repository=juancarlosjr97/renovate-test-27939)
       "pullsTotal": 2,
       "requestsTotal": 1,
       "apiQuotaAffected": true
DEBUG: findPr(renovate/configure, chore: Configure Renovate, !open) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: findFile(renovate.json) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Initializing git repository into /var/folders/73/ykcrrqpd6rjd96sptqy1cx480000gn/T/renovate/repos/github/juancarlosjr97/renovate-test-27939 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Performing blobless clone (repository=juancarlosjr97/renovate-test-27939)
DEBUG: git clone completed (repository=juancarlosjr97/renovate-test-27939)
       "durationMs": 951
DEBUG: latest repository commit (repository=juancarlosjr97/renovate-test-27939)
       "latestCommit": {
         "hash": "85b98f6c75221c878161463b108dafa5e9b6c347",
         "date": "2024-03-27T18:20:23+00:00",
         "message": "feat: updating to production dependnecies",
         "refs": "HEAD -> main, origin/main, origin/HEAD",
         "body": "",
         "author_name": "Juan Carlos Blanco Delgado",
         "author_email": "36451129+juancarlosjr97@users.noreply.github.com"
       }
DEBUG: Config file exists, fileName: renovate.json (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Retrieving issueList (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Retrieved 1 issues (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Repo is onboarded (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Found renovate.json config file (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Repository config (repository=juancarlosjr97/renovate-test-27939)
       "fileName": "renovate.json",
       "config": {
         "$schema": "https://docs.renovatebot.com/renovate-schema.json",
         "extends": ["config:base", "group:all"],
         "packageRules": [
           {
             "matchPackagePatterns": "*",
             "commitMessagePrefix": "{{#if (includes depTypes 'dependencies')}}production{{else}}notProduction{{/if}}"
           }
         ],
         "fetchChangeLogs": "off"
       }
DEBUG: migrateAndValidate() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Config migration necessary (repository=juancarlosjr97/renovate-test-27939)
       "oldConfig": {
         "$schema": "https://docs.renovatebot.com/renovate-schema.json",
         "extends": ["config:base", "group:all"],
         "packageRules": [
           {
             "matchPackagePatterns": "*",
             "commitMessagePrefix": "{{#if (includes depTypes 'dependencies')}}production{{else}}notProduction{{/if}}"
           }
         ],
         "fetchChangeLogs": "off"
       },
       "newConfig": {
         "$schema": "https://docs.renovatebot.com/renovate-schema.json",
         "extends": ["config:recommended", "group:all"],
         "packageRules": [
           {
             "matchPackagePatterns": "*",
             "commitMessagePrefix": "{{#if (includes depTypes 'dependencies')}}production{{else}}notProduction{{/if}}"
           }
         ],
         "fetchChangeLogs": "off"
       }
DEBUG: Post-massage config (repository=juancarlosjr97/renovate-test-27939)
       "config": {
         "$schema": "https://docs.renovatebot.com/renovate-schema.json",
         "extends": ["config:recommended", "group:all"],
         "packageRules": [
           {
             "matchPackagePatterns": ["*"],
             "commitMessagePrefix": "{{#if (includes depTypes 'dependencies')}}production{{else}}notProduction{{/if}}"
           }
         ],
         "fetchChangeLogs": "off"
       }
DEBUG: Setting hostRules from config (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Found repo ignorePaths (repository=juancarlosjr97/renovate-test-27939)
       "ignorePaths": [
         "**/node_modules/**",
         "**/bower_components/**",
         "**/vendor/**",
         "**/examples/**",
         "**/__tests__/**",
         "**/test/**",
         "**/tests/**",
         "**/__fixtures__/**"
       ]
DEBUG: No vulnerability alerts enabled for repo (repository=juancarlosjr97/renovate-test-27939)
DEBUG: No vulnerability alerts found (repository=juancarlosjr97/renovate-test-27939)
DEBUG: findIssue(Dependency Dashboard) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Found issue 2 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: http cache: saving https://api.github.com/repos/juancarlosjr97/renovate-test-27939/issues/2 (etag=W/"cfb3c731e3879d14765ddea6551336eb360563c35f6ca8e31182f16093799cb3", lastModified=Wed, 27 Mar 2024 18:28:38 GMT) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: No baseBranches (repository=juancarlosjr97/renovate-test-27939)
DEBUG: extract() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Setting current branch to main (repository=juancarlosjr97/renovate-test-27939)
DEBUG: latest commit (repository=juancarlosjr97/renovate-test-27939)
       "branchName": "main",
       "latestCommitDate": "2024-03-27T18:20:23+00:00"
DEBUG: Using file match: (^|/)tasks/[^/]+\.ya?ml$ for manager ansible (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)(galaxy|requirements)(\.ansible)?\.ya?ml$ for manager ansible-galaxy (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.tool-versions$ for manager asdf (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: azure.*pipelines?.*\.ya?ml$ for manager azure-pipelines (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)batect(-bundle)?\.ya?ml$ for manager batect (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)batect$ for manager batect-wrapper (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)WORKSPACE(|\.bazel)$ for manager bazel (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.bzl$ for manager bazel (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)MODULE\.bazel$ for manager bazel-module (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.bazelversion$ for manager bazelisk (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.bicep$ for manager bicep (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.?bitbucket-pipelines\.ya?ml$ for manager bitbucket-pipelines (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: buildkite\.ya?ml for manager buildkite (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.buildkite/.+\.ya?ml$ for manager buildkite (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)bun\.lockb$ for manager bun (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)Gemfile$ for manager bundler (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.cake$ for manager cake (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)Cargo\.toml$ for manager cargo (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.circleci/.+\.ya?ml$ for manager circleci (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)cloudbuild\.ya?ml for manager cloudbuild (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)Podfile$ for manager cocoapods (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)([\w-]*)composer\.json$ for manager composer (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)conanfile\.(txt|py)$ for manager conan (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)cpanfile$ for manager cpanfile (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)(?:deps|bb)\.edn$ for manager deps-edn (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)(?:docker-)?compose[^/]*\.ya?ml$ for manager docker-compose (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/|\.)([Dd]ocker|[Cc]ontainer)file$ for manager dockerfile (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)([Dd]ocker|[Cc]ontainer)file[^/]*$ for manager dockerfile (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.drone\.yml$ for manager droneci (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)fleet\.ya?ml for manager fleet (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (?:^|/)gotk-components\.ya?ml$ for manager flux (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.fvm/fvm_config\.json$ for manager fvm (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.gitmodules$ for manager git-submodules (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)(workflow-templates|\.(?:github|gitea|forgejo)/(?:workflows|actions))/.+\.ya?ml$ for manager github-actions (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)action\.ya?ml$ for manager github-actions (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.gitlab-ci\.ya?ml$ for manager gitlabci (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.gitlab-ci\.ya?ml$ for manager gitlabci-include (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)go\.mod$ for manager gomod (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.gradle(\.kts)?$ for manager gradle (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)gradle\.properties$ for manager gradle (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)gradle/.+\.toml$ for manager gradle (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)buildSrc/.+\.kt$ for manager gradle (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.versions\.toml$ for manager gradle (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)versions.props$ for manager gradle (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)versions.lock$ for manager gradle (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)gradle/wrapper/gradle-wrapper\.properties$ for manager gradle-wrapper (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)requirements\.ya?ml$ for manager helm-requirements (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)values\.ya?ml$ for manager helm-values (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)helmfile\.ya?ml(?:\.gotmpl)?$ for manager helmfile (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)Chart\.ya?ml$ for manager helmv3 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)bin/hermit$ for manager hermit (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: ^Formula/[^/]+[.]rb$ for manager homebrew (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.html?$ for manager html (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)plugins\.(txt|ya?ml)$ for manager jenkins (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)jsonnetfile\.json$ for manager jsonnet-bundler (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: ^.+\.main\.kts$ for manager kotlin-script (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)kustomization\.ya?ml$ for manager kustomize (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)project\.clj$ for manager leiningen (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/|\.)pom\.xml$ for manager maven (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: ^(((\.mvn)|(\.m2))/)?settings\.xml$ for manager maven (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|\/).mvn/wrapper/maven-wrapper.properties$ for manager maven-wrapper (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)package\.js$ for manager meteor (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)Mintfile$ for manager mint (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)mix\.exs$ for manager mix (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)flake\.nix$ for manager nix (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.node-version$ for manager nodenv (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)package\.json$ for manager npm (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.(?:cs|fs|vb)proj$ for manager nuget (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.(?:props|targets)$ for manager nuget (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)dotnet-tools\.json$ for manager nuget (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)global\.json$ for manager nuget (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.nvmrc$ for manager nvm (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)src/main/features/.+\.json$ for manager osgi (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)pyproject\.toml$ for manager pep621 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)[\w-]*requirements([-.]\w+)?\.(txt|pip)$ for manager pip_requirements (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)setup\.py$ for manager pip_setup (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)Pipfile$ for manager pipenv (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)pyproject\.toml$ for manager poetry (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.pre-commit-config\.ya?ml$ for manager pre-commit (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)pubspec\.ya?ml$ for manager pub (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)Puppetfile$ for manager puppet (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.python-version$ for manager pyenv (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.ruby-version$ for manager ruby-version (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.sbt$ for manager sbt (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: project/[^/]*\.scala$ for manager sbt (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: project/build\.properties$ for manager sbt (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)repositories$ for manager sbt (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)setup\.cfg$ for manager setup-cfg (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)Package\.swift for manager swift (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.tf$ for manager terraform (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.terraform-version$ for manager terraform-version (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)terragrunt\.hcl$ for manager terragrunt (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.terragrunt-version$ for manager terragrunt-version (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.tflint\.hcl$ for manager tflint-plugin (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: ^\.travis\.ya?ml$ for manager travis (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.vela\.ya?ml$ for manager velaci (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)vendir\.yml$ for manager vendir (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: ^\.woodpecker(?:/[^/]+)?\.ya?ml$ for manager woodpecker (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Matched 1 file(s) for manager npm: package.json (repository=juancarlosjr97/renovate-test-27939)
DEBUG: npm file package.json has name "renovate-test-27939" (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Detecting pnpm Workspaces (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Detecting workspaces (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Finding locked versions (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Found package-lock.json for package.json (repository=juancarlosjr97/renovate-test-27939)
DEBUG: manager extract durations (ms) (repository=juancarlosjr97/renovate-test-27939)
       "managers": {"npm": 7}
DEBUG: Found npm package files (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Found 1 package file(s) (repository=juancarlosjr97/renovate-test-27939)
 INFO: Dependency extraction complete (repository=juancarlosjr97/renovate-test-27939, baseBranch=main)
       "stats": {
         "managers": {"npm": {"fileCount": 1, "depCount": 2}},
         "total": {"fileCount": 1, "depCount": 2}
       }
DEBUG: PackageFiles.add() - Package file saved for base branch (repository=juancarlosjr97/renovate-test-27939, baseBranch=main)
DEBUG: Package releases lookups complete (repository=juancarlosjr97/renovate-test-27939, baseBranch=main)
DEBUG: branchifyUpgrades (repository=juancarlosjr97/renovate-test-27939)
DEBUG: detectSemanticCommits() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: getCommitMessages (repository=juancarlosjr97/renovate-test-27939)
DEBUG: semanticCommits: detected "angular" (repository=juancarlosjr97/renovate-test-27939)
DEBUG: semanticCommits: enabled (repository=juancarlosjr97/renovate-test-27939)
DEBUG: 2 flattened updates found: @graphql-eslint/eslint-plugin, jest (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Returning 1 branch(es) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: config.repoIsOnboarded=true (repository=juancarlosjr97/renovate-test-27939)
DEBUG: packageFiles with updates (repository=juancarlosjr97/renovate-test-27939, baseBranch=main)
       "config": {
         "npm": [
           {
             "deps": [
               {
                 "depType": "dependencies",
                 "depName": "@graphql-eslint/eslint-plugin",
                 "currentValue": "3.19.3",
                 "datasource": "npm",
                 "prettyDepType": "dependency",
                 "lockedVersion": "3.19.3",
                 "updates": [
                   {
                     "bucket": "latest",
                     "newVersion": "3.20.1",
                     "newValue": "3.20.1",
                     "releaseTimestamp": "2023-07-13T07:23:24.793Z",
                     "newMajor": 3,
                     "newMinor": 20,
                     "updateType": "minor",
                     "branchName": "renovate/all"
                   }
                 ],
                 "packageName": "@graphql-eslint/eslint-plugin",
                 "versioning": "npm",
                 "warnings": [],
                 "sourceUrl": "https://github.com/B2o5T/graphql-eslint",
                 "registryUrl": "https://registry.npmjs.org",
                 "currentVersion": "3.19.3",
                 "isSingleVersion": true,
                 "fixedVersion": "3.19.3"
               },
               {
                 "depType": "dependencies",
                 "depName": "jest",
                 "currentValue": "29.4.3",
                 "datasource": "npm",
                 "prettyDepType": "dependency",
                 "lockedVersion": "29.4.3",
                 "updates": [
                   {
                     "bucket": "latest",
                     "newVersion": "29.7.0",
                     "newValue": "29.7.0",
                     "releaseTimestamp": "2023-09-12T06:44:08.561Z",
                     "newMajor": 29,
                     "newMinor": 7,
                     "updateType": "minor",
                     "branchName": "renovate/all"
                   }
                 ],
                 "packageName": "jest",
                 "versioning": "npm",
                 "warnings": [],
                 "sourceUrl": "https://github.com/jestjs/jest",
                 "registryUrl": "https://registry.npmjs.org",
                 "sourceDirectory": "packages/jest",
                 "homepage": "https://jestjs.io/",
                 "currentVersion": "29.4.3",
                 "isSingleVersion": true,
                 "fixedVersion": "29.4.3"
               }
             ],
             "extractedConstraints": {"npm": ">=7"},
             "managerData": {
               "packageJsonName": "renovate-test-27939",
               "hasPackageManager": false,
               "npmLock": "package-lock.json",
               "yarnZeroInstall": false
             },
             "skipInstalls": true,
             "packageFile": "package.json",
             "lockFiles": ["package-lock.json"]
           }
         ]
       }
DEBUG: detectSemanticCommits() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: semanticCommits: returning "enabled" from cache (repository=juancarlosjr97/renovate-test-27939)
DEBUG: processRepo() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Processing 1 branch: renovate/all (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Calculating hourly PRs remaining (repository=juancarlosjr97/renovate-test-27939)
DEBUG: currentHourStart=2024-03-27T18:00:00.000+00:00 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: PR hourly limit remaining: 0 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Calculating prConcurrentLimit (10) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: getBranchPr(renovate/all) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: findPr(renovate/all, undefined, open) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: findPr(renovate/all, undefined, closed) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Found PR #3 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: 0 PRs are currently open (repository=juancarlosjr97/renovate-test-27939)
DEBUG: PR concurrent limit remaining: 10 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Calculated maximum PRs remaining this run: 0 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: PullRequests limit = 0 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Calculating hourly PRs remaining (repository=juancarlosjr97/renovate-test-27939)
DEBUG: currentHourStart=2024-03-27T18:00:00.000+00:00 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: PR hourly limit remaining: 0 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Calculating branchConcurrentLimit (10) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: 0 already existing branches found:  (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Branch concurrent limit remaining: 10 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Calculated maximum branches remaining this run: 0 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Branches limit = 0 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: syncBranchState() (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: syncBranchState(): Branch cache not found, creating minimal branchState (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: getBranchPr(renovate/all) (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: findPr(renovate/all, undefined, open) (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: findPr(renovate/all, undefined, closed) (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Found PR #3 (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: branchExists=false (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: dependencyDashboardCheck=unlimit (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: recreateClosed is true. No need to check for closed PR. (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Checking schedule(at any time, null) (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: No schedule defined (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Branch needs creating (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Using reuseExistingBranch: false (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Setting current branch to main (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: latest commit (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "branchName": "main",
       "latestCommitDate": "2024-03-27T18:20:23+00:00"
DEBUG: manager.getUpdatedPackageFiles() reuseExistingBranch=false (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: npm.updateDependency(): dependencies.@graphql-eslint/eslint-plugin = 3.20.1 (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Updating @graphql-eslint/eslint-plugin in package.json (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: npm.updateDependency(): dependencies.jest = 29.7.0 (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Updating jest in package.json (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: updateArtifacts for updatedPackageFiles (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Updated 1 package files (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Getting updated lock files (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Writing package.json files (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "packageFiles": ["package.json"]
DEBUG: Writing package-lock.json (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Massaging npm lock file before writing to disk (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Writing any updated package files (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Writing package.json (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Writing updated .npmrc file to .npmrc (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Generating package-lock.json for . (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Spawning npm install to create ./package-lock.json (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Using npm constraint >=9 for lockfileVersion=3 (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Updating lock file only (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: No node constraint found - using latest (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Setting CONTAINERBASE_CACHE_DIR to /var/folders/73/ykcrrqpd6rjd96sptqy1cx480000gn/T/renovate/cache/containerbase (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Falling back to binarySource=global (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Executing command (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "command": "npm install --package-lock-only --no-audit --ignore-scripts"
DEBUG: exec completed (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "durationMs": 1979,
       "stdout": "\nup to date in 2s\n\n37 packages are looking for funding\n  run `npm fund` for details\n",
       "stderr": ""
DEBUG: package-lock.json needs updating (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Updated 1 lock files (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "updatedArtifacts": ["package-lock.json"]
DEBUG: 2 file(s) to commit (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Preparing files for committing to branch renovate/all (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Setting git author name: Juan Carlos Blanco Delgado (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Setting git author email: juancarlosjr97@gmail.com (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: git commit (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "deletedFiles": [],
       "ignoredFiles": [],
       "result": {
         "author": null,
         "branch": "renovate/all",
         "commit": "96f07e561e234c8eb54093bccea1884189614278",
         "root": false,
         "summary": {"changes": 2, "insertions": 16, "deletions": 13}
       }
DEBUG: Pushing refSpec renovate/all:renovate/all (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: git push (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "result": {
         "pushed": [
           {
             "deleted": false,
             "tag": false,
             "branch": true,
             "new": true,
             "alreadyUpdated": false,
             "local": "refs/heads/renovate/all",
             "remote": "refs/heads/renovate/all"
           }
         ],
         "ref": {"local": "refs/remotes/origin/renovate/all"},
         "remoteMessages": {
           "all": [
             "Create a pull request for 'renovate/all' on GitHub by visiting:",
             "https://github.com/juancarlosjr97/renovate-test-27939/pull/new/renovate/all"
           ],
           "pullRequestUrl": "https://github.com/juancarlosjr97/renovate-test-27939/pull/new/renovate/all"
         }
       }
DEBUG: Setting current branch to main (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: latest commit (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "branchName": "main",
       "latestCommitDate": "2024-03-27T18:20:23+00:00"
 INFO: Branch created (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "commitSha": "96f07e561e234c8eb54093bccea1884189614278"
DEBUG: Ensuring PR (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: There are 0 errors and 0 warnings (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: getBranchPr(renovate/all) (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: findPr(renovate/all, undefined, open) (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: findPr(renovate/all, undefined, closed) (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Found PR #3 (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: getPrCache() (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Creating PR (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "prTitle": "notProduction Update all dependencies"
DEBUG: Creating PR (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "title": "notProduction Update all dependencies",
       "head": "juancarlosjr97:renovate/all",
       "base": "main",
       "draft": false
DEBUG: PR created (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "pr": 4,
       "draft": false
DEBUG: Adding labels '' to #4 (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
 INFO: PR created (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "pr": 4,
       "prTitle": "notProduction Update all dependencies"
DEBUG: addParticipants(pr=4) (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: setPrCache() (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Created Pull Request #4 (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: PR is not configured for automerge (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: setBranchCommit() (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: getBranchPr(renovate/all) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: findPr(renovate/all, undefined, open) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Found PR #4 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: getPrCache() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: ensureDependencyDashboard() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Ensuring Dependency Dashboard (repository=juancarlosjr97/renovate-test-27939)
DEBUG: http cache: saving https://api.github.com/repos/juancarlosjr97/renovate-test-27939/issues/2 (etag=W/"cfb3c731e3879d14765ddea6551336eb360563c35f6ca8e31182f16093799cb3", lastModified=Wed, 27 Mar 2024 18:28:38 GMT) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: http cache: Using cached response: https://api.github.com/repos/juancarlosjr97/renovate-test-27939/issues/2 from 2024-03-27T18:28:51.243Z (repository=juancarlosjr97/renovate-test-27939)
DEBUG: ensureIssue(Dependency Dashboard) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: http cache: saving https://api.github.com/repos/juancarlosjr97/renovate-test-27939/issues/2 (etag=W/"cfb3c731e3879d14765ddea6551336eb360563c35f6ca8e31182f16093799cb3", lastModified=Wed, 27 Mar 2024 18:28:38 GMT) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Patching issue (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Issue updated (repository=juancarlosjr97/renovate-test-27939)
DEBUG: validateReconfigureBranch() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: No reconfigure branch found (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Removing any stale branches (repository=juancarlosjr97/renovate-test-27939)
DEBUG: config.repoIsOnboarded=true (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Branch lists (repository=juancarlosjr97/renovate-test-27939)
       "branchList": ["renovate/all"],
       "renovateBranches": ["renovate/all"]
DEBUG: remainingBranches= (repository=juancarlosjr97/renovate-test-27939)
DEBUG: No branches to clean up (repository=juancarlosjr97/renovate-test-27939)
DEBUG: PackageFiles.clear() - Package files deleted (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Branch summary (repository=juancarlosjr97/renovate-test-27939)
       "cacheModified": undefined,
       "baseBranches": [{"branchName": "main", "sha": "85b98f6c75221c878161463b108dafa5e9b6c347"}],
       "branches": [
         {
           "automerge": false,
           "baseBranch": "main",
           "baseBranchSha": "85b98f6c75221c878161463b108dafa5e9b6c347",
           "branchName": "renovate/all",
           "branchSha": "96f07e561e234c8eb54093bccea1884189614278",
           "isModified": false,
           "isPristine": true
         }
       ],
       "defaultBranch": "main",
       "inactiveBranches": []
DEBUG: branches info extended (repository=juancarlosjr97/renovate-test-27939)
       "branchesInformation": [
         {
           "branchName": "renovate/all",
           "prNo": 4,
           "prTitle": "notProduction Update all dependencies",
           "result": "pr-created",
           "upgrades": [
             {
               "datasource": "npm",
               "depName": "@graphql-eslint/eslint-plugin",
               "displayPending": "",
               "fixedVersion": "3.19.3",
               "currentVersion": "3.19.3",
               "currentValue": "3.19.3",
               "newValue": "3.20.1",
               "newVersion": "3.20.1",
               "packageFile": "package.json",
               "updateType": "minor",
               "packageName": "@graphql-eslint/eslint-plugin"
             },
             {
               "datasource": "npm",
               "depName": "jest",
               "displayPending": "",
               "fixedVersion": "29.4.3",
               "currentVersion": "29.4.3",
               "currentValue": "29.4.3",
               "newValue": "29.7.0",
               "newVersion": "29.7.0",
               "packageFile": "package.json",
               "updateType": "minor",
               "packageName": "jest"
             }
           ]
         }
       ]
DEBUG: Renovate repository PR statistics (repository=juancarlosjr97/renovate-test-27939)
       "stats": {"total": 3, "open": 1, "closed": 2, "merged": 0}
DEBUG: Repository result: done, status: onboarded, enabled: true, onboarded: true (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Repository timing splits (milliseconds) (repository=juancarlosjr97/renovate-test-27939)
       "splits": {"init": 2367, "extract": 323, "lookup": 101, "onboarding": 0, "update": 4628},
       "total": 8073
DEBUG: Package cache statistics (repository=juancarlosjr97/renovate-test-27939)
       "get": {"count": 2, "avgMs": 16, "medianMs": 27, "maxMs": 27, "totalMs": 32},
       "set": {"count": 0, "avgMs": 0, "medianMs": 0, "maxMs": 0, "totalMs": 0}
DEBUG: HTTP statistics (repository=juancarlosjr97/renovate-test-27939)
       "urls": {
         "https://api.github.com/graphql": {"POST": {"200": 2}},
         "https://api.github.com/repos/juancarlosjr97/renovate-test-27939/issues/2": {
           "GET": {"200": 1, "304": 1},
           "PATCH": {"200": 1}
         },
         "https://api.github.com/repos/juancarlosjr97/renovate-test-27939/pulls": {
           "POST": {"201": 1},
           "GET": {"200": 1}
         }
       },
       "hosts": {
         "api.github.com": {
           "count": 7,
           "reqAvgMs": 337,
           "reqMedianMs": 204,
           "reqMaxMs": 942,
           "queueAvgMs": 0,
           "queueMedianMs": 0,
           "queueMaxMs": 0
         }
       },
       "requests": 7
DEBUG: HTTP cache statistics (repository=juancarlosjr97/renovate-test-27939)
       "https://api.github.com": {
         "/repos/juancarlosjr97/renovate-test-27939/issues/2": {"hit": 1, "miss": 3},
         "/repos/juancarlosjr97/renovate-test-27939/pulls": {"hit": 0, "miss": 1}
       },
       "https://registry.npmjs.org": {
         "/@graphql-eslint%2Feslint-plugin": {"hit": 0, "miss": 0, "localHit": 1},
         "/jest": {"hit": 0, "miss": 0, "localHit": 1}
       }
DEBUG: Lookup statistics (repository=juancarlosjr97/renovate-test-27939)
       "npm": {"count": 2, "avgMs": 35, "medianMs": 45, "maxMs": 45, "totalMs": 69}
DEBUG: dns cache (repository=juancarlosjr97/renovate-test-27939)
       "hosts": []
 INFO: Repository finished (repository=juancarlosjr97/renovate-test-27939)
       "cloned": true,
       "durationMs": 8073
DEBUG: Checking file package cache for expired items
DEBUG: Deleted 0 of 3 file cached entries in 6ms
```
</details>


**The fix**

* I ran a renovate execution from the branch of this PR https://github.com/renovatebot/renovate/pull/27939
* This execution raised this PR https://github.com/juancarlosjr97/renovate-test-27939/pull/3
* The expected PR title and commit is the expected title as `production Update all dependencies`
 as the identified updates are `dependencies`

<details><summary>Logs</summary>

```
> renovate@0.0.0-semantic-release prestart /Users/juancarlosjr97/Developer/Personal/renovate
> run-s 'generate:*'


> renovate@0.0.0-semantic-release generate:imports /Users/juancarlosjr97/Developer/Personal/renovate
> node tools/generate-imports.mjs

generating imports
> data/debian-distro-info.json
> data/kubernetes-api.json5
> data/node-js-schedule.json
> data/ubuntu-distro-info.json
> node_modules/emojibase-data/en/shortcodes/github.json
generating hashes

> renovate@0.0.0-semantic-release start /Users/juancarlosjr97/Developer/Personal/renovate
> ts-node lib/renovate.ts "juancarlosjr97/renovate-test-27939"

DEBUG: Using RE2 regex engine
DEBUG: Parsing configs
DEBUG: Checking for config file in config.js
DEBUG: No config file found on disk - skipping
DEBUG: File config
       "config": {}
DEBUG: CLI config
       "config": {"repositories": ["juancarlosjr97/renovate-test-27939"]}
DEBUG: Env config
       "config": {"hostRules": [], "token": "***********"}
DEBUG: Combined config
       "config": {
         "hostRules": [],
         "token": "***********",
         "repositories": ["juancarlosjr97/renovate-test-27939"]
       }
DEBUG: Enabling forkProcessing while in non-autodiscover mode
DEBUG: Found valid git version: 2.40.0
DEBUG: Setting global hostRules
DEBUG: Using default github endpoint: https://api.github.com/
DEBUG: hostRules: authentication already set for api.github.com
DEBUG: Platform config
       "platformConfig": {
         "hostType": "github",
         "endpoint": "https://api.github.com/",
         "isGHApp": false,
         "isGhe": false,
         "userDetails": {
           "username": "juancarlosjr97",
           "name": "Juan Carlos Blanco Delgado",
           "id": 36451129
         },
         "userEmail": "juancarlosjr97@gmail.com"
       },
       "renovateUsername": "juancarlosjr97"
DEBUG: Using platform gitAuthor: Juan Carlos Blanco Delgado <juancarlosjr97@gmail.com>
DEBUG: Adding token authentication for api.github.com (hostType=github) to hostRules
DEBUG: Using baseDir: /var/folders/73/ykcrrqpd6rjd96sptqy1cx480000gn/T/renovate
DEBUG: Using cacheDir: /var/folders/73/ykcrrqpd6rjd96sptqy1cx480000gn/T/renovate/cache
DEBUG: Using containerbaseDir: /var/folders/73/ykcrrqpd6rjd96sptqy1cx480000gn/T/renovate/cache/containerbase
DEBUG: Initializing Renovate internal cache into /var/folders/73/ykcrrqpd6rjd96sptqy1cx480000gn/T/renovate/cache/renovate/renovate-cache-v1
DEBUG: Commits limit = null
DEBUG: Setting global hostRules
DEBUG: Adding token authentication for api.github.com (hostType=github) to hostRules
DEBUG: validatePresets()
DEBUG: Reinitializing hostRules for repo
DEBUG: Clearing hostRules
DEBUG: Adding token authentication for api.github.com (hostType=github) to hostRules
 INFO: Repository started (repository=juancarlosjr97/renovate-test-27939)
       "renovateVersion": "0.0.0-semantic-release"
DEBUG: Using localDir: /var/folders/73/ykcrrqpd6rjd96sptqy1cx480000gn/T/renovate/repos/github/juancarlosjr97/renovate-test-27939 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: PackageFiles.clear() - Package files deleted (repository=juancarlosjr97/renovate-test-27939)
DEBUG: initRepo("juancarlosjr97/renovate-test-27939") (repository=juancarlosjr97/renovate-test-27939)
DEBUG: hostRules: authentication already set for api.github.com (repository=juancarlosjr97/renovate-test-27939)
DEBUG: juancarlosjr97/renovate-test-27939 default branch = main (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using personal access token for git init (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Resetting npmrc (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Resetting npmrc (repository=juancarlosjr97/renovate-test-27939)
DEBUG: checkOnboarding() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: isOnboarded() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: findPr(renovate/configure, Configure Renovate, !open) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: http cache: saving https://api.github.com/repos/juancarlosjr97/renovate-test-27939/pulls?per_page=100&state=all&sort=updated&direction=desc&page=1 (etag=W/"d2009bbf6898f3d4ac02cfb79e37e331ef60ef0f209d4a9f5ca96e0e911bf043", lastModified=undefined) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: getPrList success (repository=juancarlosjr97/renovate-test-27939)
       "pullsTotal": 1,
       "requestsTotal": 1,
       "apiQuotaAffected": true
DEBUG: findPr(renovate/configure, chore: Configure Renovate, !open) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: findFile(renovate.json) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Initializing git repository into /var/folders/73/ykcrrqpd6rjd96sptqy1cx480000gn/T/renovate/repos/github/juancarlosjr97/renovate-test-27939 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Performing blobless clone (repository=juancarlosjr97/renovate-test-27939)
DEBUG: git clone completed (repository=juancarlosjr97/renovate-test-27939)
       "durationMs": 951
DEBUG: latest repository commit (repository=juancarlosjr97/renovate-test-27939)
       "latestCommit": {
         "hash": "85b98f6c75221c878161463b108dafa5e9b6c347",
         "date": "2024-03-27T18:20:23+00:00",
         "message": "feat: updating to production dependnecies",
         "refs": "HEAD -> main, origin/main, origin/HEAD",
         "body": "",
         "author_name": "Juan Carlos Blanco Delgado",
         "author_email": "36451129+juancarlosjr97@users.noreply.github.com"
       }
DEBUG: Config file exists, fileName: renovate.json (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Retrieving issueList (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Retrieved 1 issues (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Repo is onboarded (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Found renovate.json config file (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Repository config (repository=juancarlosjr97/renovate-test-27939)
       "fileName": "renovate.json",
       "config": {
         "$schema": "https://docs.renovatebot.com/renovate-schema.json",
         "extends": ["config:base", "group:all"],
         "packageRules": [
           {
             "matchPackagePatterns": "*",
             "commitMessagePrefix": "{{#if (includes depTypes 'dependencies')}}production{{else}}notProduction{{/if}}"
           }
         ],
         "fetchChangeLogs": "off"
       }
DEBUG: migrateAndValidate() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Config migration necessary (repository=juancarlosjr97/renovate-test-27939)
       "oldConfig": {
         "$schema": "https://docs.renovatebot.com/renovate-schema.json",
         "extends": ["config:base", "group:all"],
         "packageRules": [
           {
             "matchPackagePatterns": "*",
             "commitMessagePrefix": "{{#if (includes depTypes 'dependencies')}}production{{else}}notProduction{{/if}}"
           }
         ],
         "fetchChangeLogs": "off"
       },
       "newConfig": {
         "$schema": "https://docs.renovatebot.com/renovate-schema.json",
         "extends": ["config:recommended", "group:all"],
         "packageRules": [
           {
             "matchPackagePatterns": "*",
             "commitMessagePrefix": "{{#if (includes depTypes 'dependencies')}}production{{else}}notProduction{{/if}}"
           }
         ],
         "fetchChangeLogs": "off"
       }
DEBUG: Post-massage config (repository=juancarlosjr97/renovate-test-27939)
       "config": {
         "$schema": "https://docs.renovatebot.com/renovate-schema.json",
         "extends": ["config:recommended", "group:all"],
         "packageRules": [
           {
             "matchPackagePatterns": ["*"],
             "commitMessagePrefix": "{{#if (includes depTypes 'dependencies')}}production{{else}}notProduction{{/if}}"
           }
         ],
         "fetchChangeLogs": "off"
       }
DEBUG: Setting hostRules from config (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Found repo ignorePaths (repository=juancarlosjr97/renovate-test-27939)
       "ignorePaths": [
         "**/node_modules/**",
         "**/bower_components/**",
         "**/vendor/**",
         "**/examples/**",
         "**/__tests__/**",
         "**/test/**",
         "**/tests/**",
         "**/__fixtures__/**"
       ]
DEBUG: No vulnerability alerts enabled for repo (repository=juancarlosjr97/renovate-test-27939)
DEBUG: No vulnerability alerts found (repository=juancarlosjr97/renovate-test-27939)
DEBUG: findIssue(Dependency Dashboard) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Found issue 2 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: http cache: saving https://api.github.com/repos/juancarlosjr97/renovate-test-27939/issues/2 (etag=W/"820a191e0aafd214612c7e6c27a96227e7063381cd54ba00f78d18daf73aa1a8", lastModified=Wed, 27 Mar 2024 18:18:09 GMT) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: No baseBranches (repository=juancarlosjr97/renovate-test-27939)
DEBUG: extract() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Setting current branch to main (repository=juancarlosjr97/renovate-test-27939)
DEBUG: latest commit (repository=juancarlosjr97/renovate-test-27939)
       "branchName": "main",
       "latestCommitDate": "2024-03-27T18:20:23+00:00"
DEBUG: Using file match: (^|/)tasks/[^/]+\.ya?ml$ for manager ansible (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)(galaxy|requirements)(\.ansible)?\.ya?ml$ for manager ansible-galaxy (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.tool-versions$ for manager asdf (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: azure.*pipelines?.*\.ya?ml$ for manager azure-pipelines (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)batect(-bundle)?\.ya?ml$ for manager batect (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)batect$ for manager batect-wrapper (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)WORKSPACE(|\.bazel)$ for manager bazel (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.bzl$ for manager bazel (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)MODULE\.bazel$ for manager bazel-module (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.bazelversion$ for manager bazelisk (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.bicep$ for manager bicep (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.?bitbucket-pipelines\.ya?ml$ for manager bitbucket-pipelines (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: buildkite\.ya?ml for manager buildkite (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.buildkite/.+\.ya?ml$ for manager buildkite (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)bun\.lockb$ for manager bun (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)Gemfile$ for manager bundler (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.cake$ for manager cake (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)Cargo\.toml$ for manager cargo (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.circleci/.+\.ya?ml$ for manager circleci (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)cloudbuild\.ya?ml for manager cloudbuild (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)Podfile$ for manager cocoapods (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)([\w-]*)composer\.json$ for manager composer (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)conanfile\.(txt|py)$ for manager conan (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)cpanfile$ for manager cpanfile (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)(?:deps|bb)\.edn$ for manager deps-edn (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)(?:docker-)?compose[^/]*\.ya?ml$ for manager docker-compose (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/|\.)([Dd]ocker|[Cc]ontainer)file$ for manager dockerfile (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)([Dd]ocker|[Cc]ontainer)file[^/]*$ for manager dockerfile (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.drone\.yml$ for manager droneci (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)fleet\.ya?ml for manager fleet (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (?:^|/)gotk-components\.ya?ml$ for manager flux (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.fvm/fvm_config\.json$ for manager fvm (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.gitmodules$ for manager git-submodules (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)(workflow-templates|\.(?:github|gitea|forgejo)/(?:workflows|actions))/.+\.ya?ml$ for manager github-actions (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)action\.ya?ml$ for manager github-actions (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.gitlab-ci\.ya?ml$ for manager gitlabci (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.gitlab-ci\.ya?ml$ for manager gitlabci-include (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)go\.mod$ for manager gomod (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.gradle(\.kts)?$ for manager gradle (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)gradle\.properties$ for manager gradle (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)gradle/.+\.toml$ for manager gradle (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)buildSrc/.+\.kt$ for manager gradle (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.versions\.toml$ for manager gradle (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)versions.props$ for manager gradle (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)versions.lock$ for manager gradle (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)gradle/wrapper/gradle-wrapper\.properties$ for manager gradle-wrapper (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)requirements\.ya?ml$ for manager helm-requirements (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)values\.ya?ml$ for manager helm-values (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)helmfile\.ya?ml(?:\.gotmpl)?$ for manager helmfile (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)Chart\.ya?ml$ for manager helmv3 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)bin/hermit$ for manager hermit (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: ^Formula/[^/]+[.]rb$ for manager homebrew (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.html?$ for manager html (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)plugins\.(txt|ya?ml)$ for manager jenkins (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)jsonnetfile\.json$ for manager jsonnet-bundler (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: ^.+\.main\.kts$ for manager kotlin-script (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)kustomization\.ya?ml$ for manager kustomize (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)project\.clj$ for manager leiningen (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/|\.)pom\.xml$ for manager maven (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: ^(((\.mvn)|(\.m2))/)?settings\.xml$ for manager maven (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|\/).mvn/wrapper/maven-wrapper.properties$ for manager maven-wrapper (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)package\.js$ for manager meteor (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)Mintfile$ for manager mint (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)mix\.exs$ for manager mix (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)flake\.nix$ for manager nix (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.node-version$ for manager nodenv (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)package\.json$ for manager npm (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.(?:cs|fs|vb)proj$ for manager nuget (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.(?:props|targets)$ for manager nuget (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)dotnet-tools\.json$ for manager nuget (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)global\.json$ for manager nuget (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.nvmrc$ for manager nvm (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)src/main/features/.+\.json$ for manager osgi (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)pyproject\.toml$ for manager pep621 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)[\w-]*requirements([-.]\w+)?\.(txt|pip)$ for manager pip_requirements (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)setup\.py$ for manager pip_setup (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)Pipfile$ for manager pipenv (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)pyproject\.toml$ for manager poetry (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.pre-commit-config\.ya?ml$ for manager pre-commit (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)pubspec\.ya?ml$ for manager pub (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)Puppetfile$ for manager puppet (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.python-version$ for manager pyenv (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.ruby-version$ for manager ruby-version (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.sbt$ for manager sbt (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: project/[^/]*\.scala$ for manager sbt (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: project/build\.properties$ for manager sbt (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)repositories$ for manager sbt (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)setup\.cfg$ for manager setup-cfg (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)Package\.swift for manager swift (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.tf$ for manager terraform (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.terraform-version$ for manager terraform-version (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)terragrunt\.hcl$ for manager terragrunt (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.terragrunt-version$ for manager terragrunt-version (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: \.tflint\.hcl$ for manager tflint-plugin (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: ^\.travis\.ya?ml$ for manager travis (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)\.vela\.ya?ml$ for manager velaci (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: (^|/)vendir\.yml$ for manager vendir (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Using file match: ^\.woodpecker(?:/[^/]+)?\.ya?ml$ for manager woodpecker (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Matched 1 file(s) for manager npm: package.json (repository=juancarlosjr97/renovate-test-27939)
DEBUG: npm file package.json has name "renovate-test-27939" (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Detecting pnpm Workspaces (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Detecting workspaces (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Finding locked versions (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Found package-lock.json for package.json (repository=juancarlosjr97/renovate-test-27939)
DEBUG: manager extract durations (ms) (repository=juancarlosjr97/renovate-test-27939)
       "managers": {"npm": 8}
DEBUG: Found npm package files (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Found 1 package file(s) (repository=juancarlosjr97/renovate-test-27939)
 INFO: Dependency extraction complete (repository=juancarlosjr97/renovate-test-27939, baseBranch=main)
       "stats": {
         "managers": {"npm": {"fileCount": 1, "depCount": 2}},
         "total": {"fileCount": 1, "depCount": 2}
       }
DEBUG: PackageFiles.add() - Package file saved for base branch (repository=juancarlosjr97/renovate-test-27939, baseBranch=main)
DEBUG: Package releases lookups complete (repository=juancarlosjr97/renovate-test-27939, baseBranch=main)
DEBUG: branchifyUpgrades (repository=juancarlosjr97/renovate-test-27939)
DEBUG: detectSemanticCommits() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: getCommitMessages (repository=juancarlosjr97/renovate-test-27939)
DEBUG: semanticCommits: detected "angular" (repository=juancarlosjr97/renovate-test-27939)
DEBUG: semanticCommits: enabled (repository=juancarlosjr97/renovate-test-27939)
DEBUG: 2 flattened updates found: @graphql-eslint/eslint-plugin, jest (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Returning 1 branch(es) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: config.repoIsOnboarded=true (repository=juancarlosjr97/renovate-test-27939)
DEBUG: packageFiles with updates (repository=juancarlosjr97/renovate-test-27939, baseBranch=main)
       "config": {
         "npm": [
           {
             "deps": [
               {
                 "depType": "dependencies",
                 "depName": "@graphql-eslint/eslint-plugin",
                 "currentValue": "3.19.3",
                 "datasource": "npm",
                 "prettyDepType": "dependency",
                 "lockedVersion": "3.19.3",
                 "updates": [
                   {
                     "bucket": "latest",
                     "newVersion": "3.20.1",
                     "newValue": "3.20.1",
                     "releaseTimestamp": "2023-07-13T07:23:24.793Z",
                     "newMajor": 3,
                     "newMinor": 20,
                     "updateType": "minor",
                     "branchName": "renovate/all"
                   }
                 ],
                 "packageName": "@graphql-eslint/eslint-plugin",
                 "versioning": "npm",
                 "warnings": [],
                 "sourceUrl": "https://github.com/B2o5T/graphql-eslint",
                 "registryUrl": "https://registry.npmjs.org",
                 "currentVersion": "3.19.3",
                 "isSingleVersion": true,
                 "fixedVersion": "3.19.3"
               },
               {
                 "depType": "dependencies",
                 "depName": "jest",
                 "currentValue": "29.4.3",
                 "datasource": "npm",
                 "prettyDepType": "dependency",
                 "lockedVersion": "29.4.3",
                 "updates": [
                   {
                     "bucket": "latest",
                     "newVersion": "29.7.0",
                     "newValue": "29.7.0",
                     "releaseTimestamp": "2023-09-12T06:44:08.561Z",
                     "newMajor": 29,
                     "newMinor": 7,
                     "updateType": "minor",
                     "branchName": "renovate/all"
                   }
                 ],
                 "packageName": "jest",
                 "versioning": "npm",
                 "warnings": [],
                 "sourceUrl": "https://github.com/jestjs/jest",
                 "registryUrl": "https://registry.npmjs.org",
                 "sourceDirectory": "packages/jest",
                 "homepage": "https://jestjs.io/",
                 "currentVersion": "29.4.3",
                 "isSingleVersion": true,
                 "fixedVersion": "29.4.3"
               }
             ],
             "extractedConstraints": {"npm": ">=7"},
             "managerData": {
               "packageJsonName": "renovate-test-27939",
               "hasPackageManager": false,
               "npmLock": "package-lock.json",
               "yarnZeroInstall": false
             },
             "skipInstalls": true,
             "packageFile": "package.json",
             "lockFiles": ["package-lock.json"]
           }
         ]
       }
DEBUG: detectSemanticCommits() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: semanticCommits: returning "enabled" from cache (repository=juancarlosjr97/renovate-test-27939)
DEBUG: processRepo() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Processing 1 branch: renovate/all (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Calculating hourly PRs remaining (repository=juancarlosjr97/renovate-test-27939)
DEBUG: currentHourStart=2024-03-27T18:00:00.000+00:00 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: PR hourly limit remaining: 1 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Calculating prConcurrentLimit (10) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: getBranchPr(renovate/all) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: findPr(renovate/all, undefined, open) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: findPr(renovate/all, undefined, closed) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Found PR #1 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: 0 PRs are currently open (repository=juancarlosjr97/renovate-test-27939)
DEBUG: PR concurrent limit remaining: 10 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Calculated maximum PRs remaining this run: 1 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: PullRequests limit = 1 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Calculating hourly PRs remaining (repository=juancarlosjr97/renovate-test-27939)
DEBUG: currentHourStart=2024-03-27T18:00:00.000+00:00 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: PR hourly limit remaining: 1 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Calculating branchConcurrentLimit (10) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: 0 already existing branches found:  (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Branch concurrent limit remaining: 10 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Calculated maximum branches remaining this run: 1 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Branches limit = 1 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: syncBranchState() (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: syncBranchState(): Branch cache not found, creating minimal branchState (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: getBranchPr(renovate/all) (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: findPr(renovate/all, undefined, open) (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: findPr(renovate/all, undefined, closed) (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Found PR #1 (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: branchExists=false (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: dependencyDashboardCheck=undefined (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: recreateClosed is true. No need to check for closed PR. (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Checking schedule(at any time, null) (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: No schedule defined (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Branch needs creating (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Using reuseExistingBranch: false (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Setting current branch to main (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: latest commit (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "branchName": "main",
       "latestCommitDate": "2024-03-27T18:20:23+00:00"
DEBUG: manager.getUpdatedPackageFiles() reuseExistingBranch=false (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: npm.updateDependency(): dependencies.@graphql-eslint/eslint-plugin = 3.20.1 (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Updating @graphql-eslint/eslint-plugin in package.json (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: npm.updateDependency(): dependencies.jest = 29.7.0 (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Updating jest in package.json (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: updateArtifacts for updatedPackageFiles (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Updated 1 package files (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Getting updated lock files (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Writing package.json files (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "packageFiles": ["package.json"]
DEBUG: Writing package-lock.json (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Massaging npm lock file before writing to disk (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Writing any updated package files (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Writing package.json (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Writing updated .npmrc file to .npmrc (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Generating package-lock.json for . (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Spawning npm install to create ./package-lock.json (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Using npm constraint >=9 for lockfileVersion=3 (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Updating lock file only (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: No node constraint found - using latest (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Setting CONTAINERBASE_CACHE_DIR to /var/folders/73/ykcrrqpd6rjd96sptqy1cx480000gn/T/renovate/cache/containerbase (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Falling back to binarySource=global (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Executing command (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "command": "npm install --package-lock-only --no-audit --ignore-scripts"
DEBUG: exec completed (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "durationMs": 813,
       "stdout": "\nup to date in 606ms\n\n37 packages are looking for funding\n  run `npm fund` for details\n",
       "stderr": ""
DEBUG: package-lock.json needs updating (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Updated 1 lock files (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "updatedArtifacts": ["package-lock.json"]
DEBUG: 2 file(s) to commit (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Preparing files for committing to branch renovate/all (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Setting git author name: Juan Carlos Blanco Delgado (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Setting git author email: juancarlosjr97@gmail.com (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: git commit (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "deletedFiles": [],
       "ignoredFiles": [],
       "result": {
         "author": null,
         "branch": "renovate/all",
         "commit": "5cb7c54e4674214de7b5c2339b175d8c28b03ecd",
         "root": false,
         "summary": {"changes": 2, "insertions": 16, "deletions": 13}
       }
DEBUG: Pushing refSpec renovate/all:renovate/all (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: git push (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "result": {
         "pushed": [
           {
             "deleted": false,
             "tag": false,
             "branch": true,
             "new": true,
             "alreadyUpdated": false,
             "local": "refs/heads/renovate/all",
             "remote": "refs/heads/renovate/all"
           }
         ],
         "ref": {"local": "refs/remotes/origin/renovate/all"},
         "remoteMessages": {
           "all": [
             "Create a pull request for 'renovate/all' on GitHub by visiting:",
             "https://github.com/juancarlosjr97/renovate-test-27939/pull/new/renovate/all"
           ],
           "pullRequestUrl": "https://github.com/juancarlosjr97/renovate-test-27939/pull/new/renovate/all"
         }
       }
DEBUG: Setting current branch to main (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: latest commit (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "branchName": "main",
       "latestCommitDate": "2024-03-27T18:20:23+00:00"
 INFO: Branch created (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "commitSha": "5cb7c54e4674214de7b5c2339b175d8c28b03ecd"
DEBUG: Ensuring PR (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: There are 0 errors and 0 warnings (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: getBranchPr(renovate/all) (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: findPr(renovate/all, undefined, open) (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: findPr(renovate/all, undefined, closed) (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Found PR #1 (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: getPrCache() (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Creating PR (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "prTitle": "production Update all dependencies"
DEBUG: Creating PR (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "title": "production Update all dependencies",
       "head": "juancarlosjr97:renovate/all",
       "base": "main",
       "draft": false
DEBUG: PR created (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "pr": 3,
       "draft": false
DEBUG: Adding labels '' to #3 (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
 INFO: PR created (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
       "pr": 3,
       "prTitle": "production Update all dependencies"
DEBUG: addParticipants(pr=3) (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: setPrCache() (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: Created Pull Request #3 (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: PR is not configured for automerge (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: setBranchCommit() (repository=juancarlosjr97/renovate-test-27939, branch=renovate/all)
DEBUG: getBranchPr(renovate/all) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: findPr(renovate/all, undefined, open) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Found PR #3 (repository=juancarlosjr97/renovate-test-27939)
DEBUG: getPrCache() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: ensureDependencyDashboard() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Ensuring Dependency Dashboard (repository=juancarlosjr97/renovate-test-27939)
DEBUG: http cache: saving https://api.github.com/repos/juancarlosjr97/renovate-test-27939/issues/2 (etag=W/"820a191e0aafd214612c7e6c27a96227e7063381cd54ba00f78d18daf73aa1a8", lastModified=Wed, 27 Mar 2024 18:18:09 GMT) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: http cache: Using cached response: https://api.github.com/repos/juancarlosjr97/renovate-test-27939/issues/2 from 2024-03-27T18:21:15.504Z (repository=juancarlosjr97/renovate-test-27939)
DEBUG: ensureIssue(Dependency Dashboard) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: http cache: saving https://api.github.com/repos/juancarlosjr97/renovate-test-27939/issues/2 (etag=W/"820a191e0aafd214612c7e6c27a96227e7063381cd54ba00f78d18daf73aa1a8", lastModified=Wed, 27 Mar 2024 18:18:09 GMT) (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Patching issue (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Issue updated (repository=juancarlosjr97/renovate-test-27939)
DEBUG: validateReconfigureBranch() (repository=juancarlosjr97/renovate-test-27939)
DEBUG: No reconfigure branch found (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Removing any stale branches (repository=juancarlosjr97/renovate-test-27939)
DEBUG: config.repoIsOnboarded=true (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Branch lists (repository=juancarlosjr97/renovate-test-27939)
       "branchList": ["renovate/all"],
       "renovateBranches": ["renovate/all"]
DEBUG: remainingBranches= (repository=juancarlosjr97/renovate-test-27939)
DEBUG: No branches to clean up (repository=juancarlosjr97/renovate-test-27939)
DEBUG: PackageFiles.clear() - Package files deleted (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Branch summary (repository=juancarlosjr97/renovate-test-27939)
       "cacheModified": undefined,
       "baseBranches": [{"branchName": "main", "sha": "85b98f6c75221c878161463b108dafa5e9b6c347"}],
       "branches": [
         {
           "automerge": false,
           "baseBranch": "main",
           "baseBranchSha": "85b98f6c75221c878161463b108dafa5e9b6c347",
           "branchName": "renovate/all",
           "branchSha": "5cb7c54e4674214de7b5c2339b175d8c28b03ecd",
           "isModified": false,
           "isPristine": true
         }
       ],
       "defaultBranch": "main",
       "inactiveBranches": []
DEBUG: branches info extended (repository=juancarlosjr97/renovate-test-27939)
       "branchesInformation": [
         {
           "branchName": "renovate/all",
           "prNo": 3,
           "prTitle": "production Update all dependencies",
           "result": "pr-created",
           "upgrades": [
             {
               "datasource": "npm",
               "depName": "@graphql-eslint/eslint-plugin",
               "displayPending": "",
               "fixedVersion": "3.19.3",
               "currentVersion": "3.19.3",
               "currentValue": "3.19.3",
               "newValue": "3.20.1",
               "newVersion": "3.20.1",
               "packageFile": "package.json",
               "updateType": "minor",
               "packageName": "@graphql-eslint/eslint-plugin"
             },
             {
               "datasource": "npm",
               "depName": "jest",
               "displayPending": "",
               "fixedVersion": "29.4.3",
               "currentVersion": "29.4.3",
               "currentValue": "29.4.3",
               "newValue": "29.7.0",
               "newVersion": "29.7.0",
               "packageFile": "package.json",
               "updateType": "minor",
               "packageName": "jest"
             }
           ]
         }
       ]
DEBUG: Renovate repository PR statistics (repository=juancarlosjr97/renovate-test-27939)
       "stats": {"total": 2, "open": 1, "closed": 1, "merged": 0}
DEBUG: Repository result: done, status: onboarded, enabled: true, onboarded: true (repository=juancarlosjr97/renovate-test-27939)
DEBUG: Repository timing splits (milliseconds) (repository=juancarlosjr97/renovate-test-27939)
       "splits": {"init": 2433, "extract": 321, "lookup": 172, "onboarding": 1, "update": 3310},
       "total": 6904
DEBUG: Package cache statistics (repository=juancarlosjr97/renovate-test-27939)
       "get": {"count": 2, "avgMs": 20, "medianMs": 33, "maxMs": 33, "totalMs": 39},
       "set": {"count": 0, "avgMs": 0, "medianMs": 0, "maxMs": 0, "totalMs": 0}
DEBUG: HTTP statistics (repository=juancarlosjr97/renovate-test-27939)
       "urls": {
         "https://api.github.com/graphql": {"POST": {"200": 2}},
         "https://api.github.com/repos/juancarlosjr97/renovate-test-27939/issues/2": {
           "GET": {"200": 1, "304": 1},
           "PATCH": {"200": 1}
         },
         "https://api.github.com/repos/juancarlosjr97/renovate-test-27939/pulls": {
           "POST": {"201": 1},
           "GET": {"200": 1}
         }
       },
       "hosts": {
         "api.github.com": {
           "count": 7,
           "reqAvgMs": 318,
           "reqMedianMs": 196,
           "reqMaxMs": 811,
           "queueAvgMs": 0,
           "queueMedianMs": 0,
           "queueMaxMs": 0
         }
       },
       "requests": 7
DEBUG: HTTP cache statistics (repository=juancarlosjr97/renovate-test-27939)
       "https://api.github.com": {
         "/repos/juancarlosjr97/renovate-test-27939/issues/2": {"hit": 1, "miss": 3},
         "/repos/juancarlosjr97/renovate-test-27939/pulls": {"hit": 0, "miss": 1}
       },
       "https://registry.npmjs.org": {
         "/@graphql-eslint%2Feslint-plugin": {"hit": 0, "miss": 0, "localHit": 1},
         "/jest": {"hit": 0, "miss": 0, "localHit": 1}
       }
DEBUG: Lookup statistics (repository=juancarlosjr97/renovate-test-27939)
       "npm": {"count": 2, "avgMs": 42, "medianMs": 53, "maxMs": 53, "totalMs": 83}
DEBUG: dns cache (repository=juancarlosjr97/renovate-test-27939)
       "hosts": []
 INFO: Repository finished (repository=juancarlosjr97/renovate-test-27939)
       "cloned": true,
       "durationMs": 6904
DEBUG: Checking file package cache for expired items
DEBUG: Deleted 0 of 3 file cached entries in 6ms
```
</details>


Both changes are using the same [renovate.json](https://github.com/juancarlosjr97/renovate-test-27939/blob/main/renovate.json) and the same commit sha is visible from the logs of the latestCommit.
