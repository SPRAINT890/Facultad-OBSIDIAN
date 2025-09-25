
## 1 Indique si es AFD o AFN? Justifique
AFD

## 2 Saque una GRD del automata

q0 -> a q1
q1 -> b q1 | a q2
q2 -> b q2 | $\lambda$

q0 = S
q1 = A
q2 = B

S -> aA
A -> bA | aB
B -> bB | $\lambda$

S es el terminal inicial y B el estado de finalizacion
## 3 Que L acepta
L es el lenguaje regular de las cadenas que empesaron con a, seguidos de cualquier cantidad de b que tienen otra a y pueden tener b* al final

## 4 Obtenga una ER del AF del grafico aplicando el teorema de Kleene y el Lema de arden

Ecuacion de Arden

1 S = aA
2 A = bA + aB
3 B = bB + $\lambda$

### Aplico Arden en 3
B = b*$\lambda$ = b*

### Sustituir B en 2
2b A = bA + ab*

### Aplico arden en 2b
A=(b)* (ab*)

### Sustituir en 1
S = ab* ab*

## 5
Ya es AFD

## 6
