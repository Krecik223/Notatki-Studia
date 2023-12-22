# Macierze

Macierz tworzą liczby wpisane do prostokątnej tabelki

$$
    A_{m,n} = 
    \begin{bmatrix}
        a_{1,1} & a_{1,2} & \cdots & a_{1,n} \\
        a_{2,1} & a_{2,2} & \cdots & a_{2,n} \\
        \vdots & \vdots & \ddots & \vdots \\
        a_{m,1} & a_{m,2} & \cdots & a_{m,n} \\
    \end{bmatrix}
$$

$$a_{ij}$$
$`i`$ - numer wiersza;
$`j`$ - numer kolumny;

$$
    M^{m \;\times\; n} \quad \text{- Zbiór wszystklich macierzy wymiaru m}  \times \text{n}
$$

## Szczególne typy macierzy

### Macierz zerowa
Maicerz złożona z samych zer

$$
    \theta _{3 \times 2} = 
    \begin{bmatrix}
        0 & 0 \\
        0 & 0 \\
        0 & 0 \\
    \end{bmatrix}
$$

### Macierz kwadratowa
Macierz w której liczba wierwszy równa się liczbie kolumn ($`m=n`$)

Wyróżniamy główną przekątną
```math
\begin{bmatrix}
    \ddots & \\
    & \ddots
\end{bmatrix}
```
$$
(a_{1,1}, \; a_{2,2}, \;\dots\; a_{n,n})
$$

### Macierz trójkątna
To macierz kwadratowa w której wszystkie elementy nad (dolna) lub pod (górna) główną przekątną wynoszą zero

```math
    \begin{bmatrix}
    \ddots &  0 \\
    \cdots & \ddots
    \end{bmatrix}
    \\
    \text{Dolna}
```

```math
    \begin{bmatrix}
    \ddots & \cdots \\
    0 & \ddots
    \end{bmatrix}
    \\
    \text{Górna}
```

### Macierz diagonalna
To macierz która jest trójkątna górna i dolna.
Inaczej mówiąc jest to macierz kwadratowa w której poza główną przekątną występują same zera

$$
    \begin{bmatrix}
    \ddots & 0 \\
    0 & \ddots
    \end{bmatrix}
$$

Każda macierz kwadratowa wymiaru **jeden** jest diagonalna

### Macierz jednostkowa
To macierz diagonalna w której na głównej przekątnej występują same `1`

$$
    I =
    \begin{bmatrix}
    1 &   &         & 0 \\
    & 1 &         &   \\
    &   & \ddots  &   \\
    0 &   &         & 1 \\
    \end{bmatrix}
$$

$$
    I_1 =
    \begin{bmatrix}
    1
    \end{bmatrix}
