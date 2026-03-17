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
| **CPL (Cost Per Lead)** | Koszt pozyskania leada/wiadomości | 30–80 zł | >100 zł = problem z lejkiem |
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

Przykład:
- Wydano: 900 zł/miesiąc
- Pozyskano: 8 leadów → 4 wizyty (konwersja 50%)
- Wartość wizyty: 200 zł
- Przychód: 4 × 200 zł = 800 zł
- ROAS: 800/900 = 0,89x (na pierwszy rzut oka — strata!)

ALE: klient wraca na kolejne wizyty!
- Średnio 5 wizyt na klienta × 200 zł = 1 000 zł LTV
- ROAS z uwzględnieniem LTV: (4 × 1000) / 900 = 4,4x ✅
```

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

### Zasada 1: Wyłączaj słabych, wzmacniaj mocnych

Co tydzień sprawdzaj wyniki i:

| Sytuacja | Akcja |
|---|---|
| Reklama ma CTR < 0,5% po 7 dniach | Wyłącz — kreacja nie działa |
| Reklama ma CTR > 2% i niski CPC | Zostaw — działa dobrze |
| Zestaw reklam ma CPL > 100 zł po 14 dniach | Wyłącz lub zmień kreacje |
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

## Źródła

- [Benchmarki Facebook Ads 2026 — kcmobile.pl](https://kcmobile.pl/baza-wiedzy/facebook-ads/benchmarki-facebook-ads-srednie-wyniki-branze/)
- [Meta Ads Benchmarks 2026 — Enrich Labs](https://www.enrichlabs.ai/blog/meta-ads-benchmarks-2025)
- [Facebook Ads Benchmarks 2025 — WordStream](https://www.wordstream.com/blog/facebook-ads-benchmarks-2025)
- [Jak czytać statystyki w Meta Ads Manager — Studio7P](https://studio7p.com/blog/jak-czytac-statystyki-w-meta-ads-manager/)
- [Optymalny budżet w Meta Ads — Fallow Deer](https://www.fallowdeer.pl/post/optymalny-budzet-reklamowy-w-meta-ads)
