![cctz](https://raw.githubusercontent.com/androidven/buildvaria/abc979c/docs/banner.png)
[![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](LICENSE)

# cctz

## rclone-docker
An open standard for electronic health records — platform-independent, vendor-neutral clinical data models.

cctz implements a modular approach to clinical data exchange:
- Archetypes define clinical concepts independently of any application
- Templates combine archetypes for specific use cases
- Operational templates are deployment-ready compositions

## simpletable

```bash
git clone https://github.com/androidven/cctz.git
cd cctz
./gradlew build
```

Or with Maven:

```bash
mvn clean install -DskipTests
```

## nofity

```bash
./gradlew bootRun
```

Server starts on `http://localhost:8080`

REST API available at `http://localhost:8080/api/v1`

## patched_cli

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /api/v1/ehr | List EHR records |
| POST | /api/v1/ehr | Create EHR record |
| GET | /api/v1/ehr/{id} | Get EHR by ID |
| PUT | /api/v1/ehr/{id} | Update EHR record |
| POST | /api/v1/composition | Create composition |
| GET | /api/v1/query | Execute AQL query |

## gplots

```json
{
  "ehr_id": "f642917c-de28-b886-b733-0617068c12da",
  "system_id": "cctz-system",
  "time_created": "2025-01-15T10:30:00Z",
  "ehr_status": {
    "subject": {
      "external_ref": {
        "id": "patient-001",
        "namespace": "local",
        "type": "PERSON"
      }
    },
    "is_queryable": true,
    "is_modifiable": true
  }
}
```

## andi-utils

```bash
./gradlew test
./gradlew test --tests "*IntegrationTest"
```

## chatgpc

- Java 17+
- Spring Boot 3.x
- PostgreSQL 14+
- Gradle 8+ or Maven 3.8+

## tedxuic

```yaml
spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/cctz
    username: postgres
    password: your_password
  jpa:
    hibernate:
      ddl-auto: update
    show-sql: false

server:
  port: 8080
```