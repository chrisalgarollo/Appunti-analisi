## Conseguenze Fondamentali della Completezza di $\mathbb{R}$

### Quadro generale delle applicazioni

- L'insieme dei numeri reali ($\mathbb{R}$) soddisfa la **proprietà di completezza**: una successione numerica reale $\{x_n\} \subseteq \mathbb{R}$ è convergente in $\mathbb{R}$ se e solo se è una **successione di Cauchy**.
- Dalla proprietà di completezza discendono tre conseguenze analitiche fondamentali:
    1. La **convergenza delle successioni monotone e limitate**.
    2. L'**esistenza dell'estremo superiore ed inferiore** per sottoinsiemi di $\mathbb{R}$.
    3. L'**esistenza di punti di accumulazione** per sottoinsiemi limitati e infiniti di $\mathbb{R}$.

---

## Successioni Monotone e Limitate nei Numeri Reali

### Definizioni operative

- **Successione monotona crescente**: una successione $\{x_n\}_{n \in \mathbb{N}} \subseteq \mathbb{R}$ è monotona crescente se: $$
\forall n \in \mathbb{N} \implies x_n \le x_{n+1}
$$ (Significato dinamico: moto discreto sulla retta reale con velocità non negativa che non torna mai indietro).
- **Successione superiormente limitata**: la successione $\{x_n\}$ è superiormente limitata se esiste un numero reale $M \in \mathbb{R}$ tale che: $$
\forall n \in \mathbb{N} \implies x_n \le M
$$ ovvero se l'intera successione è contenuta nella semiretta $(-\infty, M]$.

### Teorema di Convergenza delle Successioni Monotone e Limitate

- **Enunciato**: Ogni successione numerica reale $\{x_n\}$ monotona crescente e superiormente limitata è convergente in $\mathbb{R}$, ossia ammette un limite finito $L \in \mathbb{R}$ ($\lim_{n \to +\infty} x_n = L$).
    - Enunciato speculare: ogni successione monotona decrescente e inferiormente limitata converge ad un limite finito in $\mathbb{R}$.

### Dimostrazione del Teorema

1. Si supponga per **assurdo** che la successione non sia di Cauchy.
2. Negare la proprietà di Cauchy equivale ad affermare che: $$
\exists \varepsilon > 0 \quad \text{tale che} \quad \forall N \in \mathbb{N} , \hspace{0.5cm}\exists \hspace{0.2cm}m_{N,}n_N \ge N \quad \text{con} \quad |x_{n_N} - x_{m_N}| \ge \varepsilon
$$
3. Senza perdita di generalità, si assuma l'ordinamento degli indici $n_N > m_N$. Per la proprietà di monotonia crescente della successione, si ha $x_{n_N} \ge x_{m_N}$, da cui la rimozione del modulo fornisce: $$
x_{n_N} - x_{m_N} \ge \varepsilon \implies x_{n_N} \ge x_{m_N} + \varepsilon
$$
4. Si costruisca ricorsivamente una sequenza di indici ponendo la prima soglia $N_1 = 1$, ottenendo due indici $n_1 > m_1 \ge 1$ tali che $x_{n_1} \ge x_{m_1} + \varepsilon \ge x_1 + \varepsilon$.
5. Si scelga la soglia successiva $N_2 = n_1$. Esisteranno indici $n_2 > m_2 \ge n_1$ per cui $x_{n_2} \ge x_{m_2} + \varepsilon \ge x_{n_1} + \varepsilon \ge x_1 + 2\varepsilon$.
6. Reiterando la scelta al generico passo $k \in \mathbb{N}$, si seleziona $N_{k+1} = n_k$, ottenendo una sottosuccessione che soddisfa: $$
x_{n_k} \ge x_1 + k \cdot \varepsilon \quad \forall k \ge 1
$$
7. Poiché $\varepsilon > 0$ è una costante fissata, per $k \to +\infty$ la quantità $k \cdot \varepsilon$ diverge a $+\infty$. Di conseguenza, la sottosuccessione ${x_{n_k}}$ (e dunque la successione ${x_n}$) risulta non limitata superiormente.
8. Tale conclusione entra in palese contraddizione con l'ipotesi iniziale di **limitatezza superiore** ($x_n \le M$) (**assurdo**).
9. **Conclusione**: La successione $\{x_n\}$ è una **successione di Cauchy** e, per la proprietà di completezza di $\mathbb{R}$, **converge** a un limite finito $L \in \mathbb{R}$.