$$
$$
    I_2 =
    \begin{bmatrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1 \\
    \end{bmatrix}
$$

## Działania na macierzach

### Transponowanie (Transpozycja)

$$
    A \in M^{m\;\times\;n},\quad
    B \in M^{n\;\times\;m} \qquad
    \substack
    {
        i \in \{1,2, \cdots,m\}\\
        j \in \{1,2, \cdots,n\}
    }
    \\
    B = A^T \iff b_{ji} = a_{ij}
$$

Aby transponować macierz $`A`$ należy zamienić wiersze macierzy $`A`$ na kolumny (albo kolumny na wiersze)

$$
    A = 
    \begin{bmatrix}
    3 & 0 & 5 \\
    4 & 7 & 1
    \end{bmatrix}
    \qquad
    A^T =
    \begin{bmatrix}
    3 & 4 \\
    0 & 7 \\
    5 & 1
    \end{bmatrix}
$$

### Mnożenie macierzy przez liczbę

```math
    A,B \in M^{m\;\times\;n},\quad
    \alpha \in R \qquad
    \substack
    {
        i \in \{1,2, \cdots,m\}\\
        j \in \{1,2, \cdots,n\}
    }
    \\
    B = \alpha \cdot A \iff b_{ij} = \alpha \cdot a_{ij}
```

Aby pomnożyć Macierz $`A`$ przez liczbę $`\alpha`$ każdy element macierzy A mnożymy przez liczbę $`\alpha`$

$$
    A = 
    \begin{bmatrix}
    3 & 5 \\
    0 & -1 \\
    -4 & 8
    \end{bmatrix}\qquad
    3A = 
    \begin{bmatrix}
    9 & 15 \\
    0 & -3 \\
    -12 & 24
    \end{bmatrix}
$$

### Dodawanie i odejmowanie macierzy

$$
    A,B,C,D \in M^{m\;\times\;n}\qquad
    \substack
    {
        i \in \{1,2, \cdots,m\}\\
        j \in \{1,2, \cdots,n\}
    }
    \\
    C = A + B \iff c_{ij} = a_{ij} + b_{ij}\\
    D = A - B \iff c_{ij} = a_{ij} - b_{ij}\\
$$

Dodawanie i odejmowanie można wykonać tylko na macierzach tego samego wymiaru.

Działania te wykonujemy na współrzędnych to znaczy dodajemy/odejmujemy liczby na tych samych pozycjach.

```math
A =
\begin{bmatrix}
4 & 0 & -3 \\
-2 & 5 & 1 \\
\end{bmatrix}\quad
B =
\begin{bmatrix}
-7 & 6 & 4 \\
-9 & 8 & 0 \\
\end{bmatrix}
```

```math
A + B =
\begin{bmatrix}
4 & 0 & -3 \\
-2 & 5 & 1 \\
\end{bmatrix}
+
\begin{bmatrix}
-7 & 6 & 4 \\
-9 & 8 & 0 \\
\end{bmatrix}
=
\begin{bmatrix}
-3 & 6 & 1 \\
-11 & 13 & 1 \\
\end{bmatrix}
```

```math
A - B =
\begin{bmatrix}
4 & 0 & -3 \\
-2 & 5 & 1 \\
\end{bmatrix}
-
\begin{bmatrix}
-7 & 6 & 4 \\
-9 & 8 & 0 \\
\end{bmatrix}
=
\begin{bmatrix}
11 & -6 & -7 \\
7 & -3 & 1 \\
\end{bmatrix}
```
```math
B - A =
\begin{bmatrix}
-11 & 6 & 7 \\
-7 & 3 & -1 \\
\end{bmatrix}
```

### Mnożenie macierzy

$$
    A \in M^{m \times p},\quad
    B \in M^{p \times n},\quad
    C \in M^{m \times n}
    \qquad
    \substack
    {
        i \in \{1,2, \cdots,m\}\\
        j \in \{1,2, \cdots,n\}
    }
    \\
    C = A \cdot B \iff c_{ij} = \sum_{k=1}^p a_{ik} \cdot b_{kj}
$$

Aby wykonać mnożenie $`A`$ razy $`B`$ liczba kolumn macierzy $`A`$ musi być równa liczbie wierszy macierzy $`B`$

$$
    \begin{bmatrix}
    a_1, a_2, \cdots\!, a_n 
    \end{bmatrix}
    \cdot
    \begin{bmatrix}
    b_1\\ 
    b_2\\
    \vdots\\
     b_n 
    \end{bmatrix} =
    a_1b_1 + a_2b_2+\dots a_nb_n
$$

Aby wykonać mnożenie $`A \cdot B`$ pierwszy wiersz $`A`$ mnożymy przez wszystkie kolumny $`B`$, następnie drugi wiersz $`A`$ przez wszystkie kolumny $`B`$ i tak dalej.

$$
    A =
    \begin{bmatrix}
    4 & 0 & -2 \\
    1 & 5 & -1
    \end{bmatrix}\quad
    B =
    \begin{bmatrix}
    3 & 1 \\
    0 & 2 \\
    4 & 0
    \end{bmatrix}
$$

$$
    A \cdot B = 
    \begin{bmatrix}
    4 & 0 & -2 \\
    1 & 5 & -1
    \end{bmatrix}\cdot
    \begin{bmatrix}
    3 & 1 \\
    0 & 2 \\
    4 & 0
    \end{bmatrix} =
    \begin{bmatrix}
    4\cdot3+0\cdot0+4\cdot(-2) & 4\cdot1+0\cdot2+(-2)\cdot0 \\
    1\cdot3+5\cdot0+(-1)\cdot4 & 1\cdot1+5\cdot2+(-1)\cdot0 
    \end{bmatrix}\\ = 
    \begin{bmatrix}
    4 & 4 \\
    -1 & 11 
    \end{bmatrix} 
$$
$$
    B \cdot A = 
    \begin{bmatrix}
    3 & 1 \\
    0 & 2 \\
    4 & 0
    \end{bmatrix}\cdot
    \begin{bmatrix}
    4 & 0 & -2 \\
    1 & 5 & -1
    \end{bmatrix} =
    \begin{bmatrix}
    3\cdot4+1\cdot1 & 3\cdot0+1\cdot5 & 3\cdot(-2)+3\cdot(-1) \\
    0\cdot4+2\cdot1 & 0\cdot0+2\cdot5 & 0\cdot(-2)+2\cdot(-1) \\
    4\cdot4+0\cdot1 & 4\cdot0+0\cdot5 & 4\cdot(-2)+0\cdot(-1) 
    \end{bmatrix}\\ = 
    \begin{bmatrix}
    13 & 5 & -9 \\
    2 & 10 & -2 \\
    16 & 0 & -8 
    \end{bmatrix} 
$$

### Wyznacznik macierzy

Wyznacznik to liczba przyporządkowana macierzy kwadratowej

Macierze kwadratowe dzielimy na:
- osobliwe, tzn. $`detA = 0`$
- nieosobliwe, tzn. $`detA \neq 0`$

```math
detA \text{ - wyznacznik} 
```

```math
n=1
\quad
A =
\begin{bmatrix}
a
\end{bmatrix}
\quad
detA = a
```

```math
n=2
\quad
A =
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
\quad
detA = ad - bc
```

#### Wzory Sarrusa 
```math
    n = 3
```

```math
det
\substack{
    \begin{bmatrix}
    1 & 0 & 3 \\
    0 & 2 & 5 \\
    4 & 1 & 6
    \end{bmatrix}
    \\
    \begin{matrix}
    1 & 0 & 3 \\
    0 & 2 & 5
    \end{matrix}
} =
(1 \cdot 2 \cdot 6 + 0 \cdot 1 \cdot 3 + 4 \cdot 0 \cdot 5) - (4 \cdot 2 \cdot 3 + 1 \cdot 1 \cdot 5 + 0 \cdot 0 \cdot 6) = 12 - 29 = -17
```

#### Tw. Laplace'a
Jeżeli $`A`$ jest macierzą kwadratową wymioaru $`n \geqslant 2`$, to 

```math
detA =
\sum^{n}_{j = 1}
a_{ij}D_{ij}
\qquad
\text{Rozwinięcie względem wiersza} \; i
```
```math
detA =
\sum^{n}_{i = 1}
a_{ij}D_{ij}
\qquad
\text{Rozwinięcie względem kolumny} \; j
```

Gdzie $`D_{ij}`$ to dopełnienie algebraiczne $`a_{ij}`$

```math
D_{ij} = (-1)^{i+j} \cdot detA_{ij}
```
gdzie $`A_{ij}`$ to macierz, która powstaje z $`A`$ przez skreślenie wiersza $`i`$ oraz kolumny $`j`$

Stosując wzór laplace'a szukamy wiersza lub kolumny z największą ilością zer.
Jeżeli w maceirzy występuje wiersz lub kolumna złożona z samych zer to $`detA = 0`$.

### Macierz odwrotna
Macierz $`A^-1`$ jest macierzą odwrotną do $`A`$, jeżeli:
```math
A^{-1} \cdot A = A \cdot A^{-1} = I
```

Macierz $`A`$ jest odwracalna $`\iff A`$ jest maceirzą nieosobliwą.

Jeżeli $`A`$ jest macierzą kwadratową nieosobliwą wymiaru wymiaru $`n \geqslant 2`$, to
```math
A^{-1} = \frac{1}{detA} \cdot D^T
```
gdzie $`D = \begin{bmatrix} D_{ij} \end{bmatrix}`$ jest macierzą dopełnień algebraicznych $`A`$

Uwaga: $`n = 1`$
```math
A = \begin{bmatrix} 5 \end{bmatrix} \qquad A^{-1} = \begin{bmatrix} \frac{1}{5} \end{bmatrix} 
```

### Minor macierzy
Minor $`M`$ macierzy $`A`$ to macierz kwadratowa, która pwostaje z $`A`$ przez skreślenie pewnej ilości (być może zero) wierszy i kolumn.

#### Minor bazowy
Minor $`M`$ macierzy $`A`$ jest minorem bazowym A, jeżeli $`detM \neq 0`$ oraz wszystkie minory $`M'`$ macierzy $`A`$ wymiaru większego niż $`M`$ mają wyznaczniki równe zero ($`detM' = 0`$)

Uwaga. Macierz $`A`$ może posiadać więcej niż jeden minor bazowy, ale wszystkie minory bazowe $`A`$ są tego samego wymiaru.

#### Rząd macierzy
Rząd macierzy niezerowej to wymiar dowlonego minora bazowego tej macierzy.

Rząd macierzy zerowej wynosi zero ($`rz(\theta) = 0`$)

## Układy równań liniowych
Z układem równań liniowych można powiązać macierz $`A`$ wymiaru $`m \times n`$ nazywaną **macierzą współczynników układu równań** (macierz główna) oraz dwie macierze kolumnowe
$`x`$ (kolumna zmiennych) i $`b`$ (kolumna wyrazów wolnych).
```math
Ax = b
```

### Układ Cramera
Układ równań liniowych jest układem Cramera, jeżeli macierz główna układu $`A`$ jest kwadratowa nieosobliwa.
Czyli liczba równań w układzie jest równa liczbie zmiennych a wyznacznik macierzy głównej nie jest równy 0 ($`detA \neq 0`$).

#### Metoda macierzy odwrotnej
Układ równań liniowych Cramera ma dokładnie jedno rozwiązanie zadane wzorem
```math
x = A^{-1} \cdot b
```

#### Metoda Cramera
Układ równań liniowych Cramera ma dokładnie jedno rozwiązanie zadane wzorem
```math
x_i = \frac{detA_i}{detA},
\qquad
i = 1, 2, \dots, n
```
gdzie $`A_i`$ to macierz, która powstaje z $`A`$ przez zastąpienie kolumnu $`i`$ przez kolumnę wyrazów wolnych.

### Twierdzenie Kroneckera-Capelliego
Macierz $`U`$ (macierz uzupełniona) powstaje z macierzy $`A`$ przez dołączenie kolumny $`b`$.
```math
U =
\begin{bmatrix}
A & \vdots & b
\end{bmatrix}
```

- jeżeli $`rz(A) = rz(U) = n`$ ($`n`$ - liczba niewiadowym), to rozwiązanie jest jednyne;
- jeżeli $`rz(A) = rz(U) = r < n`$, to rozwiązań jest nieskończenie wiele i zależą od $`n - r`$ parametrów.

### Macierz schodkowa
Macierz schodkowa to macierz w której każdy pierwszy nie zerowy element wiersza jest przesunięty w prawo w stosunku do wiersza poprzedniego

Nie bierzemy pod uwagę wierszy zerowych

```math
A =
\begin{bmatrix}
5 & 0 & 8 & 0 \\
0 & 4 & 0 & 0 \\
0 & 0 & 0 & 3
\end{bmatrix}
\quad
rz(A) = 3
```

Rząd macierzy schodkowej jest równy liczbie schodków to znaczy nie zerowych wierszy.

### Operacje elementarne na wierszach
1. Pomnożyć wiersz przez liczbę różną od zera
2. do wiersza dodać inny wiersz pomnożony przez liczbę
3. zamienić dwa wiersze miejscami

Analogiczne operacje definiujemy dla kolumn

Przekształcenia elementarne nie zmieniają rzędu macierzy.

### Metoda Gaussa (eliminacji zmiennych)
Przekształcamy macierz uzupełniną układu za pomocą operacji elementarnych na wierszach do postaci schodkowej. 
Z przekształconej macierzy odczytujemy czy rząd $`A`$ jest równy rzędowy $`U`$, jeżeli nie to układ jest sprzeczny, jeżeli są równe to z przekształconej macierzy odczytujemy równania układu a następnie rozwiązania. 
