### If you want to run Docker as a non-root user, then you need to add your user to the docker group.

Create the docker group if it does not exist:
```
sudo groupadd docker
```
Add your user to the docker group:
```
sudo usermod -aG docker $USER
```
Log in to the new docker group (to avoid having to log out and log in again; but if not enough, try to reboot):
```
newgrp docker
```
Check if Docker can be run without root:
```
docker run hello-world
```
Reboot if you still get an error:
```
reboot
```

### Apply certificates (.crt)
C | A
-|-
sudo cp *.crt /usr/local/share/ca-certificates/ | Copy certificates
sudo update-ca-certificates | Update certificates
sudo systemctl daemon-reload | restart docker daemon
sudo systemctl restart docker | restart docker service
sudo docker login ... | login to docker server