# 9. Praktyczny poradnik wdrożenia — krok po kroku

> Ten dokument uzupełnia strategię o **konkretne instrukcje wykonawcze**. Jeśli strategia (doc 01–08) mówi CO robić, ten dokument mówi JAK.

---

## 9.1 Instalacja Pixela Facebooka — krok po kroku

### Czym jest Pixel?

Pixel Facebooka to fragment kodu JavaScript, który instalujesz na stronie internetowej gabinetu. Zbiera dane o odwiedzających (anonimowo) i przekazuje je do Meta, umożliwiając:
- Śledzenie konwersji (kto wypełnił formularz, zadzwonił)
- Tworzenie Custom Audiences (retargeting odwiedzających stronę)
- Optymalizację kampanii pod konwersje

### Krok po kroku: WordPress

1. Zaloguj się do **Meta Business Suite** → **Menedżer wydarzeń** (Events Manager)
2. Kliknij **"Połącz źródło danych"** → **"Internet"** → **"Pixel Facebooka"**
3. Nadaj Pixelowi nazwę (np. "Gabinet Psychodietetyczny Grójec")
4. Skopiuj **ID Pixela** (ciąg cyfr, np. 1234567890)
5. W WordPress zainstaluj wtyczkę **PixelYourSite** (darmowa wersja wystarczy)
6. W ustawieniach wtyczki wklej ID Pixela
7. Zapisz i opublikuj

### Krok po kroku: inna strona (Wix, Squarespace, HTML)

1. W Meta Events Manager → Pixel → **"Dodaj kod ręcznie"**
2. Skopiuj cały kod bazowy Pixela
3. Wklej go w sekcję `<head>` na KAŻDEJ stronie
4. Dla Wix: Ustawienia → Tracking & Analytics → Custom → Facebook Pixel
5. Dla Squarespace: Ustawienia → Advanced → Code Injection → Header

### Weryfikacja instalacji

1. Zainstaluj rozszerzenie **Meta Pixel Helper** w Chrome
2. Wejdź na swoją stronę
3. Kliknij ikonę rozszerzenia — powinien pokazać zielony checkmark i "PageView" event
4. W Meta Events Manager sprawdź, czy pojawiły się nowe zdarzenia (może potrwać do 20 min)

### Jakie zdarzenia skonfigurować?

| Zdarzenie | Kiedy się odpala | Jak skonfigurować |
|---|---|---|
| **PageView** | Każda wizyta na stronie | Automatycznie po instalacji Pixela |
| **Lead** | Wysłanie formularza kontaktowego | W PixelYourSite: Events → Add Event → Lead → na stronie "dziękujemy" |
| **Contact** | Kliknięcie w numer telefonu | W PixelYourSite: Events → Click → na linku tel: |
| **ViewContent** | Wejście na stronę cennika/usług | W PixelYourSite: Events → URL contains "/cennik" |

---

## 9.2 Landing page dla psychodietetyka — co powinno zawierać

### Minimalna struktura (one-page)

Jeśli nie masz budżetu na rozbudowaną stronę, jedna strona lądowania wystarczy. Powinna zawierać (w tej kolejności, od góry):

