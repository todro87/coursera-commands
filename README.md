# This is a repo with commands from the course

## CLI:

*mkdir
*ls
*rm
*cp
*touch
*mv
*cd
*echo
*date
*clear
*pwd

## GIT:

*git config --global user.name "todro87"
*git config --global user.email "tmszdrbzg@gmail.com"
*git config --list
*exit
*git init - inicjalizacja folderu jako folder dla repozytori�w
*git remote add origin https://github.com/todro87/test-repo.git - po��czenie repozytorium lokalnego i zdalnego
*git clone https://github.com/todro87/test-repo.git - klonowanie repozytorium na komputer

*git add . - informuje Git, �e nale�y �ledzi� wszystkie nowe pliki
*git add -u - jak wy�ej, ale dla plik�w, kt�re zosta�y usuni�te lub zmieniono im nazw�
*git add -A - robi to co dwa powy�ej
*git commit -m "message" - zapisuje wersj� repo z wiadomo�ci�, tylko dla lokalnego repozytorium
*git push - wysy�a zmiany do zdalnego repo
*git checkout -b branchname - stworzenie nowej odnogi repo
*git branch - sprawdzenie, na kt�rej odnodze jeste�my
*git checkout master - prze��czenie do g��wnej odnogi
*git status - wy�wietla status zmian w kolejce
*git log - 
*git push -u origin master
*git diff HEAD - wy�wietla r�nice pomi�dzy zmianami innych u�ytkownik�w a naszymi
*git diff --staged - wy�wietla pliki gotowe do wys�ania
*git reset file - usuwa plik z listy do za�adowania
*git branch name - tworzy now� ga���
*git branch - wy�wietla ga��zie
*git checkout name - zmienia ga���
*git rm name - ustawia usuwanie plik�w w kolejce
*git merge name - ��czy ga��� name z aktywn�
*git branch -d name - usuwa ga��� name lokalnie
*git push origin --delete name - usuwa zdaln� ga��� name
*origin - domy�lna nazwa aktywnego repozytorium
*git remote rm name - usuwa remote name
*git remote rename name1 name2 - zmiana name1 na name2

## MARKDOWN:

# naglowek 1 rzedu
## naglowek 2 rzedu
### naglowek 3 rzedu

* pierwszy elemet listy
* drugi element listy
* trzeci element listy

## R:

*install.packages("name") - instalowanie pakietu
*library(name) - za�adowanie pakietu

*getwd()
*setwd(path) - ustawiwa domy�lny folder do pracy
*dir() - zawarto�� folderu
*ls() - funkcje i zmienne w projekcie
*source("file") - dodanie skryptu

*: - np. 1:20 sekwencja liczb od 1 do 20
*1 -liczba zmiennoprzecinkowa
*1L - liczba ca�kowita

*c() - wektor, z dowoln� liczb� argument�w, np. c(1,2) to wektor liczb 1 i 2
*vector("numeric",length=10) - pusty wektor 10 liczb zmiennoprzecinkowych
*class(arg) - sprawdza klas� argumentu
*as.numeric(arg) - argument jako numeryczny
*as.logical(arg) - argument jako logiczny
*as.character(arg) - argument jako tekst
*list(arg1, arg2, arg3, ...) - tworzy list�

*matrix(nrow=x,ncol=y) - macierz o wymiarach x:y
*attributes(arg) - w przypadku macierzy wy�wietla jej wymiar
*dim(arg) - podaje wymiar arg
*m <- 1:10 - wektor od 1 do 10
*dim(m) <- c(2,5) - nadanie wektorowi m wymiaru 2:5
*cbind(x,y) - stworzenie macierzy z wektor�w x i y kolumnowo
*rbind(x,y) - j.w., tyle, �e wierszowo

*x <- factor(c("yes","yes","no","yes","yes")) - stworzenie zmiennej factor z dwoma poziomami yes i no
*table(x) - pokazuje ile jest wyst�pie� poziom�w w zmiennej factor
*unclass(x) - zamienia zmienn� factor na wektor liczb ca�kowitych
*attr(x,"levels") - pokazuje atrybuty poziom�w zmiennej factor
*x <- factor(c("yes","yes","no","yes","yes"),levels=c("yes","no")) - zmienna faktor z narzucon� kolejno�ci� *poziom�w, bez narzucenia kolejno�� jest alfabetyczna

*is.na(arg) - sprawdza czy obiekt ma brakuj�ce warto�ci
*is.nan(arg) - sprawdza czy obiekt jest NaN

*x <- data.frame(foo=1:4, bar=(T,T,F,F)) - stworzenie ramkni danych z kolumn� foo i bar
*nrow(x) - zwraca liczb� wierszy ramki danych
*ncol(x) - zwraca liczb� kolumn ramki danych

*names(x) <- c("a", "b","c") - nadanie elementom wetkora x nazw a, b, c
*x <- list(a=1, b=2, c=3) - stworzenie listy z elementami o nazwach a,b,c i warto�ciach 1,2,3
*m <- matrix(1:4, nrow=2, ncol=2)
*dimnames(m) <- list(c("a","b"),c("c","d")) - nadanie wierszom i kolumano macierzy nazw a,b,c,d

*read.table
*read.csv - separatorem jest przecinek
*readLines
*source
*dget
*load
*unserialize

*write.table
*writeLines
*dump
*dput
*save
*serialize

*data <- read.table("data.txt")
*opcja comment.char="" informuje read.table, �e w pliku nie ma komentarzy, przy�piesza to wczytywania *du�ych zbior�w danych
*colClasses="klasa danych" - wcze�niejsze podanie typ�w danych te� przy�piesza wczytywanie

*dput(y) - wy�wietla zmienn� y w formacie tekstowym z ca�� jej stryktur�
*dput(y,file="y.R") - zapisuje zmienn� w formacie tekstowym w pliku y.R
*new.y <- dget("y.R") - zapisuje zmienn� y z pliku y.R do zmiennej new.y
*dump(c("x","y"), file="data.R") - zapisuje zmienne x i y do pluku data.R w spos�b zdekonstruowany
*rm(x,y) - usuwa zmienne x i y z pami�ci
*source("data.R") - wczytuje plik data, w kt�rym s� zmienne x i y, co sprawia, �e zmienne s� ponownie dost�pne

*con <- file("foo.txt", "r") - otwiera po��czenie do pliku foo.txt w trybie czytania
*data <- read.csv(con) - wczytuje plik z po�aczenia do data
*close(con) - zamyka po��czenie
###s� r�ne typy po��cze�, gzfile tworzy po��czenie z plikiem gz, kt�ry mo�na przeczyta� p�niej funkcj� reaLines()
*con <- url("http://www.wp.pl") - tworz� po��czenie ze stron� www
*x <- readLines(con)
*head(x)

*x <- c(arg1, arg2,...)
*x[1] - pobranie elementu pierwszego z wektora x
*x[2] - pobranie elementu drugiego z wektora x
*x[1:4] - pobranie element�w od 1 do 4
*x[x>2] - pobranie wszystkich element�w wi�kszych ni� dwa
*u <- x > 2 - stworzenie wektora logicznego u, kt�ry pokazuje kt�re elementy s� wi�ksze ni� 2
*x[u] - pobranie element�w spe�niaj�cych regu�� wektora u

