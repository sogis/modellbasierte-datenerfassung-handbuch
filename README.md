# modellbasierte-datenerfassung-handbuch
Asciidoctor documentation repository für das Handbuch "modellbasierte Datenerfassung"

## System Requirements

* gradle
* java

## General usage

Clone this repository:

```
git clone https://github.com/sogis/modellbasierte-datenerfassung-handbuch.git $HOME/Projekte/modellbasierte-datenerfassung-handbuch
```

HTML-Output:
```
gradle asciidoctor
```

PDF-Output:
```
gradle generatePDF
```

## Setup Github pages

```
cd /path/to/repo-name
git symbolic-ref HEAD refs/heads/gh-pages
rm .git/index
git clean -fdx
echo "My GitHub Page" > index.html
git add .
git commit -a -m "First pages commit"
git push origin gh-pages
```

https://sogis.github.io/modellbasierte-datenerfassung-handbuch/
