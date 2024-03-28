FROM ubuntu

WORKDIR /countapp

COPY requirements.txt /countapp
COPY devops /countapp

RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip install -r requirements.txt && \
    apt-get install -y libmysqlclient-dev 

    cd devops

ENTRYPOINT ["python3"]
CMD ["init_database.py", "runserver", "0.0.0.0:8000"]
