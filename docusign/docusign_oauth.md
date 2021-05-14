Docusign OAuth
==============
## note e appunti su Docusign
### Percorso di test
**Obiettivo**: riuscire a fare un upload di un envelope con un documento e un template. L'upload deve essere fatto con un utente applicativo, quindi grant type JWT (come lo chiama Docusign, ovvero un Authorization Code a partire dall'access code già ricevuto :-\ poco chiaro questo punto)

**History**
- 2021-05-13 16:59:14 - Avvio AuthorizationServerApp embedded. \
See [Keycloak Embedded in Spring boot app](https://www.baeldung.com/keycloak-embedded-in-spring-boot-app) \
Configurato application.yml come segue 

    ```yml
    server:
    port: 8083

    spring:
    datasource:
        username: sa
        url: jdbc:h2:mem:testdb

    keycloak:
    server:
        contextPath: /auth
        adminUser:
        username: admin
        password: admin
        realmImportFile: fcg-realm.json

    ```
... 

- [2021-05-13 19:25:32] abbandonata questa via
 il programma di keycloak embedded ha diversi problemi se voglio modificare il file json di import del realm

 Altra via utilizzato docker-compose vedi progetto [keycloak_dockercompose](https://github.com/albertorugnone/keycloak_dockercompose.git)

2021-05-14 10:31:24 
## Resources
- [OAuth an introduction](https://developers.docusign.com/platform/auth/)
- [Get an access token with JWT authentication](https://www.youtube.com/watch?v=ebwN2HWpDQA&t=316s)