```
1. HERO SECTION (widoczna bez scrollowania)
   ├── Nagłówek: "Diety nie działają. Pomogę Ci zrozumieć, dlaczego jesz."
   ├── Podtytuł: "Psychodietetyk w Grójcu — konsultacje stacjonarne"
   ├── CTA: [Umów bezpłatną rozmowę] → link do Messengera lub formularz
   └── Zdjęcie specjalisty (Twoja twarz, uśmiech, kontakt wzrokowy)

2. PROBLEM (ból klienta)
   ├── "Próbowałaś wielu diet, ale żadna nie działa na dłużej?"
   ├── "Jesz pod wpływem emocji i nie wiesz, jak przestać?"
   └── "Efekt jo-jo, poczucie winy, frustracja?"

3. ROZWIĄZANIE (psychodietetyka)
   ├── Czym jest psychodietetyka (2-3 zdania)
   ├── Jak wygląda współpraca (krok 1, 2, 3)
   └── Dla kogo: "Pomagam osobom, które..."

4. O MNIE (budowanie zaufania)
   ├── Zdjęcie + krótkie bio (2-3 zdania)
   ├── Kwalifikacje (dyplom, certyfikaty — ale nie CV!)
   └── "Dlaczego wybrałam ten zawód" (osobista historia)

5. OPINIE KLIENTÓW (social proof)
   ├── 2-3 cytaty (za zgodą RODO)
   └── Zdjęcie / inicjały / "Klientka, Grójec"

6. FAQ (usuwanie obiekcji)
   ├── "Ile kosztuje wizyta?"
   ├── "Ile trwa wizyta?"
   ├── "Czy muszę ważyć się na wadze?"
   ├── "Gdzie jest gabinet i jak dojechać?"
   └── "Czy przyjmujesz mężczyzn?"

7. CTA KOŃCOWE (ponowne wezwanie do działania)
   ├── "Gotowa na pierwszy krok?"
   ├── [Napisz na Messengerze] lub [Zadzwoń: xxx-xxx-xxx]
   └── Adres gabinetu + mapa Google
```

### Narzędzia do stworzenia landing page

| Narzędzie | Koszt | Dla kogo |
|---|---|---|
| **Canva Website** | 0 zł (darmowa) | Najprostsze, ale ograniczone |
| **WordPress + Elementor** | 0–50 zł/mies. (hosting) | Standardowy wybór, dużo możliwości |
| **Carrd.co** | 0–35 zł/rok | Szybkie, proste one-page |
| **Google Sites** | 0 zł | Darmowe, ale mniej estetyczne |

### Kluczowe zasady

- **Mobile first** — 80%+ ruchu z reklam Facebook to mobile. Strona MUSI dobrze wyglądać na telefonie
- **Szybkość ładowania** — poniżej 3 sekund. Kompresuj zdjęcia (tinypng.com)
- **Jeden CTA** — nie dawaj 5 opcji. Jeden główny przycisk: "Napisz wiadomość" lub "Zadzwoń"
- **Bez menu nawigacyjnego** — landing page to NIE strona firmowa. Jeden cel: konwersja

---

## 9.3 Skrypty konwersacyjne na Messengerze

### Automatyczna wiadomość powitalna (Instant Reply)

Ustaw w: Fanpage → Ustawienia → Wiadomości → Instant Reply

```
Cześć! Cieszę się, że piszesz.

Jestem [imię], psychodietetyk w Grójcu.

Żeby jak najlepiej Ci pomóc, napisz:
1. Jak masz na imię?
2. Z czym chciałabyś/chciałbyś pracować? (np. odchudzanie, relacja z jedzeniem, zajadanie emocji)

Odezwę się osobiście, najczęściej w ciągu 1–2 godzin.
```

### Skrypt: pierwsza odpowiedź (po otrzymaniu wiadomości)

```
Cześć [imię]! Dzięki, że się odezwałaś/eś.

[Nawiąż do tego, co napisali, np.:]
"Rozumiem — wiele osób, z którymi pracuję, mierzyło się z tym samym."

Psychodietetyka to praca nie tylko z jadłospisem, ale przede wszystkim
z nawykami i emocjami związanymi z jedzeniem.

Pierwsza konsultacja trwa ok. 50 minut i wygląda tak:
→ Rozmawiamy o Twojej historii z jedzeniem
→ Razem szukamy, co stoi za problemem
→ Ustalam, czy i jak mogę Ci pomóc

Wizyta kosztuje [kwota] zł.

Mam wolne terminy w [dzień/dni].
Który pasowałby Ci najbardziej?
```

### Skrypt: obiekcja "ile to kosztuje?"

