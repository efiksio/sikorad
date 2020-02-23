---
layout: post
title:  "Git pierwszym narzędziem z listy niezbędnych"
date:   2020-01-11 06:41:05 +0000
categories: it git
---
Co to jest git i dlaczego warto moim zdaniem rozpocząć naukę właśnie od tego narzędzia.

Git to rozproszony system służący do kontroli wersji (przykładowo naszego kodu) jest on w bardzo przystępny sposób opisany na stronie [git-scm.com](https://git-scm.com/book/pl/v2/Pierwsze-kroki-Wprowadzenie-do-kontroli-wersji).

*Ponieważ zdecydowałem się prowadzić ten blog w celach pomocniczo-naukowych. Głownie do notowania postępów oraz szybkich notatek które bedą mi pozwalały na szybki powrót do danego zagadnienia, opis programów wykonywany jest w dużym uproszczeniu.*

{:refdef: style="text-align: center;"}
![Po co ten Git?](https://git-scm.com/images/logo@2x.png)
{: refdef}

Nie będę poświęcał tutaj czasu na opis gdzie i w jaki sposób możemy zapisywać/przechowywać nasz kod tj. na zewnętrznych serwerach czy tez lokalnym dysku. Na początek opiszę czego do tej pory dowiedziałem się o w/w kontroli wersji:

* Inicjalizacja kontroli wersji w katalogu, którym się znajdujemy (katalog główny naszego projektu):

{% highlight bash %}
git init
{% endhighlight %}

* Sprawdzanie stanu naszego nowego repozytorium (plików)
):

{% highlight bash %}
git status
{% endhighlight %}
(w wyniku otrzymujemy listę zmodyfikowanych lub nowo dodanych plików)

* Dodanie nowych / zmodyfikowanych plików do poczekalni:

{% highlight bash %}
git add .
{% endhighlight %}
(znak kropki oznacza, ze chcemy dodać do następnej wersji wszystkie zmiany które zostały wyświetlone podczas wykonania komendy **git status**)

* Zatwierdzanie zmian wysłanych do poczekalni:

{% highlight bash %}
git commit -m "komentarz do zmian"
{% endhighlight %}

+ Wyświetlenie historii zmian dla naszej rewizji

{% highlight bash %}
git log
{% endhighlight %}
 
+ Jeżeli chcemy ograniczyć podgląd wyświetlanej historii możemy przykładowo:

{% highlight bash %}
git log --since=2.weeks
{% endhighlight %}

+ Poniżej lista przydatnych opcji ograniczających rezultaty **git log**:

`git log -(n)` _pokarz ostatnich **n** komentarzy;_

`git log --since, --after`   _pokarz tylko komentarze zamieszczone 
po określonej dacie;_

`git log --until, --before`   _pokarz tylko komentarze zamieszczone przed 
określonej datą;_

`git log --author`   _jeżeli pracujemy w teamie możemy filtrować listę określając autora zmian._

