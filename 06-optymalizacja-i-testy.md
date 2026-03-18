# 6. Optymalizacja i testy kampanii

## 6.1 Kluczowe metryki do monitorowania

### Dashboard dzienny — co sprawdzać codziennie

| Metryka | Co oznacza | Dobry wynik | Alarm |
|---|---|---|---|
| **Wydatki** | Ile wydano dzisiaj | Zgodne z budżetem (30 zł) | Znacząco powyżej lub poniżej |
| **Wyświetlenia** | Ile razy reklama została wyświetlona | >500/dzień | <100/dzień (problem z dostarczaniem) |
| **Nowe wiadomości** | Liczba wiadomości na Messengerze | ≥1/dzień | 0 przez 3+ dni |

### Dashboard tygodniowy — co analizować co tydzień

| Metryka | Definicja | Benchmark (PL, branża zdrowotna) | Jak interpretować |
|---|---|---|---|
| **CTR (Click-Through Rate)** | % osób, które kliknęły w reklamę | >1,5% (dobrze), >2,5% (świetnie) | Niski CTR = słaba kreacja lub złe targetowanie |
| **CPC (Cost Per Click)** | Koszt jednego kliknięcia | 1,50–3,00 zł | >4 zł = drogo, optymalizuj |
| **CPM (Cost Per Mille)** | Koszt 1000 wyświetleń | 8–20 zł | >30 zł = za wąska/konkurencyjna grupa |
| **CPL (Cost Per Lead)** | Koszt pozyskania leada/wiadomości | 60–120 zł | >150 zł = problem z lejkiem |
| **Częstotliwość (Frequency)** | Ile razy średnio osoba widziała reklamę | 1,5–3,0 w ciągu 7 dni | >4 = zmęczenie reklamą (ad fatigue) |
| **Zasięg (Reach)** | Unikalne osoby, które widziały reklamę | Rośnie z tygodnia na tydzień | Spada = audience się wyczerpuje |

### Dashboard miesięczny — co raportować co miesiąc

| Metryka | Definicja | Cel (miesiąc 1) | Cel (miesiąc 3+) |
|---|---|---|---|
| **Liczba leadów** | Wiadomości + formularze + telefony z reklam | 8–15 | 15–25 |
| **Konwersja lead → wizyta** | % leadów, które umówiły wizytę | 25–40% | 35–50% |
| **CPA (Cost Per Acquisition)** | Koszt pozyskania klienta na wizytę | <150 zł | <100 zł |
| **ROAS** | Zwrot z wydatków reklamowych | — | Każda wizyta warta 150–300 zł → ROAS >1,5x |
| **Łączne wydatki** | Suma wydatków reklamowych | ~900 zł | ~900 zł |
| **Liczba wizyt z reklam** | Ile wizyt wygenerowała kampania | 3–6 | 8–12 |

### Jak liczyć ROAS dla gabinetu

```
ROAS = Przychód z wizyt / Koszt reklam

Przykład (realistyczny scenariusz):
- Wydano: 900 zł/miesiąc
- Pozyskano: 10 leadów → 3 wizyty (konwersja 30%)
- Wartość wizyty: 200 zł
- Przychód w miesiącu 1: 3 × 200 zł = 600 zł
- ROAS miesiąc 1: 600/900 = 0,67x (na pierwszy rzut oka — strata!)

ALE: klient wraca na kolejne wizyty!
- Średnie LTV z uwzględnieniem dropout: ~740 zł (patrz kalkulacja w 07-budzet-i-harmonogram.md)
- ROAS z uwzględnieniem LTV: (3 × 740) / 900 = 2,5x
- Po optymalizacji (miesiąc 3+, konwersja 40%): (4 × 740) / 900 = 3,3x ✅
```

> **Uwaga o konwersji lead→wizyta:** Wskaźnik 25–35% jest typowy dla pierwszych miesięcy kampanii. Po optymalizacji procesu odpowiedzi (szybkość reakcji na Messengerze, follow-up po 24h, skrypt rozmowy) można osiągnąć 40–50%. Kluczowy czynnik: **czas odpowiedzi** — odpowiedź w ciągu 1h zwiększa konwersję 3–5x w porównaniu do odpowiedzi po 24h.

> **Kluczowy wniosek**: Przy usługach z retencją (jak psychodietetyka, gdzie klient wraca wielokrotnie), nawet pozornie drogi CPA jest opłacalny. Liczy się LTV (Lifetime Value), nie jednorazowa wizyta.

---

## 6.2 Testy A/B — jak prowadzić

