# dev.simpubs.org dockerfile README

setup from https://www.ericjstauffer.com/blog/set-up-local-grav-environment-with-docker-step-by-step-guide  
downloaded from https://getgrav.org/download/skeletons/blog-site/2.0.0 

UID & GID fix from https://www.reddit.com/r/docker/comments/q72gyx/how_to_handle_permissions_for_apache_in_docker/

run  
`$ sudo docker-compose build`  
and  
`$ sudo UID=${UID} GID=${GID} docker-compose up -d`