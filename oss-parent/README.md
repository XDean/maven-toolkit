# OSS Parent
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.github.XDean/oss-parent/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.github.XDean/oss-parent)

Sonatype Deploy Parent

# Usage

1. add `<parent>`, `<url>` and `<scm>` into your pom.

```xml
  <parent>
    <groupId>com.github.XDean</groupId>
    <artifactId>oss-parent</artifactId>
    <version>1.0</version>
  </parent>
  
  <url>${repository.url}</url>
  
  <scm>
    <connection>scm:${scm.url}</connection>
    <developerConnection>scm:${scm.url}</developerConnection>
    <url>${scm.url}</url>
  </scm>

```

2. use `deploy -P release to deploy to sonatype`
3. use `-P jacoco` to do code coverage

# Default Properties

```
    <user.name>XDean</user.name>
    <user.email>373216024@qq.com</user.email>
    <user.domain>https://github.com</user.domain>
    <user.url>${user.domain}/${user.name}</user.url>
    <user.timezone>8</user.timezone>
    
    <repository.name>${project.artifactId}</repository.name>
    <repository.url>${user.url}/${repository.name}</repository.url>
    
    <scm.domain>git@github.com</scm.domain>
    <scm.url>${scm.domain}:${user.name}/${repository.name}.git</scm.url>
```