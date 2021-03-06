# Docker images for PIMATIC
Docker container to run [PIMATIC](https://pimatic.org).

I designed this image to run on a Synology Disk Station but it should run just fine in any other Docker environment.

## Pull the image
```docker pull petschni/pimatic```

## Run the container
The image uses a  ```config file ``` file that is located outside of the docker container. You can either use one from your local installation or the standard one.

Note: The name of the config file must be ```config-json-pimatic.json```

Use the following  ```run ``` command to run the container:

```docker run -it -p YOUR_PORT:PIMATIC_PORT -v  FOLDER_OF_CONFIG_FILE:/home/pimatic-app/configMount/ IMAGE_NAME ```

e.g.

 ```docker run -it -p 80:80 -v  ~/Documents/pimatic-app/:/home/pimatic-app/configMount/ dee4e2336b1236 ```

This will start the container and the pimatic service.

[Detailed instructions](http://www.grauvoegel.de/2017/02/10/home-automation-with-pimatic-and-docker-on-my-synology/) for running pimatic on a Synology Disk Station can be [found on my blog](http://www.grauvoegel.de/2017/02/10/home-automation-with-pimatic-and-docker-on-my-synology/). 
