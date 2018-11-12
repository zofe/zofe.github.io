# appunti docker

## requisiti per creare ambienti docker adatti allo sviluppo

- installare docker da: https://www.docker.com/
- creare un Dockerfile all'interno del progetto 

Dockerfile di esempio, prende una distro (lamp minimale basata su alpine-linux), installa pacchetti..  
configura variabili d'ambiente, copia file di configurazione, apre porte

```

    FROM janes/alpine-lamp
    RUN apk add --update nano git && rm /var/cache/apk/*
    ENV LOCAL true
    COPY httpd.conf /etc/apache2/httpd.conf
    COPY php.ini /etc/php5/php.ini
    EXPOSE 80
    EXPOSE 3306
    
```

- comandi principali docker cli

```
$ docker build -t abcsalute . (crea l'immagine "abcsalute", usando il Dockerfile della directory corrente)
$ docker run -p 8070:80 -v ${PWD}:/www -d --name abc-container abcsalute (crea il container "abcsalute-container"
usando l'immagine "abcsalute", mappando la porta 8070 sulla 80 del container, montando la directory corrente in /www)

$ docker container start abcsalute-container
$ docker image ls (elenco delle immagini)
$ docker ps  (elenco dei container )
$ docker rm 291 -f (spegne e rimuove il container con id che comincia per 291)
$ docker rmi 41e (rimuove l'immagine che comincia per 41e)
$ docker exec -it abc-container ash (entra nella shell di un container)
```

### note

"stai" attenzione ai permessi della macchina host:  
 anche se il "volume" viene montato con l'utente root nel container, se ci sono cartelle non scrivibili sulla macchina host (in cui l'applicazione tenta di scrivere.. log, cache ecc..) 