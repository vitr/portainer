# Portainer https://www.portainer.io/
Portainer simplifies Docker container management.

The fastest way to run Portainer:
```
docker volume create portainer_data
docker run -d -p 8000:8000 -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer
```

Access portainer at your localhost:

# http://localhost:9000/#/home

To update Portainer stop and remove the current image: 
```
docker stop portainer && docker rm portainer
docker pull portainer/portainer
docker run -d -p 8000:8000 -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer
```
As per now (Aug 2020) you can use native Docker Desktop UI to manage containers (to stop and delete the old portainer container).

### Windows notes
Run above commands in Windows PowerShell as Administrator.
