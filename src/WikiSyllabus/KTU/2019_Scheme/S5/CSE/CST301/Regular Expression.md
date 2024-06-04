# Regular Expression-Defenition
A Regular Expression are useful for representing certain sets of strings in algebraic fashion. It 
describes the language accepted by FSA.Regular expressions are a notation system for regular 
languages.
Regular expressions have become a standard tool to describe patterns of strings in such programs as 
editors or search algorithms.

# A Regular Expression can be recursively defined as follows −

1)ε is a Regular Expression indicates the language containing an empty string. (L (ε) = {ε})
2)φ is a Regular Expression denoting an empty language. (L (φ) = { })
3)a is a Regular Expression where L = {a}
If X is a Regular Expression denoting the language L(X) and Y is a Regular Expression denoting the language L(Y), then
a)X + Y is a Regular Expression corresponding to the language L(X) ∪ L(Y) where L(X+Y) = L(X) ∪ L(Y).
b)X . Y is a Regular Expression corresponding to the language L(X) . L(Y) where L(X.Y) = L(X) . L(Y)
c)R* is a Regular Expression corresponding to the language L(R*)where L(R*) = (L(R))*
If we apply any of the rules several times from 1 to 5, they are Regular Expressions

# Regular Grammar : 
A grammar is regular if it has rules of form A -> a or A -> aB or A -> ɛ where ɛ is a special 
symbol called NULL.

# Regular Languages : 
A language is regular if it can be expressed in terms of regular expression.