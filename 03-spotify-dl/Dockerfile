FROM alpine:3.15.0

# python base y pip 
RUN apk add --no-cache python3 py3-pip

# paquetes baes para iniciar spotify-dl, ffmpeg es necesario para transformar a mp3
RUN pip install \
  spotify-dl \
  ffmpeg

