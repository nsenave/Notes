# Java

## Utils

Lire des CSV
- https://www.geeksforgeeks.org/reading-csv-file-java-using-opencsv/

Liste d'entiers consécutifs
- https://www.baeldung.com/java-listing-numbers-within-a-range

Condition dans un stream avec .filter()
- https://howtodoinjava.com/java8/stream-if-else-logic/

getAbsolutePath vs. getCanonicalPath
- https://www.baeldung.com/java-path

Linked lists (cf. méthode pop en java)
- https://www.tutorialspoint.com/java/util/linkedlist_pop.htm

Patter Builder
- https://sidath.medium.com/builder-pattern-with-java-lombok-67c507aeb06d
- https://stackoverflow.com/questions/21086417/builder-pattern-and-inheritance
- https://www.baeldung.com/lombok-builder-inheritance

Supprimer des éléments d'une liste/map dans une boucle for :
- https://stackoverflow.com/questions/223918/iterating-through-a-collection-avoiding-concurrentmodificationexception-when-re
  - https://stackoverflow.com/a/223929/13425151

Enum "subset" :
- https://stackoverflow.com/questions/32479688/subset-of-enum-values-in-java

Validation avec des enums :
- https://www.baeldung.com/javax-validations-enums

Check if a Path represents a file or folder :
- https://stackoverflow.com/questions/12780446/check-if-a-path-represents-a-file-or-a-folder

List files of a Path :
- https://stackoverflow.com/questions/12780446/check-if-a-path-represents-a-file-or-a-folder

## Bonnes pratiques

Nombre de lignes dans une classe/une fonction
- https://stackoverflow.com/questions/107855/maximum-lines-of-code-permitted-in-a-java-class#107911
- https://dzone.com/articles/rule-30-%E2%80%93-when-method-class-or
- https://softwareengineering.stackexchange.com/questions/66523/how-many-lines-per-class-is-too-many-in-java

Numéros et tags de versions (SNAPSHOT, RELEASE, RC, M1, ...)
- https://stackoverflow.com/questions/3687208/what-does-m1-mean-in-a-maven-repository
- https://stackoverflow.com/a/43122361

Gestion des exceptions
- https://gitlab.insee.fr/sic/divers/ateliers-pratique-du-dev-metallica/-/wikis/Gestion%20des%20exceptions
- https://gitlab.insee.fr/sic/divers/ateliers-pratique-du-dev-metallica/-/wikis/home
- https://howtodoinjava.com/best-practices/java-exception-handling-best-practices/

JDK, JRE, JVM
- https://www.geeksforgeeks.org/difference-between-jdk-and-jre-in-java/
- https://stackoverflow.com/questions/4696611/jdk-jre-java-version-confusion

Choisir le bon JDK en ligne de commande
- https://stackoverflow.com/questions/10687093/java-home-and-java-version

Java Doc
- https://stackoverflow.com/questions/10088311/javadoc-return-tag-comment-duplication-necessary
- https://stackoverflow.com/a/10088414/13425151

Itérer sur les attributs d'une classe / éviter l'introspection :
- https://stackoverflow.com/questions/3333974/how-to-loop-over-a-class-attributes-in-java
  - https://stackoverflow.com/a/3333989/13425151

Paths.get vs Path.of :
- https://stackoverflow.com/questions/58631724/paths-get-vs-path-of
  - https://stackoverflow.com/a/58631951/13425151

## Tests

Tests avec junit5
- https://howtodoinjava.com/junit-5-tutorial/
- https://howtodoinjava.com/junit5/junit-5-assertions-examples/
- https://blog.jetbrains.com/idea/2020/09/writing-tests-with-junit-5/
- https://developer.ibm.com/languages/java/tutorials/j-introducing-junit5-part1-jupiter-api/
- https://www.baeldung.com/junit-5
- https://www.baeldung.com/junit5-test-templates

Naming conventions for unit testing
- https://stackoverflow.com/questions/155436/unit-test-naming-best-practices
- https://softwareengineering.stackexchange.com/questions/237561/naming-test-methods-in-java

