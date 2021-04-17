#our base image
FROM quay.io/libpod/alpine

#install python and pip
RUN apk add --update py2-pip

#install python modules needed by our application
COPY requirements.txt /usr/src/app/
RUN pip install --no-cache-dir -r /usr/src/app/requirements.txt

#copy files of our application
COPY app.py /usr/src/app/
COPY templates/index.html /usr/src/app/templates/

#port number the container should expose
EXPOSE 5000

#run!
CMD ["python", "/usr/src/app/app.py"]
