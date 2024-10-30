# Honeypot
# Hi there,
# make honeypot 
# work as virtual machine
# use docker image
# integrate AI model 


# This is docker containered Project
First Install the docker in your system and all the requirement  for install (window, macos, linux)
after this open project in terminal 
and there is makeFile in project you have to run it like

make honeypot.start

actually make command will run all command which build our project like command 


————

DOCKER_COMPOSE := $(shell which docker-compose)

ifeq (${DOCKER_COMPOSE},)
DOCKER_COMPOSE = docker compose
endif

.PHONY: honeypot.start
honeypot.start:
	${DOCKER_COMPOSE} build;
	${DOCKER_COMPOSE} up -d;

.PHONY: honeypot.stop
honeypot.stop:
	${DOCKER_COMPOSE} down;

.PHONY: test.unit
test.unit:
	go test ./...

-------


after this i will be run and 

then you can use honetpot local using docker 
Docker can be used using docker cli or docker desktop 

And then you can do want you want with project ()
