---
layout: relation
title: 'csubj'
shortdef: 'clausal subject'
udver: '2'
---

A clausal subject is a clausal syntactic subject of a clause, i.e.,
the subject is itself a clause.

~~~ sdparse
Με ενδιαφέρει ότι απολύθηκαν άνθρωποι από το κανάλι
csubj(ενδιαφέρει, απολύθηκαν)
mark(απολύθηκαν, ότι)
~~~

~~~ sdparse
Δεν με πειράζει να το πουν
csubj(πειράζει, πουν)
dobj(πειράζει, με)
aux(πειράζει, να)
~~~

~~~ sdparse
Με στεναχωρεί που έρχεται ο χειμώνας
csubj(στεναχωρεί, έρχεται)
dobj(στεναχωρεί, Με)
mark(έρχεται, που)
~~~
<!-- Interlanguage links updated So kvě 14 19:03:22 CEST 2022 -->
