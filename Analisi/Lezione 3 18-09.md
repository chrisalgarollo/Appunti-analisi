## Il Principio di Induzione

### Definizione e scopo del principio

- Il **principio di induzione** è uno strumento matematico che permette di dimostrare in un tempo finito (in un solo passaggio logico) un'infinità numerabile di formule o affermazioni ordinate $P_n$.
- Struttura formale e ipotesi del teorema:
    1. **Base dell'induzione**: si verifica che la prima affermazione della sequenza $P_{n_0}$ (tipicamente per $n_0 = 1$ o $n_0 = 0$) sia vera.
    2. **Passo induttivo**: si verifica l'implicazione logica secondo cui, ipotizzando vera la generica affermazione $P_n$ (**ipotesi induttiva**), ne consegue la veridicità dell'affermazione successiva $P_{n+1}$: $$
P_n \implies P_{n+1}
$$
- Nota metodologica: nel passo induttivo non si dimostra la verità assoluta di $P_n$ o di $P_{n+1}$, ma esclusivamente la validità della relazione di implicazione $P_n \implies P_{n+1}$.
- Fondamento teorico: si basa sulla caratterizzazione dell'insieme dei **numeri naturali** ($\mathbb{N}$) come insieme ordinato e numerabile in cui ogni elemento, eccezion fatta per lo zero, ammette un unico antecedente.

---

## Applicazioni ed Esempi del Principio di Induzione

### 1. Somme di Gauss

- Enunciato: per ogni $n \ge 1$, la somma dei primi $n$ numeri naturali è data dalla formula: $$
1 + 2 + 3 + \dots + n = \frac{n(n+1)}{2}
$$
- Dimostrazione per induzione:
    
    1. **Base dell'induzione** ($n_0 = 1$): $$
1 = \frac{1(1+1)}{2} = \frac{2}{2} = 1 \quad \text{(vera)}
$$
    2. **Passo induttivo**: si assume vera la formula $P_n$ per $n$ e si valuta la somma fino a $n+1$: $$
1 + 2 + \dots + n + (n+1) = \left(\frac{n(n+1)}{2}\right) + (n+1)
$$ Facendo il denominatore comune e raccogliendo il termine $(n+1)$: $$
\frac{n(n+1) + 2(n+1)}{2} = \frac{(n+1)(n+2)}{2} = \frac{(n+1)((n+1)+1)}{2}
$$ L'uguaglianza coincide con la formula $P_{n+1}$, confermando che $P_n \implies P_{n+1}$.
    
    - Conclusione: la formula è vera per ogni $n \ge 1$.

### 2. Somme geometriche

- Enunciato: sia $q \in \mathbb{Q}$ con $q \neq 1$. Per ogni $n \ge 1$, la somma delle prime $n$ potenze della base $q$ è data da: $$
\sum_{k=0}^n q^k = 1 + q + q^2 + \dots + q^n = \frac{1 - q^{n+1}}{1 - q}
$$
- Dimostrazione per induzione:
    1. **Base dell'induzione** ($n_0 = 1$): $$
1 + q = \frac{1 - q^2}{1 - q} = \frac{(1-q)(1+q)}{1-q} = 1 + q \quad \text{(vera)}
$$
    2. **Passo induttivo**: si assume vera la formula $P_n$ e si aggiunge il termine $q^{n+1}$: $$
(1 + q + \dots + q^n) + q^{n+1} = \frac{1 - q^{n+1}}{1 - q} + q^{n+1}
$$ Eseguendo il calcolo algebrico al numeratore: $$
\frac{1 - q^{n+1} + q^{n+1}(1 - q)}{1 - q} = \frac{1 - q^{n+1} + q^{n+1} - q^{n+2}}{1 - q} = \frac{1 - q^{n+2}}{1 - q} = \frac{1 - q^{(n+1)+1}}{1 - q}
$$ La relazione $P_{n+1}$ è verificata.

### 3. Esercizi proposti

- Ricerca e dimostrazione per induzione delle formule per:
    1. La somma dei primi $n$ numeri pari.
    2. La somma dei primi $n$ numeri dispari.
    3. La somma dei quadrati dei primi $n$ numeri naturali.

### 4. Disuguaglianza di Bernoulli

- Enunciato: per ogni $n \ge 1$ e per ogni $x > -1$ fissato, vale la disuguaglianza: $$
(1 + x)^n \ge 1 + nx
$$
- Dimostrazione per induzione:
    1. **Base dell'induzione** ($n_0 = 1$): $$
(1 + x)^1 \ge 1 + 1 \cdot x \implies 1 + x = 1 + x \quad \text{(vera)}
$$
    2. **Passo induttivo**: si assume vera la disuguaglianza $(1 + x)^n \ge 1 + nx$. Moltiplicando entrambi i membri per il fattore $(1 + x)$ (che è strettamente positivo poiché $x > -1$): $$
(1 + x)^{n+1} = (1 + x)^n (1 + x) \ge (1 + nx)(1 + x)
$$ Sviluppando il prodotto a destra: $$
(1 + nx)(1 + x) = 1 + x + nx + nx^2 = 1 + (n+1)x + nx^2
$$ Poiché $nx^2 \ge 0$, omettendo tale termine non negativo si ottiene una quantità minore o uguale: $$
1 + (n+1)x + nx^2 \ge 1 + (n+1)x
$$ Di conseguenza: $$
(1 + x)^{n+1} \ge 1 + (n+1)x
$$ La disuguaglianza $P_{n+1}$ è dimostrata.
- Utilità applicativa: le somme di Gauss, le somme geometriche e la disuguaglianza di Bernoulli verranno impiegate per il calcolo dei **limiti**.

