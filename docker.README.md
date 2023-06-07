# Docker Cheatsheet
## Mantainance 
### Remove
- Remove all dangling images
  - `docker rmi $(docker images --filter "dangling=true" -q)`

## Single image
1. Build
2. Run
3. Remove
4. 1
### [Build](https://docs.docker.com/get-started/02_our_app/)
```docker build -t getting-started .```
- `-t` name
### [Run](https://docs.docker.com/engine/reference/run/)
```docker run [OPTIONS] IMAGE[:TAG|@DIGEST] [COMMAND] [ARG...]```
- How to do volumes
  -  `$(pwd)/volume:/volume` for in same folder
- Options
  - `-v`: volume
  - `-p`: publish but really port `80:80` the left is on the outside and the right is on the inside
  - `-i`: allows STDIN
  - `-t`: get a terminal
  - `--name` yep you have to type out name

## Favorite Images
- [Node](https://hub.docker.com/_/node) `node:20-alpine3.17`
