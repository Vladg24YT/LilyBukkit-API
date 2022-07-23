LilyBukkit-API
======

A modified Bukkit Minecraft Server API.

Website: [https://vladg24yt.github.io/LilyBukkit-API](https://vladg24yt.github.io/LilyBukkit-API)  
Bugs/Suggestions: [Issues](https://github.com/Vladg24YT/LilyBukkit-API/issues) and [Discord](https://discord.gg/qzKFJZW6bZ)  
Wiki: [https://github.com/Vladg24YT/LilyBukkit-API/wiki](https://github.com/Vladg24YT/LilyBukkit-API/wiki)

## Installation
### Using precompiled `jar`s
Download the latest `jar` from [Releases](https://github.com/Vladg24YT/LilyBukkit-API/releases/latest), then follow one of the instructions below.  
**Maven**:  
Add the following code to your `pom.xml`:
```xml
<dependency>
    <groupId>ru.vladthemountain</groupId>
    <artifactId>lilybukkit</artifactId>
    <version>1.1.0</version>
    <scope>system</scope>
    <systemPath>${project.basedir}/relative/path/to/lilybukkit-1.1.0.jar</systemPath>
</dependency>
```
**Gradle**:  
Add the following code to your `build.gradle`:
```groovy
dependencies {
    implementation files('relative/path/to/lilybukkit-1.1.0.jar')
}
```
### Using GitHub Packages
* **GitHub Actions** with a **Maven** project: [see this StackOverflow answer](https://stackoverflow.com/a/67406422).
* **GitHub Actions** with a **Gradle** project: [follow this official guide](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-gradle-registry)
* **Maven** project: [follow this official guide](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-apache-maven-registry).
* **Gradle** project: add the following code to your `build.gradle`
```groovy
repositories {
    maven {
        url = uri("https://maven.pkg.github.com/Vladg24YT/LilyBukkit-API")
        credentials {
            username = project.findProperty("gpr.user") ?: System.getenv("GITHUB_USERNAME")
            password = project.findProperty("gpr.key") ?: System.getenv("GITHUB_PERSONAL_ACCESS_TOKEN")
        }
    }
}
dependencies {
    implementation 'ru.vladthemountain:lilybukkit:1.1.0'
}
```
Add the following code to your `gradle.properties`:
```groovy
org.gradle.project.gpr.user=/*your GitHub username*/
org.gradle.project.key=/*your GitHub Personal Access Token*/
```
