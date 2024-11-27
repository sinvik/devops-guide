* Start Docker Deamon
	1. ```sudo dockerd --iptables=False```
	2. ```docker info```
	3. ```sudo systemctl start docker # To start docker deamon on "systemd"```
<br><br>

* List down docker images in System:
	1. ```docker images```
	2. ```docker imgages | wc -l  # To get the count of images```
<br><br>

* Remove Container:
	1. ```docker rm <container-id>```
	2. ```docker rm <container-name>```
	3. ```docker rm <conainer1> <container2> # To remove multiple container```
	4. ```docker rm $(docker ps -a -q -f status=exited)```
	5. ```docker rm -f <container-id> # To forcefully removing container.```
<br><br>

* Remove Image:
	1. ```docker rmi <image-id>```
	2. ```docker rmi $(docker images -q)```
	3. ```docker rmi -f <image-id> # Forcefully removing image```
<br><br>

* Build docker image from docker file and push to docker-hub:
	1. ```docker login -u your_userid -p your_passwd```
	2. ```docker build -t userid/repository:<tag>```
	3. ```docker push userid/repository:<tag>```
<br><br>

* Docker Handy Commands:
	1. ```docker run <image_name> # Run Container From Image```
	2. ```docker start <container-id> # Start an existing stopped container```
	3. ```docker restart <container-id> # Restart the container which is running```
	4. ```docker stop <container-id>```
	5. ```docker ps # List all running container```
	6. ```docker ps -a # List all container running/ stopped```
<br><br>

* Deploy:
  * Flask App:<br>
    ```pip freeze > requirements.txt```
    * Create Dockerfile:
		```bash
		FROM python:3.8
		WORKDIR /app
		COPY requirements.txt requirements.txt
		RUN pip install -r requirements.txt
		COPY . .
		CMD ["python", "app.py"]
		```
  
  * NGINX App:
