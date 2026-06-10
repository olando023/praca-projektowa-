README - Analiza Kosztów Ubezpieczeń Zdrowotnych
1. Cel Analizy
Celem projektu jest zbadanie czynników wpływających na wysokość składek ubezpieczeniowych, ze szczególnym uwzględnieniem wpływu palenia tytoniu na koszty ponoszone przez pacjentów.

2. Hipotezy
Hipoteza 1: Osoby palące płacą znacznie wyższe składki ubezpieczeniowe niż osoby niepalące.
Hipoteza 2: Istnieje silna korelacja między wskaźnikiem BMI a kosztami leczenia, zwłaszcza w grupie osób palących.
Hipoteza 3: Modele uczenia maszynowego (Random Forest, Regresja Logistyczna) są w stanie z wysoką dokładnością przewidzieć status palacza na podstawie wieku, BMI i wysokości opłat.

3. Opis Bazy Danych
Wybrano zbiór danych Medical Cost Personal Datasets (plik insurance.csv). Dane zawierają 1338 rekordów i 7 kolumn:
age: wiek głównego beneficjenta.
sex: płeć (female/male).
bmi: wskaźnik masy ciała.
children: liczba dzieci/osób zależnych objętych ubezpieczeniem.
smoker: status palenia (yes/no).
region: obszar zamieszkania w USA.
charges: indywidualne koszty medyczne rozliczane przez ubezpieczenie.

4. Wyniki i Wnioski
Analiza Statystyczna: Średnie koszty dla palaczy są niemal 4-krotnie wyższe (32k USD) niż dla osób niepalących (8.4k USD).
Wizualizacja: Wykresy rozrzutu wyraźnie pokazują, że palacze o wysokim BMI tworzą grupę o najwyższych składkach (powyżej 30k USD).
Modele ML:
Random Forest osiągnął najwyższą skuteczność (Accuracy ~98-99%), bezbłędnie identyfikując większość przypadków.
Regresja Logistyczna również wykazała się bardzo wysoką precyzją, co sugeruje silną, niemal liniową zależność między kosztami a statusem palacza w tym zbiorze danych.
