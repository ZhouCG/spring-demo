# logback+elk+redis
## This is about how to use docker build elk+redis

1. Copy the logback-spring.xml file to your app/resource/
2. Add the follows content to your application.yml or application.properties:
```properties
spring.profiles.active=dev
spring.application.name=serviceaccount
logging.path=/XXXXXXXX/XXXX/
```

3. Add one env to your PC, like: 
```Bash
export ELK_DIR=/Users/XXX/docker_es_redis
```
4. Go to the directory where the docker-compose.yml exist, then run 
```Bash
docker-compose up -d
```
5. Check the logs by enter: 
```Bash
docker-compose logs -f
```
6. Go to the browser, visit localhost:5601
7. Select dev tools at the left Tab, type command: GET _search and click the [>]button to search all the data.