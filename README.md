## Docker notes

Docker is a popular platform for developing, shipping and running applications in containers. Here are some common Docker commands that you might find useful:

### Managing Containers:

1. **Run a Container:**
   ```
   docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
   ```
   Example:
   ```
   docker run --name nginx-new-app -p 8888:80 nginx
   ```
   in a browser open a tab and hit localhost:8888 we will see the welcome page of nginx
   ```
  localhost:8888 
  ```
2. **List Running Containers:**
   ```
   docker ps
   ```

3. **List All Containers (including stopped ones):**
   ```
   docker ps -a
   ```

4. **Stop a Running Container:**
   ```
   docker stop CONTAINER_ID
   ```

5. **Remove a Container:**
   ```
   docker rm CONTAINER_ID
   ```

6. **Remove All Stopped Containers:**
   ```
   docker container prune
   ```

1. **Run a Container in Detached Mode:**
   ```
   docker run -d IMAGE
   ```
   This runs a container in the background.

2. **Attach to a Running Container:**
   ```
   docker attach CONTAINER_ID
   ```
   This attaches your terminal to a running container.

3. **Run a Container with a Specific Name:**
   ```
   docker run --name CONTAINER_NAME IMAGE
   ```
   Assigns a specific name to the container.

4. **Run a Container with Port Mapping:**
   ```
   docker run -p HOST_PORT:CONTAINER_PORT IMAGE
   ```
  Example:
   ```
   docker run --name nginx-new-app -p 8888:80 nginx
   ```
   Maps a port on the host to a port on the container.

5. **Run a Container with Volume Mounting:**
   ```
   docker run -v HOST_PATH:CONTAINER_PATH IMAGE
   ```
   Mounts a host directory or file into the container.

6. **View Logs from a Container:**
   ```
   docker logs CONTAINER_ID
   ```
   Displays the logs from a running container

### Managing Images:

7. **List Downloaded Images:**
   ```
   docker images
   ```

8. **Download an Image:**
   ```
   docker pull IMAGE_NAME
   ```
   
9. **Remove an Image:**
   ```
   docker rmi IMAGE_NAME
   ```

10. **Remove All Unused Images:**
    ```
    docker image prune
    ```
11. **Build an Image with a Specific Dockerfile:**
   ```bash
   docker build -t IMAGE_NAME:TAG -f DOCKERFILE_PATH .
   ```
   Specifies a Dockerfile other than the default `./Dockerfile`.

12. **Tag an Existing Image:**
   ```bash
   docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]
   ```
   Assigns a new name to an image.

13. **Push an Image to a Registry:**
   ```bash
   docker push IMAGE_NAME
   ```
   Uploads the specified image to a container registry.

### Working with Dockerfile:

11. **Build an Image from a Dockerfile:**
    ```
    docker build -t IMAGE_NAME:TAG PATH_TO_DOCKERFILE
    ```
    Example:
    ```
    docker build -t myimage:latest .
    ```

### Networking:

12. **List Networks:**
    ```
    docker network ls
    ```

13. **Inspect a Network:**
    ```
    docker network inspect NETWORK_ID
    ```
14. **Create a Custom Bridge Network:**
    ```
    docker network create --driver bridge NETWORK_NAME
    ```
    Creates a custom bridge network.

15. **Connect a Container to a Network:**
    ```
    docker network connect NETWORK_NAME CONTAINER_NAME
    ```
    Connects a running container to a network.

16. **Disconnect a Container from a Network:**
    ```bash
    docker network disconnect NETWORK_NAME CONTAINER_NAME
    ```
    Disconnects a container from a network.

### Docker Compose:

14. **Run Containers Defined in a Compose File:**
    ```
    docker-compose up
    ```

15. **Stop Containers Defined in a Compose File:**
    ```
    docker-compose down
    ```

16. **Build and Run Containers with Compose:**
    ```
    docker-compose up --build
    ```

17. **Specify Docker Compose File:**
    ```
    docker-compose -f COMPOSE_FILE_PATH up
    ```
    Specifies a Docker Compose file other than the default `docker-compose.yml`.

18. **Scale Services in Docker Compose:**
    ```
    docker-compose up --scale SERVICE_NAME=NUM_INSTANCES
    ```
    Scales the number of containers for a specific service.

19. **Run a One-time Command in a Service:**
    ```
    docker-compose run SERVICE_NAME COMMAND
    ```
    Executes a one-time command in a service container.


### Cleaning Up:

10. **Remove All Containers:**
    ```bash
    docker rm $(docker ps -a -q)
    ```
    Removes all stopped containers.

11. **Remove All Images:**
    ```bash
    docker rmi $(docker images -a -q)
    ```
    Removes all images.

12. **Remove All Volumes:**
    ```bash
    docker volume prune
    ```
    Removes all unused volumes.










# template_readme
<!--markdown -->
Shashi kanta das    
by pressing   
2 times space
new line by  
horizontal line 

---

# I am shashi h1 tag
## I am shashi h2 tag
### I am shashi h3 tag
#### I am shashi h4 tag
##### I am shashi h5 tag
###### I am shashi h6 tag

<p> loremj;lkdfsg ;lj;lkj;lkj;lj;j;lj;klsljdsl;fkjl;kjsdfgj';jsdfgj';jksdfgj';jksdf'ljk';sdafksadfjk';dlfjksdjk';sdfjksdaksd;lksd;lfjasdkl;fj</p>

### italic letter 
---
_this is sample_  
### bold letter 
---
__this is sample__

### strikethrough 
---
~~this is a p sample line~~

### in line code
---
`kgjhgjh
khgjhgjh`

### multiple line code
---
```html
<html>
<title></title>
<head></head>
<body></body>
</html>
```

```css
body{
    background:green;
}
```

```javascript
console.log('Hello world);
```
### ordered list
---
1. item 1
2. item 2
3. item 3
   1. item item2 
   2. item 3

### unordered list
---
- item one
- item two
- item three
    - item 12
    - item 23
    - item45
- item 4

### task list
---
- [x] task one 
- [x] task one 
- [x] task one 
- [x] task one 

### link
---
[github link](https://github.com/shashidas95/shashi)

### image
---

![profile](./images/me.jpg)

### table
---

| name | age| email|
|-----|-----|-----|
shashi kanta das|39 |skd.bsti@gmail.com
shashi  das|36 |das.bsti@gmail.com
shashi kanta |37 |kanta.bsti@gmail.com
 kanta das|38 |kantadas.bsti@gmail.com
