# Шаблон отчёта (СПбПУ) [![Build Status](https://www.travis-ci.com/polytechnic-templates/report-template.svg?branch=master)](https://www.travis-ci.com/polytechnic-templates/report-template) [![Semantic Versions](https://img.shields.io/badge/%F0%9F%9A%80-semantic%20versions-informational.svg)](https://semver.org/)
В этом проекте представлен шаблон отчёта по лабораторной или курсовой работе. Это форк https://github.com/kspt-templates/report, переделанный под меня. Может, и Вам будет удобнее.

**Важно!** Шаблон не идеален и соответствует не всем требованиям.
Если консультант по нормконтролю или преподаватель высказал замечания к работе, составленной по данному шаблону, то можно смело [заводить issue](https://github.com/tiulpin/report-template/issues/new). Попробуем исправить.

Также можно отправлять Pull Request. 

## Работа с шаблоном
Рекомендуется использовать Overleaf. 
В таком случае не придётся устанавливать пакеты TeX локально и разбираться в сборке документа вручную. 
Использовать шаблон из галереи шаблонов Overleaf: [https://ru.overleaf.com/latex/templates/shablon-otchiota-spbpu/jzbtjhbjpfxg](https://ru.overleaf.com/latex/templates/shablon-otchiota-spbpu/jzbtjhbjpfxg)

#### Сборка локально
Понадобится Docker. 
```
wget https://github.com/tiulpin/xelatex-docker/raw/master/.latexmkrc -O .latexmkrc
wget https://github.com/tiulpin/xelatex-docker/raw/master/latexdockercmd.sh -O latexdockercmd.sh
chmod a+x latexdockercmd.sh
./latexdockercmd.sh latexmk -cd -f -interaction=nonstopmode -pdf main.tex
```

## Заполнение шаблона

1. Изменить `config.tex`: имя студента, название предмета и пр. параметры указаны именно там
1. Заполнить `content.tex` - файл, который будет содержать весь текст отчёта, от вступления до заключения.
1. Добавить используемую литературу (если есть) в `refs.bib`. Для удобного поиска источников можно воспользоваться [Google Books](https://books.google.com/). Использованные источники можно указывать с помощью команды `\cite{name_of_ref}`
