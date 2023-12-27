# Gradle

Comparison with Maven lifecycle:
- https://docs.gradle.org/current/userguide/migrating_from_maven.html#migmvn:build_lifecycle

Gradle Wrapper in remote ? (yes)
- https://stackoverflow.com/questions/43954932/should-i-gitignore-my-gradlew
- https://docs.gradle.org/current/userguide/gradle_wrapper.html

Setup Java-gradle project
- https://docs.gradle.org/current/samples/index.html#java

Repositories
- https://docs.gradle.org/current/userguide/declaring_repositories.html

Proxy config
- https://docs.gradle.org/current/userguide/build_environment.html#sec:accessing_the_web_via_a_proxy

Source sets (-> custom source/resources directories)
- https://docs.gradle.org/current/dsl/org.gradle.api.tasks.SourceSet.html
- https://www.baeldung.com/gradle-source-sets#1-defining-custom-source-sets

Skip a task
- https://docs.gradle.org/current/userguide/more_about_tasks.html#sec:skipping_tasks

File trees
- https://docs.gradle.org/current/userguide/gradle_wrapper.html

Get project version in console
- https://stackoverflow.com/questions/24936781/gradle-plugin-project-version-number
- https://stackoverflow.com/questions/44466728/gradle-project-version-from-build-gradle-via-shell-bash-script

Script way: `./gradlew properties --no-daemon --console=plain -q | grep "^version:" | awk '{printf $2}'`

Gradle properties / user properties
- https://stackoverflow.com/questions/21762180/should-you-include-or-ignore-gradle-wrapper-properties
  - https://stackoverflow.com/a/21762567/13425151
- https://stackoverflow.com/questions/54039948/where-to-put-user-project-specific-gradle-properties
  - https://stackoverflow.com/a/54043676/13425151
- Properties plugin:
  - https://plugins.gradle.org/plugin/net.saliman.properties
  - https://github.com/stevesaliman/gradle-properties-plugin
- Proxy: https://docs.gradle.org/current/userguide/build_environment.html#sec:accessing_the_web_via_a_proxy
- https://discuss.gradle.org/t/best-practice-for-gradle-properties-and-scm/5809

"Permission denied" with wrapper
- https://stackoverflow.com/questions/17668265/gradlew-permission-denied
  - https://stackoverflow.com/a/17669566/13425151

Spring Boot app remove the "-plain" jar
- https://stackoverflow.com/questions/67663728/spring-boot-2-5-0-generates-plain-jar-file-can-i-remove-it
  - https://stackoverflow.com/a/67663956/13425151
- https://docs.spring.io/spring-boot/docs/current/gradle-plugin/reference/htmlsingle/#packaging-executable.and-plain-archives
  - (Don't do that if you want to make a native image) https://github.com/spring-projects/spring-boot/issues/33238

Gradle property at runtime in Java through application.properties
- https://stackoverflow.com/questions/40017216/add-gradle-properties-to-application-properties-resource
- https://docs.spring.io/spring-boot/docs/2.0.0.M3/reference/html/howto-properties-and-configuration.html#howto-automatic-expansion-gradle
- https://docs.gradle.org/current/dsl/org.gradle.language.jvm.tasks.ProcessResources.html
- https://www.baeldung.com/spring-boot-auto-property-expansion
- https://github.com/eugenp/tutorials/tree/master/spring-boot-modules/spring-boot-property-exp/property-exp-default-config

### Use a private maven repo

- `gradle.properties`

```
systemProp.urlMavenRepo="https://repo.mycompany.com/releases"
```

- `settings.gradle`

```groovy
dependencyResolutionManagement {

    repositories {
        // Config for maven central repository
        mavenCentral()
        // Config for maven snapshot repositories
        maven {
            url "https://oss.sonatype.org/content/repositories/snapshots"
            mavenContent {
                snapshotsOnly()
            }
        }
        maven { // Note: see https://central.sonatype.org/news/20210223_new-users-on-s01/
            url "https://s01.oss.sonatype.org/content/repositories/snapshots"
            mavenContent {
                snapshotsOnly()
            }
        }
        // Config for private maven repository
        maven {
            url System.properties['urlMavenRepo']
        }
        // Config for local maven dependencies
        mavenLocal()
    }

}
```

Bonus: Use a local gradle properties file if you don't want to commit the url of your private repo:

- `build.gradle`

```groovy
plugins {

    // Plugin to use local gradle properties file
    id 'net.saliman.properties' version '1.5.2'

}
```

- `gradle-local.properties`

```
systemProp.urlMavenRepo="https://actual-repo.my-actual-company.com/releases"
```

### Publish on maven central

Publish your Gradle artifact to Maven Central (Medium)
- https://h4pehl.medium.com/publish-your-gradle-artifacts-to-maven-central-f74a0af085b1

Gradle maven publish plugin (generated pom etc.)
- https://docs.gradle.org/current/userguide/publishing_maven.html

### Alternatives to maven central

Bintray was a popular open-source hosting service for storing Java libraries, packages, and components that ended on May 1, 2021. 
- https://blog.jetbrains.com/idea/2021/04/migration-from-bintray/

JetBrain / IntelliJ Space Packages
- https://blog.jetbrains.com/space/2020/01/14/introducing-space-packages/

https://docs.github.com/en/actions/publishing-packages/publishing-java-packages-with-gradle
https://www.jetbrains.com/help/idea/add-a-gradle-library-to-the-maven-repository.html
https://entzik.medium.com/how-to-publish-open-source-java-libraries-to-maven-central-70f9232462f5
