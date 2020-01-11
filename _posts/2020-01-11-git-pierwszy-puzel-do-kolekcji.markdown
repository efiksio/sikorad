---
layout: post
title:  "Git pierwszym narzędziem z listy niezbędnych"
date:   2020-01-11 06:41:05 +0000
categories: it git
---
Co to jest git i dlaczego warto moim zdaniem rozpocząć naukę właśnie od tego narzędzia.

Git to rozproszony system slózący do kontroli wersji (przykładowo naszego kodu) jest on w bardzo przystępny sposób opisany na stronie [git-scm.com](https://git-scm.com/book/pl/v2/Pierwsze-kroki-Wprowadzenie-do-kontroli-wersji).

*Poniewaz zdecydowałem się prowadzić ten blog w celach pomocniczo-naukowych. Głownie do dnotowania postępów oraz szybkich notatek które bedą mi pozwalały na szybki powród do danego zagadnienia, opis prograów wykonywany jest w duzym uproszczeniu.*

{:refdef: style="text-align: center;"}
![Po co ten Git?](https://git-scm.com/images/logo@2x.png)
{: refdef}

Nie bedę poświęcał tutaj czasu na opis gdzie i w jaki sposób mozemy zapisywać/przechowywać nasz kod tj. na zewnętrznych serverach czy tez lokalnym dysku. Na początek opiszę czego do tej pory dowiedziałem się o w/w kontroli wersji:

* Inicjalizacja kontroli wersji w katalogu, którym sie znajdujemy (katalog główny naszego projektu):

{% highlight bash %}
git init
{% endhighlight %}

* Sprawdzanie stanu naszego nowego reposytorium (plików)
):

{% highlight bash %}
git status
{% endhighlight %}
(w wyniku otrzymujemy listę zmodyfikowanych lub nowo dodanych plików)

* Dodanie nowych / zmodyfikowanych plików do poczekalni:

{% highlight bash %}
git add .
{% endhighlight %}
(znak kropki oznacza, ze chcemy dodać do następnej wersji wszystkie zmiany które zostały wyświetlone podczas wykonanai komendy **git status**)

* Zatwierdzanie zmian wysłanych do poczekalni:

{% highlight bash %}
git commit -m "komentarz do zmian"
{% endhighlight %}

+ Wyświetlenie historii zmian dla naszej rewizji

{% highlight bash %}
git log
{% endhighlight %}
 
+ Jezeli chcemy ograniczyć podgląd wyświetlanej historii mzemy przykładowo:

{% highlight bash %}
git log --since=2.weeks
{% endhighlight %}

+ Ponizej lista przydatnych opcji ograniczających rezultaty **git log**:

`git log -(n)` _pokarz ostatnich **n** komentarzy;_

`git log --since, --after`   _pokarz tylko komentarze zamieszczone 
po określonej dacie;_

`git log --until, --before`   _pokarz tylko komentarze zamieszczone przed 
określonej datą;_

`git log --author`   _jezeli pracujemy w teamie mozemy filtrować listę 
określając autora zmian._

