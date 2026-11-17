# Environment Setup

## 1. Pulling the Docker Image

### Objective

Download the Docker image required to prepare the Linux Essentials lab environment.

### Command Executed

```bash
docker pull marialazaradev/linux-essentials:latest
```

### Command Explanation

The `docker pull` command downloads a Docker image from a container registry to the local machine.

- `docker pull`: downloads the image.
- `marialazaradev`: image namespace.
- `linux-essentials`: image repository.
- `latest`: image tag.

### Results

The image was successfully downloaded from Docker Hub.

The terminal confirmed:

- All image layers were downloaded successfully.
- The image digest was generated and displayed.
- Docker reported that a newer image had been downloaded.

### Evidence

<img width="1415" height="933" alt="image" src="https://github.com/user-attachments/assets/eaa771dd-788a-4122-86c8-000b92158f75" />


### Key Learning

Docker images are composed of multiple layers. These layers are used to package application dependencies and the environment required to run containers.

## 2. Creating and Starting the Docker Container

### Objective

Create and start an interactive Docker container using the previously downloaded Linux Essentials image.

### Command Executed

```bash
docker run -it --name devops-investigation marialazaradev/linux-essentials:latest
```

### Command Explanation

- `docker run`: creates and starts a new container.
- `-i`: keeps standard input open.
- `-t`: allocates a pseudo-terminal.
- `--name`: assigns a custom name to the container.
- `devops-investigation`: container name.
- `marialazaradev/linux-essentials:latest`: Docker image used.

### Results

The container started successfully.

The initialization output confirmed:

- The `billing-api` application was started in the background.
- The application process was assigned PID `8`.
- An interactive Linux shell became available.

### Environment Information

| Attribute | Value |
|---|---|
| Container | devops-investigation |
| Linux hostname | prod-web-01 |
| Current user | devops |
| Working directory | /srv/app |
| Application | billing-api |
| Application PID | 8 |

### Key Learning

Docker containers provide isolated execution environments for applications.

The `docker run` command creates and starts a container from an image, while the `-it` flags allow interactive terminal access.

### Evidence

<img width="1415" height="933" alt="image" src="https://github.com/user-attachments/assets/dc5ba3b5-bed9-40c0-ab70-ab36e9a33b78" />
