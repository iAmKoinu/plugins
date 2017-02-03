# FileBot Docker

FileBot docker images for filebot and filebot-node.


## filebot

`docker run -it -v $PWD:/volume1 -v data:/data rednoah/filebot -script fn:sysinfo`

* `filebot` [Dockerfile](https://github.com/filebot/plugins/blob/master/docker/Dockerfile)


## filebot-node

`docker run -it -v $PWD:/volume1 -v data:/data -p 5452:5452 rednoah/filebot:node`

Once the [FileBot Node Service](https://github.com/filebot/filebot-node) is running, you can access the  web interface via [http://localhost:5452/filebot/](http://localhost:5452/filebot/).

* `filebot-node` [Dockerfile.node](https://github.com/filebot/plugins/blob/master/docker/Dockerfile.node)


## filebot-watcher

`docker run -it -v $PWD:/volume1 -v data:/data rednoah/filebot:watcher /volume1/input --output /volume1/output`

The first argument `$1` is the watch folder. The remaining arguments are [amc script](https://www.filebot.net/forums/viewtopic.php?f=4&t=215) options.

* `filebot-watcher` [Dockerfile.watcher](https://github.com/filebot/plugins/blob/master/docker/Dockerfile.watcher)