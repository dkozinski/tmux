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

Aby zobaczyć zmiany, należy uruchomić tmuxa ponownie, używając polecenia "tmux source-file ~/.tmux.conf" lub po prostu zamknąć i otworzyć ponownie terminal.

## Kopiowanie tekstu


