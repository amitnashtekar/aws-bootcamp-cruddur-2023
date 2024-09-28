FROM python:3.10-slim-buster

WORKDIR /backend-flask

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}
# python3 -m flask run --host=0.0.0.0 --port=4567
# to create docker image
# docker build -t  backend-flask ./backend-flask
# to run docker image by setting env varibale
# docker run --rm -p 4567:4567 -it -e FRONTEND_URL='*' -e BACKEND_URL='*' backend-flask
# To run the docker yml file
# docker-compose up
# To stsrt psql
# psql -Upostgres --host localhost
#  to install all dependancies mentioned in requirement.txt
# pip install -r requirements.txtgit
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]