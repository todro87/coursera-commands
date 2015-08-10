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
* git init - inicjalizacja folderu jako folder dla repozytoriów
* git remote add origin https://github.com/todro87/test-repo.git - po³¹czenie repozytorium lokalnego i zdalnego
* git clone https://github.com/todro87/test-repo.git - klonowanie repozytorium na komputer

* git add . - informuje Git, ¿e nale¿y œledziæ wszystkie nowe pliki
* git add -u - jak wy¿ej, ale dla plików, które zosta³y usuniête lub zmieniono im nazwê
* git add -A - robi to co dwa powy¿ej
* git commit -m "message" - zapisuje wersjê repo z wiadomoœci¹, tylko dla lokalnego repozytorium
* git push - wysy³a zmiany do zdalnego repo
* git checkout -b branchname - stworzenie nowej odnogi repo
* git branch - sprawdzenie, na której odnodze jesteœmy
* git checkout master - prze³¹czenie do g³ównej odnogi
* git status - wyœwietla status zmian w kolejce
* git log - 
* git push -u origin master
* git diff HEAD - wyœwietla ró¿nice pomiêdzy zmianami innych u¿ytkowników a naszymi
* git diff --staged - wyœwietla pliki gotowe do wys³ania
* git reset file - usuwa plik z listy do za³adowania
* git branch name - tworzy now¹ ga³¹Ÿ
* git branch - wyœwietla ga³êzie
* git checkout name - zmienia ga³¹Ÿ
* git rm name - ustawia usuwanie plików w kolejce
* git merge name - ³¹czy ga³¹Ÿ name z aktywn¹
* git branch -d name - usuwa ga³¹Ÿ name lokalnie
* git push origin --delete name - usuwa zdaln¹ ga³¹Ÿ name
* origin - domyœlna nazwa aktywnego repozytorium
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
* library(name) - za³adowanie pakietu

* getwd()
* setwd(path) - ustawiwa domyœlny folder do pracy
* dir() - zawartoœæ folderu
* ls() - funkcje i zmienne w projekcie
* rm(list=ls()) - usuniêcie zmiennych i funkcji z projektu
* source("file") - dodanie skryptu

* : - np. 1:20 sekwencja liczb od 1 do 20
* 1 -liczba zmiennoprzecinkowa
* 1L - liczba ca³kowita

* c() - wektor, z dowoln¹ liczb¹ argumentów, np. c(1,2) to wektor liczb 1 i 2
* vector("numeric",length=10) - pusty wektor 10 liczb zmiennoprzecinkowych
* class(arg) - sprawdza klasê argumentu
* as.numeric(arg) - argument jako numeryczny
* as.logical(arg) - argument jako logiczny
* as.character(arg) - argument jako tekst
* list(arg1, arg2, arg3, ...) - tworzy listê

* matrix(nrow=x,ncol=y) - macierz o wymiarach x:y
* attributes(arg) - w przypadku macierzy wyœwietla jej wymiar
* dim(arg) - podaje wymiar arg
* m <- 1:10 - wektor od 1 do 10
* dim(m) <- c(2,5) - nadanie wektorowi m wymiaru 2:5
* cbind(x,y) - stworzenie macierzy z wektorów x i y kolumnowo
* rbind(x,y) - j.w., tyle, ¿e wierszowo

* x <- factor(c("yes","yes","no","yes","yes")) - stworzenie zmiennej factor z dwoma poziomami yes i no
* table(x) - pokazuje ile jest wyst¹pieñ poziomów w zmiennej factor
* unclass(x) - zamienia zmienn¹ factor na wektor liczb ca³kowitych
* attr(x,"levels") - pokazuje atrybuty poziomów zmiennej factor
* x <- factor(c("yes","yes","no","yes","yes"),levels=c("yes","no")) - zmienna faktor z narzucon¹ kolejnoœci¹ * poziomów, bez narzucenia kolejnoœæ jest alfabetyczna

* is.na(arg) - sprawdza czy obiekt ma brakuj¹ce wartoœci
* is.nan(arg) - sprawdza czy obiekt jest NaN

* x <- data.frame(foo=1:4, bar=(T,T,F,F)) - stworzenie ramkni danych z kolumn¹ foo i bar
* nrow(x) - zwraca liczbê wierszy ramki danych
* ncol(x) - zwraca liczbê kolumn ramki danych

