# This is a repo with commands from the course

## CLI:

* mkdir
* ls
* rm
* cp
* touch
* mv
* cd
* echo
* date
* clear
* pwd

## GIT:

* git config --global user.name "todro87"
* git config --global user.email "tmszdrbzg@gmail.com"
* git config --list
* exit
* git init - inicjalizacja folderu jako folder dla repozytori�w
* git remote add origin https://github.com/todro87/test-repo.git - po��czenie repozytorium lokalnego i zdalnego
* git clone https://github.com/todro87/test-repo.git - klonowanie repozytorium na komputer

* git add . - informuje Git, �e nale�y �ledzi� wszystkie nowe pliki
* git add -u - jak wy�ej, ale dla plik�w, kt�re zosta�y usuni�te lub zmieniono im nazw�
* git add -A - robi to co dwa powy�ej
* git commit -m "message" - zapisuje wersj� repo z wiadomo�ci�, tylko dla lokalnego repozytorium
* git push - wysy�a zmiany do zdalnego repo
* git checkout -b branchname - stworzenie nowej odnogi repo
* git branch - sprawdzenie, na kt�rej odnodze jeste�my
* git checkout master - prze��czenie do g��wnej odnogi
* git status - wy�wietla status zmian w kolejce
* git log - 
* git push -u origin master
* git diff HEAD - wy�wietla r�nice pomi�dzy zmianami innych u�ytkownik�w a naszymi
* git diff --staged - wy�wietla pliki gotowe do wys�ania
* git reset file - usuwa plik z listy do za�adowania
* git branch name - tworzy now� ga���
* git branch - wy�wietla ga��zie
* git checkout name - zmienia ga���
* git rm name - ustawia usuwanie plik�w w kolejce
* git merge name - ��czy ga��� name z aktywn�
* git branch -d name - usuwa ga��� name lokalnie
* git push origin --delete name - usuwa zdaln� ga��� name
* origin - domy�lna nazwa aktywnego repozytorium
* git remote rm name - usuwa remote name
* git remote rename name1 name2 - zmiana name1 na name2

## MARKDOWN:

# naglowek 1 rzedu
## naglowek 2 rzedu
### naglowek 3 rzedu

*  pierwszy elemet listy
*  drugi element listy
*  trzeci element listy

## R:

* install.packages("name") - instalowanie pakietu
* library(name) - za�adowanie pakietu

* getwd()
* setwd(path) - ustawiwa domy�lny folder do pracy
* dir() - zawarto�� folderu
* ls() - funkcje i zmienne w projekcie
* rm(list=ls()) - usuni�cie zmiennych i funkcji z projektu
* source("file") - dodanie skryptu

* : - np. 1:20 sekwencja liczb od 1 do 20
* 1 -liczba zmiennoprzecinkowa
* 1L - liczba ca�kowita

* c() - wektor, z dowoln� liczb� argument�w, np. c(1,2) to wektor liczb 1 i 2
* vector("numeric",length=10) - pusty wektor 10 liczb zmiennoprzecinkowych
* class(arg) - sprawdza klas� argumentu
* as.numeric(arg) - argument jako numeryczny
* as.logical(arg) - argument jako logiczny
* as.character(arg) - argument jako tekst
* list(arg1, arg2, arg3, ...) - tworzy list�

* matrix(nrow=x,ncol=y) - macierz o wymiarach x:y
* attributes(arg) - w przypadku macierzy wy�wietla jej wymiar
* dim(arg) - podaje wymiar arg
* m <- 1:10 - wektor od 1 do 10
* dim(m) <- c(2,5) - nadanie wektorowi m wymiaru 2:5
* cbind(x,y) - stworzenie macierzy z wektor�w x i y kolumnowo
* rbind(x,y) - j.w., tyle, �e wierszowo

* x <- factor(c("yes","yes","no","yes","yes")) - stworzenie zmiennej factor z dwoma poziomami yes i no
* table(x) - pokazuje ile jest wyst�pie� poziom�w w zmiennej factor
* unclass(x) - zamienia zmienn� factor na wektor liczb ca�kowitych
* attr(x,"levels") - pokazuje atrybuty poziom�w zmiennej factor
* x <- factor(c("yes","yes","no","yes","yes"),levels=c("yes","no")) - zmienna faktor z narzucon� kolejno�ci� * poziom�w, bez narzucenia kolejno�� jest alfabetyczna

