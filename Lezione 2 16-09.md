## Definizione Geometrica di Grafico e di Funzione

### Definizione informale vs impostazione geometrica

- Le definizioni tradizionali di funzione come "legge", "formula", "ricetta" o "prescrizione" risultano fumose dal punto di vista logico.
- La nozione di **grafico** è un concetto geometrico primario e rigoroso da cui discende formalmente la nozione di **funzione**.

### Definizione formale di grafico

- Dati due insiemi $X$ e $Y$, un **grafico** da $X$ a $Y$ è un sottoinsieme $G \subseteq X \times Y$ tale che ogni sezione verticale lo incontra in **al più un punto**.
- **Sezione verticale** ($S_x$): data da un elemento $x \in X$ fissato al variare di $y \in Y$: $$
S_x := { (x, y) \in X \times Y \mid y \in Y }
$$
- Condizione di grafico: per ogni $x \in X$, l'intersezione tra $G$ e la sezione verticale $S_x$ contiene al più un elemento: $$
G \cap S_x \text{ contiene al più un punto}
$$ (L'intersezione può essere costituita da un punto oppure essere l'insieme vuoto).
- Nota sulle curve non-grafico: le curve che intersecano le sezioni verticali in più punti (es. due o tre punti) non sono grafici di funzioni (un esempio fisico è il ciclo di **isteresi** di magnetizzazione di un materiale ferromagnetico). Vengono studiate successivamente come curve nel piano.

### Esempi di grafici e non-grafici nel piano razionale

1. Insieme $G = { (x, x^2) \in \mathbb{Q} \times \mathbb{Q} \mid x \in \mathbb{Q} }$:
    - È un **grafico** (rappresenta una parabola con asse verticale) poiché per ciascuna prima coordinata $x$ esiste un'unica seconda coordinata $x^2$.
2. Insieme $F = { (x^2, x) \in \mathbb{Q} \times \mathbb{Q} \mid x \in \mathbb{Q} }$:
    - **Non è un grafico** (rappresenta una parabola con asse orizzontale) poiché per un valore $x^2 > 0$ la retta verticale interseca l'insieme in due punti distinti ($x$ e $-x$).

---

## Dominio, Immagine e Costruzione della Funzione

### Dominio e immagine di un grafico

Dato un grafico $G \subseteq X \times Y$:

- **Dominio del grafico** ($\text{Dom}(G)$):
    - Definizione formale: insieme dei punti $x \in X$ per cui esiste almeno un elemento $y \in Y$ tale che la coppia $(x,y) \in G$: $$
\text{Dom}(G) := { x \in X \mid \exists y \in Y \mid (x,y) \in G }
$$
    - Significato geometrico: corrisponde alla **proiezione** del grafico $G$ sul primo fattore $X$ (asse orizzontale). Per questi punti $x$, la sezione verticale $S_x$ incontra $G$ in esattamente un punto ($\exists! y \in Y$).
- **Immagine del grafico** ($\text{Im}(G)$):
    - Definizione formale: insieme degli elementi $y \in Y$ per cui esiste un punto $x \in \text{Dom}(G)$ tale che la coppia $(x,y) \in G$: $$
\text{Im}(G) := { y \in Y \mid \exists x \in \text{Dom}(G) \mid (x,y) \in G }
$$
    - Significato geometrico: corrisponde alla **proiezione** del grafico $G$ sul secondo fattore $Y$ (asse verticale). Un punto $y$ appartiene all'immagine se la retta orizzontale alla quota $y$ incontra $G$ in almeno un punto.
- Nota sul **codominio**: l'insieme $Y$ costituisce il codominio; l'immagine $\text{Im}(G)$ può coincidere con $Y$ oppure esserne un sottoinsieme proprio (se il grafico è limitato verticalmente).

### Definizione di funzione derivata dal grafico

