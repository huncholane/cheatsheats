## Remove all dangling images

docker rmi $(docker images --filter "dangling=true" -q)
