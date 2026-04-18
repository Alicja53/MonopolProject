# ⚡ Harry Potter Monopoly - Game Design Document

Dokumentacja techniczna mechaniki gry realizowanej w silniku Godot.

---

## 🗺️ Lokacje Specjalne i Zasady Ogólne

| Nazwa Pola | Działanie / Opis | Kwota |
| :--- | :--- | :--- |
| **Peron 9 i 3/4 (START)** | Premia za przejście lub zatrzymanie się. | `+ 400 G` |
| **Azkaban** | Odwiedziny lub oczekiwanie na wyjście (dublet/karta). | Kaucja: `100 G` |
| **Pocałunek Dementora** | Natychmiastowe przeniesienie gracza do Azkabanu. | --- |
| **Bank Gringotta** | Pole darmowe (Darmowy Parking). | --- |
| **Podatek Ministerstwa** | Obowiązkowa opłata do banku (Pole nr 38). | `- 200 G` |

---

## 🏰 Akty Własności (Karty Nieruchomości)

| Grupa | Nazwa Pola | Finanse | Opłaty za postój (Czynsz) | Rozbudowa |
| :--- | :--- | :--- | :--- | :--- |
| **Kamień Filozoficzny** | **Komórka pod schodami** | Zakup: `120 G` <br> <small>Sprzedaż: `60 G`</small> | • Teren surowy: `10 G` <br> • Z 1 Chatką: `40 G` <br> • Z 2 Chatkami: `120 G` <br> • Z 3 Chatkami: `360 G` <br> • Z 4 Chatkami: `640 G` <br> • Z Zamkiem: `900 G` | Chatka: `100 G` <br> Zamek: `100 G` |
| **Kamień Filozoficzny** | **Sklep Ollivandera** | Zakup: `120 G` <br> <small>Sprzedaż: `60 G`</small> | • Teren surowy: `10 G` <br> • Z 1 Chatką: `40 G` <br> • Z 2 Chatkami: `120 G` <br> • Z 3 Chatkami: `360 G` <br> • Z 4 Chatkami: `640 G` <br> • Z Zamkiem: `900 G` | Chatka: `100 G` <br> Zamek: `100 G` |
| **Kamień Filozoficzny** | **Księgarnia Esy i Floresy** | Zakup: `120 G` <br> <small>Sprzedaż: `60 G`</small> | • Teren surowy: `10 G` <br> • Z 1 Chatką: `40 G` <br> • Z 2 Chatkami: `120 G` <br> • Z 3 Chatkami: `360 G` <br> • Z 4 Chatkami: `640 G` <br> • Z Zamkiem: `900 G` | Chatka: `100 G` <br> Zamek: `100 G` |
| **Komnata Tajemnic** | **Dom Weasleyów** | Zakup: `200 G` <br> <small>Sprzedaż: `100 G`</small> | • Teren surowy: `15 G` <br> • Z 1 Chatką: `60 G` <br> • Z 2 Chatkami: `180 G` <br> • Z 3 Chatkami: `540 G` <br> • Z 4 Chatkami: `800 G` <br> • Z Zamkiem: `1100 G` | Chatka: `100 G` <br> Zamek: `100 G` |
| **Komnata Tajemnic** | **Chatka Hagrida** | Zakup: `200 G` <br> <small>Sprzedaż: `100 G`</small> | • Teren surowy: `15 G` <br> • Z 1 Chatką: `60 G` <br> • Z 2 Chatkami: `180 G` <br> • Z 3 Chatkami: `540 G` <br> • Z 4 Chatkami: `800 G` <br> • Z Zamkiem: `1100 G` | Chatka: `100 G` <br> Zamek: `100 G` |
| **Komnata Tajemnic** | **Komnata Tajemnic** | Zakup: `240 G` <br> <small>Sprzedaż: `120 G`</small> | • Teren surowy: `20 G` <br> • Z 1 Chatką: `80 G` <br> • Z 2 Chatkami: `200 G` <br> • Z 3 Chatkami: `600 G` <br> • Z 4 Chatkami: `900 G` <br> • Z Zamkiem: `1200 G` | Chatka: `100 G` <br> Zamek: `100 G` |
| **Więzień Azkabanu** | **Dziurawy Kocioł** | Zakup: `280 G` <br> <small>Sprzedaż: `140 G`</small> | • Teren surowy: `20 G` <br> • Z 1 Chatką: `100 G` <br> • Z 2 Chatkami: `300 G` <br> • Z 3 Chatkami: `900 G` <br> • Z 4 Chatkami: `1250 G` <br> • Z Zamkiem: `1500 G` | Chatka: `200 G` <br> Zamek: `200 G` |
| **Więzień Azkabanu** | **Hogsmeade** | Zakup: `280 G` <br> <small>Sprzedaż: `140 G`</small> | • Teren surowy: `20 G` <br> • Z 1 Chatką: `100 G` <br> • Z 2 Chatkami: `300 G` <br> • Z 3 Chatkami: `900 G` <br> • Z 4 Chatkami: `1250 G` <br> • Z Zamkiem: `1500 G` | Chatka: `200 G` <br> Zamek: `200 G` |
| **Więzień Azkabanu** | **Stacja Hogsmeade** | Zakup: `320 G` <br> <small>Sprzedaż: `160 G`</small> | • Teren surowy: `25 G` <br> • Z 1 Chatką: `120 G` <br> • Z 2 Chatkami: `360 G` <br> • Z 3 Chatkami: `1000 G` <br> • Z 4 Chatkami: `1400 G` <br> • Z Zamkiem: `1800 G` | Chatka: `200 G` <br> Zamek: `200 G` |
| **Czara Ognia** | **Wrzeszcząca Chata** | Zakup: `360 G` <br> <small>Sprzedaż: `180 G`</small> | • Teren surowy: `30 G` <br> • Z 1 Chatką: `140 G` <br> • Z 2 Chatkami: `400 G` <br> • Z 3 Chatkami: `1100 G` <br> • Z 4 Chatkami: `1500 G` <br> • Z Zamkiem: `1900 G` | Chatka: `200 G` <br> Zamek: `200 G` |
| **Czara Ognia** | **Stadion Quidditcha** | Zakup: `360 G` <br> <small>Sprzedaż: `180 G`</small> | • Teren surowy: `30 G` <br> • Z 1 Chatką: `140 G` <br> • Z 2 Chatkami: `400 G` <br> • Z 3 Chatkami: `1100 G` <br> • Z 4 Chatkami: `1500 G` <br> • Z Zamkiem: `1900 G` | Chatka: `200 G` <br> Zamek: `200 G` |
| **Czara Ognia** | **Labirynt Trójmagiczny**| Zakup: `400 G` <br> <small>Sprzedaż: `200 G`</small> | • Teren surowy: `35 G` <br> • Z 1 Chatką: `160 G` <br> • Z 2 Chatkami: `440 G` <br> • Z 3 Chatkami: `1200 G` <br> • Z 4 Chatkami: `1600 G` <br> • Z Zamkiem: `2000 G` | Chatka: `200 G` <br> Zamek: `200 G` |
| **Zakon Feniksa** | **Cmentarz** | Zakup: `440 G` <br> <small>Sprzedaż: `220 G`</small> | • Teren surowy: `35 G` <br> • Z 1 Chatką: `180 G` <br> • Z 2 Chatkami: `500 G` <br> • Z 3 Chatkami: `1400 G` <br> • Z 4 Chatkami: `1750 G` <br> • Z Zamkiem: `2100 G` | Chatka: `300 G` <br> Zamek: `300 G` |
| **Zakon Feniksa** | **Kwatera Zakonu** | Zakup: `440 G` <br> <small>Sprzedaż: `220 G`</small> | • Teren surowy: `35 G` <br> • Z 1 Chatką: `180 G` <br> • Z 2 Chatkami: `500 G` <br> • Z 3 Chatkami: `1400 G` <br> • Z 4 Chatkami: `1750 G` <br> • Z Zamkiem: `2100 G` | Chatka: `300 G` <br> Zamek: `300 G` |
| **Zakon Feniksa** | **Ministerstwo Magii** | Zakup: `480 G` <br> <small>Sprzedaż: `240 G`</small> | • Teren surowy: `41 G` <br> • Z 1 Chatką: `200 G` <br> • Z 2 Chatkami: `600 G` <br> • Z 3 Chatkami: `1500 G` <br> • Z 4 Chatkami: `1850 G` <br> • Z Zamkiem: `2200 G` | Chatka: `300 G` <br> Zamek: `300 G` |
| **Książę Półkrwi** | **Pokój Życzeń** | Zakup: `520 G` <br> <small>Sprzedaż: `260 G`</small> | • Teren surowy: `45 G` <br> • Z 1 Chatką: `220 G` <br> • Z 2 Chatkami: `660 G` <br> • Z 3 Chatkami: `1600 G` <br> • Z 4 Chatkami: `1950 G` <br> • Z Zamkiem: `2300 G` | Chatka: `300 G` <br> Zamek: `300 G` |
| **Książę Półkrwi** | **Magiczne Dowcipy Weasleyów** | Zakup: `520 G` <br> <small>Sprzedaż: `260 G`</small> | • Teren surowy: `45 G` <br> • Z 1 Chatką: `220 G` <br> • Z 2 Chatkami: `660 G` <br> • Z 3 Chatkami: `1600 G` <br> • Z 4 Chatkami: `1950 G` <br> • Z Zamkiem: `2300 G` | Chatka: `300 G` <br> Zamek: `300 G` |
| **Książę Półkrwi** | **Borgin i Burkes** | Zakup: `560 G` <br> <small>Sprzedaż: `280 G`</small> | • Teren surowy: `50 G` <br> • Z 1 Chatką: `240 G` <br> • Z 2 Chatkami: `720 G` <br> • Z 3 Chatkami: `1700 G` <br> • Z 4 Chatkami: `2050 G` <br> • Z Zamkiem: `2400 G` | Chatka: `300 G` <br> Zamek: `300 G` |
| **Insygnia Śmierci I** | **Wieża Astronomiczna** | Zakup: `600 G` <br> <small>Sprzedaż: `300 G`</small> | • Teren surowy: `55 G` <br> • Z 1 Chatką: `260 G` <br> • Z 2 Chatkami: `780 G` <br> • Z 3 Chatkami: `1900 G` <br> • Z 4 Chatkami: `2200 G` <br> • Z Zamkiem: `2550 G` | Chatka: `400 G` <br> Zamek: `400 G` |
| **Insygnia Śmierci I** | **Dolina Godryka** | Zakup: `600 G` <br> <small>Sprzedaż: `300 G`</small> | • Teren surowy: `55 G` <br> • Z 1 Chatką: `260 G` <br> • Z 2 Chatkami: `780 G` <br> • Z 3 Chatkami: `1900 G` <br> • Z 4 Chatkami: `2200 G` <br> • Z Zamkiem: `2550 G` | Chatka: `400 G` <br> Zamek: `400 G` |
| **Insygnia Śmierci I** | **Dwór Malfoyów** | Zakup: `640 G` <br> <small>Sprzedaż: `320 G`</small> | • Teren surowy: `60 G` <br> • Z 1 Chatką: `300 G` <br> • Z 2 Chatkami: `900 G` <br> • Z 3 Chatkami: `2000 G` <br> • Z 4 Chatkami: `2400 G` <br> • Z Zamkiem: `2800 G` | Chatka: `400 G` <br> Zamek: `400 G` |
| **Insygnia Śmierci II** | **Wielka Sala** | Zakup: `700 G` <br> <small>Sprzedaż: `350 G`</small> | • Teren surowy: `70 G` <br> • Z 1 Chatką: `350 G` <br> • Z 2 Chatkami: `1000 G` <br> • Z 3 Chatkami: `2200 G` <br> • Z 4 Chatkami: `2600 G` <br> • Z Zamkiem: `3000 G` | Chatka: `400 G` <br> Zamek: `400 G` |
| **Insygnia Śmierci II** | **Zakazany Las** | Zakup: `800 G` <br> <small>Sprzedaż: `400 G`</small> | • Teren surowy: `100 G` <br> • Z 1 Chatką: `400 G` <br> • Z 2 Chatkami: `1200 G` <br> • Z 3 Chatkami: `2800 G` <br> • Z 4 Chatkami: `3400 G` <br> • Z Zamkiem: `4000 G` | Chatka: `400 G` <br> Zamek: `400 G` |

