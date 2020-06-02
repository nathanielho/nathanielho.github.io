One thing that never seems to be mentioned in Docker starter guides is the need to limit the log file sizes before it consumes all your hard disk space and crash the machine. This is more likely since we are running more slimmer VMs nowaways.

Find out how large your docker log files are by using this command:

`sh -c "du -ch /var/lib/docker/containers/*/*-json.log"`

## Method 1 - Enabling Log Rotation for your environment
These two articles tell you how to setup the log limits:
- [https://docs.docker.com/config/containers/logging/configure/](https://docs.docker.com/config/containers/logging/configure/)
- [https://success.docker.com/article/how-to-setup-log-rotation-post-installation](https://success.docker.com/article/how-to-setup-log-rotation-post-installation)

The important aspect is to **remove and recreate** your container to use the new log rotation rules.

## Method 2 - Enabling Log Rotation in Docker Run
If doing a docker run command you can add it in the command like this:

`docker run --log-driver json-file --log-opt max-size=10m --log-opt max-file=3 hello-world`

This will result in 3 files of 10MB max

## Method 3 - Enabling Log Rotation in Docker Compose

And if you are using docker-compose you can use this method:

  
    
    logging:
    
      driver: "json-file"
      
      options:
      
        max-size: "10m"
        
        max-file: "3" 
        
This will result in 3 files of 10MB max



Now your disks won't be filled up with logs!