* names(x) <- c("a", "b","c") - nadanie elementom wetkora x nazw a, b, c
* x <- list(a=1, b=2, c=3) - stworzenie listy z elementami o nazwach a,b,c i wartoœciach 1,2,3
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
* opcja comment.char="" informuje read.table, ¿e w pliku nie ma komentarzy, przyœpiesza to wczytywania * du¿ych zbiorów danych
* colClasses="klasa danych" - wczeœniejsze podanie typów danych te¿ przyœpiesza wczytywanie

* dput(y) - wyœwietla zmienn¹ y w formacie tekstowym z ca³¹ jej stryktur¹
* dput(y,file="y.R") - zapisuje zmienn¹ w formacie tekstowym w pliku y.R
* new.y <- dget("y.R") - zapisuje zmienn¹ y z pliku y.R do zmiennej new.y
* dump(c("x","y"), file="data.R") - zapisuje zmienne x i y do pluku data.R w sposób zdekonstruowany
* rm(x,y) - usuwa zmienne x i y z pamiêci
* source("data.R") - wczytuje plik data, w którym s¹ zmienne x i y, co sprawia, ¿e zmienne s¹ ponownie dostêpne

* con <- file("foo.txt", "r") - otwiera po³¹czenie do pliku foo.txt w trybie czytania
* data <- read.csv(con) - wczytuje plik z po³aczenia do data
* close(con) - zamyka po³¹czenie
###s¹ ró¿ne typy po³¹czeñ, gzfile tworzy po³¹czenie z plikiem gz, który mo¿na przeczytaæ póŸniej funkcj¹ reaLines()
* con <- url("http://www.wp.pl") - tworz¹ po³¹czenie ze stron¹ www
* x <- readLines(con)
* head(x)