<p>3 pole 1 grupy na mapie wzorowanej zajmuje miejsce "income taxi"</p>

---

## 🚂 Domy Hogwartu (Stacje) i 🪄 Media (Narzędzia)

| Typ | Nazwa Pola | Cena | Sprzedaż | Czynsz (Zależny od posiadania) |
| :--- | :--- | :--- | :--- | :--- |
| **Dom** | **Gryffindor** | `400 G` | `200 G` | 1: `50 G` 2: `100 G` 3: `200 G` 4: `400 G` |
| **Dom** | **Hufflepuff** | `400 G` | `200 G` | 1: `50 G` 2: `100 G` 3: `200 G` 4: `400 G` |
| **Dom** | **Ravenclaw** | `400 G` | `200 G` | 1: `50 G` 2: `100 G` 3: `200 G` 4: `400 G` |
| **Dom** | **Slytherin** | `400 G` | `200 G` | 1: `50 G` 2: `100 G` 3: `200 G` 4: `400 G` |
| **Media** | **Mapa Huncwotów** | `300 G` | `150 G` | 1 karta: Rzut x `10` \| 2 karty: Rzut x `20` |
| **Media** | **Tiara Przydziału** | `300 G` | `150 G` | 1 karta: Rzut x `10` \| 2 karty: Rzut x `20` |