### Czym jest test A/B?

Test A/B to porównanie dwóch wariantów reklamy (A i B), aby sprawdzić, który działa lepiej. Kluczowa zasada: **zmieniaj tylko JEDNĄ rzecz na raz**.

### Co testować?

| Element | Priorytet testowania | Przykład testu |
|---|---|---|
| **Kreacja wizualna** | Najwyższy | Zdjęcie specjalisty vs grafika z tekstem |
| **Nagłówek** | Wysoki | "Diety nie działają" vs "Jest inny sposób" |
| **Tekst reklamy** | Wysoki | Krótki (3 zdania) vs długi (akapit) |
| **Format** | Średni | Grafika vs wideo vs karuzela |
| **CTA** | Średni | "Wyślij wiadomość" vs "Dowiedz się więcej" |
| **Grupa docelowa** | Niski (na start) | Zainteresowania vs Lookalike |

### Jak prowadzić test A/B przy 30 zł/dzień

Przy małym budżecie testy A/B wymagają dyscypliny:

#### Metoda 1: Wiele kreacji w jednym zestawie reklam (zalecana)

```
Zestaw reklam (budżet: 18 zł/dzień)
├── Reklama A: Grafika + nagłówek 1
├── Reklama B: Grafika + nagłówek 2
└── Reklama C: Wideo + nagłówek 1
```

Algorytm Meta automatycznie przesunie budżet na najlepszą reklamę. Po 7–10 dniach wyłącz najsłabszą i dodaj nową.

**Zalety:** Algorytm optymalizuje za Ciebie; nie musisz dzielić budżetu.
**Wady:** Mniej kontroli nad dokładnym podziałem budżetu.

#### Metoda 2: Oficjalny test A/B Meta (dla ważnych decyzji)

W Ads Manager → Eksperymenty → Test A/B. Meta automatycznie podzieli ruch 50/50.

**Kiedy używać:** Gdy porównujesz coś fundamentalnego (np. cel kampanii: Wiadomości vs Leady).
**Minimalny czas testu:** 7 dni.
**Minimalny budżet:** 30 zł/dzień na test (= cały budżet dzienny).

#### Metoda 3: Testy sekwencyjne (najpraktyczniejsza dla małego budżetu)

Zamiast testować równolegle (dzieląc budżet), testuj **sekwencyjnie**:

```
Tydzień 1–2: Reklama A (pełny budżet)
→ Zapisz wyniki: CTR, CPC, liczba leadów

Tydzień 3–4: Reklama B (pełny budżet)
→ Porównaj wyniki z Reklamą A

Tydzień 5+: Wygrywa lepsza wersja. Testuj kolejny element.
```

**Zalety:** Każda reklama dostaje pełny budżet; wyraźniejsze wyniki.
**Wady:** Wolniejsze; zmienne zewnętrzne (np. sezonowość) mogą wpływać.

### Harmonogram testów

| Tydzień | Co testujemy | Wariant A | Wariant B |
|---|---|---|---|
| 1–2 | Kreacja | Zdjęcie specjalisty | Grafika z cytatem |
| 3–4 | Nagłówek | "Diety nie działają" | "Jest inny sposób niż dieta" |
| 5–6 | Format | Grafika statyczna | Wideo 30 sek |
| 7–8 | Długość tekstu | Krótki (3 zdania) | Długi (storytelling) |
| 9–10 | CTA | "Wyślij wiadomość" | "Dowiedz się więcej" |

---

## 6.3 Optymalizacja przy małym budżecie — praktyczne wskazówki

> **Kluczowe ograniczenie: "Learning Limited"**: Przy budżecie 30 zł/dzień kampania najprawdopodobniej będzie trwale w statusie **"Learning Limited"** — zbyt mało konwersji (2–5/tydzień) dla pełnej optymalizacji algorytmu Meta (wymóg: ~50/tydzień). To **normalne dla mikro-budżetów** i nie oznacza, że kampania nie działa. Workaroundy:
> 1. **Optymalizuj pod szersze zdarzenie** — "Link Click" lub "Landing Page View" zamiast "Lead" (więcej zdarzeń = szybsze uczenie)
> 2. **Konsoliduj do 1 zestawu reklam** — cały budżet w jednym miejscu, nie rozpraszaj
> 3. **Włącz Advantage+ Audience** — algorytm ma więcej swobody w szukaniu konwersji
> 4. **Porównuj z własną tabelką** — dane Meta mogą być niepełne; prowadź ręczny tracking leadów

