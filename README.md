# git-maven-build-docker

Repository that helps in creating a docker image which will clone the github repo using token based authentication.
This contains Dockerfile and other files that helps in configuring the Maven tool inside the container


run the "docker build -t gitdocker ."
start the container using "docker run -it --rm --name my-maven-project -v "$PWD":/tmp gitdocker mvn clean install package"

In the application SampleTest that we clone in the Docker file, i added the maven plugin to generate the last war file in the 
/tmp location. During the docker start container , we will attach the current directory as a volume to the container on /tmp
location. this way the generated war file will be in our current working directory.
