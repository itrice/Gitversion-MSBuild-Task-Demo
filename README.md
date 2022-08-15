Gitversion MSBuild Task Demo

this demo tells you how to use Gitversion to help Semver with Conventional Commit.

## Working with MSBuild Task

Just install with NuGet and GitVersion will automatically generate assembly version information that is compiled into the resulting artifact.

[[GitVersion - MSBuild Task](https://gitversion.net/docs/usage/msbuild)]

Step 1: Create a .net core \ .net Framework project. Remove the assembly file in your project, or comment on the version lines.

![image](https://user-images.githubusercontent.com/10216853/184575613-ba0b02ce-56c3-43ce-a30d-65d94a92ad9c.png)


Step 2: Initial git repository in the project folder.

Step 3: Install the Nuget package, with the command `Install-Package GitVersion.MsBuild -Version 5.10.3`

Step 4: Do some git commits, and build your project. And then, congratulations, you can see the Gitversion Task has worked.

Setp 5: As to use some advanced featrues, you could create a gitversion.yml file in your local. Just look like below:

```next-version: 8.1.0
assembly-versioning-scheme: MajorMinorPatch
assembly-file-versioning-scheme: MajorMinorPatch
assembly-informational-format: '{Major}.{Minor}.{Patch}'
commit-date-format: yyMMddTHHmmss
mode: ContinuousDeployment
increment: Inherit
continuous-delivery-fallback-tag: ci
tag-prefix: '[vV]'
major-version-bump-message: "^(BREAKING CHANGE)(\\([\\w\\s-]*\\))?:"
minor-version-bump-message: "^(feat)(\\([\\w\\s-]*\\))?:"
patch-version-bump-message: "^(build|chore|ci|docs|fix|perf|refactor|revert|style|test)(\\([\\w\\s-]*\\))?:"
no-bump-message: '\+semver:\s?(none|skip)'
legacy-semver-padding: 4
build-metadata-padding: 4
commits-since-version-source-padding: 4
tag-pre-release-weight: 60000
commit-message-incrementing: Enabled

ignore:
  sha: []
  commits-before: 
merge-message-formats: {}
update-build-number: true
```
