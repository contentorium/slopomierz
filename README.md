# Slopomierz

Linter redakcyjny do polskich tekstów. Wklejasz szkic, a strona zaznacza miejsca do poprawy. Sama niczego nie zmienia, decyzja zostaje przy osobie, która redaguje.

## Co sprawdza

- słowa i frazy z listy zakazanych (np. „kluczowy”, „warto”, „w dzisiejszych czasach”, „wydaje się”)
- figury kontrastu typu „nie X, tylko Y” i „X, nie Y”, z licznikiem, który czerwienieje powyżej trzech
- możliwe triady, wyliczenia „po pierwsze, po drugie” i anafory (trzy zdania z rzędu od tego samego słowa)
- śródtytuły w formie pytania i generyczne śródtytuły
- liczby bez przypisu `[^n]` w tym samym zdaniu
- przypisy bez źródła na dole i źródła, do których nic w tekście nie odsyła

Oznaczenia mają trzy kolory: czerwony to fraza zakazana, żółty to miejsce do sprawdzenia, niebieski to figura, której nie można przesolić.

## Własna lista fraz

Na dole strony jest pole „Twoja lista fraz”. Jedna fraza w linii, gwiazdka zastępuje końcówkę, więc `dedykowan*` złapie „dedykowany”, „dedykowanej” i resztę odmian. Lista i ostatni szkic zapisują się w przeglądarce (localStorage), nic nie jest wysyłane na serwer.

## Jak uruchomić

To jeden plik `index.html` bez zależności poza fontami z Google Fonts. Można go otworzyć lokalnie w przeglądarce albo opublikować przez GitHub Pages: Settings → Pages → Deploy from a branch → `main`, folder `/ (root)`.

## Ograniczenia

Reguły to wyrażenia regularne, więc nie rozumieją sensu. Najwięcej fałszywych alarmów pojawia się przy triadach i przy wzorcu „X, nie Y”. Dlatego te miejsca są oznaczone jako do sprawdzenia, a nie jako błąd.
