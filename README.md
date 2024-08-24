
## Para iniciar a imagem !
docker build -t moul/icecast
docker run -p 8000:8000 moul/icecast

 
Docker-compose

```
 yaml
icecast:
  image: moul/icecast
  volumes:
  - logs:/var/log/icecast2
  - /etc/localtime:/etc/localtime:ro
  environment:
  - ICECAST_SOURCE_PASSWORD=aaa
  - ICECAST_ADMIN_PASSWORD=bbb
  - ICECAST_PASSWORD=ccc
  - ICECAST_RELAY_PASSWORD=ddd
  - ICECAST_HOSTNAME=noise.example.com
  ports:
  - 8000:8000
```

Link Video 
https://www.youtube.com/watch?v=-mUsdHLSxYA