```
Wizyta trwa ok. 50 minut i kosztuje [kwota] zł.

Jeśli chcesz, mogę najpierw opowiedzieć Ci trochę więcej
o tym, jak wygląda współpraca — żebyś mogła zdecydować,
czy to jest coś dla Ciebie. Bez żadnych zobowiązań.

Czy chciałabyś się umówić na pierwszą rozmowę?
```

### Skrypt: obiekcja "muszę się zastanowić"

```
Jasne, rozumiem. Decyzja o rozpoczęciu pracy nad sobą
to duży krok i nie ma żadnego pośpiechu.

Jeśli będziesz mieć jakiekolwiek pytania — pisz śmiało.
Jestem tu, kiedy będziesz gotowa/y.
```

**Follow-up po 3 dniach (jeśli nie odpisali):**
```
Cześć [imię]! Piszę, bo chciałam się upewnić,
że moja wiadomość dotarła.

Jeśli masz jakieś pytania, z chęcią odpowiem.
A jeśli zdecydowałaś, że to nie teraz — też jest OK.

Pozdrawiam, [imię specjalisty]
```

**Follow-up po 7 dniach (ostatni):**
```
Cześć [imię], wracam z krótką wiadomością.

Jeśli kiedykolwiek poczujesz, że chcesz popracować
nad swoją relacją z jedzeniem — wystarczy napisać.

Życzę Ci wszystkiego dobrego! [imię]
```

### Skrypt: obiekcja "wstydzę się"

```
Naprawdę rozumiem to uczucie.
Wiele osób, które do mnie przychodzą, czuło się dokładnie tak samo.

W moim gabinecie nie ma oceniania. Nie ważymy się na wejściu.
Nie będę mówić Ci, co "musisz" jeść.
Rozmawiamy — i tyle.

Mogę Ci zagwarantować, że będziesz czuła się bezpiecznie.
Czy chciałabyś spróbować?
```

### Skrypt: "Nie jestem z Grójca, czy mogę dojechać?"

```
Oczywiście! Wielu moich klientów dojeżdża
z [Warki / Nowego Miasta / Mogielnicy / okolic].

Gabinet jest w centrum Grójca, przy [ulica].
Dojazd z [miejscowość] to ok. [X] minut samochodem.
Parking jest [opis parkingu].

Czy chciałabyś umówić termin?
```

---

## 9.4 Zarządzanie no-show i retencja klientów

### Problem: klient umówił wizytę, ale nie przyszedł

Typowy wskaźnik no-show w gabinetach: **15–25%**. Przy 6 umówionych wizytach/miesiąc to 1–2 stracone sloty.

### System przypomnień (minimalizacja no-show)

| Kiedy | Kanał | Treść |
|---|---|---|
| **48h przed wizytą** | SMS | "Przypomnienie: Twoja wizyta u psychodietetyka [imię] w [dzień] o [godzina]. Adres: [adres]. Potwierdź odpowiadając TAK lub odwołaj." |
| **24h przed wizytą** | Messenger | "Cześć [imię]! Przypominam o jutrzejszej wizycie o [godzina]. Do zobaczenia! Jeśli coś się zmieniło — daj znać." |
| **2h przed wizytą** | SMS (opcjonalnie) | "Za 2h Twoja wizyta u [imię]. Adres: [adres]. Zapraszam!" |

### Co robić po no-show

1. **W dniu no-show (tego samego dnia):**
   ```
   Cześć [imię], widzę że nie udało Ci się dotrzeć na dzisiejszą wizytę.
   Mam nadzieję, że wszystko w porządku!
   Chętnie umówię nowy termin — daj znać, kiedy Ci pasuje.
   ```

2. **Po 3 dniach bez odpowiedzi:**
   ```
   Cześć [imię], piszę jeszcze raz.
   Jeśli chcesz umówić nowy termin — jestem do dyspozycji.
   Jeśli zmieniłaś zdanie — też jest OK, rozumiem.
   ```

3. **Po 7 dniach:** Nie kontaktuj więcej. Osoba trafi do Custom Audience "nie umówili" i zobaczy reklamy retargetingowe.

