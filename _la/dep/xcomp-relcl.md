---
layout: relation
title: 'xcomp:relcl'
shortdef: 'double pronoun construction or free relative acting as complement clause'
udver: '2'
---

This syntactic subrelation (also implemented for [csubj](la-dep/ccomp-relcl), [ccomp](la-dep/ccomp-relcl) and [advcl](la-dep/advcl-relcl)) is used to distinguish a so-called free [relative clause](la-dep/acl-relcl) from other occurrences of [clauses acting as arguments](la-dep/ccomp) in another matrix clause, according to its function. 

This is a kind of relative clause that might be interpreted as having an internal head which, in Latin, is always represented by a relative [relative](la-feat/PronType#Rel) [pronoun](la-pos/PRON) (typically, but not limited to, *qui*). Such pronoun is said to be "double" because it is seen to have a twofold function: one as argument inside the free relative clause, and one inside the matrix clause, the latter being the same function carried out by the whole clause itself (which is thus subordinate). There appear to be strong constraints for a similar construction, in that the relative pronoun has to assume the same identical forms in both functions, even they are different inside and outside of the free relative clause: e.g., a *quod* ([neuter](la-feat/Gender) [singular](la-feat/Number) [nominative/accusative](la-feat/Case)) can act indifferently in any combination of [(passive) subject](la-dep/nsubj) or [object](la-dep/obj) in the relative or the matrix clause; conversely, the occurrence of *quibus* (any [gender](la-feat/Gender) [plural](la-feat/Number) [dative/ablative](la-feat/Case)) should be ruled out to occur e.g. as [oblique](la-dep/obl) argument in the relative clause and at the same time as object in the matrix clause. Sometimes, however, we observe that this happens. In any case, the double pronoun is annotated morphosyntactically according to its function inside the free relative clause. It is also observed that this pronoun extremely regularly appears at the beginning of the free relative clause: this behaviour seems to be typical for relative(/interrogative) pronouns in general, also for "prototypical" relative clauses (i.e. with an external head).


~~~ sdparse
Nec adimitanda recenseo cum dorsa non vultus ad Sponse vehiculum habeatis et vere dici possetis qui Prophete ostensi sunt male versi ad templum vobis ignem de celo missum despicientibus ubi nunc are ab alieno calescunt vobis columbas in templo vendentibus ubi que pretio mensurari non possunt in detrimentum hinc inde commutantium venalia facta sunt
xcomp(possetis, dici)
nsubj:pass(ostensi, qui)
xcomp:relcl(dici, ostensi)
~~~ 

'Nor do I recount examples for your imitation, seeing that you turn your backs, not your faces, to the car of the Spouse, and verily might be likened **to them that were shown to the prophet with their backs turned towards the temple**; you who scorn the fire sent down from heaven upon the altars, which now are alight with strange fire; you who sell doves in the temple where that which cannot be measured by price is made merchandise to the hurt of them that come and go therein.' (`UDante Epi-185`, *De Monarchia* XI vi, Dante Alighieri)

* *qui* is the masculine singular nominative form of *qui* 'that, who, which', which is annotated with `Case=Nom` acting as passive subject of *ostensi* 'shown', the whole clause acting as the complement of *dici* 'being said' with the subject necessarily intended as coinciding with *qui* and the same as that of *possetis* 'you (pl.) could well'.


#### Note on the former annotation style

In previous (pre v2.11) versions of some treebanks, especially UDante, the annotation of this construction followed a different logic. Noticing the constraints on the combination of internal and external functions of the relative pronoun, its position and making a parallelism with other relative construction with explicite double pronouns (i.e. *quod* 'what' = *id quod* 'that which'), the double pronoun was promoted as head, marked for its function in the matrix clause, and the rest of the clause made dependent as a relative clause where the relativised position is empty. So, the first example above appeared as:

~~~ sdparse
et vere dici possetis qui Prophete ostensi sunt male versi ad templum
xcomp(dici, qui)
xcomp(possetis,dici)
acl:relcl(qui,ostensi)
~~~ 

























