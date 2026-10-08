## Operazioni sui Numeri Complessi in Forma Algebrica

### Richiamo delle definizioni di base

- Un numero complesso $z \in \mathbb{C}$ è definito come una coppia ordinata di numeri reali $(a, b) \in \mathbb{R} \times \mathbb{R}$, rappresentabile geometricamente nel **piano di Gauss**.
- **Immersione dei numeri reali**: la funzione iniettiva $x \mapsto (x, 0)$ identifica la retta reale con l'asse orizzontale del piano complesso, consentendo la notazione $x \equiv (x, 0)$.
- **Unità immaginaria** ($i$): definita come la coppia $i := (0, 1)$.
- **Proprietà fondamentale dell'unità immaginaria**: $i^2 = -1$.
- **Risoluzione dell'equazione $z^2 = -1$**: ammette due soluzioni complesse distinte, rappresentate da $i$ e $-i$ (poiché sia $(+i)^2 = -1$ sia $(-i)^2 = -1$).
- **Forma algebrica**: ogni numero complesso $z = (a, b)$ si esprime come $z = a + i b$, dove $a = \text{Re}(z)$ è la **parte reale** e $b = \text{Im}(z)$ è la **parte immaginaria**.

### Somma di numeri complessi in forma algebrica

Siano $z = a + i b$ e $w = c + i d$ due numeri complessi espresso in forma algebrica, con $a, b, c, d \in \mathbb{R}$:

- Applicando le proprietà commutativa, associativa e distributiva della somma e del prodotto: $$
z + w = (a + i b) + (c + i d) = (a + c) + i(b + d)
$$
- Risultato:
    - **Parte reale della somma**: $\text{Re}(z + w) = a + c$.
    - **Parte immaginaria della somma**: $\text{Im}(z + w) = b + d$.

### Prodotto di numeri complessi in forma algebrica

Siano $z = a + i b$ e $w = c + i d$:

- Sviluppando il prodotto con le proprietà algebriche standard: $$
z \cdot w = (a + i b)(c + i d) = a c + a(i d) + (i b)c + (i b)(i d) = a c + i(a d + b c) + i^2 b d
$$
- Sostituendo la relazione $i^2 = -1$: $$
z \cdot w = (a c - b d) + i(a d + b c)
$$
- Risultato:
    - **Parte reale del prodotto**: $\text{Re}(z \cdot w) = a c - b d$.
    - **Parte immaginaria del prodotto**: $\text{Im}(z \cdot w) = a d + b c$.
- Vantaggio operativo: l'esecuzione dei calcoli in forma algebrica richiede soltanto l'applicazione delle consuete proprietà algebriche e la sostituzione di $i^2$ con $-1$, evitando la memorizzazione della formula per componenti.

### Calcolo delle potenze dell'unità immaginaria

- $i^0 := 1$
- $i^1 = i$
- $i^2 = -1$
- $i^3 = i^2 \cdot i = (-1) \cdot i = -i$
- $i^4 = i^2 \cdot i^2 = (-1) \cdot (-1) = 1$
- $i^5 = i^4 \cdot i = 1 \cdot i = i$
- **Periodicità delle potenze di $i$**: le potenze intere di $i$ sono periodiche di periodo 4. L'elemento $i$ costituisce un elemento di **torsione** (elevato alla quarta potenza riproduce l'unità $1$).

---

## Rappresentazione nel Piano di Gauss e Punti Notevoli

### Parti reale e immaginaria

