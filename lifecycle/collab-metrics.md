# Collaboration metrics - Stirling-PDF

Appended by `_system/scripts/collab_metrics.py`. Derived from git and GitHub after the fact; nothing here proves a merge was clean, because squash-merge erases that.

## 2026-09-21 05:00 (last 7 days)

**Abandoned pull requests (closed, never merged): 19.**
  - #8100 AI settings status page, and Stirling Cloud AI for linked instances
  - #8096 build(deps): bump webview2-com from 0.38.2 to 0.39.1 in /frontend/editor/src-tau
  - #8094 build(deps): bump the tauri group across 1 directory with 13 updates
  - #8087 AI settings status page, and Stirling Cloud AI for linked instances
  - #8079 fix(nav): open from computer works while reading
  - #8071 build(deps-dev): bump vitest from 3.2.7 to 5.0.1 in /frontend
  - #8069 build(deps-dev): bump fast-uri from 3.1.7 to 3.1.8 in /frontend
  - #8047 Storybook: typecheck desktop stories under the desktop cascade instead of exclud
  - #8040 perf(build): precompress the dist, shrink startup, defer the pdfium wasm
  - #8004 Hide local MFA enrollment for SSO accounts
  - *Says nothing about why. A superseded duplicate and a failed change look the same.*

**Leftovers: 0 worktree records to prune, 1 branches with no merged pull request (1 older than 7 days).**
  - chore/dev-system-integration (27 days)
  - *Expect this to look alarming and mostly not be. Squash-merge rewrites commits, so a branch whose work IS merged still reads as unmerged; these are matched against merged pull request branches by name only. Review candidates, not findings.*

**File collisions: 71 pair(s) of the 40 open pull requests touch the same file.**
  - #8035 and #8036 share 8 file(s): app/proprietary/src/main/java/stirling/software/proprietary/policy/controller/ProcessingFolderController.java, app/proprietary/src/main/java/stirling/software/proprietary/policy/engine/PolicyRunner.java, app/proprietary/src/main/java/stirling/software/proprietary/policy/input/FolderInputSource.java, app/proprietary/src/main/java/stirling/software/proprietary/policy/input/InputSource.java, app/proprietary/src/main/java/stirling/software/proprietary/policy/input/S3InputSource.java
  - #8035 and #8085 share 3 file(s): app/proprietary/src/main/java/stirling/software/proprietary/policy/engine/PolicyRunner.java, app/proprietary/src/test/java/stirling/software/proprietary/policy/engine/PolicyRunnerTest.java, app/proprietary/src/test/java/stirling/software/proprietary/policy/input/StorageFolderAuthorizationTest.java
  - #8036 and #8043 share 1 file(s): app/core/build.gradle
  - #8036 and #8053 share 2 file(s): app/proprietary/src/main/java/stirling/software/proprietary/accountlink/DeviceCredentialRepository.java, app/proprietary/src/main/java/stirling/software/proprietary/security/service/UserService.java
  - #8036 and #8056 share 1 file(s): .taskfiles/frontend.yml
  - #8036 and #8061 share 6 file(s): .gitignore, app/proprietary/build.gradle, app/proprietary/src/main/java/stirling/software/proprietary/policy/seed/DefaultClassificationPolicySeeder.java, app/proprietary/src/main/java/stirling/software/proprietary/security/controller/api/UserController.java, app/proprietary/src/main/java/stirling/software/proprietary/security/repository/TeamRepository.java
  - #8036 and #8062 share 7 file(s): .gitignore, app/proprietary/build.gradle, app/proprietary/src/main/java/stirling/software/proprietary/policy/seed/DefaultClassificationPolicySeeder.java, app/proprietary/src/main/java/stirling/software/proprietary/security/controller/api/UserController.java, app/proprietary/src/main/java/stirling/software/proprietary/security/database/repository/UserRepository.java
  - #8036 and #8063 share 6 file(s): .gitignore, app/proprietary/build.gradle, app/proprietary/src/main/java/stirling/software/proprietary/policy/seed/DefaultClassificationPolicySeeder.java, app/proprietary/src/main/java/stirling/software/proprietary/security/controller/api/UserController.java, app/proprietary/src/main/java/stirling/software/proprietary/security/repository/TeamRepository.java
  - #8036 and #8064 share 6 file(s): .gitignore, app/proprietary/build.gradle, app/proprietary/src/main/java/stirling/software/proprietary/policy/seed/DefaultClassificationPolicySeeder.java, app/proprietary/src/main/java/stirling/software/proprietary/security/controller/api/UserController.java, app/proprietary/src/main/java/stirling/software/proprietary/security/repository/TeamRepository.java
  - #8036 and #8067 share 1 file(s): app/core/src/main/resources/static/3rdPartyLicenses.json
  - *Only counts pull requests open right now, so two agents who collided and already merged are invisible to it.*

**Rework: 19 of the 39 merged pull requests carrying a GitHub review got more commits after the first one.**
  - #7997: 6 commit(s) after review
  - #7998: 4 commit(s) after review
  - #8044: 3 commit(s) after review
  - #8025: 3 commit(s) after review
  - #8002: 3 commit(s) after review
  - #8081: 2 commit(s) after review
  - #8038: 2 commit(s) after review
  - #8000: 2 commit(s) after review
  - #7996: 2 commit(s) after review
  - #8080: 1 commit(s) after review
  - *More commits after a review can mean the review worked, not that the process failed.*

**Time from opening to merge: median 11.8 h, longest 50.6 h, across 39 merged pull requests.** *The long tail is where friction hides; a merge that waited on a human is counted the same as one that fought the code.*

