# Quick Start

This container runs tzutalin's 'labelImg' tool.

I decided to take ownership of this container image. Feel free to pull request and create issues as I plan to maintain this.

## How to use

Note that you need to provide your images path instead of `/path/to/images`.

~~~
xhost +

docker run -ti --rm \
	-e DISPLAY=$DISPLAY \
	-v /tmp/.X11-unix:/tmp/.X11-unix \
	-v /path/to/images:/images/ \
	spiridonovpolytechnic/labelimg:latest
~~~

~~~
xhost +

docker run -ti --rm \
	-e DISPLAY=$DISPLAY \
	-v /tmp/.X11-unix:/tmp/.X11-unix \
	-v $(pwd)/images:/images/ \
	spiridonovpolytechnic/labelimg:latest
~~~

## Credit

Originally the container was created by ludwigprager, but was not updated for latest labelImg. Then guysoft forked it, updated it (and pull requested back to ludwigprager who let things slip through the cracks or ignored it). Guysoft published his image on docker hub but set the entry point as the shell instead of calling labelImg. 

Originally by `ludwigprager`:
```
Credit goes to darrenl/tzutalin and his labelImg tool. Thanks to him for his effort.
However, I did not understand the docker container he provides and created this simpler version.
```