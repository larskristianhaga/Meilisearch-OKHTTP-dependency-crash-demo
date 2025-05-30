# Meilisearch OKHTTP

Running `mvn clean install`, and then `mvn dependency:tree` gives this:
``` Maven
[INFO] \- com.meilisearch.sdk:meilisearch-java:jar:0.14.4:compile
[INFO]    +- com.squareup.okhttp3:okhttp:jar:5.0.0-alpha.16:compile
```
When in reality it should resolve to `4.12.0`.

Full result of `mvn dependency:tree`:
``` Maven
> dependency:tree
[INFO] Scanning for projects...
[INFO] 
[INFO] ---------------< no.cappelendamm:meilisearchOKHTTPDemo >----------------
[INFO] Building meilisearchOKHTTPDemo 0.0.1-SNAPSHOT
[INFO]   from pom.xml
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- dependency:3.8.1:tree (default-cli) @ meilisearchOKHTTPDemo ---
[INFO] no.cappelendamm:meilisearchOKHTTPDemo:jar:0.0.1-SNAPSHOT
[INFO] +- org.springframework.boot:spring-boot-starter:jar:3.5.0:compile
[INFO] |  +- org.springframework.boot:spring-boot:jar:3.5.0:compile
[INFO] |  |  \- org.springframework:spring-context:jar:6.2.7:compile
[INFO] |  |     +- org.springframework:spring-aop:jar:6.2.7:compile
[INFO] |  |     +- org.springframework:spring-beans:jar:6.2.7:compile
[INFO] |  |     +- org.springframework:spring-expression:jar:6.2.7:compile
[INFO] |  |     \- io.micrometer:micrometer-observation:jar:1.15.0:compile
[INFO] |  |        \- io.micrometer:micrometer-commons:jar:1.15.0:compile
[INFO] |  +- org.springframework.boot:spring-boot-autoconfigure:jar:3.5.0:compile
[INFO] |  +- org.springframework.boot:spring-boot-starter-logging:jar:3.5.0:compile
[INFO] |  |  +- ch.qos.logback:logback-classic:jar:1.5.18:compile
[INFO] |  |  |  \- ch.qos.logback:logback-core:jar:1.5.18:compile
[INFO] |  |  +- org.apache.logging.log4j:log4j-to-slf4j:jar:2.24.3:compile
[INFO] |  |  |  \- org.apache.logging.log4j:log4j-api:jar:2.24.3:compile
[INFO] |  |  \- org.slf4j:jul-to-slf4j:jar:2.0.17:compile
[INFO] |  +- jakarta.annotation:jakarta.annotation-api:jar:2.1.1:compile
[INFO] |  +- org.springframework:spring-core:jar:6.2.7:compile
[INFO] |  |  \- org.springframework:spring-jcl:jar:6.2.7:compile
[INFO] |  \- org.yaml:snakeyaml:jar:2.4:compile
[INFO] +- org.springframework.boot:spring-boot-starter-test:jar:3.5.0:test
[INFO] |  +- org.springframework.boot:spring-boot-test:jar:3.5.0:test
[INFO] |  +- org.springframework.boot:spring-boot-test-autoconfigure:jar:3.5.0:test
[INFO] |  +- com.jayway.jsonpath:json-path:jar:2.9.0:test
[INFO] |  |  \- org.slf4j:slf4j-api:jar:2.0.17:compile
[INFO] |  +- jakarta.xml.bind:jakarta.xml.bind-api:jar:4.0.2:test
[INFO] |  |  \- jakarta.activation:jakarta.activation-api:jar:2.1.3:test
[INFO] |  +- net.minidev:json-smart:jar:2.5.2:test
[INFO] |  |  \- net.minidev:accessors-smart:jar:2.5.2:test
[INFO] |  |     \- org.ow2.asm:asm:jar:9.7.1:test
[INFO] |  +- org.assertj:assertj-core:jar:3.27.3:test
[INFO] |  |  \- net.bytebuddy:byte-buddy:jar:1.17.5:test
[INFO] |  +- org.awaitility:awaitility:jar:4.3.0:test
[INFO] |  +- org.hamcrest:hamcrest:jar:3.0:test
[INFO] |  +- org.junit.jupiter:junit-jupiter:jar:5.12.2:test
[INFO] |  |  +- org.junit.jupiter:junit-jupiter-api:jar:5.12.2:test
[INFO] |  |  |  +- org.opentest4j:opentest4j:jar:1.3.0:test
[INFO] |  |  |  +- org.junit.platform:junit-platform-commons:jar:1.12.2:test
[INFO] |  |  |  \- org.apiguardian:apiguardian-api:jar:1.1.2:test
[INFO] |  |  +- org.junit.jupiter:junit-jupiter-params:jar:5.12.2:test
[INFO] |  |  \- org.junit.jupiter:junit-jupiter-engine:jar:5.12.2:test
[INFO] |  |     \- org.junit.platform:junit-platform-engine:jar:1.12.2:test
[INFO] |  +- org.mockito:mockito-core:jar:5.17.0:test
[INFO] |  |  +- net.bytebuddy:byte-buddy-agent:jar:1.17.5:test
[INFO] |  |  \- org.objenesis:objenesis:jar:3.3:test
[INFO] |  +- org.mockito:mockito-junit-jupiter:jar:5.17.0:test
[INFO] |  +- org.skyscreamer:jsonassert:jar:1.5.3:test
[INFO] |  |  \- com.vaadin.external.google:android-json:jar:0.0.20131108.vaadin1:test
[INFO] |  +- org.springframework:spring-test:jar:6.2.7:test
[INFO] |  \- org.xmlunit:xmlunit-core:jar:2.10.1:test
[INFO] \- com.meilisearch.sdk:meilisearch-java:jar:0.14.4:compile
[INFO]    +- com.squareup.okhttp3:okhttp:jar:5.0.0-alpha.16:compile
[INFO]    |  +- org.jetbrains.kotlin:kotlin-stdlib:jar:1.9.25:runtime
[INFO]    |  |  \- org.jetbrains:annotations:jar:13.0:runtime
[INFO]    |  \- com.squareup.okio:okio:jar:3.12.0:runtime
[INFO]    |     \- com.squareup.okio:okio-jvm:jar:3.12.0:runtime
[INFO]    +- com.google.code.gson:gson:jar:2.13.1:runtime
[INFO]    |  \- com.google.errorprone:error_prone_annotations:jar:2.38.0:runtime
[INFO]    +- org.json:json:jar:20250107:runtime
[INFO]    \- com.auth0:java-jwt:jar:4.5.0:runtime
[INFO]       +- com.fasterxml.jackson.core:jackson-core:jar:2.19.0:runtime
[INFO]       \- com.fasterxml.jackson.core:jackson-databind:jar:2.19.0:runtime
[INFO]          \- com.fasterxml.jackson.core:jackson-annotations:jar:2.19.0:runtime
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  3.556 s
[INFO] Finished at: 2025-05-30T12:12:56+02:00
[INFO] ------------------------------------------------------------------------

Process finished with exit code 0
```