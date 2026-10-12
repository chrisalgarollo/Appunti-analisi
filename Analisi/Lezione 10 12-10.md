## Interpretazione Geometrica delle Radici $n$-esime (Corollario della Seconda Formula di De Moivre)

### Disposizione geometrica delle radici nel piano complesso

- Le $n$ **radici $n$-esime** $z_0, z_1, \dots, z_{n-1}$ di un numero complesso non nullo $w \in \mathbb{C} \setminus \{0\}$ (soluzioni dell'equazione $z^n = w$) si distribuiscono sul cerchio centrato nell'origine $0$ e di raggio $r = \sqrt[n]{|w|} = \rho^{1/n}$.
- Congiungendo i punti $z_0, z_1, \dots, z_{n-1}$ nel piano di Gauss si ottiene un **poligono regolare di $n$ lati** inscritto nella circonferenza di centro $0$ e raggio $r = \sqrt[n]{\rho}$.
- Espressione trigonometrica della $k$-esima radice $z_k$: $$
z_k = \rho^{1/n} \left( \cos \theta_k + i \sin \theta_k \right)
$$ con argomenti espressi da: $$
\theta_k = \frac{\theta}{n} + k \frac{2\pi}{n} \quad \text{per } k = 0, 1, \dots, n-1
$$ dove $\theta$ rappresenta l'argomento di $w$.
- Il primo vertice $z_0$ ha argomento $\theta_0 = \frac{\theta}{n}$. I vertici successivi si ottengono incrementando l'argomento di frazioni successive dell'angolo giro $\frac{2\pi}{n}$. Dopo $n$ passaggi si compie una rotazione completa e si riottiene il vertice iniziale $z_0$.

### Esempi applicativi

1. **Radici quadrate di $-1$ ($z^2 = -1$)**:
    - Esprimentazione trigonometrica di $-1$: modulo $\rho = 1$, argomento $\theta = \pi$.
    - Essendo $n = 2$, il raggio del cerchio vale $r = \sqrt{1} = 1$.
    - Gli argomenti delle due radici sono: $$
\theta_k = \frac{\pi}{2} + k\pi \quad \text{per } k \in {0, 1}
$$
        - Per $k = 0$: $\theta_0 = \frac{\pi}{2} \implies z_0 = 1 \cdot \left(\cos \frac{\pi}{2} + i \sin \frac{\pi}{2}\right) = i$.
        - Per $k = 1$: $\theta_1 = \frac{\pi}{2} + \pi = \frac{3\pi}{2} \implies z_1 = 1 \cdot \left(\cos \frac{3\pi}{2} + i \sin \frac{3\pi}{2}\right) = -i$.
    - Il poligono regolare a due lati si identifica geometricamente con il segmento avente per estremi $i$ e $-i$.
2. **Radici quarte di $1$ ($z^4 = 1$)**:
    - Essendo $n = 4$, le radici sono quattro e formano i vertici di un **quadrato** inscritto nella circonferenza unitaria.
    - Una radice immediata è $z_0 = 1$.
    - Per simmetria del quadrato inscritto, i quattro vertici sono univocamente determinati: $$
z_0 = 1, \quad z_1 = i, \quad z_2 = -1, \quad z_3 = -i
$$ tutti aventi potenza quarta pari a $+1$ (in accordo con la periodicità di periodo 4 delle potenze di $i$).
3. **Radici cubiche di $1$ ($z^3 = 1$)**:
    - Essendo $n = 3$, le tre radici costituiscono i vertici di un **triangolo equilatero** inscritto nel cerchio unitario.
    - Vertice noto: $z_0 = 1$ (con $\theta_0 = 0$).
    - Gli argomenti dei vertici si ottengono sommando l'angolo $\frac{2\pi}{3}$: $$
\theta_0 = 0, \quad \theta_1 = \frac{2\pi}{3}, \quad \theta_2 = \frac{4\pi}{3}
$$

---

## Il Teorema Fondamentale dell'Algebra

### Definizione di funzione polinomiale

- Un **polinomiale** $P$ di grado $n \ge 1$ è una funzione $P: \mathbb{C} \to \mathbb{C}$ definita dall'espressione: $$
P(z) = c_0 + c_1 z + c_2 z^2 + \dots + c_n z^n
$$ dove $c_0, c_1, \dots, c_n \in \mathbb{C}$ sono numeri complessi fissati detti **coefficienti** (con $c_n \neq 0$).

### Enunciato del Teorema Fondamentale dell'Algebra

- Ogni polinomio $P(z)$ di grado $n \ge 1$ a coefficienti complessi ammette **esattamente $n$ radici** $z_1, z_2, \dots, z_n \in \mathbb{C}$ (non necessariamente distinte), tali che $P(z_k) = 0$ per ogni $k \in \{1, \dots, n\}$.
- **Fattorizzazione nei complessi**: ogni polinomio di grado $n$ si scompone in $\mathbb{C}$ nel prodotto di $n$ fattori lineari di primo grado: $$
P(z) = c_n (z - z_1)(z - z_2) \dots (z - z_n)
$$

### Fattorizzazione mediante radici distinte e molteplicità

- Siano $w_1, w_2, \dots, w_N$ le radici **distinte** del polinomio $P(z)$.
- Per ogni radice distinta $w_k$ esiste un intero $m_k \ge 1$, detto **molteplicità** della radice, tale che il polinomio si fattorizza come: $$
P(z) = c_n (z - w_1)^{m_1} (z - w_2)^{m_2} \dots (z - w_N)^{m_N}
$$
- La somma delle molteplicità di tutte le radici distinte coincide con il grado $n$ del polinomio: $$
m_1 + m_2 + \dots + m_N = n
$$

### Confronto tra il campo reale e il campo complesso

- La fattorizzazione completa in fattori di primo grado è sempre garantita nel campo complesso $\mathbb{C}$, ma non è in generale possibile nel campo reale $\mathbb{R}$.
- Esempio: il polinomio $x^2 + 1$ non possiede radici reali e non ammette fattorizzazione in $\mathbb{R}$. In $\mathbb{C}$ il polinomio $z^2 + 1$ possiede le due radici $z_1 = i$ e $z_2 = -i$ (ciascuna con molteplicità 1) e si fattorizza come $(z + i)(z - i)$.
- Limitazioni sulle formule risolutive: per polinomi di grado $n \ge 5$ non esistono formule algebriche generali per l'estrazione esplicita delle radici (risultato dimostrato da Cardano/Abel).
- **Caso particolare del polinomio di secondo grado ($n = 2$)**:
    - Per $P(z) = a z^2 + b z + c$ con $a \neq 0$, le radici complesse sono date dalla formula: $$
z = \frac{-b + \sqrt{b^2 - 4ac}}{2a}
$$
    - Notazione nel campo complesso: il simbolo $\sqrt{b^2 - 4ac}$ sotto radice indica l'insieme delle due radici quadrate complesse del discriminante, rendendo superfluo l'uso del doppio segno $\pm$.
- Risoluzione dell'equazione $P(z) = w$: equivale a determinare le radici (o zeri) del polinomio $P(z) - w = 0$, avente il medesimo grado di $P(z)$.

---

## Equazioni Non Algebriche nel Piano Complesso

### Caratteristiche delle equazioni non algebriche

- Le equazioni che coinvolgono operatori non algebrici, quali il **modulo** $|z|$ o il **complesso coniugato** $\bar{z}$, **non sono algebriche**.
- Per tali equazioni non si applica il Teorema Fondamentale dell'Algebra, il numero delle soluzioni non è vincolato dal grado e non sussistono metodi risolutivi generali.

### Esempio risolutivo: $z^4 = \bar{z}$

1. **Soluzione immediata**: $z = 0$ soddisfa $0^4 = \bar{0} = 0$.
2. **Ricerca delle soluzioni non nulle ($z \neq 0$)**:
    - Moltiplicando entrambi i membri per $z$: $$
z^5 = z \cdot \bar{z}
$$
    - Ricordando la relazione $z \cdot \bar{z} = |z|^2$, l'equazione diventa: $$
z^5 = |z|^2
$$
    - Applicando il modulo a entrambi i membri e sfruttando la proprietà $|z^5| = |z|^5$: $$
|z|^5 = |z|^2
$$
    - Essendo $|z| \neq 0$, dividendo per $|z|^2$ si ottiene: $$
|z|^3 = 1 \implies |z| = 1
$$
    - Sostituendo $|z| = 1$ nell'equazione $z^5 = |z|^2$, ci si riconduce all'equazione algebrica: $$
z^5 = 1
$$
    - Le soluzioni di $z^5 = 1$ sono le 5 radici quinte dell'unità $z_k$ (con $|z_k| = 1$): $$
z_k = \cos\left(\frac{2k\pi}{5}\right) + i \sin\left(\frac{2k\pi}{5}\right) \quad \text{per } k \in {0, 1, 2, 3, 4}
$$ che rappresentano i vertici di un pentagono regolare inscritto nel cerchio unitario avente un vertice in $z_0 = 1$.
3. **Numero totale di soluzioni**: l'equazione ammette **6 soluzioni distinte** ($z = 0$ e le 5 radici $z_0, z_1, z_2, z_3, z_4$).

---

## Luoghi Geometrici nel Piano Complesso

I sottoinsiemi di punti del piano di Gauss si descrivono sinteticamente mediante equazioni o disuguaglianze complesse:

1. **Retta verticale**: $$
A = \{ z \in \mathbb{C} \mid \text{Re}(z) = x_0 \} \quad (x_0 \in \mathbb{R} \text{ fissato})
$$
    - Rappresenta l'insieme dei punti con longitudine fissata a $x_0$. Per $x_0 = 0$ coincide con l'asse immaginario.
2. **Retta orizzontale**: $$
B = { z \in \mathbb{C} \mid \text{Im}(z) = y_0 } \quad (y_0 \in \mathbb{R} \text{ fissato})
$$
    - Rappresenta l'insieme dei punti con latitudine/quota fissata a $y_0$.
3. **Bisettrice del I e III quadrante**: $$
C = { z \in \mathbb{C} \mid \text{Re}(z) = \text{Im}(z) }
$$
4. **Disco chiuso di centro $z_0$ e raggio $R$**: $$
D = { z \in \mathbb{C} \mid |z - z_0| \le R } \quad (z_0 \in \mathbb{C}, , R > 0 \text{ fissati})
$$
    - Esprime la condizione per cui la distanza euclidea tra $z$ e $z_0$ non supera $R$.
5. **Circonferenza di centro $z_0$ e raggio $R$**: $$
{ z \in \mathbb{C} \mid |z - z_0| = R }
$$
6. **Asse di un segmento (Retta dei punti equidistanti)**: $$
F = { z \in \mathbb{C} \mid |z - z_1| = |z - z_2| } \quad (z_1, z_2 \in \mathbb{C} \text{ fissati e distinti})
$$
    - Rappresenta l'insieme dei punti $z$ la cui distanza da $z_1$ è uguale alla distanza da $z_2$.
    - Geometria del luogo: coincide con la **retta perpendicolare** al segmento congiungente $z_1$ e $z_2$, passante per il loro punto medio $z_M = \frac{z_1 + z_2}{2}$.

---

## Interpretazione Geometrica delle Trasformazioni nel Piano Complesso

### Rotazione pura attorno all'origine

- Sia $w \in \mathbb{C}$ un numero complesso unitario ($|w| = 1$) con argomento $\alpha = \text{arg}(w)$.
- Si consideri la trasformazione $r: \mathbb{C} \to \mathbb{C}$ definita da $r(z) := z \cdot w$.
- Valutazione del modulo e dell'argomento del trasformato:
    - Modulo: $|r(z)| = |z \cdot w| = |z| \cdot |w| = |z| \cdot 1 = |z|$ (la distanza dall'origine rimane inalterata).
    - Argomento: $\text{arg}(r(z)) = \text{arg}(z) + \text{arg}(w) = \theta + \alpha$.
- Significato geometrico: la moltiplicazione per un numero complesso di modulo unitario $|w| = 1$ rappresenta una **rotazione pura del piano** con centro nell'origine ed angolo $\alpha$ in senso antiorario.

### Dilatazione e contrazione

- Si consideri la trasformazione $f(z) := R \cdot z$ con $R > 0$ reale positivo fissato.
- Valutazione del modulo e dell'argomento:
    - Modulo: $|f(z)| = R \cdot |z|$.
    - Argomento: $\text{arg}(f(z)) = \text{arg}(R) + \text{arg}(z) = 0 + \theta = \theta$.
- Significato geometrico: l'argomento non varia, per cui il punto $f(z)$ giace sulla medesima semiretta uscente dall'origine passante per $z$.
    - Se $R > 1$: **dilatazione** (il punto si allontana dall'origine).
    - Se $R = 1$: trasformazione identica.
    - Se $0 < R < 1$: **contrazione** (il punto si avvicina all'origine).
    - Se $R < 0$: composizione di una dilatazione con la simmetria centrale rispetto all'origine.

### Esempio di trasformazione mista (Trasformazione di Joukowsky)

- Consideriamo la funzione $f: \mathbb{C} \setminus {0} \to \mathbb{C}$ definita da: $$
f(z) = \frac{1}{2} \left( z + \frac{1}{z} \right)
$$
- Effetto geometrico: trasforma la circonferenza unitaria centrata nell'origine nel segmento reale $[-1, 1]$.
- Applicazione in aerodinamica e fluidodinamica: trasforma profili geometrici complessi (come il profilo alare di un aeroplano o la carena di una nave) in figure a simmetria circolare (dischi), consentendo la risoluzione semplificata delle equazioni del flusso per poi riportare le soluzioni alla geometria reale mediante la trasformazione inversa.

---

## Introduzione ai Limiti e alla Continuità per Funzioni Reali

### Dominio e punti di accumulazione

- Si consideri una funzione $f: D \to \mathbb{R}$ definita su un sottoinsieme $D \subseteq \mathbb{R}$ (intervalli, semirette o unioni di essi).
- Sia $x_0 \in \mathbb{R}$ un **punto di accumulazione per il dominio** $D$.
- Motivazione teorica: la condizione di punto di accumulazione per $D$ è indispensabile per potersi avvicinare indefinitamente a $x_0$ mediante punti appartenenti al dominio $D$ in cui la funzione è definita. (Nei punti isolati di $D$ non è possibile valutare il comportamento limite locale).

### Definizione formale di limite finito

Si dice che la funzione $f(x)$ ha **limite finito** $L \in \mathbb{R}$ per $x$ che tende a $x_0$ (in simboli $\lim_{x \to x_0} f(x) = L$), se: $$
\forall \varepsilon > 0, , \exists \delta > 0 \quad \text{tale che} \quad \forall x \in D, , 0 < |x - x_0| < \delta \implies |f(x) - L| < \varepsilon
$$

- Formulazione insiemistica equivalente: $$
f((x_0 - \delta, x_0 + \delta) \setminus {x_0} \cap D) \subseteq (L - \varepsilon, L + \varepsilon)
$$
- Significato analitico: fissato arbitrariamente un intervallo trappola $(L - \varepsilon, L + \varepsilon)$ centrato in $L$ sull'asse verticale, è possibile individuare un raggio $\delta > 0$ sull'asse orizzontale tale che l'immagine di tutti i punti di $D$ distanti da $x_0$ meno di $\delta$ (eccettuato al più $x_0$) ricada all'interno della trappola.

### Definizione di funzione continua

- Se il punto $x_0 \in D$ è di accumulazione per $D$ e appartiene al dominio ($x_0 \in D$), e il limite per $x \to x_0$ coincide con il valore assunto dalla funzione nel punto: $$
\lim_{x \to x_0} f(x) = f(x_0)
$$ allora la funzione $f$ si dice **continua nel punto $x_0$**.
- Interpretazione: in una funzione continua, ad argomenti $x$ prossimi a $x_0$ corrispondono valori $f(x)$ prossimi a $f(x_0)$, garantendo massima prevedibilità e regolarità locale.
- Convenzione: nei punti isolati del dominio ogni funzione si considera banalmente continua.
- L'insieme di tutte le funzioni continue su un dominio $D$ si indica con la notazione $C(D)$.

---

## Variazioni sul Tema del Limite: Asintoti e Limiti Infiniti

### Asintoto verticale a $+\infty$ e $-\infty$

1. **Divergenza a $+\infty$ ($\lim_{x \to x_0} f(x) = +\infty$)**: $$
\forall M \in \mathbb{R}, , \exists \delta > 0 \quad \text{tale che} \quad \forall x \in D, , 0 < |x - x_0| < \delta \implies f(x) > M
$$
    - Significato geometrico: per qualunque quota $M$ fissata (anche enormemente grande), in un opportuno intorno di $x_0$ il grafico della funzione si colloca al di sopra di $M$, schiacciandosi attorno alla semiretta verticale uscente da $x_0$ verso $+\infty$ (**asintoto verticale positivo**).
2. **Divergenza a $-\infty$ ($\lim_{x \to x_0} f(x) = -\infty$)**: $$
\forall M \in \mathbb{R}, , \exists \delta > 0 \quad \text{tale che} \quad \forall x \in D, , 0 < |x - x_0| < \delta \implies f(x) < M
$$
    - Significato geometrico: il grafico della funzione si schiaccia verso il basso lungo la semiretta verticale diretta a $-\infty$ (**asintoto verticale negativo**).

### Asintoto orizzontale a $+\infty$

- Sia il dominio $D$ illimitato superiormente. Si dice che la funzione ammette **asintoto orizzontale** a $+\infty$ con limite $L \in \mathbb{R}$ (in simboli $\lim_{x \to +\infty} f(x) = L$), se: $$
\forall \varepsilon > 0, , \exists N \in \mathbb{R} \quad \text{tale che} \quad \forall x \in D, , x > N \implies |f(x) - L| < \varepsilon
$$
- Significato geometrico: fissata una striscia orizzontale arbitrariamente sottile $(L - \varepsilon, L + \varepsilon)$ attorno alla quota $L$, superata la soglia orizzontale $N$, l'intero grafico della funzione per $x > N$ rimane racchiuso all'interno della semistriscia orizzontale.

### Divergenza a $+\infty$ per $x \to +\infty$

- Si dice che $\lim_{x \to +\infty} f(x) = +\infty$ se: $$
\forall M \in \mathbb{R}, , \exists N \in \mathbb{R} \quad \text{tale che} \quad \forall x \in D, , x > N \implies f(x) > M
$$
- Significato geometrico: superata la soglia $N$, il grafico della funzione è interamente contenuto nel quadrante $(N, +\infty) \times (M, +\infty)$.

---

## Esempi Elementari e Sviluppi Teorici sui Limiti di Funzioni

### Verifiche di limite per funzioni elementari

1. **Funzione costante ($f(x) = C$)**:
    - Per qualsiasi punto $x_0$, vale $\lim_{x \to x_0} C = C$.
    - Dimostrazione: fissato $\varepsilon > 0$, la disuguaglianza $|f(x) - C| = |C - C| = 0 < \varepsilon$ è verificata per ogni $x \in \mathbb{R}$ senza restrizioni sul raggio $\delta > 0$.
2. **Funzione identità ($f(x) = x$)**:
    - Per qualsiasi punto $x_0$, la funzione è continua e vale $\lim_{x \to x_0} x = x_0$.
    - Dimostrazione: la disuguaglianza $|f(x) - x_0| < \varepsilon$ equivale a $|x - x_0| < \varepsilon$. È sufficiente scegliere il raggio di intorno $\delta = \varepsilon$.

### Prospettiva sui teoremi algebrici e d'ordine per le funzioni

- La quasi totalità delle funzioni modellate mediante formule algebriche risulta continua in quasi tutti i punti del proprio dominio (i punti di discontinuità costituiscono eccezioni ben delimitate).
- Per l'analisi e il calcolo dei limiti di funzioni complesse si estendono i teoremi generali già introdotti per le successioni:
    - Algebra dei limiti e della continuità (somma, prodotto, quoziente).
    - Teorema di permanenza del segno e teoremi di monotonia.
    - Teorema del confronto (dei due carabinieri).
    - Teoremi sul limite e la continuità della **funzione inversa** e della **funzione composta**.