### Zasady dotyczące no-show

- **Nigdy nie karż finansowo** za pierwszy no-show (niszczy zaufanie)
- **Wprowadź politykę odwoływania** po 2+ no-show: "Proszę o odwołanie min. 24h przed wizytą"
- **Zapisuj no-show** w swojej tabelce — jeśli osoba zrobiła 3+ no-show, nie umawiaj kolejnej
- **Analizuj wzorce** — no-show częstsze w poniedziałki? wieczorem? po dłuższej przerwie?

### Retencja po pierwszej wizycie

Dropout po pierwszej wizycie: **30–40%** (dane branżowe). Jak zmniejszyć?

| Działanie | Kiedy | Treść |
|---|---|---|
| **Podsumowanie wizyty** | W dniu wizyty (wieczorem) | SMS/Messenger: "Dziękuję za dzisiejszą wizytę! Podsumowanie naszych ustaleń: [1-2 zdania]. Następna wizyta: [data]. Jeśli masz pytania — pisz!" |
| **Check-in** | 3–5 dni po wizycie | "Cześć [imię]! Jak się czujesz po naszej rozmowie? Czy udało się spróbować [cokolwiek ustalone]?" |
| **Przypomnienie o następnej wizycie** | 48h przed kolejną | Standardowe przypomnienie |

---

## 9.5 Szablon śledzenia leadów i budżetu

### Tabelka leadów (Google Sheets / Excel)

Stwórz arkusz z kolumnami:

| Data | Źródło | Imię | "Skąd o nas?" | Temat | Odpowiedź (czas) | Status | Data wizyty | Wizyta odbyta? | Wartość | Uwagi |
|---|---|---|---|---|---|---|---|---|---|---|
| 15.03 | Messenger (reklama) | Anna K. | "Z reklamy na FB" | Efekt jo-jo | 45 min | Umówiła ✅ | 20.03 | Tak ✅ | 200 zł | Planuje kolejną wizytę |
| 16.03 | Messenger (reklama) | Kasia M. | "Widziałam post" | Zajadanie emocji | 2h | Pytała o cenę, nie odpisała ❌ | — | — | 0 zł | Follow-up 19.03 |
| 18.03 | Telefon | Marek W. | "Żona znalazła na FB" | Cholesterol | — | Umówił ✅ | 22.03 | No-show ❌ | 0 zł | Wysłano wiadomość 22.03 |

**Statusy leadów:**
- Nowy — dopiero napisał
- W rozmowie — trwa wymiana wiadomości
- Umówiony — wizyta zarezerwowana
- Wizyta odbyta — przyszedł
- Utracony — nie odpowiada / zrezygnował
- No-show — nie przyszedł na wizytę

### Tabelka budżetowa (miesięczna)

| Tydzień | Wydatki Meta | Leady (Meta) | Leady (rzeczywiste) | Wizyty umówione | Wizyty odbyte | Przychód | ROAS* |
|---|---|---|---|---|---|---|---|
| Tydzień 1 | 210 zł | 2 | 3 | 1 | 1 | 200 zł | — |
| Tydzień 2 | 210 zł | 3 | 3 | 2 | 2 | 400 zł | — |
| Tydzień 3 | 210 zł | 2 | 4 | 1 | 1 | 200 zł | — |
| Tydzień 4 | 210 zł | 3 | 3 | 2 | 1 | 200 zł | — |
| **SUMA** | **840 zł** | **10** | **13** | **6** | **5** | **1 000 zł** | **1,2x** |

*ROAS w miesiącu 1 nie uwzględnia LTV. Po kilku miesiącach klienci wracają i realny ROAS rośnie.

**Kolumna "Leady (rzeczywiste)"** — to leady, które faktycznie otrzymałeś (z Messengera, telefonu, polecenia) — mogą być WYŻSZE niż leady raportowane przez Meta (patrz [06-optymalizacja-i-testy.md](06-optymalizacja-i-testy.md), sekcja 6.6 o atrybucji).