### Applicazione: Dimostrazione di Convergenza della Successione Ricorsiva della Radice di 2

- Si consideri la successione definita per ricorrenza da: $$
x_1 = 2, \quad x_{n+1} = \frac{x_n}{2} + \frac{1}{x_n} \quad \forall n \ge 1
$$

1. **Buona definizione e limitatezza inferiore**:
    - Si dimostra per induzione che $x_n > 0$ per ogni $n \ge 1$.
    - Utilizzando la disuguaglianza algebrica $(a - b)^2 \ge 0 \implies a^2 + b^2 \ge 2ab$ per $a = \frac{x_n}{2}$ e $b = \frac{1}{x_n}$: $$
x_{n+1} = \frac{x_n}{2} + \frac{1}{x_n} \ge 2 \sqrt{\frac{x_n}{2} \cdot \frac{1}{x_n}} = \sqrt{2}
$$ Pertanto $x_n^2 \ge 2$ per ogni $n \ge 2$. La successione è **inferiormente limitata** da $\sqrt{2} > 0$.
2. **Monotonia decrescente**:
    - Si valuti la differenza tra due termini consecutivi: $$
x_n - x_{n+1} = x_n - \left( \frac{x_n}{2} + \frac{1}{x_n} \right) = \frac{x_n}{2} - \frac{1}{x_n} = \frac{x_n^2 - 2}{2x_n}
$$
    - Poiché $x_n^2 \ge 2$ e $x_n > 0$, il numeratore ed il denominatore sono non negativi, da cui $x_n - x_{n+1} \ge 0 \implies x_{n+1} \le x_n$.
3. **Convergenza**:
    - Essendo monotona decrescente e inferiormente limitata, per il teorema appena dimostrato la successione **converge** a un limite reale $L \in \mathbb{R}$.
4. **Calcolo del limite**:
    - Passando al limite per $n \to +\infty$ in entrambi i membri della relazione di ricorrenza: $$
L = \frac{L}{2} + \frac{1}{L} \implies \frac{L}{2} = \frac{1}{L} \implies L^2 = 2 \implies L = \sqrt{2}
$$
    - Il limite reale $L = \sqrt{2}$ dimostra la risolvibilità dell'equazione $x^2 = 2$ in $\mathbb{R}$ e l'esistenza di numeri irrazionali ($\mathbb{R} \setminus \mathbb{Q} \neq \emptyset$).

---

## Estremo Superiore ed Estremo Inferiore di un Insieme

### Definizioni di maggiorante, minorante ed estremi

Sia $A \subseteq \mathbb{R}$ un sottoinsieme non vuoto di numeri reali:

