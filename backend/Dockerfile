# pull official base image
FROM python:3.10-alpine

# set work directory
WORKDIR /code

# set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# copy requirements file
COPY app/requirements.txt /code/requirements.txt
# install python dependencies
RUN pip install --upgrade pip
# install dependencies
RUN pip install --no-cache-dir --upgrade -r /code/requirements.txt

# copy project
COPY /app /code/app

#CMD ["uvicorn", "code.app.main:app", "--host", "0.0.0.0", "--port", "80"]