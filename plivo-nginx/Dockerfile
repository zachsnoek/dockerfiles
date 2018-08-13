FROM debian:jessie

RUN apt-get update && apt-get install -y \
    wget nginx python python3 && \
    python setup.py install && \ 
    pip install plivo && \
    pip install Flask

RUN wget https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-arm.zip && \
    unzip ngrok-stable-linux-arm.zip && \
    mv ngrok /usr/bin && \
    rm ngrok-stable-linux-arm.zip

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]