
**INDICE**

- [Note generali su Gradle](#note-generali-su-gradle)
  - [Per iniziare](#per-iniziare)
    - [Scopes](#scopes)
    - [Plugins](#plugins)
  - [References](#references)


# Note generali su Gradle
## Per iniziare

  - 
### Scopes
Anche in gradle come in Maven ci sono gli scoper per le dipendenze. Qui alcune corrispondenze

runtime -> runtimOnly
compileOnly -> provided

### Plugins
Qui un esempio tipico di applicazione di plugin per spring boot

```groovy

    plugins {
        id 'org.springframework.boot' version '2.4.5'
        id 'io.spring.dependency-management' version '1.0.11.RELEASE'
        id 'java'
    }

```

## References
* https://docs.gradle.org/current/userguide/declaring_dependencies.html
* https://stackoverflow.com/questions/30731084/provided-dependency-in-gradle
* https://docs.spring.io/spring-boot/docs/2.4.5/gradle-plugin/reference/htmlsingle/
* https://docs.gradle.org/current/userguide/plugins.html