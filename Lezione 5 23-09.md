## Variazioni sul Tema del Limite di una Successione

### Limite per $n \to -\infty$

- **Definizione formale**: data una successione ${x_n}$ avente come dominio un insieme di indici interi negativi ($n \le 0$), si dice che $\lim_{n \to -\infty} x_n = L \in \mathbb{Q}$ se: $$
\forall \varepsilon > 0, , \exists N_\varepsilon \le 0 \quad \text{tale che} \quad \forall n \le N_\varepsilon \implies |x_n - L| < \varepsilon
$$
- **Significato analitico**: la soglia temporale $N_\varepsilon$ e gli indici $n$ assumono valori interi negativi con valore assoluto arbitrariamente grande. I valori della successione si concentrano definitivamente all'interno dell'intervallo $(L-\varepsilon, L+\varepsilon)$.

### Limiti infiniti per $n \to +\infty$ e $n \to -\infty$

- **Divergenza a $+\infty$ ($\lim_{n \to +\infty} x_n = +\infty$)**: $$
\forall M \in \mathbb{Q}, , \exists N_M \in \mathbb{N} \quad \text{tale che} \quad \forall n \ge N_M \implies x_n > M
$$
    - **Esempio canonico**: la successione identità $x_n = n$ ammette limite $+\infty$ (con scelta della soglia intera $N_M > M$).
- **Divergenza a $-\infty$ ($\lim_{n \to +\infty} x_n = -\infty$)**: $$
\forall M \in \mathbb{Q}, , \exists N_M \in \mathbb{N} \quad \text{tale che} \quad \forall n \ge N_M \implies x_n < M
$$
    - Interpretazione: fissata una qualunque barriera $M$ (positiva o negativa), la successione si colloca definitivamente a sinistra di $M$, ovvero nella semiretta $(-\infty, M)$.
- **Divergenza a $-\infty$ per $n \to -\infty$ ($\lim_{n \to -\infty} x_n = -\infty$)**: $$
\forall M \in \mathbb{Q}, , \exists N_M \le 0 \quad \text{tale che} \quad \forall n \le N_M \implies x_n < M
$$

---

## Casi di Indecisione (Forme Indeterminate)

### Estensione dei teoremi algebrici e forme di indecisione

- Le proprietà algebriche dei limiti (somma, prodotto, quoziente) mantengono la loro validità anche quando i limiti delle singole successioni sono $+\infty$ oppure $-\infty$, **eccetto** nei seguenti **casi di indecisione** (o forme indeterminate):
    1. $+\infty - \infty$ (oppure $-\infty + \infty$): limite della differenza di due successioni entrambe divergenti a $+\infty$.
    2. $\frac{0}{0}$: limite del quoziente di due successioni entrambe infinitesime.
    3. $\frac{\infty}{\infty}$: limite del quoziente di due successioni entrambe divergenti.
    4. $0 \cdot \infty$: limite del prodotto di una successione infinitesima per una successione divergente.
- **Natura analitica delle forme di indecisione**: il comportamento asintotico globale dipende dalla velocità relativa con cui le singole successioni tendono a zero o all'infinito. I teoremi generali sull'algebra dei limiti non si applicano direttamente e occorre sciogliere l'indecisione tramite manipolazioni e trasformazioni algebriche caso per caso.

---

## Proprietà di Ordine dei Limiti

### Teorema di Permanenza del Segno

- **Enunciato**: Sia ${x_n}$ una successione numerica a valori non negativi ($x_n \ge 0$ per ogni $n \in \mathbb{N}$, o definitivamente). Se esiste il limite $\lim_{n \to +\infty} x_n = L \in \mathbb{Q}$, allora anche il limite è non negativo: $$
L \ge 0
$$
- **Dimostrazione per assurdo**:
    1. Si supponga per **assurdo** che $L < 0$.
    2. Nella definizione di limite, si scelga il valore positivo arbitrario $\varepsilon = -L/2 > 0$.
    3. Per la definizione di limite, esiste una soglia $N \in \mathbb{N}$ tale che per tutti gli indici $n \ge N$: $$
L - \varepsilon < x_n < L + \varepsilon
$$
    4. Valutando la disuguaglianza destra per $n \ge N$: $$
