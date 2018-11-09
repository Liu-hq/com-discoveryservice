注册中心
================
        discoveryservices对外提供的注册服务,主要各服务的服务发现，端口8052
```        
java -jar D:\git-crm\com-nscrm-discoveryservice\build\libs\com-nscrm-discoveryservice-1.0-SNAPSHOT.jar --spring.profiles.active=test     
```
## 服务注册
* client<br>
    在各服务的配置文件里配置如下信息，向注册中心建立链接、心跳、服务注册；  
```
    eureka:
      instance:
        preferIpAddress: true
      client:
        serviceUrl:
          defaultZone: "http://localhost:8051/eureka"
```  
* gradle依赖<br>

```
    compile group: 'org.springframework.cloud', name: 'spring-cloud-starter-eureka', version: '1.4.5.RELEASE'
```  