* is.na(arg) - sprawdza czy obiekt ma brakuj�ce warto�ci
* is.nan(arg) - sprawdza czy obiekt jest NaN

* x <- data.frame(foo=1:4, bar=(T,T,F,F)) - stworzenie ramkni danych z kolumn� foo i bar
* nrow(x) - zwraca liczb� wierszy ramki danych
* ncol(x) - zwraca liczb� kolumn ramki danych

* names(x) <- c("a", "b","c") - nadanie elementom wetkora x nazw a, b, c
* x <- list(a=1, b=2, c=3) - stworzenie listy z elementami o nazwach a,b,c i warto�ciach 1,2,3
* m <- matrix(1:4, nrow=2, ncol=2)
* dimnames(m) <- list(c("a","b"),c("c","d")) - nadanie wierszom i kolumano macierzy nazw a,b,c,d

* read.table
* read.csv - separatorem jest przecinek
* readLines
* source
* dget
* load
* unserialize

* write.table
* writeLines
* dump
* dput
* save
* serialize

* data <- read.table("data.txt")
* opcja comment.char="" informuje read.table, �e w pliku nie ma komentarzy, przy�piesza to wczytywania * du�ych zbior�w danych
* colClasses="klasa danych" - wcze�niejsze podanie typ�w danych te� przy�piesza wczytywanie

* dput(y) - wy�wietla zmienn� y w formacie tekstowym z ca�� jej stryktur�
* dput(y,file="y.R") - zapisuje zmienn� w formacie tekstowym w pliku y.R
* new.y <- dget("y.R") - zapisuje zmienn� y z pliku y.R do zmiennej new.y
* dump(c("x","y"), file="data.R") - zapisuje zmienne x i y do pluku data.R w spos�b zdekonstruowany
* rm(x,y) - usuwa zmienne x i y z pami�ci
* source("data.R") - wczytuje plik data, w kt�rym s� zmienne x i y, co sprawia, �e zmienne s� ponownie dost�pne

* con <- file("foo.txt", "r") - otwiera po��czenie do pliku foo.txt w trybie czytania
* data <- read.csv(con) - wczytuje plik z po�aczenia do data
* close(con) - zamyka po��czenie
###s� r�ne typy po��cze�, gzfile tworzy po��czenie z plikiem gz, kt�ry mo�na przeczyta� p�niej funkcj� reaLines()
* con <- url("http://www.wp.pl") - tworz� po��czenie ze stron� www
* x <- readLines(con)
* head(x)

