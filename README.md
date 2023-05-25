Zaliczenie Programowanie Zaawansowane - Patryk13988 semestr VI

Kod programu został napisany w języku Python przy użyciu Pytcharma w celu zaliczenia przedmiotu Wzorce Projektowe, 
Zadaniem programu jest umożliwienie i pokazanie drogi jaką przebywa obenie kanapka zamówiona przez użytkownika, 
Na końcu użytkownik jest informowany o odbiorze produktu.
Podobne programy są często wykorzystywane podczas zamówień internetowych 
Albo zamówieniach stacjonarnych np:. Maszyny do jedzenia

Działenie Programu:
1. Program prosi użytkownika o wybranie rodzaju kanapki na jaką ma ochotę
2. Po wybraniu odpowiedniej opcji (litera w nawiasie) program zaczyna kompilację kanapki
3. Cały proces jest opisywany, tak by użytkownik wiedział na jakim etapie jest proces tworzenia jego kanapki.
4. Po zakończeniu użytownik jest informowany o możliwości odbioru

Struktura systemu:
1. Program zaczyna się od wywołania Fukncji main()
2. Do zmiennej builders przypisujemy literę do odpowiedniej klasy np: t = TraditionSandwich
3. Następnie wykonujemy pętle, która wykonuje się do czasu gdy zmienna valid_input jest fałszywa, dzięki temu mamy pewność, 
   Że program nie zostanie przerwany po pierszej próbie.
4. W pętli jest odniesienie do funkcji def validate_style(builders), której zadaniem jest pobranie od użytkownika zmiennej,
   Dzięki dodanej pętli oraz obsłudze wyjątków, program w przypadu nieprawidłowej informacji, nie spowoduje błedów
5. Następnie wywołuje się klasa Waiter(), której zadaniem jest wywowałanie odpowiedniej klasy (według danych które podał użytkownik)
   A następnie wywołanie poszczególnych funkcji tej klasy, 
6. Każda funkcja posiada opisany proces, jaki jest potrzebny do stworzenia kanapki
7. Po zakończeniu procesu użytkownik dostaje informacji o możliwości odebrania kanapki

Problemy, które napotkał program:
1. Próba wpisania dowolnej wartości do programu (innej niż powinna być):
- Wpisanie dowolnej wartości innej niż dozwolona, spowodowało wyjątek ErroKey, aby mu zapobiec została wprowadzona obsługa wyjątków
2. Problem z pozycji numer 1, powoduje problemy w dalszej części programu:
- Jeśli użytkownik wprowadzi nie prawidłową wartość (tak jak opisałe w pkt. 1), program nie może przejść do kolejnego etapu
  Nie mogę wybrać za użytkownika kanapki jaką by chciał kupić, więc musze go ponownie zapytać i poinformować o umyślnym/przypadkowym błędzie
  Dlatego zastosowałem pętle while, która bedzie próbowała odpowiednio przetworzyć wartość użytkownika, jeśli się uda, petla zostanie przerwana
  A pozostały kod bedzie kontynuowany, jeśli sie nie uda program próbuje ponownie.
  
Wykorzystane bilbioteki:
1. Enum
2. Time
3. Unittest

Scenariusze testów:
1. Akceptacyjny:
- Przeprowadzono symulację użytkownika, program nie wykazał błędu. Otrzymałem komunikat Ran 1 test in 29.430s OK
2. Jednostkowy:
- Przeprowadziłem testy jednostkowe, których zadaniem było sprawdzenie funkcji, a konretnie zmiennej takiej jak czas ogrzewania
  Testy zostały przeprowadzone dla każdej kanapki, gdyby czas się nie zgadzał, mogłoby to skutkować przypaleniem kanapek
