followed instructions from here <https://hub.docker.com/r/cgrima/i-librarian> with

    export DATA_PATH=...

    sudo docker run -d -p 7070:80 \
            -v ${DATA_PATH}$:/app/data \
            -v /etc/localtime:/etc/localtime:ro \
            --name=i-librarian \
            --rm\
            cgrima/i-librarian
