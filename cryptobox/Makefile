NAME		:= drsmith/cryptobox
TAG			:= $$(git log -1 --pretty=%H)
IMG			:= ${NAME}:${TAG}
LATEST		:= ${NAME}:latest
DOCKER_USER	:= drsmith

build:
	@docker build -t ${IMG} .
	@docker tag ${IMG} ${LATEST}

push:
	@docker push ${NAME}
 
login:
	@docker login -u ${DOCKER_USER}

run:
	@docker run -it --rm --name cryptobox ${NAME} 
