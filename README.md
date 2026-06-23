Projekt: Przewidywanie kosztów ubezpieczeń medycznych (Programowanie 2)

Cel analizy
Głównym celem projektu jest stworzenie modelu uczenia maszynowego (Regresja), który na podstawie danych demograficznych i zdrowotnych pacjenta potrafi oszacować roczne koszty jego ubezpieczenia medycznego. 

Opis danych
Do analizy wykorzystano zestaw danych `insurance.csv` pobrany z platformy GitHub (pierwotnie z Kaggle). Zbiór zawiera 1338 wierszy (pacjentów) oraz 7 kolumn:
* **age** - wiek pacjenta
* **sex** - płeć
* **bmi** - wskaźnik masy ciała
* **children** - liczba posiadanych dzieci
* **smoker** - informacja, czy pacjent jest palaczem
* **region** - region zamieszkania w USA
* **charges** - docelowa wartość przewidywana (koszty medyczne)

Realizacja kroków
1. **Pobranie i podział danych:** Zbiór został podzielony na część treningową (80%) i testową (20%).
2. **Wizualizacja i korelacja:** Przeprowadzono EDA (Exploratory Data Analysis), w którym wykazano silny wpływ palenia papierosów oraz wieku na ostateczne koszty.
3. **Potoki (Pipelines):** Zbudowano `ColumnTransformer` do automatycznego radzenia sobie z brakami (SimpleImputer), standaryzacji (StandardScaler) oraz kodowania zmiennych tekstowych (OneHotEncoder).
4. **Modele:** Zbudowano dwa modele regresyjne: **Linear Regression** oraz **Random Forest Regressor**.

Wyniki i Wnioski
Model poddano ewaluacji przy pomocy metryki **RMSE** (Root Mean Squared Error).
Ponieważ model Random Forest radzi sobie znacznie lepiej z nieliniowościami (co widać na wykresach korelacji palenia z kosztami), zastosowano na nim optymalizację hiperparametrów za pomocą `GridSearchCV`. Zoptymalizowany model **Random Forest okazał się lepszy**, uzyskując najmniejszy błąd na danych, których nigdy wcześniej nie widział.
