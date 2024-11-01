# GameSense.pub Loader and Cheat Engine

## Board Status
[![Board Status](https://dev.azure.com/wwwgamesensepub/85926823-5bbc-4a97-87aa-78e79db23598/1043a6c1-41d4-435f-8291-997110805037/_apis/work/boardbadge/f2ef5ef6-ce58-4b4a-bfbf-b8a7373f3069)](https://dev.azure.com/wwwgamesensepub/85926823-5bbc-4a97-87aa-78e79db23598/_boards/board/t/1043a6c1-41d4-435f-8291-997110805037/Microsoft.RequirementCategory)

> **_NOTE:_** This site is live at `https://h4xr0x.cc` and `https://discord.gg/EYCBURUPcm`.

## Project Overview
### Application Details
- **GroupId:** `gamesense.org.acme`
- **ArtifactId:** `gs`
- **Version:** `1.0.0-SNAPSHOT`
- **Quarkus Version:** `2.3.0.Final`

### Description
This project uses Quarkus, the Supersonic Subatomic Java Framework. It includes a cracked loader, cheat engine, and scripting CLI for GameSense.pub.

## Prerequisites
1. **Install WSL2:** [WSL2 Tutorial](https://ubuntu.com/tutorials/working-with-visual-studio-code-on-ubuntu-on-wsl2#1-overview)
2. **Install Ubuntu 20.04:** [Ubuntu 20.04 LTS](https://apps.microsoft.com/store/detail/ubuntu-20044-lts/9MTTCL66CPXJ)
3. **Install NodeJS:** [NodeJS Tutorial](https://ubuntu.com/tutorials/working-with-visual-studio-code-on-ubuntu-on-wsl2#5-install-nodejs-and-create-a-new-project)
4. **Install SDKMAN:**
  ```sh
  curl -s "https://get.sdkman.io" | bash
  ```
5. **Install Required Tools:**
  ```sh
  sdk install maven
  sdk install spring-boot
  sudo apt-get install openjdk-11-jdk
  sdk list java
  sdk install quarkus
  ```
6. **Install Visual Studio Code:** [VS Code](https://code.visualstudio.com/)
7. **Install Remote Development Extension:** [Remote Development Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)
8. **Install Docker Desktop:** [Docker Desktop](https://docs.docker.com/desktop/install/windows-install/)

## Running the Application in Dev Mode
Run your application in dev mode with live coding enabled:
```sh
./mvnw compile quarkus:dev
```
> **_NOTE:_** Quarkus Dev UI is available in dev mode at [http://localhost:8080/q/dev/](http://localhost:8080/q/dev/).

## Packaging and Running the Application
Package the application:
```sh
./mvnw package
```
Run the application:
```sh
java -jar target/quarkus-app/quarkus-run.jar
```
Build an _über-jar_:
```sh
./mvnw package -Dquarkus.package.type=uber-jar
```
Run the _über-jar_:
```sh
java -jar target/*-runner.jar
```

## Creating a Native Executable
Create a native executable:
```sh
./mvnw package -Pnative
```
Or use a container:
```sh
./mvnw package -Pnative -Dquarkus.native.container-build=true
```
Run the native executable:
```sh
./target/gs-1.0.0-SNAPSHOT-runner
```
For more details, visit [Quarkus Maven Tooling Guide](https://quarkus.io/guides/maven-tooling.html).

## Related Guides
- **YAML Configuration:** [Guide](https://quarkus.io/guides/config#yaml)
- **Quarkus Extension for Spring Web API:** [Guide](https://quarkus.io/guides/spring-web)

## Provided Code
### YAML Config
Configure your application with YAML. The configuration is located in `src/main/resources/application.yml`.

### Spring Web
Start your RESTful Web Services with a Spring Controller. The configuration is located in `src/main/resources/application.yml`.

## About GameSense
- **Steam Group Administrators:** NmChris and Wish
- **Steam Group Moderators:** Beta Users Only
- **Steam Group:** [Gamesensical](https://steamcommunity.com/groups/gamesensical)
- **Documentation:** [Gamesensical Docs](https://gamesensical.gitbook.io/docs/)

## Building the GameSense.pub Loader
### Environment Setup
1. **Install SDKMAN:**
  ```sh
  curl -s "https://get.sdkman.io" | bash
  ```
2. **Install Required Tools:**
  ```sh
  sdk install maven
  sdk install spring-boot
  sudo apt-get install openjdk-11-jdk
  sdk list java
  sdk install quarkus
  ```
3. **Install Visual Studio Code:** [VS Code](https://code.visualstudio.com/)
4. **Install Remote Development Extension:** [Remote Development Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)
5. **Install Docker Desktop:** [Docker Desktop](https://docs.docker.com/desktop/install/windows-install/)

### Install NodeJS
```sh
sudo apt update
sudo apt upgrade
sudo apt-get install nodejs
sudo apt install npm
```

### Create a New Folder for the Server
```sh
mkdir server/
cd server/
```

### Open the Folder in Visual Studio Code
```sh
code .
```

### Install OpenSSH Server on Ubuntu 20.04
1. **Install Remote SSH Extension:** [Remote SSH Extension](https://code.visualstudio.com/docs/remote/ssh-tutorial)
2. **Update Packages:**
  ```sh
  sudo apt-get update
  sudo apt-get upgrade
  ```
3. **Install OpenSSH:**
  ```sh
  sudo apt-get install openssh-server
  ```

### Create an SSH Key
```sh
ssh-keygen -t ed25519
```

### Enable SSH Traffic on Firewall
```sh
sudo ufw allow ssh
sudo ufw status
sudo ufw enable
sudo ufw reset
```

### Enable SSH Server on System Boot
```sh
sudo systemctl enable ssh
sudo systemctl restart sshd
sudo systemctl status sshd
```

### Enable Port 8080 for the API
```sh
netstat -tulpn | grep 8080
```

### Connect to SSH Server
```sh
ssh -p <port> <username>@<ip_address>
```

### Disable SSH Server
```sh
sudo systemctl stop sshd
sudo systemctl status sshd
```

## Fork the Repo and Load the Project in Visual Studio Code
### Create the Hello World Quarkus App
```sh
mvn io.quarkus.platform:quarkus-maven-plugin:2.12.0.Final:create \
  -DprojectGroupId=gamesense.org.acme \
  -DprojectArtifactId=gs
```

### Run the Application
```sh
./mvnw quarkus:dev
```

### Request the Provided Endpoint
```sh
curl -w "\n" http://localhost:8080/hello
```

## Using Injection
### Restart the Application
```sh
./mvnw quarkus:dev
```

### Check the Endpoint
```sh
curl -w "\n" http://localhost:8080/hello/greeting/quarkus
```

## Package and Run the Application
```sh
./mvnw quarkus:dev
```
Open your browser to [http://localhost:8080/greeting](http://localhost:8080/greeting).

## Run the Application as a Native Executable
### Prerequisites
1. **Install Podman and Docker:**
  ```sh
  sudo apt install podman podman-docker docker-compose
  ```
2. **Enable Podman Socket:**
  ```sh
  systemctl --user enable podman.socket --now
  ```
3. **Set Environment Variables:**
  ```sh
  export DOCKER_HOST=unix:///run/user/${UID}/podman/podman.sock
  ```

### Build the Native Executable
```sh
./mvnw package -Pnative
```

### Using the Builder Image on Windows with Docker Desktop
```sh
powershell -c "Invoke-WebRequest -OutFile quarkus.zip -Uri https://code.quarkus.io/d?e=io.quarkus:quarkus-resteasy-reactive"
powershell -c "Expand-Archive -Path quarkus.zip -DestinationPath . -Force"
cd code-with-quarkus
mvnw package -Pnative -Dquarkus.native.container-build=true -Dquarkus.native.builder-image=quay.io/quarkus/ubi-quarkus-mandrel:22.2.0.0-Final-java17
docker build -f src/main/docker/Dockerfile.native -t my-quarkus-mandrel-app .
docker run -i --rm -p 8080:8080 my-quarkus-mandrel-app
```

### Add OpenAPI and Swagger-UI Extension
```sh
./mvnw quarkus:add-extension -Dextensions="io.quarkus:quarkus-smallrye-openapi"
```

### Generate OpenAPI Schema Document
```sh
curl http://localhost:8080/q/openapi
```

### If Successful
You can now open `launcher.exe` and use the GameSense cheat.

### If Unsuccessful
Join [GameSense Cloud](https://gamesense.cloud) and get a FREE API key with the registration of your account.

## Original Source
[GameSense Cloud](https://github.com/h4xrOx/gamesense.cloud/tree/main/demo/gs)