x_n < L + \left(-\frac{L}{2}\right) = \frac{L}{2} < 0
$$
    5. Risulterebbe $x_n < 0$ per tutti gli indici $n \ge N$, in palese contraddizione con l'ipotesi iniziale $x_n \ge 0$ (**assurdo**).
    6. Pertanto, deve valere $L \ge 0$.
- **Nota sulla disuguaglianza stretta**: se una successione è strettamente positiva ($x_n > 0$), il suo limite conserva la non negatività ($L \ge 0$), ma non è garantito che sia strettamente positivo (es. $x_n = \frac{1}{n} > 0$ per ogni $n \ge 1$, ma $\lim_{n \to +\infty} \frac{1}{n} = 0$).
- Specularmente, per una successione a valori non positivi ($x_n \le 0$), se esiste il limite $L$, esso soddisfa $L \le 0$.

### Teorema di Monotonia (Conservazione dell'ordine)

- **Enunciato**: Siano ${x_n}$ e ${y_n}$ due successioni numeriche tali che $x_n \le y_n$ per ogni $n \in \mathbb{N}$ (o definitivamente). Se esistono i limiti $\lim_{n \to +\infty} x_n = L_1 \in \mathbb{Q}$ e $\lim_{n \to +\infty} y_n = L_2 \in \mathbb{Q}$, allora: $$
L_1 \le L_2
$$
- **Dimostrazione**:
    1. Si definisca la successione differenza $z_n := y_n - x_n$.
    2. Dall'ipotesi $x_n \le y_n$, la successione $z_n$ è non negativa ($z_n \ge 0$ per ogni $n$).
    3. Per il teorema sul limite della somma/differenza di successioni convergenti, il limite di $z_n$ esiste e vale: $$
\lim_{n \to +\infty} z_n = \lim_{n \to +\infty} (y_n - x_n) = L_2 - L_1
$$
    4. Applicando il **Teorema di permanenza del segno** alla successione non negativa $z_n \ge 0$, si conclude che: $$
L_2 - L_1 \ge 0 \implies L_1 \le L_2
$$

---

## Calcolo di Limiti di Potenze e Somme Geometriche

### Limite della potenza $q^n$

Sia $q \in \mathbb{Q}$ con $q \ge 0$:

1. **Caso $q > 1$**:
    - Si ponga $q = 1 + x$ con $x > 0$.
    - Per la **disuguaglianza di Bernoulli**: $$
q^n = (1 + x)^n \ge 1 + nx
$$
    - Poiché $1 + nx \to +\infty$ per $n \to +\infty$, per il teorema di monotonia si ottiene: $$
\lim_{n \to +\infty} q^n = +\infty
$$
2. **Caso $q = 1$**:
    - Successione costante $1^n = 1$, per cui $\lim_{n \to +\infty} 1^n = 1$.
3. **Caso $0 < q < 1$**:
    - Si esprima la potenza mediante la reciproca: $q^n = \frac{1}{(q^{-1})^n}$.
    - Essendo $0 < q < 1$, la base reciproca $q^{-1} = \frac{1}{q} > 1$.
    - Pertanto $(q^{-1})^n \to +\infty$, da cui il reciproco tende a zero: $$
\lim_{n \to +\infty} q^n = 0
$$

### Limite delle somme geometriche

- Sia $0 < q < 1$. Si consideri la somma delle prime $n$ potenze positive della base $q$: $$
\sum_{k=1}^n q^k = q + q^2 + \dots + q^n
$$
- Dalla formula algebrica per le somme geometriche: $$
\sum_{k=1}^n q^k = \frac{q - q^{n+1}}{1 - q}
$$
- Passando al limite per $n \to +\infty$, poiché per $0 < q < 1$ si ha $q^{n+1} = q \cdot q^n \to 0$: $$
\lim_{n \to +\infty} \sum_{k=1}^n q^k = \frac{q - 0}{1 - q} = \frac{q}{1 - q}
$$

### Applicazioni ed esempi numerici