- **Maggiorante**: un numero reale $\bar{x} \in \mathbb{R}$ si dice maggiorante di $A$ se: $$
\forall x \in A \implies x \le \bar{x}
$$ (ovvero l'insieme $A$ è interamente contenuto nella semiretta $(-\infty, \bar{x}]$).
- **Minorante**: un numero reale $\underline{x} \in \mathbb{R}$ si dice minorante di $A$ se: $$
\forall x \in A \implies x \ge \underline{x}
$$
- **Estremo Superiore** ($\sup A$): un numero reale $\bar{x} \in \mathbb{R}$ è l'**estremo superiore** di $A$ (in simboli $\bar{x} = \sup A$) se soddisfa due condizioni:
    1. $\bar{x}$ è un **maggiorante** di $A$ ($\forall x \in A \implies x \le \bar{x}$).
    2. $\bar{x}$ è il **minimo dei maggioranti**: per ogni $\varepsilon > 0$, la quantità $\bar{x} - \varepsilon$ non è più un maggiorante di $A$, ovvero: $$
\forall \varepsilon > 0 , \hspace{0.5cm}\exists \hspace{0.2cm}x \in A \quad \text{tale che} \quad x > \bar{x} - \varepsilon
$$

### Relazione tra Estremo Superiore e Massimo

- **Massimo di un insieme** ($\max A$): se l'estremo superiore appartiene all'insieme stesso ($\sup A \in A$), esso è detto **massimo** dell'insieme ($\max A := \sup A$).
- Se $\sup A \notin A$, l'insieme **non ammette massimo**, ma possiede comunque l'estremo superiore in $\mathbb{R}$.
- Esempi comparativi:
    1. Intervallo chiuso $A = [a, b]$: $\sup A = b$. Poiché $b \in A$, si ha $\max A = b$.
    2. Intervallo semiaperto $A = [a, b)$: $\sup A = b$. Poiché $b \notin A$, l'insieme **non possiede massimo**, ma l'estremo superiore vale $\sup A = b$.
- Convenzione per insiemi illimitati superiormente: se l'insieme $A$ non è superiormente limitato, non ammette maggioranti reali e si pone per convenzione $\sup A = +\infty$.

### Teorema di Esistenza dell'Estremo Superiore

- **Enunciato**: Ogni sottoinsieme non vuoto $A \subseteq \mathbb{R}$ superiormente limitato ammette **estremo superiore finito** in $\mathbb{R}$ ($\sup A \in \mathbb{R}$).

### Dimostrazione del Teorema dell'Estremo Superiore (Metodo di Dicotomia)

1. Poiché $A$ è superiormente limitato, esiste un maggiorante $B_0 \in \mathbb{R}$. Essendo $A$ non vuoto, si scelga un elemento $A_0 \in A$.
2. Si consideri l'intervallo chiuso $[A_0, B_0]$. Per esso vale che $A_0 \in A \cap [A_0, B_0] \neq \emptyset$ e $B_0$ è un maggiorante di $A$.
3. Si calcoli il punto medio $C_1 = \frac{A_0 + B_0}{2}$, che suddivide l'intervallo $[A_0, B_0]$ nei due sottointervalli $[A_0, C_1]$ e $[C_1, B_0]$.
4. **Regola di selezione dicotomica**:
    - Se la metà di destra $[C_1, B_0]$ contiene elementi di $A$, si definisce il nuovo intervallo $[A_1, B_1] := [C_1, B_0]$. In questo caso $B_1 = B_0$ rimane un maggiorante di $A$.
    - Se la metà di destra non contiene elementi di $A$, gli elementi di $A$ risiedono nella metà di sinistra $[A_0, C_1]$. Si definisce $[A_1, B_1] := [A_0, C_1]$. Il punto medio $B_1 = C_1$ è un maggiorante di $A$ (poiché a sua destra non vi sono punti di $A$).
5. Iterando il procedimento di dicotomia $k$ volte, si genera una successione di intervalli incapsulati $[A_k, B_k]$ tali che:
    - $[A_{k+1}, B_{k+1}] \subseteq [A_k, B_k]$ per ogni $k \ge 0$.
    - L'intersezione $[A_k, B_k] \cap A \neq \emptyset$ per ogni $k \ge 0$.
    - L'estremo destro $B_k$ è un **maggiorante** di $A$ per ogni $k \ge 0$.
    - L'ampiezza dell'intervallo $k$-esimo è data da: $$
B_k - A_k = \frac{B_0 - A_0}{2^k}
$$
6. Dalla costruzione segue che la successione degli estremi sinistri ${A_k}$ è **monotona crescente** e superiormente limitata da $B_0$. Per il teorema sulle successioni monotone, essa converge ad un limite reale: $$
\lim_{k \to +\infty} A_k = \bar{x} \in \mathbb{R}
$$
7. Analogamente, la successione degli estremi destri ${B_k}$ è **monotona decrescente** e inferiormente limitata da $A_0$, per cui converge ad un limite reale: $$
\lim_{k \to +\infty} B_k = \bar{y} \in \mathbb{R}
$$
8. Valutando la differenza tra i due limiti: $$
\bar{y} - \bar{x} = \lim_{k \to +\infty} (B_k - A_k) = \lim_{k \to +\infty} \frac{B_0 - A_0}{2^k} = 0 \implies \bar{x} = \bar{y}
$$
9. Si verifica che il limite comune $\bar{x} \in \mathbb{R}$ è l'**estremo superiore** di $A$:
    - _Verifica di maggiorante_: poiché ogni $B_k$ è maggiorante di $A$ ($x \le B_k$ per ogni $x \in A$), dal teorema di monotonia dei limiti segue che $x \le \lim_{k \to +\infty} B_k = \bar{x}$ per ogni $x \in A$. Dunque $\bar{x}$ è un maggiorante.
    - _Verifica di minimo dei maggioranti_: fissato un generico $\varepsilon > 0$, poiché $A_k \to \bar{x}$, esiste un indice $k$ per cui $A_k > \bar{x} - \varepsilon$. Poiché l'intervallo $[A_k, B_k]$ contiene elementi di $A$, esiste un $x \in A$ tale che $x \ge A_k > \bar{x} - \varepsilon$. Pertanto $\bar{x} - \varepsilon$ non è un maggiorante.
10. Si conclude che $\bar{x} = \sup A \in \mathbb{R}$.

---

## Punti Isolati e Punti di Accumulazione

### Definizione di Punto Isolato

Sia $E \subseteq \mathbb{R}$ un sottoinsieme di numeri reali e sia $\bar{x} \in \mathbb{R}$.

- Il punto $\bar{x}$ si dice **punto isolato** per l'insieme $E$ se esiste un raggio $\varepsilon > 0$ tale che l'intorno simmetrico di $\bar{x}$ privo del punto stesso non interseca l'insieme $E$: $$
((\bar{x} - \varepsilon, \bar{x} + \varepsilon) \setminus \{\bar{x}\}) \cap E = \emptyset
$$
- Interpretazione: attorno al punto $\bar{x}$ è possibile costruire una trappola circolare sufficientemente piccola che non contiene alcun altro elemento di $E$.

### Definizione di Punto di Accumulazione

- Il punto $\bar{x} \in \mathbb{R}$ si dice **punto di accumulazione** per l'insieme $E$ se **non è isolato** per $E$, ossia se per ogni raggio $\varepsilon > 0$ l'intorno simmetrico centrato in $\bar{x}$ contiene almeno un elemento di $E$ distinto da $\bar{x}$: $$
\forall \varepsilon > 0 \implies ((\bar{x} - \varepsilon, \bar{x} + \varepsilon) \setminus \{\bar{x}\}) \cap E \neq \emptyset
$$

### Caratterizzazioni equivalenti di punto di accumulazione

Un punto $\bar{x} \in \mathbb{R}$ è di accumulazione per $E$ se e solo se è soddisfatta una delle seguenti condizioni equivalenti:

1. **Formulazione insiemistica infinita**: per ogni $\varepsilon > 0$, l'intersezione dell'intorno centrato in $\bar{x}$ con l'insieme $E$ contiene un **numero infinito di punti**: $$
\vert (\bar{x} - \varepsilon, \bar{x} + \varepsilon) \cap E \vert = +\infty
$$
2. **Formulazione per successioni (Avvicinamento vincolato non banale)**: esiste una successione $\{x_k\}_{k \in \mathbb{N}} \subseteq E$ di punti appartenenti ad $E$, **tutti distinti tra loro e tutti distinti da $\bar{x}$** ($x_k \neq \bar{x}$ per ogni $k$), che converge a $\bar{x}$: $$
\lim_{k \to +\infty} x_k = \bar{x}
$$

### Proprietà distintive ed esempio illustrativo

- Il punto di accumulazione $\bar{x}$ **può sia appartenere sia non appartenere** all'insieme $E$.
- L'esclusione esplicita del punto $\bar{x}$ nelle definizioni serve a garantire un **avvicinamento non banale** (vincolato agli elementi dell'insieme $E$, mantenendo una distanza strettamente positiva).