### Zasada 1: Wyłączaj słabych, wzmacniaj mocnych

Co tydzień sprawdzaj wyniki i:

| Sytuacja | Akcja |
|---|---|
| Reklama ma CTR < 0,5% po 7 dniach | Wyłącz — kreacja nie działa |
| Reklama ma CTR > 2% i niski CPC | Zostaw — działa dobrze |
| Zestaw reklam ma CPL > 150 zł po 14 dniach | Wyłącz lub zmień kreacje |
| Częstotliwość > 4 w ciągu 7 dni | Odśwież kreację lub rozszerz audience |

### Zasada 2: Nie zmieniaj zbyt często

```
❌ Poniedziałek: zmiana nagłówka
   Wtorek: zmiana grafiki
   Środa: zmiana grupy docelowej
   → Algorytm nigdy nie przejdzie fazy uczenia!

✅ Poniedziałek: uruchomienie reklamy
   Poniedziałek +7 dni: przegląd wyników
   Poniedziałek +14 dni: decyzja o zmianach
   → Algorytm miał czas na optymalizację
```

**Reguła:** Minimum 5–7 dni bez zmian po uruchomieniu/modyfikacji zestawu reklam.

### Zasada 3: Rotacja kreacji co 3–4 tygodnie

Nawet najlepsza reklama traci skuteczność po ~3–4 tygodniach (ad fatigue). Sygnały:
- CTR spada
- CPC rośnie
- Częstotliwość rośnie powyżej 4

**Rozwiązanie:** Co 3 tygodnie przygotuj 1–2 nowe kreacje. Nie musisz wyrzucać starych — wystarczy odświeżyć grafikę lub nagłówek.

### Zasada 4: Optymalizuj czas wyświetlania

Sprawdź w raportach Meta, **o jakiej godzinie i w jakie dni** reklamy mają najlepsze wyniki. Typowo dla branży zdrowotnej:

| Dzień | Najlepsze godziny | Uzasadnienie |
|---|---|---|
| Poniedziałek–Piątek | 19:00–22:00 | Po pracy, wieczorne scrollowanie |
| Niedziela | 10:00–14:00 | Niedzielne planowanie tygodnia |
| Poniedziałek rano | 7:00–9:00 | "Nowy tydzień, nowe postanowienia" |

**Opcja:** Ustaw harmonogram reklam (Ad Scheduling) — wyświetlaj reklamy tylko w najlepszych godzinach, oszczędzając budżet.

### Zasada 5: Testuj cel kampanii

Jeśli kampania na Wiadomości nie przynosi wyników po 3–4 tygodniach, przetestuj:
- **Leady (formularz)** — może jest wygodniejszy
- **Ruch na stronę** — z jasnym CTA i formularzem na landing page
- **Telefon** — reklama z przyciskiem "Zadzwoń"

### Zasada 6: Monitoruj "jakość" leadów

Nie wszystkie leady są równe. Prowadź prostą tabelkę:

| Data | Źródło leada | Imię | Status | Notatki |
|---|---|---|---|---|
| 15.03 | Messenger | Anna K. | Umówiła wizytę ✅ | Segment "efekt jo-jo" |
| 16.03 | Messenger | Kasia M. | Nie odpisała ❌ | Pytała o cenę |
| 18.03 | Formularz | Marek W. | Umówił wizytę ✅ | Segment "lekarz kazał" |

To pomoże Ci zrozumieć:
- Które reklamy generują najlepsze (konwertujące) leady
- Jaki jest realny koszt pozyskania KLIENTA (nie tylko leada)
- Które segmenty odbiorców są najcenniejsze

---

## 6.4 Diagnostyka problemów

### Problem: Reklama się nie wyświetla (niski zasięg)

| Możliwa przyczyna | Rozwiązanie |
|---|---|
| Grupa docelowa za mała (<1 000) | Rozszerz zainteresowania lub promień |
| Budżet za niski dla grupy | Skonsoliduj zestawy reklam |
| Reklama odrzucona przez Meta | Sprawdź Powiadomienia w Ads Manager |
| Faza uczenia | Poczekaj 3–5 dni |

### Problem: Wysoki CTR, ale brak leadów

| Możliwa przyczyna | Rozwiązanie |
|---|---|
| Ludzie klikają z ciekawości, ale nie piszą | Wzmocnij CTA w tekście reklamy |
| Automatyczna wiadomość na Messengerze odstraszająca | Uprość welcome message |
| Strona docelowa (jeśli Traffic) nie konwertuje | Popraw landing page / formularz |

