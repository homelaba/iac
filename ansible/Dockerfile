FROM python:3.12.1-slim 

RUN apt update && apt upgrade -y
RUN pip install --upgrade pip && pip install ansible proxmoxer requests
RUN apt install sshpass -y

WORKDIR /ansible