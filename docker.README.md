# Docker Cheatsheet
## Mantainance 
### Remove
- Remove all dangling images
  - `docker rmi $(docker images --filter "dangling=true" -q)`

## Single imagg
### Run
```docker run [OPTIONS] IMAGE[:TAG|@DIGEST] [COMMAND] [ARG...]```
- How to do volumes
  -  `$(pwd)/volume:/volume` for in same folder
- Options
  - `-v`: volume
  - `-p`: publish but really port `80:80` the left is on the outside and the right is on the inside
  - `-i`: allows STDIN
  - `-t`: get a terminal
  - `--name` yep you have to type out name
