FROM ubuntu

WORKDIR /app

COPY requirements.txt /app
COPY devops /app

RUN apt update && \
    apt install -y python3 python3-pip --break-system-packages && \
    pip install -r requirements.txt --break-system-packages && \
    cd devops

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