- Dato un grafico $G \subseteq X \times Y$, per ogni $x \in \text{Dom}(G)$ esiste un unico $y \in Y$ tale che $(x,y) \in G$.
- Si dice che $y$ è **funzione** di $x$ (esprime la dipendenza per cui al variare di $x$ nel dominio cambia $y$) e si scrive $y = f_G(x)$ (oppure $f(x)$).
- Ricostruzione del grafico tramite la funzione: $$
G = { (x, f_G(x)) \in X \times Y \mid x \in \text{Dom}(G) }
$$
- **Dominio e Immagine della funzione**:
    - $\text{Dom}(f_G) := \text{Dom}(G)$
    - $\text{Im}(f_G) := \text{Im}(G)$
    - Notazione sintetica: $f_G : \text{Dom}(f_G) \to \text{Im}(f_G) \subseteq Y$.

### Prassi applicativa e studio dell'immagine

- Nella pratica si parte da una formula espressa algebricamente (es. $f(x) = x^2$) e si determina:
    1. Il massimo insieme di definizione (**dominio della funzione**).
    2. Il grafico $G_f = { (x, f(x)) \in \mathbb{Q} \times \mathbb{Q} \mid x \in \mathbb{Q} }$.
    3. L'**immagine della funzione** ($\text{Im}(f)$).
- Esempio per $f(x) = x^2$ definiti sui razionali $\mathbb{Q}$:
    - $\text{Dom}(f) = \mathbb{Q}$.
    - $\text{Im}(f) = { x^2 \mid x \in \mathbb{Q} }$.
    - Il numero $2 \notin \text{Im}(f)$ poiché $2$ non è il quadrato di alcun numero razionale.
    - Tutto il semiasse verticale negativo non appartiene all'immagine $\text{Im}(f)$.
- Importanza applicativa: la determinazione dell'immagine è fondamentale nelle scienze applicate (es. valori assunti dalla temperatura di un sistema fisico sottoposta a vincoli di funzionamento).

---

## Proprietà delle Funzioni: Iniettività

### Le tre proprietà di classificazione

- Proprietà di interesse per lo studio delle funzioni: **iniettività**, **suriettività** e **bigettività** (enunciate come strumenti di qualificazione per distinguere e classificare le funzioni).

### Definizione di funzione iniettiva

- Una funzione $f: X \to Y$ è **iniettiva** se punti distinti del dominio hanno immagini distinte: $$
\forall x_1, x_2 \in X, \quad x_1 \neq x_2 \implies f(x_1) \neq f(x_2)
$$
- Formulazione contronominale equivalente: $$
\forall x_1, x_2 \in X, \quad f(x_1) = f(x_2) \implies x_1 = x_2
$$
- Interpretazione: la funzione non "confonde" i punti.
- Significato geometrico: ogni retta orizzontale interseca il grafico della funzione in **al più un punto**.
- Collegamento: l'iniettività è legata alla proprietà di **invertibilità** della funzione.

### Esempi di verifica dell'iniettività

1. Funzione $f(x) = 2x$ con $x \in \mathbb{Q}$:
    - È **iniettiva**. Infatti: $$
f(x_1) = f(x_2) \implies 2x_1 = 2x_2 \implies x_1 = x_2
$$
2. Funzione $f(x) = x^2$ con $x \in \mathbb{Q}$:
    - **Non è iniettiva**. Infatti per $x_1 = 1$ e $x_2 = -1$ (punti distinti) si ha $f(1) = f(-1) = 1$. Geometricamente, le rette orizzontali ad ampiezza positiva intersecano il grafico della parabola in due punti distinti ($x$ e $-x$).

---

## Relazioni di Equivalenza

### Definizione formale di relazione di equivalenza

