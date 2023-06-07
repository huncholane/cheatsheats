# Docker Cheatsheet
## Removing stuff
- Remove all dangling images
  - `docker rmi $(docker images --filter "dangling=true" -q)`
## Run
- How to do volumes
  -  `$(pwd)/volume:/volume` for in same folder
- Flags
  - `v`: volume
  - `p`: publish but really port `80:80` the left is on the outside and the right is on the inside
  - `i`: allows STDIN
  - `t`: get a terminal