### Miesięczne podsumowanie

Na koniec każdego miesiąca odpowiedz na pytania:

1. **Ile wydałem?** [kwota] zł / budżet [kwota] zł
2. **Ile leadów z reklam?** [Meta] vs [rzeczywiste]
3. **Ile wizyt umówionych?** [liczba] (konwersja: [%])
4. **Ile wizyt odbyło się?** [liczba] (no-show: [%])
5. **Jaki przychód wygenerowały reklamy?** [kwota] zł (miesiąc 1) + [szacunek] zł (przyszłe wizyty)
6. **Która reklama działała najlepiej?** [nazwa, CTR, CPL]
7. **Co zmieniam w następnym miesiącu?** [1-3 konkretne działania]

---

## 9.6 Plan tygodnia 1 — dzień po dniu

### Przed startem (Dzień -3 do -1)

| Dzień | Czas | Zadanie |
|---|---|---|
| **Dzień -3** | 2h | Zainstaluj Pixel (§9.1). Stwórz Custom Audience "Zaangażowani fanpage 180 dni" w Ads Manager |
| **Dzień -2** | 2h | Przygotuj 3 grafiki w Canva (1080x1350px). Napisz 2 warianty tekstu reklamy |
| **Dzień -1** | 1h | Ustaw auto-odpowiedź na Messengerze (§9.3). Stwórz tabelkę leadów (§9.5). Dodaj metodę płatności w Ads Manager |

### Tydzień 1 (start kampanii)

| Dzień | Czas | Zadanie | Szczegóły |
|---|---|---|---|
| **Dzień 1 (pon)** | 1,5h | Uruchom Kampanię 1 | Cel: Wiadomości. Budżet: 30 zł/dzień. Zestaw reklam: Custom Audience (zaangażowani) + Advantage+ Audience z lokalizacją 25 km, kobiety 28–50. Dodaj 2–3 reklamy (różne grafiki + teksty). SAC: Zdrowie ✅ |
| **Dzień 1** | 15 min | Sprawdź po 2h | Czy kampania jest "Aktywna"? Czy pojawiają się wyświetlenia? Jeśli "W trakcie przeglądu" — normalne, poczekaj do 24h |
| **Dzień 2 (wt)** | 15 min | Sprawdź Ads Manager | Ile wyświetleń? Ile kliknięć? Czy są wiadomości? Zapisz w tabelce. Odpowiedz na wiadomości |
| **Dzień 3 (śr)** | 15 min | Sprawdź i odpowiedz | To samo co Dzień 2. NIE ZMIENIAJ NICZEGO W KAMPANII |
| **Dzień 4 (czw)** | 15 min | Sprawdź i odpowiedz | Jeśli 0 wyświetleń przez 3 dni → sprawdź, czy kampania nie jest odrzucona (Powiadomienia w Ads Manager) |
| **Dzień 5 (pt)** | 30 min | Mini-przegląd | Zapisz: CTR, CPC, liczba wiadomości. Porównaj z benchmarkami. NIE ZMIENIAJ NICZEGO |
| **Dzień 6–7 (sob-nd)** | 10 min/dzień | Odpowiedz na wiadomości | Nawet w weekend — ludzie scrollują FB w niedzielę |

### Czego NIE robić w tygodniu 1

- Nie zmieniaj budżetu
- Nie wyłączaj reklam (chyba że CTR = 0% po 5 dniach)
- Nie dodawaj nowych kreacji
- Nie zmieniaj targetowania
- Nie panikuj, jeśli CPL jest wysoki — to normalne w fazie uczenia

### Troubleshooting tygodnia 1

