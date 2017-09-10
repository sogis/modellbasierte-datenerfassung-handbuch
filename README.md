# modellbasierte-datenerfassung-handbuch
Sphinx documentation repository für das Handbuch "modellbasierte Datenerfassung"

## System Requirements

* Docker
* git

## General usage

Clone this repository:

```
git clone https://github.com/sogis/modellbasierte-datenerfassung-handbuch.git $HOME/Projekte/modellbasierte-datenerfassung-handbuch
```

Start the Docker Container:

```
docker run -it -v $HOME/Projekte/modellbasierte-datenerfassung-handbuch:/documents/ sogis/docker-sphinx
``` 

This will take some time for the first time since it will download the whole docker image. You will be logged in into the running docker container. The terminal changes to something like `root@6f2114c76845:/documents#`.  

Create HTML output:

```
make html
```

To make a clean html output (that deletes everything in the output folder before build the html files):

```
make clean html
```
