Kilka uwag na początek:

1) Projekt na githubie nie zawiera danych źródłowych z notowaniami giełdowymi oraz skryptów do ich oczyszczenia i wyeksportowania (same dane zajmowały zbyt dużo miejsca a github nie pozwala na import danych większych niż 25MB), ani skryptów do webscrapingu newsów ze strony infostrefa.com

2) Jest to draft, z pewnością ostateczna forma będzie zawierała nieco szerszy opis teoretyczny topic modellingu

3) Zdecydowałem się do modelu użyć tytułów a nie pełnych wiadomości, ponieważ tytuły zawierają mniej szumu informacyjnego i są bardziej spójne jeśli chodzi o długość jak i słownictwo

4) Przeanalizowałem wszystkie często powtarzające się słowa w tytułach (nie było ich dużo, wszystkich słów w sumie jest około 11000) i stworzyłem osobny słownik stopwords, który należy zaimportować do katalogu nltk (nie jest to optymalne rozwiązanie, ale na razie nie skupiałem się na optymalizacji kodu)

Topic modelling:

Wybrałem metodę LDA... ale nie wiem czy takie podejście ma sens - porównując wymodelowane tematy z tytułami, w wielu przypadkach są one nietrafione (dla pozostałych metod wyniki nie były lepsze)


Pytanie: 
Jakie, Twoim zdaniem, powinny być następne kroki? 
Oczywiście poeksperymentuję jeszcze trochę z parametrami modelu i badanymi słowami, żeby osiągnąć lepsze rezultaty.

Celem projektu jest odpowiedź na pytanie 'czy po opublikowaniu wiadomości dana spółka przynosi większy zysk niż reszta rynku?'
więc wydaje mi się, że teraz należałoby pogrupować tytuły według wymodelowanych tematów i dokonać predykcji nadwyżkowej stopy zwrotu w zależności od tematu. Co o tym myślisz?
