FROM python:3.10-slim-buster

#Inside container
WORKDIR /backend-flask

#From outside to inside
#contains library to install
COPY requirements.txt requirements.txt

#Inside container
#install python libraries used for app
RUN pip3 install -r requirements.txt

#Outside container to inside container
#. means everything
# first . /backend-flask (outside container)
# second . /backend-flask (inside container)
COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}

CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]