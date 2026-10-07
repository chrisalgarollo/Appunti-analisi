## Punti di Accumulazione e Insieme Derivato

### Richiamo della definizione di punto di accumulazione

- Sia $E \subseteq \mathbb{R}$ un sottoinsieme di numeri reali e sia $\bar{x} \in \mathbb{R}$.
- Il punto $\bar{x}$ si dice **punto di accumulazione** per l'insieme $E$ se per ogni $\varepsilon > 0$, l'intersezione tra l'intorno simmetrico $(\bar{x} - \varepsilon, \bar{x} + \varepsilon)$ e l'insieme $E$, privato al più del punto $\bar{x}$ stesso, contiene un numero infinito di punti: $$
\vert (\bar{x} - \varepsilon, \bar{x} + \varepsilon) \cap (E \setminus \{\bar{x}\}) \vert = +\infty
$$
- **Esclusione dell'avvicinamento banale**: la rimozione di $\bar{x}$ dall'insieme garantisce che l'avvicinamento al punto avvenga mediante elementi di $E$ distinti da $\bar{x}$, evitando il caso banale in cui $\bar{x} \in E$ e si consideri la coincidenza del punto con se stesso.
- **Caratterizzazione mediante successioni**:
    - Scegliendo $\varepsilon = \frac{1}{n}$ per ogni $n \in \mathbb{N}^*$, esiste un punto $x_n \in E$ con $x_n \neq \bar{x}$ tale che la distanza euclidea soddisfa: $$
\vert x_n - \bar{x} \vert < \frac{1}{n}
$$
    - Un punto $\bar{x} \in \mathbb{R}$ è di accumulazione per $E$ se e solo se esiste una successione $\{x_n\} \subseteq E \setminus \{\bar{x}\}$ di punti dell'insieme, tutti distinti da $\bar{x}$, che converge a $\bar{x}$: $$
\lim_{n \to +\infty} x_n = \bar{x}
$$

### Definizione di Insieme Derivato

- Si definisce **insieme derivato** dell'insieme $E$ (indicato con la notazione $E'$) l'insieme formato da tutti i punti di accumulazione di $E$: $$
E' := \{ x \in \mathbb{R} \mid x \text{ è punto di accumulazione per } E \}
$$

### Esempi di calcolo dell'insieme derivato

1. **Insieme dei numeri razionali** ($E = \mathbb{Q}$):
    - Poiché l'insieme dei numeri razionali $\mathbb{Q}$ è **denso** nei numeri reali $\mathbb{R}$, in ogni intorno arbitrariamente piccolo di qualsiasi numero reale cade almeno un numero razionale.
    - Di conseguenza, ogni numero reale è punto di accumulazione per $\mathbb{Q}$ e l'insieme derivato coincide con l'intero asse reale: $$
