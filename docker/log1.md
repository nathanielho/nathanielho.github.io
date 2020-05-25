One thing that never seems to be mentioned in Docker starter guides is the need to limit the log file sizes before it consumes all your hard disk space and crash the machine. This is more likely since we are running more slimmer VMs nowaways.

These two articles tell you how to do it.
https://docs.docker.com/config/containers/logging/configure/
https://success.docker.com/article/how-to-setup-log-rotation-post-installation

The important aspect is to remove and recreate your container to use the new log rotation rules.
