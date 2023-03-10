# tmux

## Konfiguracja

Tmux to narzędzie linii poleceń, które pozwala na zarządzanie wieloma oknami i panelami w terminalu.

Konfiguracja tmuxa pozwala dostosować jego działanie do indywidualnych potrzeb użytkownika.
Aby skonfigurować tmuxa, należy utworzyć plik konfiguracyjny i zdefiniować w nim preferencje, takie jak kolory, rozmiar czcionki, skróty klawiaturowe i wiele innych opcji.

Plik konfiguracyjny dla tmuxa nazywa się .tmux.conf i zazwyczaj powinien znajdować się w katalogu domowym użytkownika (czyli w lokalizacji /home/nazwa_użytkownika/ lub /Users/nazwa_użytkownika/ w zależności od systemu operacyjnego).

Jeśli plik nie istnieje, można go utworzyć w edytorze tekstowym.

W pliku konfiguracyjnym można definiować wiele opcji, takich jak skróty klawiszowe do obsługi tmuxa, wygląd interfejsu użytkownika, tryb kopiowania, styl i kolory terminala oraz wiele innych ustawień.

Przykładowo, można ustawić klawisz Ctrl+A jako klawisz startowy (zamiast domyślnego Ctrl+B), zmienić kolor tła lub tekstu, zmienić wielkość czcionki, a także dostosować wiele innych opcji związanych z wyglądem i funkcjonalnością tmuxa.

Warto pamiętać, że zmiany wprowadzone w pliku konfiguracyjnym nie będą miały natychmiastowego efektu.

### Przeładowanie konfiguracji
 
Aby zobaczyć zmiany, należy uruchomić tmuxa ponownie, używając polecenia 

```bash
tmux source-file ~/.tmux.conf
```

lub po prostu zamknąć i otworzyć ponownie terminal.

### Podłączenie się do istniejącej seji tmux

Aby dołączyć do istniejącej sesji tmux, należy użyć polecenia tmux attach-session w terminalu. Aby to zrobić, wykonaj następujące kroki:

Otwórz terminal na swoim komputerze.

Uruchom polecenie tmux ls, aby wyświetlić listę istniejących sesji tmux.

Znajdź nazwę lub numer sesji, do której chcesz się dołączyć.

Uruchom polecenie 

```bash
tmux attach-session -t nazwa_sesji
``` 
lub 

```bash
tmux attach-session -t numer_sesji
```

aby dołączyć do wybranej sesji.

Można również użyć skrótu klawiszowego tmuxa jako alternatywy dla tmux attach-session.

Po wykonaniu tych kroków powinieneś być w stanie dołączyć do istniejącej sesji tmux i kontynuować pracę tam, gdzie ją przerwałeś.

### Zarządzanie oknami

W tmuxie istnieje możliwość zmiany kolejności okien, czyli przemieszczania ich w lewo lub prawo.

Aby to zrobić, należy użyć jednego z dwóch poleceń:

bash```swap-window -s nr_okna -t nr_okna
```
Przenosi okno o numerze nr_okna na pozycję okna o numerze nr_okna.

bash```move-window -s nr_okna -t nr_okna
``` 
Przenosi okno o numerze nr_okna na pozycję okna o numerze nr_okna i dostosowuje numery innych okien w odpowiedni sposób.

Oto przykładowe użycie poleceń, aby zmienić kolejność okien:

Aby przenieść okno o numerze 2 na pozycję pierwszą, wykonaj polecenie: 
bash```
tmux swap-window -s 2 -t 1
```

Aby przenieść okno o numerze 3 na pozycję drugą i dostosować numery innych okien, wykonaj polecenie:
bash```
tmux move-window -s 3 -t 2
```

Pamiętaj, że numery okien zaczynają się od 0, więc pierwsze okno ma numer 0, drugie okno ma numer 1, itd.


### Usuwanie okna

Aby usunąć okno w tmuxie, należy użyć polecenia tmux kill-window. Aby to zrobić, wykonaj następujące kroki:

1. Otwórz terminal ii uruchom sesję tmux.

2. Przejdź do okna, które chcesz usunąć.

3. Wykonaj polecenie 

bash```
tmux kill-window
```
 lub skrót klawiszowy Ctrl-b &.

4. Potwierdź usunięcie okna naciskając klawisz y.

Po wykonaniu tych kroków okno zostanie usunięte z sesji tmux. Pamiętaj, że usuwanie okna jest trwałe, więc upewnij się, że nie chcesz już dłużej z niego korzystać przed wykonaniem tego polecenia.


