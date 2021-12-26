### Spotify-dl 

Descargar musica para mi viejo a través de spotify-list, internamente utiliza youtube-dl 

paquetes necesarios 

- spotify-dl
- ffmpeg 


### Variables de entorno 

export SPOTIPY_CLIENT_ID=''

export SPOTIPY_CLIENT_SECRET=''

### Ejecución 

```docker build  -t spotifydl```

```mkdir mp3```

```docker run --name mp3 -it -v $PWD:/tmp -d spotifydl```


:wq! 