Get test resource
- https://stackoverflow.com/questions/5529532/how-to-get-a-test-resource-file
- https://stackoverflow.com/a/40875374/13425151

Tester les méhodes privées ?
- https://stackoverflow.com/questions/3299405/how-should-i-test-private-methods-in-java
- https://stackoverflow.com/a/3299443/13425151

BeforeEach pour un groupe de tests
- https://stackoverflow.com/questions/1548462/junit-before-only-for-some-test-methods
- https://stackoverflow.com/a/58605274/13425151

Tests avec Cucumber
- https://maven.apache.org/surefire-archives/surefire-3.0.0-M2/maven-surefire-plugin/examples/cucumber.html

Liste de String dans un scénario Cucumber :
- https://stackoverflow.com/questions/64366164/passing-list-of-strings-as-cucumber-parameter
  - https://stackoverflow.com/a/64380567/13425151

## Maven

Maven Surefire Plugin
- https://www.baeldung.com/maven-surefire-plugin
- https://maven.apache.org/surefire-archives/surefire-3.0.0-M2/maven-surefire-plugin/usage.html

Maven Dependency Scopes
- https://www.baeldung.com/maven-dependency-scopes

Maven pom > dependency > optional
- https://maven.apache.org/guides/introduction/introduction-to-optional-and-excludes-dependencies.html

Projet multi-module
- https://www.baeldung.com/maven-multi-module-project-java-jpms

Change version in multi-module maven project
- https://stackoverflow.com/questions/5726291/updating-version-numbers-of-modules-in-a-multi-module-maven-project
  - https://stackoverflow.com/a/5726599/13425151

## Spring

Properties
- https://www.baeldung.com/java-properties
- https://docs.spring.io/spring-boot/docs/current/reference/html/application-properties.html#application-properties.core.logging.pattern.console
- https://stackoverflow.com/questions/34845990/spring-use-one-application-properties-for-production-and-another-for-debug#34846351
- https://stackoverflow.com/questions/36415599/how-to-unit-test-the-class-that-reads-properties-file

Logging
- https://docs.spring.io/spring-boot/docs/current/reference/html/features.html#features.logging
- https://www.baeldung.com/spring-boot-logging
- https://blog.engineering.publicissapient.fr/2010/07/07/java-en-production-les-fichiers-de-logs/
- https://howtodoinjava.com/spring-boot2/logging/multiple-log-files/
- https://www.baeldung.com/java-logging-rolling-file-appenders
- https://www.codejava.net/frameworks/spring-boot/logback-rolling-files-example
- https://stackoverflow.com/questions/39103771/spring-boot-multiple-log-files
- https://stackoverflow.com/questions/42525987/spring-boot-logging-into-multiple-files
- https://stackoverflow.com/questions/49925150/logback-xml-to-logback-property-file
  - https://docs.spring.io/spring-boot/docs/2.0.1.RELEASE/reference/html/boot-features-logging.html
  - https://docs.spring.io/spring-boot/docs/2.0.1.RELEASE/reference/html/howto-logging.html
  - https://www.logicbig.com/tutorials/spring-framework/spring-boot/logging-file.html
- https://stackoverflow.com/questions/50253424/springboot-with-logback-creating-log-file-is-undefined-folder


Tests avec Spring Boot
- https://gitlab.insee.fr/animation-developpement/ateliers/spring-boot-tests

Maven / Spring profiles
- https://www.baeldung.com/maven-profiles
- https://maven.apache.org/guides/introduction/introduction-to-profiles.html
- https://mkyong.com/spring-boot/spring-boot-profile-based-properties-and-yaml-example/
- https://stackoverflow.com/questions/37700352/setting-the-default-active-profile-in-spring-boot
- https://stackoverflow.com/a/37700521/13425151
- https://stackoverflow.com/questions/38970146/how-to-exclude-default-application-properties-add-custom-properties-file-using-p
- https://stackoverflow.com/questions/25385444/loading-properties-based-on-maven-profiles
- https://stackoverflow.com/questions/11824328/default-build-profile-for-maven