1. **Suddivisione dell'intervallo unitario ($q = 1/2$)**: $$
\lim_{n \to +\infty} \sum_{k=1}^n \left(\frac{1}{2}\right)^k = \frac{1}{2} + \frac{1}{4} + \frac{1}{8} + \dots = \frac{1/2}{1 - 1/2} = 1
$$
    - Risolve formalmente il paradosso della suddivisione dell'intervallo unitario \(\) in un'infinità numerabile di sottointervalli dimezzati.
2. **Giustificazione del decimale periodico ($q = 1/10$)**: $$
\lim_{n \to +\infty} \sum_{k=1}^n \left(\frac{1}{10}\right)^k = 0{,}1 + 0{,}01 + 0{,}001 + \dots = \frac{1/10}{1 - 1/10} = \frac{1/10}{9/10} = \frac{1}{9}
$$
    - Fornisce la giustificazione analitica rigorosa per cui la notazione decimale periodica $0{,}\bar{1}$ corrisponde esattamente al numero razionale $\frac{1}{9}$, formalizzando la somma di infiniti addendi mediante il concetto di limite.

---

## Successioni di Cauchy nei Numeri Razionali

### Definizione formale di successione di Cauchy

- Una successione numerica ${x_n} \subseteq \mathbb{Q}$ si dice **successione di Cauchy** (oppure soddisfa la **proprietà di Cauchy**) se: $$
\forall \varepsilon > 0 (\in \mathbb{Q}), , \exists N_\varepsilon \in \mathbb{N} \quad \text{tale che} \quad \forall m, n > N_\varepsilon \implies |x_m - x_n| < \varepsilon
$$
- **Significato analitico**: esprime la condizione per cui i termini della successione si accumulano e si concentrano arbitrariamente **su se stessi** per indici sufficientemente grandi, senza fare alcun riferimento esplicito al valore del limite $L$.

### Condizione necessaria di convergenza

- **Teorema**: Se una successione ${x_n} \subseteq \mathbb{Q}$ converge a un limite $L \in \mathbb{Q}$, allora ${x_n}$ è una **successione di Cauchy**.
- **Dimostrazione**:
    1. Si supponga che $\lim_{n \to +\infty} x_n = L$. Per definizione di limite, fissato arbitrariamente $\varepsilon > 0$, esiste una soglia $N_\varepsilon \in \mathbb{N}$ tale che per ogni $k > N_\varepsilon$ si ha $|x_k - L| < \frac{\varepsilon}{2}$.
    2. Presi due indici arbitrari $m, n > N_\varepsilon$, si valuti la distanza mutua $|x_m - x_n|$.
    3. Aggiungendo e sottrando $L$ all'interno del modulo ed applicando la disuguaglianza triangolare: $$
|x_m - x_n| = |(x_m - L) + (L - x_n)| \le |x_m - L| + |x_n - L| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon
$$
    4. La proprietà di Cauchy risulta verificata.

### Incompletezza di $\mathbb{Q}$ (Non sufficienza della condizione di Cauchy)

- La proprietà di Cauchy **non è sufficiente** a garantire la convergenza di una successione all'interno dell'insieme dei numeri razionali $\mathbb{Q}$.
- **Controesempio (successione definita per ricorrenza)**:
    - Si consideri la successione definita da: $$
x_0 = 2, \quad x_{n+1} = \frac{x_n}{2} + \frac{1}{x_n} \quad \forall n \ge 0
$$
    - Si dimostra per induzione che $x_n \in \mathbb{Q}$ e $x_n > 0$ per ogni $n \in \mathbb{N}$ (la formula è ben posta).
    - Si dimostra che ${x_n}$ soddisfa la proprietà di Cauchy.
    - Se per assurdo la successione ammettesse un limite $L \in \mathbb{Q}$, applicando i teoremi algebrici sui limiti alla relazione di ricorrenza: $$
L = \frac{L}{2} + \frac{1}{L} \implies \frac{L}{2} = \frac{1}{L} \implies L^2 = 2
$$
    - Poiché l'equazione $L^2 = 2$ non possiede alcuna soluzione nell'insieme dei numeri razionali $\mathbb{Q}$, la successione di Cauchy ${x_n}$ **non converge** in $\mathbb{Q}$.
    - Ciò dimostra che la condizione di Cauchy in $\mathbb{Q}$ è solo necessaria ma non sufficiente, evidenziando la mancanza della proprietà di **completezza** dei numeri razionali.

