# Meilisearch OKHTTP

Running `mvn clean install`, and then `mvn dependency:tree` gives this:
``` Maven
[INFO] \- com.meilisearch.sdk:meilisearch-java:jar:0.14.4:compile
[INFO]    +- com.squareup.okhttp3:okhttp:jar:5.0.0-alpha.16:compile
```
When in reality it should resolve to `4.12.0`.
