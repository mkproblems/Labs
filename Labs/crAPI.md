Intentionally vulnerable web app focused on the OWASP Top 10 API Vulns.

https://github.com/OWASP/crAPI

Stop all containers:
```bash
docker stop $(docker ps -a -q)
```
Removing all Containers:
```bash
docker rm $(docker ps -a -q)
```

Start crAPI:
```bash
docker-compose -f docker-compose.yml --compatibility up -d
```
![](Pasted%20image%2020250208184452.png)


To Connect:
```
localhost:8888
```
