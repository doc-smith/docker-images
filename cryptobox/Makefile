NAME		:= drsmith/cryptobox
TAG			:= latest
IMG			:= ${NAME}:${TAG}
DOCKER_USER	:= drsmith

build:
	@docker build -t ${IMG} .

push:
	@docker push ${NAME}
 
login:
	@docker login -u ${DOCKER_USER}

run:
	@docker run -it --rm --name cryptobox ${NAME} 