### Esempio: Insieme dei reciproci dei numeri naturali

- Si consideri l'insieme $E = \left\{ \frac{1}{n} \middle|\hspace{0.2cm} n \in \mathbb{N}^* \right\} = \left\{1, \frac{1}{2}, \frac{1}{3}, \dots \right\} \subset \mathbb{R}$.
- **Analisi del punto $\bar{x} = 0$**:
    - Per ogni $\varepsilon > 0$, scegliendo un indice $n > \frac{1}{\varepsilon}$, si ha che $\frac{1}{n} \in (0, \varepsilon) \subset (-\varepsilon, \varepsilon)$.
    - Poiché $\lim_{n \to +\infty} \frac{1}{n} = 0$ con $\frac{1}{n} \neq 0$ per ogni $n$, il punto $\bar{x} = 0$ è un **punto di accumulazione** per l'insieme $E$.
    - Si noti che $0 \notin E$ (il punto di accumulazione risiede all'esterno dell'insieme).
- **Analisi degli elementi $x_n = \frac{1}{n} \in E$**:
    - Per ogni punto fissato $\frac{1}{n} \in E$, scegliendo un raggio $\varepsilon < \min\left( \frac{1}{n-1} - \frac{1}{n}, \frac{1}{n} - \frac{1}{n+1} \right)$, l'intorno $\left(\frac{1}{n} - \varepsilon, \frac{1}{n} + \varepsilon\right)$ non contiene alcun altro elemento di $E$ eccetto $\frac{1}{n}$.
    - Pertanto, tutti i punti dell'insieme $E$ sono **punti isolati** per $E$.
