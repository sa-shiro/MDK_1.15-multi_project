# Forge MDK 1.14.4 Multiproject setup
How to import projects to IntelliJ:
* un/comment module(s) in `settings.gradle` and change the path to match the submodule source directory
* change the following entries in `build.gradle`
```gradle
outputDir = new File("C:\\_minecraft\\1.15\\\\build\\out\\${project.name}")
testOutputDir = new File("C:\\_minecraft\\1.15\\build\\out\\test\\${project.name}")

buildDir = "C:\\_minecraft\\1.14.4\\build\\${project.name}"

runs {
 client {
  workingDirectory 'C:\\_minecraft\\1.15\\run'
 }
}
```
`outputDir` output dir for compiled source files

`buildDir` the build output location

`workingDirectory` the location of minecraft gamefiles
---
# The following Projects are depending on this multi-project setup
[The Compressed Blocks Mod](https://github.com/sa-shiro/Minecraft-Compressed-Blocks)
