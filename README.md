# Statistics-R-Markdown
Simple R Markdown statistics project showing understanding of applied statistics.

# Przedziały ufności: weryfikacja metodą Monte Carlo

Projekt w R sprawdzający, jak naprawdę działają przedziały ufności, czyli
jak często pokrywają prawdziwy parametr przy nominalnym poziomie 95%.
Wszystko oparte na symulacjach Monte Carlo (1000 powtórzeń na scenariusz).

## Co jest w projekcie

**1. Przedział dla średniej i wariancji (rozkład t-Studenta i χ²)**
Badane rozkłady: N(0,1), N(0,4), t(3), t(10), t(30) oraz próby n = 10, 50, 200.

**2. Przedział Walda vs Agresti-Coull dla proporcji**
Porównanie pokrycia dla θ od 0.005 do 0.5 i n od 20 do 1000, zaprezentowane na heatmapie.

**3. Centralne Twierdzenie Graniczne**
Histogramy i wykresy Q-Q dla rozkładu średnich z prób (n = 50, 100, 200).

## Najciekawsze wnioski

- Przedział dla **średniej** jest odporny na odstępstwa od normalności,
  a pokrycie szybko zbliża się do 0.95 wraz ze wzrostem n.
- Przedział dla **wariancji** jest bardzo wrażliwy na ciężkie ogony:
  dla t(3) pokrycie spada do ok. 0.45 przy n = 200, więc większa próba
  tego nie naprawia.
- **Klasyczny przedział Walda** zawodzi dla małych θ i małych n
  (np. θ = 0.005, n = 20: pokrycie ok. 10%), bo przy zerowej liczbie
  sukcesów przedział redukuje się do punktu.
- **Agresti-Coull** utrzymuje pokrycie blisko 0.95 w całym badanym zakresie.

## Technologie

R, R Markdown, ggplot2 (heatmapa)

## Jak uruchomić

Otwórz `raport4.Rmd` w RStudio i kliknij **Knit**.
Gotowy raport jest w pliku `raport4.pdf`.

## Autor

Oliwia Binkul
