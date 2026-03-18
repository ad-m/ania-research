# 2. Strategia kampanii Facebook Ads (Meta Ads)

## 2.1 Dobór celów kampanii

### Rekomendowane cele kampanii Meta Ads

Przy budżecie ~30 zł/dzień i celu pozyskania klientów na wizyty stacjonarne, rekomendujemy następującą hierarchię celów kampanii:

| Priorytet | Cel kampanii w Meta Ads | Zastosowanie | Dlaczego |
|---|---|---|---|
| **1 (główny)** | **Wiadomości (Messages)** | Generowanie rozmów na Messengerze | Najniższy próg wejścia dla klienta; osobisty kontakt od razu; łatwy do obsługi |
| **2** | **Leady (Lead Generation)** | Formularz kontaktowy | Zbieranie danych bez opuszczania Facebooka; szybkie i wygodne |
| **3** | **Ruch (Traffic)** | Kierowanie na stronę/landing page | Tylko jeśli istnieje dobra strona z formularzem rezerwacji |
| **4** | **Rozpoznawalność (Awareness)** | Budowanie świadomości marki | Dla treści edukacyjnych TOFU; niski koszt dotarcia |

### Ograniczenia Meta dla reklam zdrowotnych (2025–2026)

> **Uwaga krytyczna**: Od stycznia 2025 Meta wprowadziła dodatkowe restrykcje dla reklam dotyczących zdrowia i wellness ([szczegóły](https://ehmresults.com/meta-ad-2025-2026-restrictions-what-healthcare-practices-need-to-know/)). Psychodietetyka łączy zdrowie z psychologią — prawdopodobnie podlega kategorii **Special Ad Categories**.

**Co to oznacza w praktyce:**
- **Nie można** optymalizować kampanii pod zdarzenia Purchase / Add to Cart / Complete Registration
- **Można** optymalizować pod: Lead, Landing Page View, Link Click, Engagement, Messages
- Targetowanie po szczegółowych zainteresowaniach zdrowotnych jest ograniczone
- Kampanię należy oznaczyć jako Special Ad Category "Zdrowie" w Ads Manager

**Praktyczna rekomendacja:** Cel "Wiadomości" i "Leady" działają bez ograniczeń. Cel "Konwersje" wymaga optymalizacji pod dozwolone zdarzenia. Szczegóły konfiguracji → [03-targetowanie-szczegolowe.md](03-targetowanie-szczegolowe.md), sekcja 3.8.

### Dlaczego "Wiadomości" jako cel nr 1?

Dla lokalnego gabinetu zdrowotnego **kampania na wiadomości Messenger jest optymalnym wyborem** z kilku powodów:

1. **Niski próg wejścia** — napisanie wiadomości jest łatwiejsze niż wypełnienie formularza czy zadzwonienie
2. **Osobisty kontakt** — od pierwszej wiadomości budujesz relację; możesz od razu odpowiedzieć na wątpliwości
3. **Wysoka jakość leadów** — osoba, która pisze wiadomość, jest bardziej zaangażowana niż ta, która tylko kliknie
4. **Prosty w obsłudze** — nie potrzebujesz landing page'a, CRM-a ani integracji
5. **Naturalność** — w małym mieście ludzie wolą "pogadać" niż wypełniać formularze
6. **Zgodność z polityką Meta** — cel "Wiadomości" nie podlega ograniczeniom Special Ad Categories

> **Case study branżowy**: Według [Practice Tech Solutions](https://practicetechsolutions.com/facebook-advertising-cases/), lokalne gabinety medyczne, które wcześniej nie korzystały z Facebook Ads, po uruchomieniu kampanii pozyskiwały kilkanaście leadów w pierwszym miesiącu, z usługami wartymi tysiące złotych. Kluczem był **precyzyjny targeting lokalny** i **bezpośredni kontakt z pacjentem**.

### Messenger vs Lead Ads — porównanie

Choć rekomendujemy Messenger jako cel nr 1, warto przetestować oba podejścia w miesiącu 1–2:

| Cecha | Messenger (Wiadomości) | Lead Ads (Formularz) |
|---|---|---|
| **Próg wejścia dla klienta** | Bardzo niski — "napisz wiadomość" | Niski — auto-uzupełniany formularz |
| **Open rate** | ~88% (wiadomości otwierane natychmiast) | N/D (formularz wypełniany od razu) |
| **CTR w wiadomości** | ~56% (bardzo wysoki) | N/D |
| **Jakość leada** | Wysoka — wymaga aktywnego zaangażowania | Średnia — auto-fill może generować "przypadkowe" leady |
| **Średni CVR (healthcare)** | Brak precyzyjnych danych | ~7,72% ([WordStream 2025](https://www.wordstream.com/blog/facebook-ads-benchmarks-2025)) |
| **Łatwość śledzenia** | Trudniejsza — ręczne notowanie z Messengera | Łatwiejsza — dane w Ads Manager, eksport do CRM |
| **Automatyzacja** | Wymaga ręcznej odpowiedzi (lub chatbot) | Automatyczny e-mail/SMS po wypełnieniu |
| **Najlepsze dla** | Małe gabinety z osobistym podejściem | Gabinety z systemem rezerwacji online |

**Rekomendacja:** Zacznij od Messengera (miesiąc 1). W miesiącu 2 uruchom test A/B: Messenger vs Lead Form. Porównaj koszt za lead i konwersję lead→wizyta.

---

## 2.2 Struktura kampanii — rekomendacja

### Zasada: prostota przy małym budżecie

Przy budżecie 30 zł/dzień **najważniejsza zasada to uproszczenie struktury**. Zbyt wiele kampanii, zestawów reklam i wariantów kreacji rozproszy budżet i uniemożliwi algorytmowi Meta optymalizację.

> Zgodnie z [rekomendacjami ekspertów](https://www.fallowdeer.pl/post/optymalny-budzet-reklamowy-w-meta-ads), reklamodawcy powinni upraszczać swoje kampanie, co lepiej współgra z algorytmami AI Meta, poprawia efektywność uczenia i wyniki reklam.

### Rekomendowana struktura — Faza 1 (miesiąc 1–2)

```
KAMPANIA 1: "Świadomość + Edukacja" (TOFU)
├── Budżet: 12 zł/dzień
├── Cel: Rozpoznawalność / Zasięg
├── Zestaw reklam 1: Zainteresowania dietetyczne + lokalizacja
│   ├── Reklama A: Wideo edukacyjne "Czym jest psychodietetyka?"
│   └── Reklama B: Grafika z pytaniem angażującym
└── Zestaw reklam 2: Zainteresowania psychologiczne + lokalizacja
    ├── Reklama A: Post o zajadaniu emocji
    └── Reklama B: Karuzela "5 sygnałów, że jedzenie to nie głód"

KAMPANIA 2: "Pozyskanie klientów" (MOFU/BOFU)
├── Budżet: 18 zł/dzień
├── Cel: Wiadomości (Messenger)
├── Zestaw reklam 1: Zainteresowania dieta/odchudzanie + lokalizacja
│   ├── Reklama A: Opinia zadowolonego klienta + CTA
│   └── Reklama B: "Umów bezpłatną rozmowę wstępną"
└── Zestaw reklam 2: Custom Audience (zaangażowani z fanpage)
    ├── Reklama A: Oferta pierwszej konsultacji
    └── Reklama B: Storytelling — historia klienta
```

### Rekomendowana struktura — Faza 2 (miesiąc 3+)

Po zebraniu danych (min. 1000 kliknięć, 50+ konwersji), dodajemy:

```
KAMPANIA 3: "Retargeting" (BOFU)
├── Budżet: 5–8 zł/dzień (przesunięcie z kampanii 1)
├── Cel: Wiadomości lub Leady
├── Zestaw reklam 1: Retargeting — odwiedzający stronę (ostatnie 30 dni)
│   └── Reklama: "Wciąż się zastanawiasz? Porozmawiajmy"
└── Zestaw reklam 2: Retargeting — zaangażowani w reklamy (ostatnie 14 dni)
    └── Reklama: Social proof + silne CTA
```

---

## 2.3 Strategia przy małym budżecie lokalnym

### Złote zasady kampanii za 30 zł/dzień

#### 1. Maksymalnie 2–3 kampanie jednocześnie

Każda kampania potrzebuje minimum **~50 konwersji tygodniowo**, żeby algorytm Meta mógł się dobrze zoptymalizować (tzw. faza uczenia). Przy 30 zł/dzień rozbijanie budżetu na wiele kampanii sprawia, że żadna nie zbiera wystarczająco danych.

**Praktyczna reguła:** Nie uruchamiaj więcej niż **2 kampanie** w pierwszych 2 miesiącach.

#### 2. Konsoliduj zestawy reklam

Zamiast tworzyć 5 zestawów reklam po 6 zł/dzień, lepiej mieć 2 zestawy po 15 zł/dzień. Więcej danych = szybsza optymalizacja.

#### 3. Advantage+ — kluczowa zmiana w 2025–2026

Meta w 2025–2026 przeszła na model **Advantage+**, który obejmuje znacznie więcej niż tylko umiejscowienia:

- **Advantage+ Placements** — algorytm sam wybiera, gdzie wyświetlić reklamę (Facebook feed, Instagram, Stories, Reels, itp.) ✅ Zawsze włączaj
- **Advantage+ Audience** — algorytm sam dobiera grupę docelową na podstawie Twojej kreacji i danych Pixela. Zamiast ręcznego targetowania po zainteresowaniach, ustawiasz tylko lokalizację + wiek + płeć, a AI Meta robi resztę
- **Advantage+ Creative** — automatyczna optymalizacja kreacji (przycinanie, dodawanie podpisów)

> **Dlaczego to ważne**: Według [danych Meta z 2025](https://brawnmediany.com/blog/how-metas-targeting-works-in-2025-a-complete-guide/), kampanie z Advantage+ Audience mają o **9,7% niższy koszt per lead** niż kampanie z ręcznym targetowaniem. Przy budżecie 30 zł/dzień każdy procent optymalizacji się liczy.

**Praktyczna rekomendacja dla 30 zł/dzień:** Włącz Advantage+ Audience z "sugestiami" (dawniej "szczegółowe targetowanie") zamiast sztywnych zainteresowań. Ustaw: lokalizacja 25 km od Grójca + kobiety 28–50 lat + jako sugestie dodaj 2–3 zainteresowania. Algorytm rozszerzy zasięg tam, gdzie widzi szansę na konwersję.

#### 4. Testuj kreacje, nie grupy

Przy małym budżecie lepiej testować **różne kreacje reklamowe** (teksty, grafiki, wideo) w ramach jednego zestawu reklam, niż tworzyć wiele zestawów z identycznymi reklamami dla różnych grup.

#### 5. Cierpliwość w fazie uczenia — realistyczne oczekiwania

> **Ważne ograniczenie**: Meta wymaga ~50 konwersji tygodniowo na zestaw reklam, aby wyjść z fazy uczenia ([źródło](https://lebesgue.io/facebook-ads/facebook-ads-learning-phase-what-you-need-to-know-2024-update)). Przy budżecie 30 zł/dzień i realnym CPL 60–120 zł, osiągniesz **2–5 leadów tygodniowo** — daleko od 50. Kampania najprawdopodobniej pozostanie w statusie **"Learning Limited"**.

**Czy to problem?** Nie aż tak, jak brzmi. "Learning Limited" oznacza, że algorytm optymalizuje wolniej, ale kampania nadal działa i generuje leady. Większość lokalnych mikro-budżetów pracuje w tym trybie.

**Workaroundy:**
1. **Optymalizuj pod szersze zdarzenie** — zamiast "Lead" optymalizuj pod "Link Click" lub "Landing Page View" (więcej zdarzeń = szybsze uczenie)
2. **Konsoliduj do 1 zestawu reklam** — cały budżet w jednym miejscu
3. **Włącz Advantage+ Audience** — algorytm ma więcej swobody w szukaniu konwersji
4. **Nie modyfikuj ustawień przez minimum 7–14 dni** — każda zmiana resetuje fazę uczenia
5. **Akceptuj "Learning Limited"** — to normalne przy mikro-budżetach; nie oznacza, że kampania nie działa

### Strategia "drabinkowa" (Ladder Strategy)

Rekomendujemy podejście stopniowe:

```
Miesiąc 1:  Jedna kampania na wiadomości (30 zł/dzień)
            → Zbierasz dane, testujesz kreacje, budujesz Custom Audiences

Miesiąc 2:  Kampania na wiadomości (18 zł) + kampania świadomościowa (12 zł)
            → Rozszerzasz zasięg, zasilasz lejek

Miesiąc 3:  Kampania konwersyjna (15 zł) + świadomościowa (10 zł) + retargeting (5 zł)
            → Pełny lejek działa

Miesiąc 4+: Optymalizujesz i skalizujesz to, co działa najlepiej
```

> **Uwaga o spójności**: Powyższa strategia drabinkowa jest rozwinięta szczegółowo (z konkretnymi kwotami i fazami) w [07-budzet-i-harmonogram.md](07-budzet-i-harmonogram.md). W razie rozbieżności, doc 07 jest dokumentem wiodącym dla podziału budżetu.

---

## 2.4 Targetowanie — przegląd strategiczny

### Podejście do targetowania

Przy małym budżecie i lokalnym zasięgu, strategia targetowania powinna być:

1. **Precyzyjna lokalizacyjnie** — promień 25–30 km od Grójca
2. **Umiarkowanie szeroka zainteresowaniami** — nie za wąsko (mały zasięg), nie za szeroko (nieprecyzyjne dotarcie)
3. **Wykorzystująca istniejące zasoby** — Custom Audiences z 2 500 obserwujących
4. **Stopniowo rozbudowywana** — od prostych zainteresowań do Lookalike i retargetingu

### Szacowany zasięg

| Konfiguracja | Szacowany zasięg |
|---|---|
| 25 km od Grójca, 25–55 lat, kobiety | ~30 000–50 000 osób |
| + zainteresowania dietetyczne | ~8 000–15 000 osób |
| Custom Audience (zaangażowani fanpage) | ~2 000–3 000 osób |
| Lookalike 1% z zaangażowanych | ~20 000–40 000 osób |

> **Uwaga**: Przy zasięgu poniżej 5 000 osób kampania może mieć problem z dostarczaniem reklam. Idealny zasięg przy budżecie 30 zł/dzień to **10 000–50 000 osób** w grupie docelowej.

Szczegółowe ustawienia targetowania → patrz [03-targetowanie-szczegolowe.md](03-targetowanie-szczegolowe.md).

---

## 2.5 Harmonogram wdrożenia kampanii

### Tydzień 0 (przygotowanie)

- [ ] Zainstaluj Pixel Facebooka na stronie internetowej gabinetu (instrukcja krok po kroku → [09-praktyczny-poradnik-wdrozenia.md](09-praktyczny-poradnik-wdrozenia.md), §9.1)
- [ ] Skonfiguruj zdarzenia konwersji (np. "Wyślij formularz", "Kliknij telefon")
- [ ] Przygotuj 3–4 warianty kreacji reklamowych (grafiki + teksty)
- [ ] Stwórz Custom Audience z obserwujących fanpage
- [ ] Stwórz Custom Audience z osób zaangażowanych w posty (ostatnie 90 dni)
- [ ] Przygotuj automatyczną odpowiedź na Messengerze (skrypty → [09-praktyczny-poradnik-wdrozenia.md](09-praktyczny-poradnik-wdrozenia.md), §9.3)

### Tydzień 1–2 (start)

- [ ] Uruchom Kampanię 1 (wiadomości) z 2 zestawami reklam
- [ ] Monitoruj codziennie, ale NIE modyfikuj (faza uczenia)
- [ ] Odpowiadaj na wiadomości Messenger w ciągu max 1 godziny

### Tydzień 3–4 (pierwsza optymalizacja)

- [ ] Wyłącz reklamy z najsłabszym CTR/najwyższym kosztem
- [ ] Dodaj 1–2 nowe kreacje do najlepszego zestawu reklam
- [ ] Oceń: czy cel wiadomości się sprawdza? Czy lepiej przejść na leady?

### Miesiąc 2 (rozbudowa)

- [ ] Dodaj Kampanię 2 (świadomość/edukacja)
- [ ] Przetestuj Lookalike Audience (1% z zaangażowanych)
- [ ] Stwórz pierwsze reklamy wideo (nawet prostym telefonem)

### Miesiąc 3+ (pełny lejek)

- [ ] Dodaj kampanię retargetingową
- [ ] Testuj nowe segmenty odbiorców
- [ ] Skaluj to, co daje najlepsze wyniki (koszt/lead)

---

## Źródła

- [Optymalny budżet reklamowy w Meta Ads — Fallow Deer](https://www.fallowdeer.pl/post/optymalny-budzet-reklamowy-w-meta-ads)
- [Facebook Advertising Case Studies for Medical Practices — Practice Tech Solutions](https://practicetechsolutions.com/facebook-advertising-cases/)
- [Facebook CBO Blueprints: Full-Funnel Strategy — Adscook](https://adscook.com/blog/facebook-cbo-blueprints-full-funnel-strategy/)
- [Jak zrobić reklamę na Facebooku dla trenera, fizjoterapeuty i dietetyka — Tomasz Guzik](https://tomaszguzik.pl/reklama-dla-trenera-fizjoterapeuty-dietetyka/)
- [Skuteczna reklama w Meta Ads dla dietetyka — Karolina Kosmalska](https://karoadsy.pl/skuteczna-reklama-w-meta-ads-dla-dietetyka/)
