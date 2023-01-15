[![Build status](https://dev.azure.com/APS-SD-Stewards/APS-SD/_apis/build/status/proscrumdev.battleship-java-CI)](https://dev.azure.com/APS-SD-Stewards/APS-SD/_build/latest?definitionId=15)

# Battleship Java

A simple game of Battleship, written in Java. The purpose of this repository is to serve as an entry point into coding exercises and it was especially created for scrum.orgs Applying Professional Scrum for Software Development course (www.scrum.org/apssd). The code in this repository is unfinished by design.

# Getting started

This project requires a Java JDK 8 or higher. To prepare to work with it, pick one of these
options:

## Run locally

Run battleship with Gradle

```bash
./gradlew run --console plain
```

Execute tests with Gradle

```bash
./gradlew test
```

## Docker

If you don't want to install anything Java-related on your system, you can
run the game inside Docker instead.

### Run a Docker Container from the Image

```bash
docker run -it -v ${PWD}:/battleship -w /battleship openjdk:15 bash
```

This will run a Docker container with your battleship case study mounted into it. The container will run in interactive mode and you can execute Gradle commands from the shell (see examples below).

If you are using Docker for Windows you might run into issues and get a message like
```bash
env: ‘sh\r’: No such file or directory
```
The reason for this is that Windows uses CRLF while Linux (in the Docker Container) uses only CR
You can solve the issue by cloning the repository with a specific parameter:
```bash
git clone https://github.com/proscrumdev/battleship-java.git  --config core.autocrlf=input
```

# Launching the game

```bash
./gradlew run --console plain
```

# Running the Tests

```
./gradlew test
```
