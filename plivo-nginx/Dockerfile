FROM debian:jessie

RUN apt-get update && apt-get install -y \
    nginx python3 && \
    python setup.py install && \ 
    pip install plivo && \
    pip install Flask

EXPOSE 80