---

## Costruzione Rigorosa dei Numeri Reali ($\mathbb{R}$)

### Proprietà dell'insieme delle successioni di Cauchy

Sia $\mathcal{C}$ l'insieme di tutte le successioni di Cauchy in $\mathbb{Q}$:

1. **Lemma 1 (Limitatezza)**: Ogni successione di Cauchy ${x_n} \in \mathcal{C}$ è **limitata**.
    - _Dimostrazione_: Nella definizione di Cauchy si scelga $\varepsilon = 1$, ottenendo una soglia $N_1 \in \mathbb{N}$ tale che per $m, n \ge N_1 \implies |x_m - x_n| < 1$. Fissando $m = N_1$, si ha $|x_n| \le |x_{N_1}| + 1$ per ogni $n \ge N_1$. L'insieme dei valori dell'intera successione è limitato poiché unione dell'insieme finito ${x_0, \dots, x_{N_1-1}}$ con l'insieme limitato dei termini per $n \ge N_1$.
2. **Lemma 2 (Chiusura algebrica)**: Se ${x_n}, {y_n} \in \mathcal{C}$, allora la successione somma ${x_n + y_n}$ e la successione prodotto ${x_n \cdot y_n}$ appartengono a $\mathcal{C}$.

### Relazione di Equivalenza su $\mathcal{C}$

- Sull'insieme $\mathcal{C}$ delle successioni di Cauchy si definisce la relazione $\sim$: $$
{x_n} \sim {y_n} \iff \lim_{n \to +\infty} (x_n - y_n) = 0
$$
- **Verifica delle proprietà di equivalenza**:
    1. _Riflessività_: ${x_n} \sim {x_n}$ poiché $\lim (x_n - x_n) = \lim 0 = 0$.
    2. _Simmetria_: se $\lim (x_n - y_n) = 0$, allora $\lim (y_n - x_n) = -\lim (x_n - y_n) = 0$.
    3. _Transitività_: se ${x_n} \sim {y_n}$ e ${y_n} \sim {z_n}$, allora $\lim (x_n - z_n) = \lim [(x_n - y_n) + (y_n - z_n)] = 0 + 0 = 0$.
- **Significato analitico**: due successioni di Cauchy equivalenti rappresentano due diverse approssimazioni razionali del medesimo numero reale.

### Definizione di $\mathbb{R}$ come Insieme Quoziente

- L'insieme dei **numeri reali** ($\mathbb{R}$) è definito formalmente come l'**insieme quoziente** di $\mathcal{C}$ rispetto alla relazione di equivalenza $\sim$: $$
\mathbb{R} := \mathcal{C} / \sim
$$
- Un **numero reale** $R \in \mathbb{R}$ è una classe di equivalenza di successioni di Cauchy razionali: $$
R = [{x_n}] = \left{ {y_n} \in \mathcal{C} ;\middle|; \lim_{n \to +\infty} (x_n - y_n) = 0 \right}
$$

### Operazioni algebriche in $\mathbb{R}$ e immersione di $\mathbb{Q}$

- **Somma e prodotto tra numeri reali**: $$
[{x_n}] + [{y_n}] := [{x_n + y_n}]
$$
$$
[{x_n}] \cdot [{y_n}] := [{x_n \cdot y_n}]
$$ Le operazioni risultano ben poste ed indipendenti dai particolari rappresentanti scelti all'interno delle classi.
- **Immersione dei numeri razionali in $\mathbb{R}$**:
    - Si definisce la funzione $f: \mathbb{Q} \to \mathbb{R}$ che associa ad ogni $q \in \mathbb{Q}$ la classe di equivalenza della successione costante $x_n = q$: $$
f(q) := [{q, q, q, \dots}]
$$
    - La funzione $f$ è **iniettiva** e conserva la struttura algebrica: $$
f(q_1 + q_2) = f(q_1) + f(q_2), \quad f(q_1 q_2) = f(q_1) f(q_2)
$$
    - Ciò consente di identificare formalmente l'insieme dei numeri razionali $\mathbb{Q}$ come sottoinsieme proprio dei numeri reali ($\mathbb{Q} \subset \mathbb{R}$).
