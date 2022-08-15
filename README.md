Gitversion MSBuild Task Demo

this demo tells you how to use Gitversion to help Semver with Conventional Commit.

## Working with MSBuild Task

Just install with NuGet and GitVersion will automatically generate assembly version information that is compiled into the resulting artifact.

[[GitVersion - MSBuild Task](https://gitversion.net/docs/usage/msbuild)]

Step 1: Create a .net core \ .net Framework project. Remove the assembly file in your project, or comment on the version lines.

![image](https://user-images.githubusercontent.com/10216853/184575613-ba0b02ce-56c3-43ce-a30d-65d94a92ad9c.png)


Step 2: Initial git repository in the project folder.

Step 3: Install the Nuget package, with the command `Install-Package GitVersion.MsBuild -Version 5.10.3`

Step 4: Do some git commits, and then you can build your project. And then, you can see the Gitversion Task has worked.

Setp 5: As you 