* x <- c(arg1, arg2,...)
* x[1] - pobranie elementu pierwszego z wektora x
* x[2] - pobranie elementu drugiego z wektora x
* x[1:4] - pobranie element�w od 1 do 4
* x[x>2] - pobranie wszystkich element�w wi�kszych ni� dwa
* u <- x > 2 - stworzenie wektora logicznego u, kt�ry pokazuje kt�re elementy s� wi�ksze ni� 2
* x[u] - pobranie element�w spe�niaj�cych regu�� wektora u
* x <- list(foo=1:4, bar=0.6, baz="hello")
* x[1] - zwraca list�
* x[[1]] - zwraca sekwencj� (wektor?)
* x$bar - dzia�a jak x[[2]], zwraca wektor
* x[["bar"]] - dzia�a jak x$bar, zwraca wektor
* x["bar"] - zwraca list�
* x[c(1,3)] - zwraca elementy 1 i 3 listy
* x[1:3] - zwraca elementy od 1 do 3 listy
* name <- "foo"
* x[[name]] - zadzia�a ze zmienn� name
* x$name - nie zadzia�a ze zmienn� name, nie ma jej na li�cie
* x <- list(a=list(10,12,14), b=c(3.14,2.81))
* x[[c(1,3)]] - pobranie elemetu trzeciego z elementu pierwszego listy, 14
* x[[1]][[3]] - to samo co powy�ej, 14
* x <- matrix(1:6,2,3)
* x[1,2] - pobranie elementu z pierwszego wiersza i drugiej kolumny macierzy
* x[1,] - pobranie pierwszego wiersza macierzy
* x[,2] - pobranie drugiej kolumny macierzy
* x[1,2,drop=F] - zachowuje wynik w postaci macierzy
* x[1,,drop=F] - jak wy�ej
* x <- list(aardvark=1:5)
* x$a - zadzia�a z powy�sz� list�, szuka nazwy na a
* x[["a"]] - nie zadzia�a, bo dopasowanie jest dok�adne
* x[["a", exact=F]] - zadzia�a
* x["a", exact=F] - nie zadzia�a bo R my�li, �e podajemy dwa argumenty
* x <- c(1,2,NA,4,NA,5)
* bad <- is.na(x)
* x[!bad] - zwraca elementy, kt�re nie s� NA
* x[bad] - zwraca elementy, kt�re s� NA
* good  <- complete.cases(x,y) - je�elix i y maj� NA na tym samym miejscu to wektor good jest wwktoremlogicznym z F na miejscach NA, sprawdza, kt�re wiersze lub kolumny s� kompletne
* x <- 1:4; y <- 6:9
* x+y - dodanie wektor�w
* x>2 - sprawdza, kt�re elementy s� wi�ksze ni� 2
* y==8 - sprawdza, kt�ry element jest r�wny 8
* x * y - pomno�enie wektor�w
* x/y - podzielenie wektor�w
* dla macierz x * y mno�y elementy przez siebie, x/y dzieli je
* x %*% y - mno�enie macierzowe
* args(function) - pokazuje argumwnty, kt�re przyjmuje funkcja
* dir.create("name") - tworzy katalog name w WD
* file.create("name") - tworzy plik name
* file.exists("name") - sprawdza czy plik name istnieje
* file.info("name") - wy�wietla informacje o pliku name
* file.rename("name1","name2") - zmienia nazw� pliku z name1 na name2
* file.copy("name1","name2") - tworzy kopi� pliku name1 jako plik name2
* file.path("name") - podaje �cie�k� pliku name
* file.path("folder1","folder2") - tworzy �cie�k� folder1/folder2
* dir.create(file.path("folder1","folder2"), recursive=TRUE) - tworzy �cie�k� folder1/folder2, recursive po to, �eby utworzy� oba foldery
* unlink("name", recursive=TRUE) - usuwa folder name, recursive po to, �eby usun�� r�wnie� wewn�trzne foldery
* ?function_name - w��czenie pomocy dla funkcji
* ?`:` - w��czenie pomocy dla operatora, w tym przypadku :
* seq(0,10,by=0.5) - liczby od 0 do 10 co 0.5
* seq_along(vector) - stworzenie sekwencji liczb d�ugiej jak vector
* rep(0,times=40) - powtarza 0 40 razy
* paste(vector, collapse=" ") - ��czy elementy vector u�ywaj�c spacji
* paste(word1, word2, sep=" ") - ��czy dwa s�owa u�ywaj�c spacji
* LETTERS - predefiniowana zmienna w R z wszystkimi literami
* sample(vector1, vector3, n) - wybiera n losowych warto�ci z vector1 i vector2
* sum(is.na(vector)) - zlicza wyst�pienia NA licz�c sum� vector, R traktuje TRUE jako 1 a FALSE jako 0
* if (x > 3) {y <-10} else {y <- 0} - konstrukcja if
* y <- if (x > 3) {10} else {0} - to te� jest poprawna konstrukcja
* for (i in 1:10) {print(i)} - przykladowa konstrukcja petli for
* x <- c("a", "b", "c", "d")
* for (i in 1:4) {print(x[i])} - to i poni�sze zapisy to poprawne wywo�ania funkcji for z tym samym rezlutatem
* for (i in seq_along(x) {print(x[i])}
* for (i in seq_along(x)) {print(x[i])}
* for (i in 1:4) print(x[i])
* for (i in seq_len(nrow(x))) {for (j in seq_len(ncol(x))) {print(x[i,j])}} - wypisanie kolejnych element�w macierzy
* seq_len(n) - tworzy sekwencj� liczb od 1 do n
* while (count<10) {print(count) count <- count+1} - przyk��dowa funkcja while
* repeat - powtarza dop�ki nie b�dzie komendy break
* next - przeskakuje iteracj� gry spe�niony jest warunek
* f <- function(arguments) {##kod} - stworzenie funkcji f
* formals(function) - zwraca argumenty funkcji
* sd(data) - oblicza odchylenie standardowe
* ... - rozszerza list� argument�w, np. myplot <- function(x,y,type="1",...) { plot(x,y,type=type,...)}
* args(paste) - wy�wietla spos�by wywo�ania funkcji paste, wszystko co jest po ... musi zosta� dok�adnie podane, w funkcji paste nie ma "partial matching"
* cat(1,2) - ��czy argumenty i wy�wietla
}
* x[C(-2,-10)] - wy�wietla wszystkie elementy wektora x poza elementem nr 2 i 10