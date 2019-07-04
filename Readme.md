Test ratings locally
- delete database schemas
- Launch MySql
- Run config server `./gradlew bootRun`
- Run discovery server `./gradlew bootRun`
- Launch ratings API first to create tables
```
SPRING_PROFILES_ACTIVE=local java -jar target/ratings-api-0.0.1-SNAPSHOT.jar
```
- Launch ratings loader to load data (you should see COMPLETED in logs)
```
SPRING_PROFILES_ACTIVE=local java -jar target/ratings-loader-0.0.1-SNAPSHOT.jar localFilePath=classpath:data.csv
```
- access http :8081/ratings and you should have 3 results
```
SPRING_PROFILES_ACTIVE=local java -jar target/trades-loader-0.0.1-SNAPSHOT.jar localFilePath=classpath:data.csv
```



What we have
- Multiple datasources
- 

TODO
- Review all files
- Add the api call

# Note on DB's
- rating table does not grow, so no incrementing apis.  JPA creates table through API launch