\mathbb{Q}' = \mathbb{R}
$$
2. **Insieme finito di punti**:
    - Se $E$ è un insieme finito, ogni suo elemento è isolato (intorno sufficientemente piccolo non contiene altri punti dell'insieme).
    - Poiché non esistono punti a cui avvicinarsi in maniera non banale, l'insieme derivato è l'**insieme vuoto**: $$
E' = \emptyset
$$
3. **Insieme dei numeri naturali** ($E = \mathbb{N}$):
    - Sebbene l'insieme $\mathbb{N}$ contenga infiniti punti, gli elementi sono distanziati tra loro di almeno una unità.
    - Attorno a un qualsiasi numero reale è possibile costruire un intorno di raggio inferiore a $0{,}5$ che contiene al più un solo numero naturale (rendendo l'avvicinamento banale) o nessun numero naturale.
    - Pertanto, l'insieme dei numeri naturali non possiede punti di accumulazione: $$
\mathbb{N}' = \emptyset
$$

---

## Il Teorema di Bolzano-Weierstrass

### Enunciato del Teorema

Sia $E \subseteq \mathbb{R}$ un sottoinsieme dei numeri reali che sia **limitato** e **infinito** (avente cardinalità non finita). Allora l'insieme dei suoi punti di accumulazione è non vuoto ($E' \neq \emptyset$), ossia esiste almeno un punto di accumulazione $\bar{x} \in \mathbb{R}$ per l'insieme $E$.

### Necessità e indipendenza delle ipotesi

- Se si rimuove l'ipotesi di **infinità** (insieme limitato ma finito), l'insieme non ammette punti di accumulazione (es. insieme di un numero finito di punti ha $E' = \emptyset$).
- Se si rimuove l'ipotesi di **limitatezza** (insieme infinito ma illimitato), l'insieme può non ammettere punti di accumulazione (es. $E = \mathbb{N}$ ha $\mathbb{N}' = \emptyset$).
- La combinazione simultanea di limitatezza ed infinità garantisce la presenza di almeno un punto di accumulazione.

### Dimostrazione del Teorema (Metodo di Dicotomia)

1. Poiché l'insieme $E$ è **limitato**, esso è interamente contenuto in un intervallo chiuso $[a_0, b_0] \subset \mathbb{R}$.
2. L'intersezione $[a_0, b_0] \cap E = E$ contiene un **numero infinito di punti**.
3. Si consideri il punto medio $c = \frac{a_0 + b_0}{2}$, che suddivide l'intervallo $[a_0, b_0]$ nei due sottointervalli $[a_0, c]$ e $[c, b_0]$.
4. **Regola di selezione dicotomica**: almeno uno dei due sottointervalli deve contenere infiniti punti dell'insieme $E$. (Se infatti entrambi i sottointervalli contenessero un numero finito di punti di $E$, la loro unione $[a_0, b_0]$ conterrebbe un numero finito di punti di $E$, contraddicendo l'ipotesi che $E$ è infinito).
5. Si seleziona una delle metà che contiene infiniti punti di $E$ (se entrambe ne contengono infiniti, si sceglie una delle due) e la si denota con $[a_1, b_1]$.
6. Iterando ricorsivamente il procedimento di dicotomia $k$ volte, si genera una successione incapsulata di intervalli $[a_k, b_k]$ aventi le seguenti proprietà:
    - $[a_{k+1}, b_{k+1}] \subseteq [a_k, b_k] \subseteq \dots \subseteq [a_0, b_0]$ per ogni $k \ge 0$.
    - L'intersezione $[a_k, b_k] \cap E$ contiene **infiniti punti** di $E$ per ogni $k \ge 0$.
    - L'ampiezza del $k$-esimo intervallo vale: $$
b_k - a_k = \frac{b_0 - a_0}{2^k}
$$ .
7. Dalle proprietà della dicotomia, la successione degli estremi sinistri ${a_k}$ è **monotona crescente** e la successione degli estremi destri ${b_k}$ è **monotona decrescente**. Entrambe le successioni convergono allo stesso limite reale $\bar{x} \in \mathbb{R}$: $$
\lim_{k \to +\infty} a_k = \lim_{k \to +\infty} b_k = \bar{x}
$$
8. **Costruzione della successione vincolata**:
    - Poiché ogni intervallo $[a_k, b_k]$ contiene infiniti punti di $E$, per ogni $k \in \mathbb{N}$ è possibile scegliere un punto $x_k \in E \cap [a_k, b_k]$ tale che $x_k \neq \bar{x}$ (essendoci infiniti punti, se ne trova sempre uno distinto dal valore limite $\bar{x}$).
    - Per ogni $k \in \mathbb{N}$, il punto $x_k$ soddisfa la catena di disuguaglianze: $$
a_k \le x_k \le b_k
$$ .
9. **Applicazione del Teorema dei due carabinieri (del confronto)**:
    - Poiché $a_k \to \bar{x}$ e $b_k \to \bar{x}$ per $k \to +\infty$, per il teorema dei due carabinieri la successione ${x_k}$ converge a $\bar{x}$: $$
\lim_{k \to +\infty} x_k = \bar{x}
$$
10. **Conclusione**: Essendo ${x_k} \subseteq E \setminus {\bar{x}}$ una successione di punti dell'insieme tutti distinti da $\bar{x}$ e convergente a $\bar{x}$, il numero reale $\bar{x}$ è un **punto di accumulazione** per l'insieme $E$ ($\bar{x} \in E'$).

---

## Introduzione ai Numeri Complessi ($\mathbb{C}$)

### Motivazione algebrica

- Nell'insieme dei numeri reali $\mathbb{R}$, l'equazione algebrica $x^2 = -1$ (o $x^2 + 1 = 0$) non possiede alcuna soluzione, poiché il quadrato di qualsiasi numero reale è non negativo ($x^2 \ge 0$ per ogni $x \in \mathbb{R}$) e non può essere uguale a $-1$.
- Origine storica: l'esigenza di risolvere equazioni algebriche di grado superiore sviluppata nel XV e XVI secolo (Cardano e altri matematici) portò all'invenzione di un sistema numerico esteso capace di gestire le radici di quantità negative.

### Definizione formale dell'insieme dei numeri complessi

- L'insieme dei **numeri complessi** (indicato con $\mathbb{C}$) è definito formalmente come il **prodotto cartesiano** di due copie dell'insieme dei numeri reali: $$
\mathbb{C} := \mathbb{R} \times \mathbb{R} = { (a, b) \mid a \in \mathbb{R} \land b \in \mathbb{R} }
$$
- Un **numero complesso** $z \in \mathbb{C}$ è una **coppia ordinata** di numeri reali $(a, b)$. L'ordine degli elementi è vincolante: scambiando le componenti si ottiene un numero complesso distinto.

### Rappresentazione geometrica: Il Piano di Gauss

- Un numero complesso $z = (a, b)$ si rappresenta geometricamente come un punto in un piano cartesiano a due assi ortogonali.
- Coordinate geografiche del punto:
    - La prima coordinata $a \in \mathbb{R}$ rappresenta la **longitudine** (posizione sull'asse orizzontale).
    - La seconda coordinata $b \in \mathbb{R}$ rappresenta la **latitudine** (posizione sull'asse verticale).
- **Distinzione terminologica**:
    - Si definisce **piano cartesiano** il piano della geometria euclidea bidimensionale basato su distanze ed angoli.
    - Si definisce **piano di Gauss** il medesimo piano quando si evidenzia la struttura algebrica dei numeri complessi associata ai suoi punti.

---

## Operazioni Algebriche sui Numeri Complessi

Dati due numeri complessi $z = (a, b)$ e $w = (c, d) \in \mathbb{C}$:

### Somma di numeri complessi

- **Definizione formale**: la somma $z + w$ è il numero complesso ottenuto sommando le componenti omologhe: $$
z + w := (a + c, , b + d)
$$
- **Significato geometrico (Legge del parallelogramma)**:
    - Nel piano di Gauss, sommare due numeri complessi $z$ e $w$ corrisponde ad individuare il quarto vertice del parallelogramma formato dall'origine $(0,0)$, da $z$ e da $w$.

### Prodotto di numeri complessi

- **Definizione formale**: il prodotto $z \cdot w$ è il numero complesso definito dalla legge: $$
z \cdot w := (ac - bd, , ad + bc)
$$

### Elementi neutri dell'algebra complessa

1. **Elemento neutro per la somma**: la coppia $(0, 0) \in \mathbb{C}$.
    - Per ogni $z = (a, b) \in \mathbb{C}$: $$
(a, b) + (0, 0) = (a + 0, b + 0) = (a, b)
$$ .
2. **Elemento neutro per il prodotto (Unità complessa)**: la coppia $(1, 0) \in \mathbb{C}$.
    - Per ogni $z = (a, b) \in \mathbb{C}$: $$
(a, b) \cdot (1, 0) = (a \cdot 1 - b \cdot 0, , a \cdot 0 + b \cdot 1) = (a, b)
$$ .
3. **Proprietà dello zero nel prodotto**: $$
(a, b) \cdot (0, 0) = (a \cdot 0 - b \cdot 0, , a \cdot 0 + b \cdot 0) = (0, 0)
$$ .

### Proprietà algebriche della somma e del prodotto

Le operazioni estese ereditano le proprietà fondamentali dell'algebra reale:

- **Commutatività**: $$
z + w = w + z, \quad z \cdot w = w \cdot z
$$ .
- **Associatività**: $$
(z + w) + u = z + (w + u), \quad (z \cdot w) \cdot u = z \cdot (w \cdot u)
$$ .
- **Distributività del prodotto rispetto alla somma**: $$
z \cdot (w + u) = z \cdot w + z \cdot u
$$ .

### Reciproco di un numero complesso

- Oggetto: determinare l'elemento $1/z \in \mathbb{C}$ tale che $z \cdot \left(\frac{1}{z}\right) = (1, 0)$.
- Condizione di esistenza: il numero complesso deve essere non nullo, ovvero $z = (a, b) \neq (0, 0)$, il che equivale a richiedere che la somma dei quadrati delle componenti sia strettamente positiva ($a^2 + b^2 > 0$).
- **Formula del reciproco**: $$
\frac{1}{z} := \left( \frac{a}{a^2 + b^2}, , \frac{-b}{a^2 + b^2} \right)
$$ .
- **Verifica algebrica**: $$
(a, b) \cdot \left( \frac{a}{a^2 + b^2}, , \frac{-b}{a^2 + b^2} \right) = \left( \frac{a^2}{a^2 + b^2} - \frac{-b^2}{a^2 + b^2}, , \frac{-ab}{a^2 + b^2} + \frac{ba}{a^2 + b^2} \right) = (1, 0)
$$ .
- L'unico numero complesso privo di reciproco è lo zero $(0, 0)$.

---

## Immersione dei Numeri Reali nei Numeri Complessi

### Definizione della funzione di immersione

- Si definisce la funzione $f: \mathbb{R} \to \mathbb{C}$ che associa ad ogni numero reale $x \in \mathbb{R}$ la coppia complessa con seconda coordinata nulla: $$
f(x) := (x, 0)
$$

### Proprietà dell'immersione

1. **Iniettività**: la funzione $f$ è **iniettiva**, permettendo di identificare l'insieme dei numeri reali $\mathbb{R}$ con la sua immagine $f(\mathbb{R}) = { (x, 0) \mid x \in \mathbb{R} } \subset \mathbb{C}$ (corrispondente all'asse orizzontale del piano di Gauss).
2. **Conservazione delle operazioni algebriche**:
    - Per ogni $x, y \in \mathbb{R}$: $$
f(x + y) = (x + y, 0) = (x, 0) + (y, 0) = f(x) + f(y)
$$
$$
f(x \cdot y) = (x \cdot y, 0) = (x, 0) \cdot (y, 0) = f(x) \cdot f(y)
$$ .

- **Notazione semplificata**: grazie alla conservazione algebrica, si identifica la coppia $(x, 0)$ direttamente con il numero reale $x$ ($x \equiv (x, 0)$), considerando $\mathbb{R}$ come sottoinsieme proprio di $\mathbb{C}$ ($\mathbb{R} \subset \mathbb{C}$).

---

## Unità Immaginaria e Forma Algebrica dei Numeri Complessi

### Decomposizione algebrica di un numero complesso

Ogni numero complesso $z = (a, b) \in \mathbb{C}$ si scompone nella somma di due coppie: $$
(a, b) = (a, 0) + (0, b)
$$ Sfruttando la definizione del prodotto di numeri complessi, la coppia $(0, b)$ si esprime come prodotto: $$
(0, b) = (0, 1) \cdot (b, 0)
$$ Pertanto: $$
z = (a, b) = (a, 0) + (0, 1) \cdot (b, 0)
$$ .

### Definizione dell'Unità Immaginaria ($i$)

- Si definisce **unità immaginaria** (indicata con il simbolo $i$) il numero complesso rappresentato dalla coppia avente prima coordinata nulla e seconda coordinata unitaria: $$
i := (0, 1)
$$

### Forma Algebrica dei Numeri Complessi

Sostituendo le identificazioni dei numeri reali $(a, 0) = a$, $(b, 0) = b$ e l'unità immaginaria $(0, 1) = i$, ogni numero complesso $z = (a, b)$ si scrive in **forma algebrica** come: $$
z = a + i b
$$

- nomenclature:
    - $a = \text{Re}(z)$: **parte reale** del numero complesso $z$.
    - $b = \text{Im}(z)$: **parte immaginaria** del numero complesso $z$ (numero reale che moltiplica l'unità immaginaria).
    - $z = \text{Re}(z) + i \text{Im}(z)$.

### Proprietà Fondamentale dell'Unità Immaginaria

- Calcolo del quadrato di $i$: $$
i^2 = i \cdot i = (0, 1) \cdot (0, 1) = (0 \cdot 0 - 1 \cdot 1, , 0 \cdot 1 + 1 \cdot 0) = (-1, 0)
$$ .
- Poiché $(-1, 0)$ si identifica con il numero reale $-1$, si ottiene la relazione algebrica fondamentale: $$
i^2 = -1
$$
- **Risoluzione dell'equazione $z^2 = -1$**:
    - L'unità immaginaria $i = (0, 1)$ (unitamente al suo opposto $-i = (0, -1)$) costituisce la soluzione esplicita dell'equazione algebrica $z^2 = -1$ nel campo dei numeri complessi $\mathbb{C}$.