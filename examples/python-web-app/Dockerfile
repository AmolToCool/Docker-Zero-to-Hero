FROM ubuntu

WORKDIR /app

COPY requirements.txt /app
COPY devops /app

RUN apt update && \
    sudo apt install python3-venv && \
    python3 -m venv .venv && \
    source .venv/bin/activate && \
    apt install -y python3 python3-pip && \
    pip install -r requirements.txt && \
    cd devops

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




