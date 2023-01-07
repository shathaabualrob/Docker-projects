# import the same base image as before
FROM python:3.9
# create a another dir in the base dir of the container 
WORKDIR  /code
# copy and install all our requirments from the virtual evniroment
# In the terminal: "pip freeze > requirments.txt". This will put all the dependencies that we've installed in a file
# now i must copy all the requierments
COPY ./requierments.txt /code/requierments.txt
# Now run this container
RUN pip install --no-cache-dir --upgrade -r /code/requierments.txt
# --no-cache-dir: This is specifi to the PIP INSTALL command will tell the pip to not use a cache which allows the docker cache to work better, it saves a lot of time when re-building an image
# now we need to copy our app into /code dir in docker container
COPY ./app /code/app
# Now i need to run this command: "uvicorn app.main:app"
CMD ["uvicorn","app.main:app","--host","0.0.0.0", "--port", "80"]
# create the .dockerignore file
# Now build the image using the command: "docker build -t fastapi-tutorial ." in the terminal which will creae an image in the root dir


