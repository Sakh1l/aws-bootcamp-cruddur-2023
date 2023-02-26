FROM python:3.10-slim-buster
# Inside Container
# make a new folder inside container
WORKDIR /backend-flask

#copy requirements.txt file Outside Container -> to Inside the Container 
#this contains the libraries to install to run the app
COPY requirements.txt requirements.txt

#Inside container 
#Install the python libraries used for the app
RUN pip3 install -r requirements.txt

#copy everything from Outside the container ->  to Inside the Container
# . means everthing in the current directory 
# first period . - /backend-flask (outside the container )
# second period . /backend-flask (inside the container )

COPY . .

# Set Environment Variables (Env Vars)
# Inside Container and will remain set when the container is running

ENV FLASK_ENV=development

EXPOSE ${PORT}

# CMD (Command)
# python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]