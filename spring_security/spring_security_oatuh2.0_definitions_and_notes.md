# Spring Security and OAuth 2.0
## Notes and Definitions

### JWT (JSON Web Token)
JWT è un modo per trasferire informazioni sensibili in formato JSOn.[RFC7519](https://datatracker.ietf.org/doc/html/rfc7519)

Garantisce che l'informazione contenuta sia stata effettivamente mandata da chi l'ha creato (è firmato). 

Non garantisce il criptaggio del contenuto (è un base64 facilmente leggibile, si veda ad esempio  [jwt.io](http://jwt.io))

### Opaque token
Si tratta di un token il cui contenuto non è inteso essere leggibile. Solo l'emittente (issuer) conosce il formato del token.

### Resources Server
Un  Resource Server è un'applicazione che protegge una risorsa tramite token OAuth. Questi token sono emessi da Authorization Server, indicati come emittenti (issuer).Obiettivo del Resource Server è quello di validare il token prima di servire la risorsa richiesta.

### Authorization code Flow

![./AuthCodeFlowSequenceDiagram-1.webp](AuthCodeFlowSequenceDiagram-1.webp)

### Spring Boot Starter OAuth2 Resource Server
spring-boot-starter-oauth2-resource-server è lo starter spring per il supporto alla creazione di un resource server


### Resource Server component

* Model – the resource to protect
* API – a REST controller to expose the resource
* Security Configuration – a class to define access control for the protected resource that the API exposes
* application.yml – a config file to declare properties including information about the authorization server


## Resources
* https://www.baeldung.com/spring-security-oauth-resource-server
* https://jwt.io/
* https://datatracker.ietf.org/doc/html/rfc7519