---

## Successioni Numeriche

### Definizione formale e notazione

- Una **successione** in un insieme $X$ è una funzione $f: D \to X$ il cui dominio $D$ è un insieme **numerabile** ($\vert D \vert = \vert \mathbb{N} \vert$, ad esempio $D = \mathbb{N}, \mathbb{N}^*, \mathbb{Z}$).
- Notazione standard:
    - Si definisce $\{x_n \}:= f(n)$ per ogni $n \in D$.
    - La successione si indica con la notazione ${x_n}_{n \in D} \subseteq X$.
    - Si identifica formalmente la funzione con la sua **immagine** (insieme discreto di punti presi nell'insieme $X$).

### Interpretazione come Sistema Dinamico

- L'insieme degli indici $n \in D$ rappresenta una sequenza di **tempi discreti**.
- Il valore $x_n$ rappresenta la **posizione** occupata da un punto/particella sulla retta numerica al tempo $n$.

### Esempi di successioni e classificazione dei sistemi dinamici

1. **Successione** $\{x_n \} = n$ con $n \in \mathbb{N}$:
    - Descrive un **moto uniforme** lungo la retta razionale con velocità positiva e costante ($x_0 = 0, x_1 = 1, x_2 = 2, \dots$).
2. **Successione** $x_n = \frac{1}{n}$ con $n \in \mathbb{N}^* = \mathbb{N} \setminus {0}$:
    - Valori assunti: $x_1 = 1, x_2 = \frac{1}{2}, x_3 = \frac{1}{3}, \dots$.
    - Descrive un **moto limitato** nell'intervallo $(0, 1]$ che si sposta da destra verso sinistra con velocità negativa e modulo decrescente (**moto accelerato**).
3. **Successione** $x_n = (-1)^n$ con $n \in \mathbb{N}$:
    - Assume alternativamente i valori $+1$ (se $n$ è pari) e $-1$ (se $n$ è dispari).
    - Descrive un **sistema dinamico periodico** (orologio o pendolo discreto) con periodo $T = 2$ e orbita limitata a due soli punti (${+1, -1}$).
4. **Successione** $x_n = n(1 - (-1)^n)$ con $n \in \mathbb{N}$:
    - Se $n$ è pari: $(-1)^n = 1 \implies x_n = 0$.
    - Se $n$ è dispari: $(-1)^n = -1 \implies x_n = 2n$.
    - Sequenza dei valori: $x_0 = 0, x_1 = 2, x_2 = 0, x_3 = 6, x_4 = 0, x_5 = 10, \dots$.
    - Descrive un sistema dinamico con **orbita non limitata ma ricorrente** (ritorna infinitamente all'origine $0$ a tutti i tempi pari, mentre per i tempi dispari si allontana verso destra).
    - Differenza con i sistemi **transienti** (sistemi che si allontanano indefinitamente senza ritornare alla posizione iniziale).

---

## Introduzione al Limite di una Successione

### Oggetto e finalità

- Lo studio del limite analizza le **proprietà asintotiche** della successione, ovvero il comportamento dell'orbita del sistema dinamico per valori arbitrariamente grandi dell'indice o del tempo $n$.

### Definizione formale di limite

Sia ${x_n}_{n \in \mathbb{N}}$ una successione numerica in $\mathbb{Q}$ e sia $L \in \mathbb{Q}$. Si dice che la successione ha **limite** $L$, oppure che **converge** al valore $L$ (in simboli $\lim_{n \to +\infty} x_n = L$ o $x_n \to L$ per $n \to +\infty$), se: $$
\forall \varepsilon > 0, , \exists N_\varepsilon \in \mathbb{N} \quad \text{tale che} \quad \forall n > N_\varepsilon \implies L - \varepsilon < x_n < L + \varepsilon
$$ (scrittura equivalente mediante modulo: $\vert x_n - L \vert < \varepsilon$).

### Interpretazione geometrica

- L'intervallo $(L - \varepsilon, L + \varepsilon)$ rappresenta una **trappola** centrata in $L$ di ampiezza arbitrariamente piccola $\varepsilon > 0$.
- L'indice $N_\varepsilon$ costituisce la **soglia temporale**: oltre tale soglia ($n > N_\varepsilon$), tutti gli infiniti termini della successione rimangono definitivamente racchiusi all'interno dell'intervallo.
- Un numero al più finito di elementi della successione (i termini con $n \le N_\varepsilon$) può trovarsi all'esterno della trappola.
- Il limite $L$ funge da punto di **attrazione** per i valori della successione, rendendo il comportamento asintotico regolare e prevedibile.

### Anticipazioni sulle successioni analizzate

- Per $x_n = \frac{1}{n}$, si verificherà che $\lim_{n \to +\infty} \frac{1}{n} = 0$.
- Per $x_n = (-1)^n$, la successione non ammette alcun limite nell'insieme dei numeri razionali (sistema oscillante non convergente).
