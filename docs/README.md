# Tutorial

## 2021-02-20

```js
// Exists to contain the tutorial 'getting-started' 

// That was auto-built inside of ../jeffr
  // NOT jeffr/.docker
```

-----

Step (1)(Clone)

```js
First, clone a repository
The Getting Started project is a simple GitHub repository which contains everything you need to build an image and run it as a container.
Clone the repository by running Git in a container.
```

```cmd
docker run -- name repo alpine/git clone\ 
  https://github.com/docker/getting-started.git
docker cp repo:/git/getting-started/  .
```

console.log

- See
  
  -> `https://i.imgur.com/ZESyQQK.png`

  ![console.log (1)](https://i.imgur.com/ZESyQQK.png)

-----

Step (2)(Build)

```js
Now, build the image
A Docker image is a private file system just for your container. It provides all the files and code your container needs.
```

```cmd
cd getting-started
docker build -t docker101tutorial .
```

console.log

- See
  
  -> `https://i.imgur.com/pdoMLTM.png`

  ![console.log (2)](https://i.imgur.com/pdoMLTM.png)

-----

Step (3)(Run)

```js
Run your first container
Start a container based on the image you built in the previous step. Running a container launches your application with private resources, securely isolated from the rest of your machine.
```

```cmd
docker run -d -p 80:80 \
  --name docker-tutorial docker101tutorial
```

console.log

- See
  
  -> `https://i.imgur.com/UHemYlN.png`

  ![console.log (3)](https://i.imgur.com/UHemYlN.png)

-----

Step (4)(Share)

```js
Now save and share your image
Save and share your image on Docker Hub to enable other users to easily download and run the image on any destination machine.
See what youve saved on Hub
```

```cmd
docker tag docker101tutorial jeffreybodin/docker101tutorial
docker push jeffreybodin/docker101tutorial
```

docker/repositories

- See (1)
  
  -> "what you've saved on [Hub](https://hub.docker.com/repositories)"
  
  ![Hub (1)](https://i.imgur.com/ZTswKCo.png)

- See (2)
  
  `jeffreybodin/docker101tutorial`
  `https://hub.docker.com/repository/docker/jeffreybodin/docker101tutorial`
  
  -> [General](https://hub.docker.com/repository/docker/jeffreybodin/docker101tutorial/general)
  `https://hub.docker.com/repository/docker/jeffreybodin/docker101tutorial/general`
  ![Hub (2)](https://i.imgur.com/ogmrbhQ.png)
  
  -> [Tags](https://hub.docker.com/repository/docker/jeffreybodin/docker101tutorial/tags)
  `https://hub.docker.com/repository/docker/jeffreybodin/docker101tutorial/tags`
  ![Hub (3)](https://i.imgur.com/MbzSYAH.png)
  
  -> [Builds](https://hub.docker.com/repository/docker/jeffreybodin/docker101tutorial/builds)
  `https://hub.docker.com/repository/docker/jeffreybodin/docker101tutorial/builds`
  ![Hub (4)](https://i.imgur.com/AmCsnyp.png)
  
  -> [Collaborators](https://hub.docker.com/repository/docker/jeffreybodin/docker101tutorial/collaborators)
  `https://hub.docker.com/repository/docker/jeffreybodin/docker101tutorial/collaborators`
  ![Hub (5)](https://i.imgur.com/09UlS9k.png)
  
  -> [Webhooks](https://hub.docker.com/repository/docker/jeffreybodin/docker101tutorial/webhooks)
  `https://hub.docker.com/repository/docker/jeffreybodin/docker101tutorial/webhooks`
  ![Hub (6)](https://i.imgur.com/3KnSjMM.png)

  -> [Settings](https://hub.docker.com/repository/docker/jeffreybodin/docker101tutorial/settings)  
  `https://hub.docker.com/repository/docker/jeffreybodin/docker101tutorial/settings`
  ![Hub (7)](https://i.imgur.com/ZJInYdN.png)

console.log

- See
  
  -> `https://i.imgur.com/jbpsm7x.png`
  
  ![console.log (4)](https://i.imgur.com/jbpsm7x.png)

-----
