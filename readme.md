## Test

### require
<pre>
  - Install postgresql (or Docker)
  - Create two database rock_db (dev) rocky_db_prod (prod)
  - configure application.yaml
</pre>
### 1 - In order to create migration for dev and prod en
<pre>
 create sql file in folder src/main/resources/db/migration
</pre>
### 2 - Migration file for dev only
<pre>
    create sql file in folder src/main/resources/db/migration-dev
</pre>
### 3 - Test Dev Env
<pre>
  for dev you must do : mvn spring-boot:run
  result: two lines must be added in the table test
</pre>
### 4 - Test Prod Env
<pre>
   - mvn package
   - java -jar -Dspring.profiles.active=prod target/flyway-migration-env-0.0.1-SNAPSHOT.jar
   result : one line added in the table test
</pre>