- Per $z = a + i b$:
    - $\text{Re}(z) = a \in \mathbb{R}$ (longitudine sull'asse orizzontale).
    - $\text{Im}(z) = b \in \mathbb{R}$ (latitudine sull'asse verticale; è il coefficiente reale di $i$ e non include l'unità immaginaria $i$).
    - Espressione sintetica: $z = \text{Re}(z) + i \text{Im}(z)$.

### Posizione dei punti fondamentali nel piano complesso

- **Origine** $0 = (0, 0)$: $\text{Re}(0) = 0$, $\text{Im}(0) = 0$.
- **Unità reale** $1 = (1, 0)$: collocata sull'asse reale orizzontale.
- **Unità immaginaria** $i = (0, 1)$: collocata sull'asse immaginario verticale, con $\text{Re}(i) = 0$ e $\text{Im}(i) = 1$.
- Opposti: $-1 = (-1, 0)$ sull'asse orizzontale e $-i = (0, -1)$ sull'asse verticale.
- **Costruzione di $1 + i$**: punto ottenuto mediante la regola del parallelogramma (o diagonale del quadrato unitario) con parte reale $1$ e parte immaginaria $1$. Punti simmetrici correlati: $1 - i$, $-1 + i$, $-1 - i$.

---

## Complesso Coniugato e Modulo

### Definizione di Complesso Coniugato

- Dato un numero complesso $z = \text{Re}(z) + i \text{Im}(z)$, si definisce **complesso coniugato** di $z$ (indicato con la notazione $\bar{z}$) il numero complesso: $$
\bar{z} := \text{Re}(z) - i \text{Im}(z)
$$
- Proprietà delle componenti:
    - $\text{Re}(\bar{z}) = \text{Re}(z)$
    - $\text{Im}(\bar{z}) = -\text{Im}(z)$
- **Significato geometrico**: la funzione di coniugazione $z \mapsto \bar{z}$ rappresenta la **simmetria speculare rispetto all'asse reale** (asse orizzontale) nel piano di Gauss.

### Definizione di Modulo di un Numero Complesso

- Dato $z = a + i b \in \mathbb{C}$, si definisce **modulo** di $z$ (indicato con $|z|$) la quantità reale non negativa: $$
|z| := \sqrt{[\text{Re}(z)]^2 + [\text{Im}(z)]^2} = \sqrt{a^2 + b^2}
$$
- **Relazione tra prodotto per il coniugato e modulo**:
    - Calcolo del prodotto $\bar{z} \cdot z$: $$
\bar{z} \cdot z = (\text{Re}(z) - i \text{Im}(z))(\text{Re}(z) + i \text{Im}(z)) = [\text{Re}(z)]^2 - i^2 [\text{Im}(z)]^2 = [\text{Re}(z)]^2 + [\text{Im}(z)]^2
$$
    - Pertanto: $$
\bar{z} \cdot z = |z|^2 \implies |z| = \sqrt{z \cdot \bar{z}}
$$

### Significato Geometrico del Modulo e Distanza Euclidea

- Nel piano di Gauss, per il teorema di Pitagora applicato al triangolo rettangolo di cateti $|\text{Re}(z)|$ e $|\text{Im}(z)|$, l'ipotenusa ha lunghezza $\sqrt{[\text{Re}(z)]^2 + [\text{Im}(z)]^2} = |z|$.
- Il modulo $|z|$ rappresenta la **distanza euclidea di $z$ dall'origine** $0 = (0, 0)$.
- **Distanza Euclidea tra due numeri complessi**: dati $z, w \in \mathbb{C}$, la distanza euclidea tra i due punti è definita come: $$
d(z, w) := |z - w|
$$ ovvero il modulo della loro differenza.

---

## Proprietà del Modulo, del Coniugato e della Distanza

### Proprietà fondamentali

1. **Modulo dell'opposto**: $$
|-z| = |z|
$$
    - Giustificazione algebrica: $\text{Re}(-z) = -\text{Re}(z)$ e $\text{Im}(-z) = -\text{Im}(z)$, i cui quadrati coincidono con quelli di $z$.
    - Giustificazione geometrica: la trasformazione $z \mapsto -z$ rappresenta la **simmetria centrale rispetto all'origine**, che costituisce un'**isometria** (conserva la distanza dall'origine).
2. **Modulo del coniugato**: $$
|\bar{z}| = |z|
$$
    - Giustificazione geometrica: la coniugazione $z \mapsto \bar{z}$ è una **simmetria speculare rispetto all'asse reale**, la quale conserva le distanze (isometria).
3. **Disuguaglianza triangolare nei numeri complessi**:
    - Per ogni terna di numeri complessi $z_1, z_2, z_3 \in \mathbb{C}$: $$
|z_1 - z_2| \le |z_1 - z_3| + |z_3 - z_2|
$$
    - Interpretazione geometrica: nel triangolo di vertici $z_1, z_2, z_3$ nel piano di Gauss, la lunghezza del lato $|z_1 - z_2|$ non può superare la somma delle lunghezze degli altri due lati $|z_1 - z_3| + |z_3 - z_2|$.
4. **Proprietà algebriche della coniugazione**:
    - Coniugato della somma: $\overline{z + w} = \bar{z} + \bar{w}$
    - Coniugato del prodotto: $\overline{z \cdot w} = \bar{z} \cdot \bar{w}$
5. **Modulo del prodotto**:
    - Per ogni $z_1, z_2 \in \mathbb{C}$: $$
|z_1 \cdot z_2| = |z_1| \cdot |z_2|
$$ (il modulo del prodotto è il prodotto dei moduli).

### Calcolo pratico del reciproco in forma algebrica

- Per ogni $z \in \mathbb{C}$ non nullo ($z \neq 0 \iff |z| > 0$), moltiplicando e dividendo per il coniugato $\bar{z}$: $$
\frac{1}{z} = \frac{\bar{z}}{z \cdot \bar{z}} = \frac{\bar{z}}{|z|^2} = \frac{\text{Re}(z) - i \text{Im}(z)}{[\text{Re}(z)]^2 + [\text{Im}(z)]^2} = \frac{\text{Re}(z)}{|z|^2} - i \frac{\text{Im}(z)}{|z|^2}
$$
- **Esempio applicativo**: calcolo del reciproco di $z = 1 + i$.
    - Il modulo al quadrato vale $|1+i|^2 = 1^2 + 1^2 = 2$.
    - Moltiplicando e dividendo per il coniugato $1 - i$: $$
\frac{1}{1+i} = \frac{1-i}{(1+i)(1-i)} = \frac{1-i}{1^2 - i^2} = \frac{1-i}{2} = \frac{1}{2} - i \frac{1}{2}
$$

---

## Forma Trigonometrica di un Numero Complesso

### Derivazione della forma trigonometrica

- Sia $z \in \mathbb{C}$ con $z \neq 0$ (ovvero col modulo $\rho := |z| > 0$).
- Esprimendo $z$ come prodotto del suo modulo per un numero complesso unitario $w$: $$
z = |z| \cdot \frac{z}{|z|} = \rho \cdot w \quad \text{con} \quad w := \frac{z}{|z|}
$$
- Verificazione del modulo di $w$: $$
|w| = \left| \frac{z}{|z|} \right| = \frac{|z|}{|z|} = 1
$$ Pertanto, $w$ è un punto appartenente alla circonferenza unitaria centrata nell'origine.
- Sia $\theta$ (**argomento**) l'angolo orientato in senso antiorario formato dalla semiretta uscente dall'origine e passante per $z$ con l'asse reale positivo.
- Per la definizione delle funzioni trigonometriche nel triangolo rettangolo iscritto nella circonferenza unitaria: $$
\text{Re}(w) = \cos \theta, \quad \text{Im}(w) = \sin \theta \implies w = \cos \theta + i \sin \theta
$$
- Sostituendo $w$ nell'espressione di $z$: $$
z = \rho (\cos \theta + i \sin \theta)
$$

### Nomenclatura e relazioni fondamentali

- $\rho = |z| > 0$: **modulo** del numero complesso $z$.
- $\theta = \text{arg}(z)$: **argomento** del numero complesso $z$, definito a meno di un multiplo intero di $2\pi$ ($\theta + 2k\pi$ con $k \in \mathbb{Z}$). Nelle applicazioni si fissa un intervallo di periodicità di ampiezza $2\pi$ (es. $[0, 2\pi)$ oppure $(-\pi, \pi]$).
- Conversione dalla forma trigonometrica alla forma algebrica:
    - $\text{Re}(z) = \rho \cos \theta$
    - $\text{Im}(z) = \rho \sin \theta$
- Conversione dalla forma algebrica alla forma trigonometrica:
    - $\rho = \sqrt{[\text{Re}(z)]^2 + [\text{Im}(z)]^2}$
    - $\tan \theta = \frac{\text{Im}(z)}{\text{Re}(z)}$ (per $\text{Re}(z) \neq 0$).

### Esempi di conversione in forma trigonometrica

1. **Numero reale positivo** $z = 1$:
    - $\rho = |1| = 1$, $\theta = 0$.
    - Forma trigonometrica: $1 = 1(\cos 0 + i \sin 0)$.
2. **Numero reale negativo** $z = -1$:
    - $\rho = |-1| = 1$, $\theta = \pi$.
    - Forma trigonometrica: $-1 = 1(\cos \pi + i \sin \pi)$.
3. **Numero complesso** $z = 1 + i$:
    - Modulo: $\rho = \sqrt{1^2 + 1^2} = \sqrt{2}$.
    - Argomento (diagonale del primo quadrante): $\theta = \frac{\pi}{4}$ ($45^\circ$).
    - Forma trigonometrica: $1 + i = \sqrt{2} \left( \cos \frac{\pi}{4} + i \sin \frac{\pi}{4} \right)$.
4. **Analisi dell'espressione** $z = \rho (\cos \theta - i \sin \theta)$ con $\rho > 0$:
    - L'espressione non è in forma trigonometrica standard a causa del segno negativo.
    - Sfruttando la parità del coseno ($\cos(-\theta) = \cos \theta$) e la disparità del seno ($\sin(-\theta) = -\sin \theta$): $$
z = \rho (\cos(-\theta) + i \sin(-\theta))
$$
    - Modulo: $|z| = \rho$; Argomento: $\text{arg}(z) = -\theta$.

---

## Prodotto e Potenze in Forma Trigonometrica (Prima Formula di De Moivre)

### Prodotto di numeri complessi in forma trigonometrica

- Siano $z_1 = \rho_1 (\cos \theta_1 + i \sin \theta_1)$ e $z_2 = \rho_2 (\cos \theta_2 + i \sin \theta_2)$.
- Calcolo del prodotto: $$
z_1 \cdot z_2 = \rho_1 \rho_2 [(\cos \theta_1 \cos \theta_2 - \sin \theta_1 \sin \theta_2) + i (\cos \theta_1 \sin \theta_2 + \sin \theta_1 \cos \theta_2)]
$$
- Applicando le formule di addizione per il coseno e per il seno: $$
z_1 \cdot z_2 = \rho_1 \rho_2 [\cos(\theta_1 + \theta_2) + i \sin(\theta_1 + \theta_2)]
$$
- **Regole operative del prodotto**:
    - Il modulo del prodotto è il **prodotto dei moduli**: $|z_1 \cdot z_2| = \rho_1 \cdot \rho_2$.
    - L'argomento del prodotto è la **somma degli argomenti**: $\text{arg}(z_1 \cdot z_2) = \theta_1 + \theta_2$.

### Prima Formula di De Moivre (Potenza $n$-esima)

- Estendendo la regola del prodotto a $n$ fattori identici $z = \rho (\cos \theta + i \sin \theta)$ per $n \in \mathbb{N}$: $$
z^n = \rho^n [\cos(n\theta) + i \sin(n\theta)]
$$
- Proprietà della potenza:
    - Modulo: $|z^n| = \rho^n$.
    - Argomento: $\text{arg}(z^n) = n\theta$.
- **Esempio applicativo**: calcolo di $z^8$ per $z = \frac{1+i}{\sqrt{2}}$.
    - Modulo: $\rho = \sqrt{\left(\frac{1}{\sqrt{2}}\right)^2 + \left(\frac{1}{\sqrt{2}}\right)^2} = 1$.
    - Argomento: $\theta = \frac{\pi}{4}$.
    - Applicazione della formula: $$
z^8 = 1^8 \left[ \cos\left(8 \cdot \frac{\pi}{4}\right) + i \sin\left(8 \cdot \frac{\pi}{4}\right) \right] = 1 \cdot [\cos(2\pi) + i \sin(2\pi)] = 1 \cdot (1 + i \cdot 0) = 1
$$

---

## Estrazione delle Radici $n$-esime (Seconda Formula di De Moivre)

### Teorema sulle Radici $n$-esime nei Numeri Complessi

- Dato un numero complesso $w \neq 0$ avente modulo $\rho = |w| > 0$ ed argomento $\theta = \text{arg}(w)$, e dato un intero $n \ge 1$.
- L'equazione algebrica $z^n = w$ ammette esattamente $n$ soluzioni complesse **distinte e non nulle** $z_0, z_1, \dots, z_{n-1}$ (dette **radici $n$-esime** di $w$).

### Formule esplicite per le radici $n$-esime

Le $n$ soluzioni $z_k = r_k (\cos \theta_k + i \sin \theta_k)$ per $k = 0, 1, \dots, n-1$ sono date da:

1. **Modulo unico**: $$
r_k = \sqrt[n]{\rho} = \sqrt[n]{|w|}
$$ (radice $n$-esima reale aritmetica del modulo $\rho$).
2. **Argomenti delle $n$ radici**: $$
\theta_k = \frac{\theta + 2k\pi}{n} = \frac{\theta}{n} + k \frac{2\pi}{n} \quad \text{per } k = 0, 1, \dots, n-1
$$

### Dimostrazione

1. **Verifica che $z_k$ sono soluzioni**:
    - Elevando $z_k$ alla potenza $n$-esima mediante la prima formula di De Moivre: $$
(z_k)^n = (r_k)^n [\cos(n\theta_k) + i \sin(n\theta_k)]
$$
    - Sostituendo $r_k = \sqrt[n]{\rho}$ e $n\theta_k = n \left( \frac{\theta + 2k\pi}{n} \right) = \theta + 2k\pi$: $$
(z_k)^n = \rho [\cos(\theta + 2k\pi) + i \sin(\theta + 2k\pi)] = \rho (\cos \theta + i \sin \theta) = w
$$
2. **Dimostrazione dell'inesistenza di ulteriori soluzioni**:
    - Sia $z = r (\cos \alpha + i \sin \alpha)$ una generica soluzione dell'equazione $z^n = w$.
    - Per la prima formula di De Moivre: $z^n = r^n [\cos(n\alpha) + i \sin(n\alpha)] = \rho (\cos \theta + i \sin \theta)$.
    - Uguagliando i moduli: $r^n = \rho \implies r = \sqrt[n]{\rho}$.
    - Uguagliando gli argomenti (a meno di un multiplo intero di $2\pi$): $$
n\alpha = \theta + 2k\pi \implies \alpha = \frac{\theta + 2k\pi}{n} \quad (k \in \mathbb{Z})
$$
    - Al variare di $k \in {0, 1, \dots, n-1}$, le formule generano $n$ valori angolari geometricamente distinti. Per valori di $k \ge n$ o $k < 0$, gli angoli differiscono da quelli ottenuti nei primi $n$ passi per multipli interi di $2\pi$, riproducendo esattamente le medesime $n$ radici.