| Problem | Możliwa przyczyna | Co zrobić |
|---|---|---|
| "Kampania w trakcie przeglądu" od 48h | Reklama mogła być odrzucona | Sprawdź Powiadomienia; jeśli odrzucona → zmień treść/grafikę i wyślij ponownie |
| 0 wyświetleń po 3 dniach | Grupa za mała / problem z płatnością | Sprawdź: (1) czy płatność przeszła, (2) czy zasięg grupy >5000, (3) czy SAC dobrze oznaczona |
| Dużo wyświetleń, 0 kliknięć | Kreacja nie przyciąga uwagi | Poczekaj do dnia 7; jeśli CTR <0,3% → zmień grafikę |
| Wiadomości, ale same "Cześć" bez dalszej rozmowy | Auto-odpowiedź nie angażuje | Popraw auto-odpowiedź (§9.3); dodaj pytanie otwarte |
| Wiadomości, ale nikt nie umawia wizyty | Brak follow-upu / za wolna odpowiedź | Odpowiadaj w ciągu 1–2h; użyj skryptów z §9.3 |

---

## 9.7 Produkcja kreacji telefonem — praktyczne wskazówki

### Minimalny zestaw do nagrywania wideo

| Element | Rekomendacja | Koszt |
|---|---|---|
| **Telefon** | Dowolny smartfon z 2021+ (iPhone 12+, Samsung S21+, Xiaomi itp.) | Już masz |
| **Statyw na telefon** | Statyw ze stojakiem na biurko (np. z Allegro, "statyw do telefonu") | 30–60 zł |
| **Światło** | Naturalne światło z okna (najlepsze). Alternatywnie: ring light LED | 0–80 zł |
| **Mikrofon** | Wbudowany w telefon wystarczy, ale mikrofon krawatowy poprawi dźwięk znacząco | 40–80 zł |
| **Tło** | Czysta ściana lub gabinet (naturalny, niestaged) | 0 zł |

### Zasady nagrywania

1. **Pionowo** (9:16) — do Reels, Stories, reklam na mobile
2. **Twarz w centrum** — kontakt wzrokowy z kamerą (nie w bok!)
3. **Dobry dźwięk > dobry obraz** — nagrywaj w cichym miejscu. Unikaj echa (dywan/meble tłumią)
4. **Światło z przodu** — stań twarzą do okna. NIGDY tyłem do okna (ciemna twarz)
5. **Haczyk w pierwszych 3 sekundach** — "Czy wiesz, że 95% diet nie działa?" (nie zaczynam od "Cześć, jestem...")
6. **Napisy** — 80% osób ogląda bez dźwięku. Dodaj napisy w Capcut (darmowa apka) lub CapCut Web
7. **Długość** — 15–60 sek na Reels. 30–90 sek na reklamę w feedzie
8. **Naturalne, nie perfekcyjne** — autentyczne wideo z telefonu > profesjonalne i sztywne

### Priorytety produkcji (co nagrać NAJPIERW)

| Priorytet | Typ wideo | Czas produkcji | Dlaczego najpierw |
|---|---|---|---|
| **1** | "Czym jest psychodietetyka?" (30–60 sek) | 30 min | Podstawa — edukuje rynek |
| **2** | "Jak wygląda pierwsza wizyta?" (30–60 sek) | 30 min | Usuwa barierę strachu |
| **3** | 3 krótkie tipy (15 sek każdy) | 45 min | Content do rotacji w reklamach |
| **4** | Opinia klienta (za zgodą) | 20 min | Social proof — najsilniejszy format |

### Grafiki w Canva

1. Wejdź na **canva.com** → Utwórz design → "Instagram Post (1080x1350)"
2. Wybierz szablon o spokojnej kolorystyce (beże, zielenie, pastele)
3. Dodaj nagłówek (max 6 słów na grafice — resztę w tekście reklamy)
4. Dodaj swoje zdjęcie lub spokojne zdjęcie tła
5. Dodaj "📍 Grójec" w rogu
6. Pobierz jako PNG
7. **Powtórz 3 razy** z różnymi nagłówkami → masz 3 kreacje do testowania

---

## 9.8 Obsługa obiekcji cenowych i kwalifikacja leadów

### Obiekcja: "To za drogo"

**Nie obniżaj ceny.** Zamiast tego:

