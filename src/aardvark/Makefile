# CI/ CD

IMAGE:=aardvark
PREFIX:=nearlyunique

list-goals: # default, list the goals for this makefile
	@ag '^[a-z-_]+' -s --nonumbers Makefile

build:      # build the docker image
	docker build -t ${PREFIX}/${IMAGE} .

run:        # run the docker as named container
	docker run --rm -d --name ${IMAGE} -p 5000:5000 ${PREFIX}/${IMAGE}

stop:       # stop the docker container
	docker stop ${IMAGE}
