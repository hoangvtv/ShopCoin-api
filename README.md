# ShopCoin-api
Springboot, JWT



# Steps to Setup
## Server Properties
server.port= 8081
server.compression.enabled=true

## Spring DATASOURCE (DataSourceAutoConfiguration & DataSourceProperties)
spring.datasource.url= jdbc:mysql://localhost:3306/{{DATABASE__NAME}}?useSSL=false&serverTimezone=UTC&useLegacyDatetimeCode=false
spring.datasource.username= {{USER_NAME}}
spring.datasource.password= {{PASS_WORD}}


## Hibernate Properties
# The SQL dialect makes Hibernate generate better SQL for the chosen database
spring.jpa.properties.hibernate.dialect = org.hibernate.dialect.MySQL5InnoDBDialect
spring.jpa.hibernate.ddl-auto = update

## Hibernate Logging
logging.level.org.hibernate.SQL= DEBUG

# Initialize the datasource with available DDL and DML scripts
spring.datasource.initialization-mode=always
spring.jpa.defer-datasource-initialization= true

## Jackson Properties
spring.jackson.serialization.WRITE_DATES_AS_TIMESTAMPS= false
spring.jackson.time-zone= UTC

## App Properties
app.jwtSecret= 9a02115a835ee03d5fb83cd8a468ea33e4090aaaec87f53c9fa54512bbef4db8dc656c82a315fa0c785c08b0134716b81ddcd0153d2a7556f2e154912cf5675f
app.jwtExpirationInMs = 604800000

# Comma separated list of allowed origins
app.cors.allowedOrigins = http://localhost:3000

## Spring Profiles
# spring.profiles.active=prod
