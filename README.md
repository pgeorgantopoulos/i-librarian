followed instructions from here <https://hub.docker.com/r/cgrima/i-librarian> with

    export DATA_PATH=...

    sudo docker run -d -p 7070:80 \
            -v ${DATA_PATH}$:/app/data \
            -v /etc/localtime:/etc/localtime:ro \
            --name=i-librarian \
            --rm\
            cgrima/i-librarian


Export library or collection from **Zotero** and Import to **i-librarian**
---

Install [Better BibTex](https://retorque.re/zotero-better-bibtex/). Download latest **.xpi** released from [here](https://retorque.re/zotero-better-bibtex/#features).

Zotero > Plugins > Install from file: provide **.xpi** file

Right click on your library or collection you'd like to export

From the BetterBibTex menu > Export and download **.bib** from the generated link.

i-librarian > Import Wizard > BibTex > Local File: provide **.bib** file.

Known bugs
---

* some meta-data are not always preserved, e.g. URLs.