### Problem: Dużo wiadomości, ale mało wizyt

| Możliwa przyczyna | Rozwiązanie |
|---|---|
| Zbyt wolna odpowiedź | Odpowiadaj w ciągu 1h (max 2h) |
| Brak follow-upu | Po 24h bez odpowiedzi → wyślij delikatne przypomnienie |
| Bariera cenowa | Rozważ ofertę "pierwsza rozmowa wstępna gratis" |
| Bariera logistyczna | Podaj dokładny adres, parking, dojazd |

### Problem: Rosnący CPL z tygodnia na tydzień

| Możliwa przyczyna | Rozwiązanie |
|---|---|
| Ad fatigue (zmęczenie reklamą) | Odśwież kreacje |
| Audience się wyczerpuje | Rozszerz grupę lub dodaj nowe zainteresowania |
| Sezonowość | Normalny wzrost w wakacje, spadek po Nowym Roku |
| Konkurencja wzrosła | Sprawdź Auction Overlap; wyróżnij się kreacją |

---

## 6.5 Raportowanie — co i jak raportować

### Szablon raportu tygodniowego

```markdown
## Raport tygodniowy — Facebook Ads
### Tydzień: [data od] – [data do]

**Wydatki:** [kwota] zł / [budżet] zł
**Zasięg:** [liczba] unikalnych osób
**Wyświetlenia:** [liczba]
**Kliknięcia:** [liczba] (CTR: [%])
**CPC:** [kwota] zł
**Nowe wiadomości/leady:** [liczba] (CPL: [kwota] zł)
**Umówione wizyty:** [liczba]

**Najlepsza reklama:** [nazwa] (CTR: [%], CPL: [kwota] zł)
**Najsłabsza reklama:** [nazwa] (CTR: [%], CPL: [kwota] zł)

**Działania na przyszły tydzień:**
- [ ] [akcja 1]
- [ ] [akcja 2]
```

---

## 6.6 Prywatność i śledzenie — iOS, Conversion API, atrybucja

### Problem: iOS 14.5+ i App Tracking Transparency (ATT)

Od kwietnia 2021 (iOS 14.5) użytkownicy iPhone'ów widzą popup pytający o zgodę na śledzenie przez aplikacje. **Około 75–85% użytkowników odmawia.** Dla kampanii Meta Ads oznacza to:

| Aspekt | Wpływ |
|---|---|
| **Pixel Facebooka** | Widzi tylko ~60–70% konwersji z urządzeń Apple |
| **Custom Audiences ze strony** | Mniejsze, mniej precyzyjne (brakuje danych iOS) |
| **Retargeting** | Dociera do mniejszej grupy (nie widzi części odwiedzających) |
| **Lookalike Audiences** | Mniejsza seed audience = mniej precyzyjny Lookalike |
| **Raportowanie konwersji** | Zaniżone — realne wyniki są LEPSZE niż pokazuje Ads Manager |
| **Okno atrybucji** | Skrócone do 7 dni klik / 1 dzień view (dawniej: 28 dni) |

### Co to oznacza dla gabinetu psychodietetycznego?

**Dobra wiadomość:** Kampanie na Messenger i Lead Ads są mniej dotknięte niż kampanie konwersyjne, ponieważ konwersja (wiadomość / formularz) dzieje się WEWNĄTRZ platformy Meta i nie wymaga Pixela.

**Zła wiadomość:** Retargeting odwiedzających stronę (CA 3) i optymalizacja pod konwersje na stronie będą mniej skuteczne bez dodatkowych rozwiązań.

### Conversion API (CAPI) — rozwiązanie problemu iOS

**Czym jest CAPI?** Server-side API, które przesyła dane o konwersjach bezpośrednio z Twojego serwera do Meta. Działa niezależnie od przeglądarki i blokad iOS.

**Dla kogo?** Dla każdego, kto ma stronę internetową i używa Pixela Facebooka.

**Jak wdrożyć (od najprostszego)?**

| Metoda | Trudność | Koszt | Dla kogo |
|---|---|---|---|
| **Wtyczka WordPress** (np. PixelYourSite, Facebook for WordPress) | Łatwa | 0–200 zł/rok | Strony na WordPress |
| **Integracja Zapier/Make** | Średnia | 50–100 zł/mies. | Strony z formularzami |
| **Google Tag Manager Server-Side** | Trudna | 100–200 zł/mies. (serwer) | Zaawansowani |
| **Ręczna implementacja** | Trudna | Jednorazowa praca developera | Niestandardowe strony |

