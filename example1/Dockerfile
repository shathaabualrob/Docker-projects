# You need 3 things: Docker file, D Image, D container
# A docker file is a blueprint for building images.
# A docker image is a template for running containers.
# A docker container is the running process with your application in it.
# First we need to specify a base image
FROM  python:3.9
# Then, we add our file into the container. We get the main.py file and add it to . which is the base folder in our container
ADD main.py .
# After that, we need to install our third party libraries. Exactly like you would enter it into a terminal.
RUN pip install requests beautifulsoup4
# Finally, add the command that will be executed when the container is started
# We need to write: python main.py to run the app but this here needs to be represented as a comma seperated list:
CMD [ "python", "./main.py" ]
# Now you can build a docker image using the command: "docker build -t python-imdb ." in the temrinal
# this command will create a docker image with a (-t) tag or a name of python-imdb and it will be located in the current dir
# now you can run this image using the command:"docker run python-imdb"

# CASE 2
# If you commented the break in line 38 you will need to enter a user input into that container in order for it to continue
# i need to create a new image after editing the main.py file
# then i need to use the following command: "docker run -i -t python-imdb"
# thos will allow the docker container to (-i) interact with the user and take an input using the (-t) terminal 

