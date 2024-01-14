## How to run

1. Install Docker
2. `docker-compose build`
3. `docker-compose up`
4. Open OBS and in settings set the server to `rtmp://localhost:1935/live` and the stream key to `test?key=ACP_Stream`
5. Open a browser and go to `http://localhost:3000` to view your live stream!


## Congifure Ubantu
1. sudo -s
2. apt-get update
3. apt install docker
4. apt install docker-compose
4.1 git clone https://github.com/Abdisalan/blog-code-examples.git
5. Go to folder 
6. docker-compose build
7. docker-compose up 
8. GO To OBS :
    8.1. Live stream 
    8.2. rtmp://{server}:1935/live 
9.

To show only running containers use the given command:

docker ps
To show all containers use the given command:

docker ps -a
To show the latest created container (includes all states) use the given command:

docker ps -l
To show n last created containers (includes all states) use the given command:

docker ps -n=-1
To display total file sizes use the given command:

docker ps -s

The content presented above is from docker.com.

In the new version of Docker, commands are updated, and some management commands are added:

docker container ls
It is used to list all the running containers.

docker container ls -a
And then, if you want to clean them all,

docker rm $(docker ps -aq)
It is used to list all the containers created irrespective of its state.

And to stop all the Docker containers (force)

docker rm -f $(docker ps -a -q)  