---

## 🔮 Mechaniki Specjalne

* **Kapitał Startowy:** `3000 G`.
* **Podwójny czynsz:** Jeśli posiadasz wszystkie pola w danym kolorze (a nie ma na nich budynków), czynsz za "Teren surowy" jest podwojony.
* **Zasady budowy:** Możesz budować tylko po zebraniu kompletu kolorystycznego. Budujesz równomiernie (nie może być różnicy większej niż 1 poziom budowy między polami tej samej grupy).

### 🎁 Insygnia Śmierci (Zamiast Community Chest)
W miejscu skrzyń są odpowiednio pola:
* **Peleryna Niewidka:** Pozwala graczowi natychmiast wybrać dowolne pole na planszy i się na nie przenieść (karta do użycia).
* **Kamień Wskrzeszenia:** Pozwala na natychmiastowe opuszczenie Azkabanu (karta trzymana przez gracza do użycia).
* **Czarna Różdżka:** Pozwala cofnąć dowolnego wybranego gracza na pole START (**Peron 9 i 3/4**).

### 📜 Magia (Zamiast Szans)
Pola Szansy dzielą się na trzy kategorie: **Uroki, Zaklęcia i Eliksiry**.
* **Uroki (Złe):** Zawsze przynoszą negatywny efekt dla gracza, np. klątwy finansowe lub przymusowy ruch wstecz.
* **Zaklęcia i Eliksiry:** Mogą przynosić efekty mieszane lub pozytywne (np. premie galeonów lub ochrona przed opłatami).