- Una **relazione di equivalenza** su un insieme $X$ è un sottoinsieme $R \subseteq X \times X$ (formato da coppie ordinate) che soddisfa le seguenti tre proprietà:
    1. **Riflessività**: per ogni $x \in X$, la coppia $(x,x) \in R$ (ogni elemento è in relazione con se stesso; geometricamente $R$ contiene la diagonale principale).
    2. **Simmetria**: se $(x,y) \in R$, allora $(y,x) \in R$ (geometricamente l'insieme $R$ è simmetrico rispetto alla diagonale principale).
    3. **Transitività**: per ogni $x, y, z \in X$, se $(x,y) \in R$ e $(y,z) \in R$, allora $(x,z) \in R$.
- Notazione: se $(x,y) \in R$, si scrive $x \sim_R y$ oppure $x \sim y$ e si dice che "$x$ è **in relazione** con $y$".

### Classe di equivalenza

- Dato un elemento $x \in X$, si definisce **classe di equivalenza** di $x$ (indicata con $[x]_R$ o $[x]_\sim$) l'insieme di tutti gli elementi $y \in X$ in relazione con $x$: $$
[x]_R := { y \in X \mid x \sim y }
$$
- Ogni classe di equivalenza è un sottoinsieme di $X$ (elemento dell'insieme delle parti $\mathcal{P}(X)$).

### Analogia intuitiva (calciatori e squadre)

- Insieme $X$: calciatori del campionato di Serie A.
- Relazione: due calciatori sono equivalenti se indossano la stessa maglia (appartengono alla stessa squadra).
- Classe di equivalenza di un calciatore: l'insieme di tutti i calciatori della sua squadra.
- Insieme delle classi di equivalenza: l'insieme delle squadre (entità usata per stilare il calendario del campionato, distinta dai singoli giocatori).

---

## Insieme Quoziente ed Esempi di Costruzione

### Definizione di insieme quoziente

- L'**insieme quoziente** (indicato con $X / R$ oppure $X / \sim$) è definito come l'insieme di tutte le classi di equivalenza: $$
X / R := { [x]_R \mid x \in X }
$$
- Costituisce un nuovo insieme i cui elementi sono sottoinsiemi di $X$ (elementi dell'insieme delle parti $\mathcal{P}(X)$).

### Esempio 1: Relazione geometrica nel piano razionale

- Insieme $X = \mathbb{Q} \times \mathbb{Q}$.
- Definizione della relazione: $(x,y) \sim (x',y') \iff x = x'$ (due punti sono in relazione se hanno la stessa prima coordinata).
- Verifica delle proprietà:
    - Riflessività: $(x,y) \sim (x,y)$ poiché $x = x$.
    - Simmetria: se $x = x'$, allora $x' = x$.
    - Transitività: se $x = x'$ e $x' = x''$, ne segue $x = x''$.
- Classe di equivalenza di un punto $(x,y)$: la **retta verticale** passante per la prima coordinata $x$.
- Insieme quoziente $X / \sim$: l'insieme di tutte le **rette verticali** del piano razionale.

### Esempio 2: Costruzione rigorosa dei numeri razionali $\mathbb{Q}$

- Insieme di partenza $X$: sottoinsieme di $\mathbb{Z} \times \mathbb{Z}$ formato dalle coppie di interi $(m,n)$ con secondo elemento non nullo: $$
X := { (m,n) \in \mathbb{Z} \times \mathbb{Z} \mid n \neq 0 }
$$
- Definizione della relazione di equivalenza: $$
(m,n) \sim (m',n') \iff m \cdot n' = m' \cdot n
$$
- Esempio di elementi in relazione: la coppia $(1,2)$ è in relazione con $(2,4)$ poiché $1 \cdot 4 = 2 \cdot 2$.
- Insieme quoziente $X / R$: corrisponde esattamente all'insieme dei **numeri razionali** ($\mathbb{Q}$).
- Interpretazione formale:
    - La scrittura frazionaria $\frac{m}{n}$ rappresenta la classe di equivalenza del punto $(m,n)$.
    - Uno stesso numero razionale (ad esempio il valore decimale $0{,}5$) ammette **molteplici rappresentazioni equivalenti**: $$
\frac{1}{2}, \quad \frac{2}{4}, \quad \frac{3}{6}, \quad \frac{50}{100}
$$ che costituiscono elementi distinti equivalenti tra loro appartenenti a un'unica classe di equivalenza nell'insieme quoziente.