**Dla gabinetu z budżetem 30 zł/dzień:** Jeśli strona jest na WordPress — wtyczka PixelYourSite (darmowa wersja) wystarczy na start. Jeśli nie — zainwestuj 200–400 zł w jednorazową konfigurację przez specjalistę.

### Okna atrybucji — dlaczego raporty Meta zaniżają wyniki

**Domyślne okno atrybucji Meta:** 7 dni po kliknięciu / 1 dzień po wyświetleniu.

**Co to znaczy?** Jeśli klient:
- Kliknął reklamę w poniedziałek
- Przyszedł na stronę w środę
- Napisał na Messengerze w następny poniedziałek (dzień 7) → **Meta policzy tę konwersję** ✅
- Napisał na Messengerze w następny wtorek (dzień 8) → **Meta NIE policzy tej konwersji** ❌

**Problem z lejkiem 4-tygodniowym:** Opisany w [05-lejek-marketingowy.md](05-lejek-marketingowy.md) lejek zakłada 4 tygodnie od pierwszego kontaktu do wizyty. Przy 7-dniowym oknie atrybucji **~60-75% konwersji z TOFU/MOFU nie będzie przypisane** do kampanii w raportach Meta.

### Jak radzić sobie z niedokładną atrybucją?

1. **Prowadź ręczny tracking** — prostą tabelkę (Excel/Google Sheets):

| Data leada | Źródło | Imię | "Skąd o nas?" | Wizyta umówiona? | Wizyta odbyta? |
|---|---|---|---|---|---|
| 15.03 | Messenger | Anna | "Z reklamy na FB" | Tak | Tak |
| 18.03 | Telefon | Marek | "Żona znalazła na FB" | Tak | Tak |
| 20.03 | Formularz | Kasia | "Widziałam post" | Nie | — |

2. **Pytaj klientów "Skąd o nas?"** — to darmowa metoda atrybucji. Dodaj pytanie w formularz lub na Messengerze.

3. **Porównuj dane Meta z rzeczywistością** — co miesiąc porównuj:
   - Ile leadów raportuje Meta?
   - Ile leadów faktycznie otrzymałeś? (mogą być wyższe!)
   - Stosunek "nieprzypisanych" leadów do przypisanych

4. **Zmień okno atrybucji (opcjonalnie)** — w Ads Manager → Kolumny → Okno atrybucji → zmień na 28 dni po kliknięciu (jeśli dostępne). Pokaże pełniejszy obraz, ale **nie wszystkie konfiguracje na to pozwalają** (ograniczenie iOS).

### Podsumowanie: prywatność a mikro-budżet

| Priorytet | Działanie | Koszt | Wpływ |
|---|---|---|---|
| **1 (krytyczny)** | Prowadź ręczny tracking leadów | 0 zł | Pełny obraz konwersji |
| **2 (wysoki)** | Pytaj "skąd o nas?" | 0 zł | Realna atrybucja |
| **3 (średni)** | Zainstaluj CAPI (wtyczka WP) | 0–200 zł | +30–40% widocznych konwersji |
| **4 (niski)** | Zmień okno atrybucji na 28 dni | 0 zł | Pełniejsze raporty |

---

## Źródła

- [Benchmarki Facebook Ads 2026 — kcmobile.pl](https://kcmobile.pl/baza-wiedzy/facebook-ads/benchmarki-facebook-ads-srednie-wyniki-branze/)
- [Meta Ads Benchmarks 2026 — Enrich Labs](https://www.enrichlabs.ai/blog/meta-ads-benchmarks-2025)
- [Facebook Ads Benchmarks 2025 — WordStream](https://www.wordstream.com/blog/facebook-ads-benchmarks-2025)
- [Jak czytać statystyki w Meta Ads Manager — Studio7P](https://studio7p.com/blog/jak-czytac-statystyki-w-meta-ads-manager/)
- [Optymalny budżet w Meta Ads — Fallow Deer](https://www.fallowdeer.pl/post/optymalny-budzet-reklamowy-w-meta-ads)
- [iOS Privacy Changes Impact on Meta Ad Targeting — Adamigo](https://www.adamigo.ai/blog/ios-privacy-changes-impact-on-meta-ad-targeting)
- [Meta Ads, iOS 18 Privacy with AI-Driven Attribution — Dool Agency](https://dool.agency/meta-ads-ios-18-privacy-with-ai-driven-attribution/)
- [Facebook Ads Learning Phase — Lebesgue](https://lebesgue.io/facebook-ads/facebook-ads-learning-phase-what-you-need-to-know-2024-update)
