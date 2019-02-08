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
git checkout --orphan gh-pages
git rm -rf .
echo "My Page" > index.html
git add index.html
git commit -a -m "First pages commit"
git push --set-upstream origin gh-pages
```
