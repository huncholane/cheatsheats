# Docker Cheatsheet
## Removing stuff
- Remove all dangling
  - `docker rmi $(docker images --filter "dangling=true" -q)`
