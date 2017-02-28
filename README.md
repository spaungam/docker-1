# Custom Jenkins Docker image for Bluemix
- `docker build -t myjenkins .`
- `docker run -p 8080:8080 -p 50000:50000 -v ~/jenkinsdata:/var/jenkins_home myjenkins`
- `docker tag myjenkins registry.ng.bluemix.net/mycontainers/myjenkins`
- `docker push registry.ng.bluemix.net/mycontainers/myjenkins`
- `cf ic images`

- `cf ic run --name myjenkins -p 8080 -m 512 registry.ng.bluemix.net/mycontainers/myjenkins`
- `cf ic ps`
- `cf ic ip list`
- `cf ic ip request`

- `cf ic ip bind 123.12.123.20 myjenkins`
- `cf ic inspect myjenkins`
- `cf ic logs myjenkins`

http://123.13.123.20:8080
