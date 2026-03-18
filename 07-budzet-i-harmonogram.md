# 7. Budżet i harmonogram

## 7.1 Analiza budżetu: 30 zł/dzień (900 zł/miesiąc)

### Kontekst rynkowy

Budżet 30 zł/dzień to **mikro-budżet** w skali Meta Ads. Dla porównania:

| Typ reklamodawcy | Typowy budżet dzienny |
|---|---|
| Duży e-commerce | 500–5 000 zł |
| Agencja / średnia firma | 100–500 zł |
| Lokalny biznes (miasto 50k+) | 50–150 zł |
| **Lokalny gabinet (małe miasto)** | **20–50 zł** |
| Minimalny sensowny budżet Meta | 10–15 zł |

Przy 30 zł/dzień gabinet mieści się w typowym budżecie dla lokalnego biznesu w małym mieście. To wystarczająca kwota, by **systematycznie pozyskiwać klientów**, pod warunkiem mądrego zarządzania.

### Co można uzyskać za 900 zł/miesiąc?

Szacunki oparte na [benchmarkach dla polskiego rynku zdrowotnego](https://kcmobile.pl/baza-wiedzy/facebook-ads/benchmarki-facebook-ads-srednie-wyniki-branze/) i [case studies polskich kampanii healthcare](https://www.ministerstworeklamy.pl/blog/case-study/case-study-dokonala-kampania-meta-ads-na-pozyskiwanie-kontaktow-formularz/):

> **Case study z PL (healthcare, Śląsk 2024):** Kampania leadowa z formularzem instant osiągnęła CPL **19,39 zł** przy 20 000+ wyświetleń i 28 leadach. 99% wyświetleń z targetowanego regionu. To wskazuje, że przy dobrze zoptymalizowanej kampanii CPL **15–40 zł jest osiągalny** dla lokalnych usług zdrowotnych B2C w Polsce.
>
> **Case study terapeuty (USA 2025):** Kampania wideo na Facebooku/Instagramie osiągnęła CPL **~70 zł** ($17), z leadami pojawiającymi się w ciągu 24h od startu ([PolyAds](https://polayads.com/5-facebook-ad-campaigns-that-work-for-therapists/)).

| Metryka | Optymistyczny scenariusz | Realistyczny scenariusz | Pesymistyczny scenariusz |
|---|---|---|---|
| **Wyświetlenia** | 80 000 | 50 000 | 25 000 |
| **Zasięg (unikalne osoby)** | 25 000 | 12 000 | 6 000 |
| **Kliknięcia** | 450 | 280 | 150 |
| **CPC** | 2,00 zł | 3,20 zł | 6,00 zł |
| **Wiadomości/leady** | 18 | 10 | 5 |
| **CPL** | 50 zł | 90 zł | 180 zł |
| **Umówione wizyty (konwersja ~30%)** | 6 | 3 | 1–2 |
| **CPA (koszt/wizytę)** | 150 zł | 300 zł | 450–900 zł |

### Kalkulacja opłacalności

```
Koszt pozyskania klienta (CPA): ~300 zł (realistyczny scenariusz)
Cena jednej konsultacji: ~150–250 zł
Średnia liczba wizyt na klienta: 4–8 (psychodietetyka to proces)
```

**Scenariusz optymistyczny (bez dropout):**
```
LTV = 6 wizyt × 200 zł = 1 200 zł
ROAS: (3 klientów × 1 200 zł) / 900 zł = 4:1
```

**Scenariusz realistyczny (z dropout 30–40% po 2. wizycie):**
```
Rozkład klientów:
- 60% kończy po 3 wizytach: 3 × 200 zł = 600 zł
- 30% kończy pełny cykl (6 wizyt): 6 × 200 zł = 1 200 zł
- 10% rezygnuje po 1 wizycie: 1 × 200 zł = 200 zł

Średnie LTV = 0.60 × 600 + 0.30 × 1200 + 0.10 × 200 = 740 zł

Przy 3 nowych klientach/miesiąc (realistyczny scenariusz):
= 3 × 740 zł = 2 220 zł przychodu z 900 zł wydatków
= ROAS 2,5:1

Po optymalizacji (miesiąc 3+, 5 klientów/miesiąc):
= 5 × 740 zł = 3 700 zł przychodu z 900 zł wydatków
= ROAS 4,1:1
```

> **Wniosek:** Realny ROAS to **2,5–4x** (nie 8x jak w idealistycznym modelu). Nadal jest to **opłacalna inwestycja**, szczególnie biorąc pod uwagę, że: (1) zadowoleni klienci polecają gabinet, generując darmowe leady, (2) LTV rośnie, jeśli klient wraca po latach z nowym problemem, (3) opinie klientów wzmacniają przyszłe kampanie.
>
> **Ważne:** Powyższe obliczenia zakładają pełną atrybucję. Ze względu na ograniczenia iOS i 7-dniowe okno atrybucji Meta (patrz [06-optymalizacja-i-testy.md](06-optymalizacja-i-testy.md), sekcja 6.6), część konwersji nie będzie widoczna w raportach. Prowadź ręczny tracking.

---

## 7.2 Podział budżetu — rekomendacja

### Faza 1: Miesiąc 1 (start — uczenie się)

**Priorytet: szybkie wyniki + zbieranie danych**

| Kampania | Cel | Budżet dzienny | Budżet miesięczny | % budżetu |
|---|---|---|---|---|
| Kampania na wiadomości (Messenger) | Pozyskanie leadów | 30 zł | 900 zł | 100% |
| **SUMA** | | **30 zł** | **900 zł** | **100%** |

**Dlaczego 100% na jedną kampanię?**
- Cały budżet trafia w jedno miejsce → szybsza faza uczenia
- Szybko sprawdzisz, czy wiadomości Messenger działają
- Zbierzesz Custom Audiences (zaangażowani) do późniejszego retargetingu
- Po 2–4 tygodniach będziesz mieć dane do optymalizacji

> **Uwaga o spójności z lejkiem:** Ten model startowy (100% na jedną kampanię BOFU) celowo różni się od docelowego podziału lejka 40/35/25% (TOFU/MOFU/BOFU) opisanego w [05-lejek-marketingowy.md](05-lejek-marketingowy.md). W miesiącu 1 **świadomie rezygnujemy z lejka**, aby: (1) zebrać dane o tym, co działa, (2) nie rozpraszać algorytmu przy minimalnym budżecie, (3) przetestować czy Messenger/Lead Ads generuje leady. Podział lejka wprowadzamy w Fazie 2, gdy mamy już Custom Audiences i doświadczenie.

### Faza 2: Miesiąc 2–3 (rozbudowa lejka)

**Priorytet: budowanie świadomości + konwersja**

| Kampania | Cel | Budżet dzienny | Budżet miesięczny | % budżetu |
|---|---|---|---|---|
| Edukacja / Świadomość (TOFU) | Wyświetlenia wideo / zasięg | 12 zł | 360 zł | 40% |
| Pozyskanie klientów (MOFU/BOFU) | Wiadomości / leady | 18 zł | 540 zł | 60% |
| **SUMA** | | **30 zł** | **900 zł** | **100%** |

### Faza 3: Miesiąc 4+ (pełny lejek + retargeting)

**Priorytet: optymalizacja + retargeting**

| Kampania | Cel | Budżet dzienny | Budżet miesięczny | % budżetu |
|---|---|---|---|---|
| Edukacja / Świadomość (TOFU) | Zasięg / wideo | 10 zł | 300 zł | 33% |
| Pozyskanie klientów (MOFU/BOFU) | Wiadomości / leady | 15 zł | 450 zł | 50% |
| Retargeting (BOFU) | Wiadomości | 5 zł | 150 zł | 17% |
| **SUMA** | | **30 zł** | **900 zł** | **100%** |

---

## 7.3 Kampania ciągła vs pulsowa

### Opcja A: Kampania ciągła (always-on) — REKOMENDOWANA

**Reklamy wyświetlane codziennie, 30 zł/dzień, non-stop.**

| Zalety | Wady |
|---|---|
| Stały napływ leadów | Budżet rozłożony cienko |
| Algorytm ma czas na optymalizację | Możliwe ad fatigue przy małej grupie |
| Budowanie rozpoznawalności w czasie | Mniej elastyczności |
| Prostsze zarządzanie | |

### Opcja B: Kampania pulsowa (flight scheduling)

**Reklamy wyświetlane w blokach: 2 tygodnie ON → 1 tydzień OFF → 2 tygodnie ON.**

| Zalety | Wady |
|---|---|
| Wyższy budżet w dniach "ON" (~45 zł/dzień) | Przerwy w napływie leadów |
| Mniejsze ryzyko ad fatigue | Algorytm traci optymalizację w przerwie |
| Elastyczność (np. przerwa na urlop) | Trudniejsze planowanie |

### Opcja C: Hybrydowa — ALTERNATYWA

**Bazowa kampania ciągła (20 zł/dzień) + pulsowe wzmocnienia (dodatkowe 20–30 zł/dzień w wybranych tygodniach).**

Najlepszy scenariusz, ale wymaga dodatkowego budżetu (np. 1 100–1 200 zł/miesiąc zamiast 900 zł).

### Rekomendacja

**Kampania ciągła (always-on)** jest lepsza dla gabinetu psychodietetycznego, ponieważ:

1. **Regularność** — klienci potrzebują wielu "dotknięć" z marką zanim podejmą decyzję. Przerwy przerywają lejek.
2. **Algorytm Meta** — działa lepiej przy ciągłych kampaniach. Przerwy resetują fazę uczenia.
3. **Stały napływ** — nawet 2–3 leady tygodniowo to wystarczający pipeline dla jednego specjalisty.
4. **Prostota** — łatwiej zarządzać jedną ciągłą kampanią niż planować pulsacje.

**Jedyny wyjątek:** Pauza kampanii na czas urlopu specjalisty (nie reklamuj, jeśli nie możesz obsłużyć klientów).

---

## 7.4 Kalendarz sezonowy

> **Ważne zastrzeżenie:** Poniższy kalendarz to **hipoteza** oparta na typowych wzorcach branży wellness w Polsce i ogólnej wiedzy o zachowaniach konsumentów. Nie jest poparty danymi Google Trends ani historycznymi danymi kliniki. Zalecamy:
> 1. Weryfikację z [Google Trends](https://trends.google.pl/) — wyszukaj "dietetyk", "odchudzanie", "dieta" dla Polski
> 2. Po pierwszym kwartale kampanii — porównaj z własnymi danymi (liczba leadów/miesiąc)
> 3. Traktuj ten kalendarz jako punkt wyjścia do testów, nie jako dogmat

### Sezonowość popytu na usługi dietetyczne w Polsce (hipoteza)

| Miesiąc | Popyt | Strategia budżetowa | Uwagi |
|---|---|---|---|
| **Styczeń** | Bardzo wysoki | Zwiększ budżet +30–50% | "Noworoczne postanowienia" — najgorętszy miesiąc |
| **Luty** | Wysoki | Utrzymaj zwiększony budżet | Kontynuacja trendu ze stycznia |
| **Marzec** | Wysoki | Standardowy budżet | "Wiosenne przebudzenie", przygotowanie do lata |
| **Kwiecień** | Średni/wysoki | Standardowy budżet | Sezon przedwakacyjny rośnie |
| **Maj** | Wysoki | Zwiększ budżet +20% | "Bikini body" — presja wakacyjna |
| **Czerwiec** | Średni | Standardowy budżet | Początek wakacji |
| **Lipiec** | Niski | Zmniejsz budżet -20% | Wakacje, ludzie mniej myślą o diecie |
| **Sierpień** | Niski/średni | Standardowy budżet | Powroty z wakacji, "od września zaczynam" |
| **Wrzesień** | Wysoki | Zwiększ budżet +30% | "Nowy rok szkolny" — silny impuls do zmian |
| **Październik** | Średni | Standardowy budżet | Stabilny popyt |
| **Listopad** | Średni/niski | Standardowy budżet | Pre-świąteczny spadek |
| **Grudzień** | Niski | Zmniejsz budżet -20% | Okres świąteczny, ludzie "zaczynają od stycznia" |

### Jak dostosować budżet sezonowo

Przy bazowym budżecie 900 zł/miesiąc:

| Miesiąc | Modyfikator | Budżet | Dzienny |
|---|---|---|---|
| Styczeń | +50% | 1 350 zł | 45 zł |
| Wrzesień | +30% | 1 170 zł | 39 zł |
| Maj | +20% | 1 080 zł | 36 zł |
| Lipiec | -20% | 720 zł | 24 zł |
| Grudzień | -20% | 720 zł | 24 zł |
| Pozostałe | 100% | 900 zł | 30 zł |

**Roczna suma:** ~10 800 zł + sezonowe korekty ≈ **~11 500 zł/rok**

---

## 7.5 Skalowanie kampanii

### Kiedy skalować?

Skaluj kampanię, gdy:
- CPL jest stabilnie poniżej 80 zł przez 2+ tygodnie
- Konwersja lead → wizyta wynosi 30%+
- Masz wolne terminy w grafiku (nie warto reklamować, jeśli nie obsłużysz)
- CPA (koszt/klienta) jest poniżej wartości pierwszej wizyty

### Jak skalować przy małym budżecie?

#### Metoda 1: Stopniowe zwiększanie budżetu (najlepsza)

```
Tydzień 1: 30 zł/dzień (bazowy)
Tydzień 3: 36 zł/dzień (+20%)
Tydzień 5: 43 zł/dzień (+20%)
Tydzień 7: 52 zł/dzień (+20%)
```

**Zasada:** Nie zwiększaj budżetu o więcej niż 20% na raz. Większe skoki resetują fazę uczenia algorytmu.

#### Metoda 2: Dodanie nowego zestawu reklam

Zamiast zwiększać budżet istniejącego zestawu, stwórz nowy z:
- Inną grupą docelową (np. Lookalike)
- Inną kreacją
- Osobnym budżetem (np. +15 zł/dzień)

#### Metoda 3: Rozszerzenie lokalizacji

Jeśli kampania na 25 km wyczerpuje się:
1. Rozszerz na 30–35 km
2. Testuj okolice Piaseczna/Tarczyna (bliżej Warszawy, ale nie Warszawa)
3. Dodaj kampanię na "dojazd z Warszawy" — osobny przekaz ("Nie chcesz kolejki w Warszawie? Przyjdź do Grójca")

#### Metoda 4: Nowe kanały (poza Meta Ads)

Gdy Meta Ads działa stabilnie, rozważ:
- **Google Ads** — reklamy w wyszukiwarce na "psychodietetyk Grójec", "dietetyk okolice Grójca"
- **Google Moja Firma** — optymalizacja wizytówki (darmowe!)
- **Instagram Reels** — organiczny zasięg (darmowy content marketing)

### Kiedy NIE skalować

- CPL rośnie, a nie wiesz dlaczego → najpierw zdiagnozuj
- Kalendarz wizyt jest pełny → niepotrzebne wydatki
- Okres świąteczny / wakacyjny → niższy popyt = wyższe koszty
- Nie masz nowych kreacji → zwiększony budżet przy tych samych reklamach = ad fatigue

---

## 7.6 Harmonogram działań — pierwsze 90 dni

### Tydzień 0 (przygotowanie) — PRZED uruchomieniem kampanii

| Zadanie | Czas | Priorytet |
|---|---|---|
| Zainstaluj Pixel Facebooka na stronie | 1h | Krytyczny |
| Skonfiguruj zdarzenia konwersji | 30 min | Krytyczny |
| Przygotuj 3–4 grafiki reklamowe | 2–3h | Krytyczny |
| Napisz 3–4 warianty tekstów reklamowych | 1–2h | Krytyczny |
| Stwórz Custom Audience z fanpage'a | 15 min | Wysoki |
| Ustaw auto-odpowiedź na Messengerze | 15 min | Wysoki |
| Wybierz formę płatności i skonfiguruj konto reklamowe | 30 min | Krytyczny |

### Tydzień 1–2 (start kampanii)

| Dzień | Zadanie |
|---|---|
| Dzień 1 | Uruchom Kampanię 1 (wiadomości) — pełny budżet 30 zł/dzień |
| Dzień 1–5 | FAZA UCZENIA — nie modyfikuj! Monitoruj, odpowiadaj na wiadomości |
| Dzień 7 | Pierwszy przegląd wyników: CTR, CPC, liczba wiadomości |
| Dzień 7–10 | Wyłącz najsłabszą reklamę, dodaj 1 nową kreację |
| Dzień 14 | Pełny przegląd tygodniowy. Decyzja: kontynuować / zmienić grupę |

### Tydzień 3–4 (optymalizacja)

| Dzień | Zadanie |
|---|---|
| Dzień 15 | Analiza: które kreacje i grupy działają najlepiej |
| Dzień 16 | Odśwież kreacje (nowe grafiki/nagłówki) |
| Dzień 21 | Przegląd: CPL, liczba wizyt, jakość leadów |
| Dzień 28 | Podsumowanie miesiąca 1. Decyzja o Fazie 2 |

### Miesiąc 2 (rozbudowa)

| Tydzień | Zadanie |
|---|---|
| Tydzień 5 | Dodaj Kampanię 2 (świadomość/edukacja) — 12 zł/dzień. Zmniejsz Kampanię 1 do 18 zł/dzień |
| Tydzień 6 | Nagraj pierwsze wideo (nawet telefonem) — test formatu wideo |
| Tydzień 7 | Test Lookalike Audience 1% z zaangażowanych |
| Tydzień 8 | Podsumowanie miesiąca 2. Analiza pełnego lejka |

### Miesiąc 3 (pełny lejek)

| Tydzień | Zadanie |
|---|---|
| Tydzień 9 | Dodaj retargeting (5 zł/dzień z budżetu TOFU) |
| Tydzień 10 | Test A/B: kreacja graficzna vs wideo |
| Tydzień 11 | Analiza: który etap lejka najlepiej konwertuje |
| Tydzień 12 | Podsumowanie Q1. Plan na kolejny kwartał. Decyzja o skalowaniu |

---

## 7.7 Koszty dodatkowe (poza budżetem reklamowym)

| Koszt | Kwota | Częstotliwość | Obowiązkowy? |
|---|---|---|---|
| Kreacje graficzne (Canva Pro) | ~50 zł/mies. | Miesięcznie | Opcjonalny (darmowa wersja wystarczy) |
| Landing page (jeśli brak strony) | 0–200 zł | Jednorazowo | Opcjonalny |
| Narzędzie do zarządzania (np. Meta Business Suite) | 0 zł | — | Darmowy |
| Czas na obsługę kampanii | ~3–5h/tydzień | Tygodniowo | Własny czas |
| Czas na odpowiadanie na wiadomości | ~30 min/dzień | Codziennie | Krytyczny |

**Łączny realny koszt miesięczny:** ~900 zł (reklamy) + 0–50 zł (narzędzia) + czas (~20h/miesiąc)

---

## Źródła

- [Optymalny budżet reklamowy w Meta Ads — Fallow Deer](https://www.fallowdeer.pl/post/optymalny-budzet-reklamowy-w-meta-ads)
- [Cennik Facebook Ads — Scorise](https://www.scorise.com/pl/cennik-facebook-ads/)
- [Ile kosztuje reklama na Facebooku — Divloy](https://divloy.pl/blog/ile-kosztuje-reklama-na-facebooku-cena-kampanii-meta-ads/)
- [Meta Ads cennik — Intense](https://intense.com.pl/meta-ads-cennik/)
- [Benchmarki Facebook Ads — kcmobile.pl](https://kcmobile.pl/baza-wiedzy/facebook-ads/benchmarki-facebook-ads-srednie-wyniki-branze/)
