# config-server
Demo cloud config server - spring micro service
Demo ConfigServer từ GitHub
Gồm 3 file
	- Application.properties ( chứa thông tin config mặc định)
	Sample.properties1=…
	Sample.properties2=…
	- Config-client-prod.properties ( chứa thông tin config cho ứng dụng có tên là config-client và triển khai trên production)
	Sample.properties1=…
	Sample.properties2=…
	- Config-client.properties ( chứa thông tin config cho ứng dụng có tên à config-client)
	Sample.properties1=…
	Sample.properties2=…
----
Tao springboot : configServer
	- Add Dependency: Actuator, configServer, Eureka Discovery Client.
	- ConfigserverApplication.java ( @EnabledDiscoveryServer, @EnabledConfigServer)
	- Application.properties:
	Spring.application.name=configserver
	Server.port=8888
	Eureka.client.service-url.defaultZone= http://localhost:8761/eureka/
	Spring.cloud.config-server-git.url= …..( địa chỉ url github)
	Spring.cloud.config.server.git.default-label=main ( brand đang sử dụng trên github)
Run đọc thông tin câu hinh. Localhost:8888/service-name/default![image](https://user-images.githubusercontent.com/51884047/185036399-bd79f67d-2b59-4bdd-99c1-31493ecbb230.png)