```
Rozumiem, że to inwestycja. Wizyta kosztuje [kwota] zł
i trwa ok. 50 minut.

Wiele moich klientek mówi, że wydały więcej pieniędzy
na diety pudełkowe, suplementy i programy odchudzania,
które nie zadziałały.

Psychodietetyka pracuje z PRZYCZYNĄ problemu,
nie tylko z objawami. Dlatego efekty są trwalsze.

Czy chciałabyś umówić jedną wizytę na próbę?
Żadnych zobowiązań — po niej zdecydujesz.
```

### Obiekcja: "Nie mam czasu"

```
Rozumiem — wiem, że dzień jest krótki.

Wizyta trwa 50 minut, raz na 2 tygodnie.
Mam terminy wieczorne i w soboty, żeby łatwiej było dopasować.

Czy mam sprawdzić wolne terminy w [dniu]?
```

### Kiedy lead NIE jest Twoim klientem

Nie każdy lead będzie idealnym klientem. Rozpoznaj sygnały:

| Sygnał | Co robić |
|---|---|
| Pyta tylko o cenę i nie reaguje na wyjaśnienia | Podziękuj i zakończ rozmowę grzecznie |
| Szuka "cudownej diety na 2 tygodnie" | Wyjaśnij, że psychodietetyka to proces; jeśli szuka szybkich efektów — nie pasujesz |
| Opisuje poważne zaburzenie psychiczne (anoreksja, bulimia ciężka) | Skieruj do psychiatry/psychologa klinicznego: "Chcę Ci pomóc jak najlepiej. Myślę, że w Twojej sytuacji warto najpierw porozmawiać z [specjalistą]. Mogę polecić [kontakt]." |
| Agresywny / wymagający natychmiastowej odpowiedzi | Odpowiedz spokojnie, ustaw granice. Nie musisz pracować z każdym |

---

## 9.9 Content calendar — synergia organic + paid

### Tygodniowy plan postów (organic)

| Dzień | Typ posta | Przykład | Cel |
|---|---|---|---|
| **Poniedziałek** | Edukacyjny | "3 sygnały, że problem to emocje, nie dieta" | Budowanie Custom Audience (zaangażowani) |
| **Środa** | Angażujący | "A Ty? Co najchętniej jesz pod wpływem stresu? Napisz w komentarzu!" | Budowanie zaangażowania → algorytm nagradza |
| **Piątek** | Osobisty/storytelling | "Dzisiaj w gabinecie miałam piękny moment..." (bez danych klienta) | Budowanie relacji, ludzki wymiar |
| **Sobota** | Social proof / oferta | Opinia klienta LUB "Wolne terminy w przyszłym tygodniu" | Konwersja obserwujących → klienci |

### Jak organic wspiera paid

```
ORGANIC (darmowy)              →  PAID (30 zł/dzień)
Post edukacyjny (pon)          →  Najlepszy post → promuj jako reklamę
                                  (jeśli CTR organiczny > 3%)
Post angażujący (śr)           →  Osoby reagujące → Custom Audience
                                  → retargeting z ofertą
Reel/wideo (kiedy masz)       →  Osoby, które obejrzały 75%
                                  → Custom Audience → retargeting
```

**Złota zasada:** Publikuj 3–4 posty organiczne tygodniowo. Najlepsze (z najwyższym zaangażowaniem) promuj jako reklamy. To tańsze niż tworzenie reklam od zera, bo algorytm widzi, że post już "działa".

---

## Źródła

- [PixelYourSite — instalacja Pixela na WordPress](https://www.pixelyoursite.com/)
- [Meta Events Manager — oficjalna dokumentacja](https://www.facebook.com/business/help/952192354843755)
- [Canva — darmowe szablony reklam](https://www.canva.com/templates/?query=facebook-ad)
- [CapCut — darmowy edytor wideo z napisami](https://www.capcut.com/)
- [Healthcare Facebook Ads: 18 Strategies — Linear Design](https://lineardesign.com/blog/healthcare-facebook-ads/)