* x <- c(arg1, arg2,...)
* x[1] - pobranie elementu pierwszego z wektora x
* x[2] - pobranie elementu drugiego z wektora x
* x[1:4] - pobranie elementów od 1 do 4
* x[x>2] - pobranie wszystkich elementów wiêkszych ni¿ dwa
* u <- x > 2 - stworzenie wektora logicznego u, który pokazuje które elementy s¹ wiêksze ni¿ 2
* x[u] - pobranie elementów spe³niaj¹cych regu³ê wektora u
* x <- list(foo=1:4, bar=0.6, baz="hello")
* x[1] - zwraca listê
* x[[1]] - zwraca sekwencjê (wektor?)
* x$bar - dzia³a jak x[[2]], zwraca wektor
* x[["bar"]] - dzia³a jak x$bar, zwraca wektor
* x["bar"] - zwraca listê
* x[c(1,3)] - zwraca elementy 1 i 3 listy
* x[1:3] - zwraca elementy od 1 do 3 listy
* name <- "foo"
* x[[name]] - zadzia³a ze zmienn¹ name
* x$name - nie zadzia³a ze zmienn¹ name, nie ma jej na liœcie
* x <- list(a=list(10,12,14), b=c(3.14,2.81))
* x[[c(1,3)]] - pobranie elemetu trzeciego z elementu pierwszego listy, 14
* x[[1]][[3]] - to samo co powy¿ej, 14
* x <- matrix(1:6,2,3)
* x[1,2] - pobranie elementu z pierwszego wiersza i drugiej kolumny macierzy
* x[1,] - pobranie pierwszego wiersza macierzy
* x[,2] - pobranie drugiej kolumny macierzy
* x[1,2,drop=F] - zachowuje wynik w postaci macierzy
* x[1,,drop=F] - jak wy¿ej
* x <- list(aardvark=1:5)
* x$a - zadzia³a z powy¿sz¹ list¹, szuka nazwy na a
* x[["a"]] - nie zadzia³a, bo dopasowanie jest dok³adne
* x[["a", exact=F]] - zadzia³a
* x["a", exact=F] - nie zadzia³a bo R myœli, ¿e podajemy dwa argumenty
* x <- c(1,2,NA,4,NA,5)
* bad <- is.na(x)
* x[!bad] - zwraca elementy, które nie s¹ NA
* x[bad] - zwraca elementy, które s¹ NA
* good  <- complete.cases(x,y) - je¿elix i y maj¹ NA na tym samym miejscu to wektor good jest wwktoremlogicznym z F na miejscach NA, sprawdza, które wiersze lub kolumny s¹ kompletne
* x <- 1:4; y <- 6:9
* x+y - dodanie wektorów
* x>2 - sprawdza, które elementy s¹ wiêksze ni¿ 2
* y==8 - sprawdza, który element jest równy 8
* x * y - pomno¿enie wektorów
* x/y - podzielenie wektorów
* dla macierz x * y mno¿y elementy przez siebie, x/y dzieli je
* x %*% y - mno¿enie macierzowe
* args(function) - pokazuje argumwnty, które przyjmuje funkcja
* dir.create("name") - tworzy katalog name w WD
* file.create("name") - tworzy plik name
* file.exists("name") - sprawdza czy plik name istnieje
* file.info("name") - wyœwietla informacje o pliku name
* file.rename("name1","name2") - zmienia nazwê pliku z name1 na name2
* file.copy("name1","name2") - tworzy kopiê pliku name1 jako plik name2
* file.path("name") - podaje œcie¿kê pliku name
* file.path("folder1","folder2") - tworzy œcie¿kê folder1/folder2
* dir.create(file.path("folder1","folder2"), recursive=TRUE) - tworzy œcie¿kê folder1/folder2, recursive po to, ¿eby utworzyæ oba foldery
* unlink("name", recursive=TRUE) - usuwa folder name, recursive po to, ¿eby usun¹æ równie¿ wewnêtrzne foldery
* ?function_name - w³¹czenie pomocy dla funkcji
* ?`:` - w³¹czenie pomocy dla operatora, w tym przypadku :
* seq(0,10,by=0.5) - liczby od 0 do 10 co 0.5
* seq_along(vector) - stworzenie sekwencji liczb d³ugiej jak vector
* rep(0,times=40) - powtarza 0 40 razy
* paste(vector, collapse=" ") - ³¹czy elementy vector u¿ywaj¹c spacji
* paste(word1, word2, sep=" ") - ³¹czy dwa s³owa u¿ywaj¹c spacji
* LETTERS - predefiniowana zmienna w R z wszystkimi literami
* sample(vector1, vector3, n) - wybiera n losowych wartoœci z vector1 i vector2
* sum(is.na(vector)) - zlicza wyst¹pienia NA licz¹c sumê vector, R traktuje TRUE jako 1 a FALSE jako 0
* if (x > 3) {y <-10} else {y <- 0} - konstrukcja if
* y <- if (x > 3) {10} else {0} - to te¿ jest poprawna konstrukcja
* for (i in 1:10) {print(i)} - przykladowa konstrukcja petli for
* x <- c("a", "b", "c", "d")
* for (i in 1:4) {print(x[i])} - to i poni¿sze zapisy to poprawne wywo³ania funkcji for z tym samym rezlutatem
* for (i in seq_along(x) {print(x[i])}
* for (i in seq_along(x)) {print(x[i])}
* for (i in 1:4) print(x[i])
* for (i in seq_len(nrow(x))) {for (j in seq_len(ncol(x))) {print(x[i,j])}} - wypisanie kolejnych elementów macierzy
* seq_len(n) - tworzy sekwencjê liczb od 1 do n
* while (count<10) {print(count) count <- count+1} - przyk³¹dowa funkcja while
* repeat - powtarza dopóki nie bêdzie komendy break
* next - przeskakuje iteracj¹ gry spe³niony jest warunek
* f <- function(arguments) {##kod} - stworzenie funkcji f
* formals(function) - zwraca argumenty funkcji
* sd(data) - oblicza odchylenie standardowe
* ... - rozszerza listê argumentów, np. myplot <- function(x,y,type="1",...) { plot(x,y,type=type,...)}
* args(paste) - wyœwietla sposóby wywo³ania funkcji paste, wszystko co jest po ... musi zostaæ dok³adnie podane, w funkcji paste nie ma "partial matching"
* cat(1,2) - ³¹czy argumenty i wyœwietla
}
* x[C(-2,-10)] - wyœwietla wszystkie elementy wektora x poza elementem nr 2 i 10