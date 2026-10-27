## Riepilogo delle Proprietà delle Funzioni Continue e Scopo del Calcolo Differenziale

### Richiamo dei teoremi generali sulle funzioni continue

- **Teorema dei valori intermedi**: una funzione continua su un intervallo chiuso e limitato assume tutti i valori compresi tra il suo minimo e il suo massimo assoluto.
- **Teorema degli zeri**: una funzione continua su un intervallo chiuso e limitato che assume valori di segno opposto agli estremi ammette almeno uno zero all'interno dell'intervallo.
- **Teorema di Weierstrass**: una funzione continua su un intervallo chiuso e limitato ammette sempre sia un **massimo assoluto** sia un **minimo assoluto** (non necessariamente unici).

### Scopi del calcolo differenziale

- **Scopo analitico**: studiare funzioni complesse approssimandole localmente (nell'intorno di un punto) tramite funzioni più semplici, come i polinomi di primo grado (funzioni affini o lineari).
- **Scopo geometrico**: approssimare curve complesse nel piano (grafici di funzioni) mediante le curve più semplici possibili, ossia le rette.

### Richiamo della definizione di derivata e differenziabilità

- **Rapporto incrementale**: quoziente tra l'incremento o oscillazione della funzione $f(x) - f(x_0)$ e la lunghezza con segno dell'intervallo $x - x_0$.
- **Derivata**: limite del rapporto incrementale per $x \to x_0$: $$
\lim_{x \to x_0} \frac{f(x) - f(x_0)}{x - x_0} = f'(x_0)
$$
- **Interpretazione geometrica**: l'arcotangente della derivata $f'(x_0)$ rappresenta l'angolo limite a cui tendono le rette secanti passanti per $(x_0, f(x_0))$ e $(x, f(x))$ quando $x \to x_0$.
- **Continuità come condizione necessaria**: se una funzione è derivabile in un punto, essa è necessariamente **continua** in quel punto. Se presenta un salto o una discontinuità, non può essere derivabile.
- **Differenziabilità**: equivalenza analitica della derivabilità. Una funzione derivabile $f(x)$ si scompone nella sua **parte principale** (polinomiale di primo grado) più un **resto** o **funzione di errore** $r(x)$: $$
f(x) = f(x_0) + f'(x_0)(x - x_0) + r(x)
$$ con la condizione che il resto sia un **infinitesimo di ordine superiore al primo**: $$
\lim_{x \to x_0} \frac{r(x)}{x - x_0} = 0 \quad (\text{notazione di Landau: } r(x) = o(x - x_0))
$$ L'errore $r(x)$ tende a zero più rapidamente della potenza $1$ dell'incremento $x - x_0$ (in certi casi come il quadrato, il cubo o potenze dell'ordine di $1{,}5$).
- **Derivate elementari note**:
    - **Funzione costante** ($f(x) = C$): derivata ovunque nulla ($f'(x) = 0$), poiché il grafico è una retta orizzontale priva di inclinazione.
    - **Funzione identità** ($f(x) = x$): derivata ovunque unitaria ($f'(x) = 1$), corrisponde all'inclinazione a $45^\circ$ della bisettrice del primo e terzo quadrante.
    - **Funzione quadratica** ($f(x) = x^2$): derivata pari a $f'(x) = 2x$.

---

## Dimostrazione delle Regole di Derivazione

### 1. Derivata della Somma (Proprietà 1)

- **Enunciato**: Siano $f$ e $g$ due funzioni derivabili nel punto $x_0$. Allora la funzione somma $f + g$ è derivabile in $x_0$ e vale: $$
(f + g)'(x_0) = f'(x_0) + g'(x_0)
$$
- **Dimostrazione**:
    1. Si scrive il rapporto incrementale della funzione somma $f + g$: $$
\frac{(f + g)(x) - (f + g)(x_0)}{x - x_0} = \frac{f(x) + g(x) - f(x_0) - g(x_0)}{x - x_0}
$$
    2. Riorganizzando i termini al numeratore, il rapporto incrementale si scompone nella somma dei singoli rapporti incrementali di $f$ e di $g$: $$
\frac{(f + g)(x) - (f + g)(x_0)}{x - x_0} = \frac{f(x) - f(x_0)}{x - x_0} + \frac{g(x) - g(x_0)}{x - x_0}
$$
    3. Poiché per ipotesi $f$ e $g$ sono derivabili in $x_0$, esistono finiti i limiti dei singoli rapporti incrementali per $x \to x_0$.
    4. Per il **teorema del limite della somma**, il limite della somma è uguale alla somma dei singoli limiti: $$
\lim_{x \to x_0} \frac{(f + g)(x) - (f + g)(x_0)}{x - x_0} = \lim_{x \to x_0} \frac{f(x) - f(x_0)}{x - x_0} + \lim_{x \to x_0} \frac{g(x) - g(x_0)}{x - x_0} = f'(x_0) + g'(x_0)
$$

### 2. Derivata del Prodotto per una Costante (Proprietà 2)

- **Enunciato**: Se $f$ è derivabile in $x_0$ e $\alpha \in \mathbb{R}$, allora $(\alpha f)'(x_0) = \alpha f'(x_0)$.
- Dimostrazione lasciata per esercizio (discende dal portare la costante $\alpha$ fuori dal limite del rapporto incrementale).

### 3. Regola di Leibniz per la Derivata del Prodotto (Proprietà 3)

- **Enunciato**: Siano $f$ e $g$ due funzioni derivabili nel punto $x_0$. Allora la funzione prodotto $f \cdot g$ è derivabile in $x_0$ e la sua derivata vale: $$
(f \cdot g)'(x_0) = f'(x_0)g(x_0) + f(x_0)g'(x_0)
$$
- **Dimostrazione**:
    1. Si consideri il rapporto incrementale della funzione prodotto $f \cdot g$: $$
\frac{(f \cdot g)(x) - (f \cdot g)(x_0)}{x - x_0} = \frac{f(x)g(x) - f(x_0)g(x_0)}{x - x_0}
$$
    2. Si aggiunga e si sottragga la quantità intermedia $f(x_0)g(x)$ al numeratore: $$
\frac{f(x)g(x) - f(x_0)g(x) + f(x_0)g(x) - f(x_0)g(x_0)}{x - x_0}
$$
    3. Raccogliendo $g(x)$ nei primi due termini e $f(x_0)$ negli ultimi due, si separa l'espressione in due addendi: $$
\frac{f(x) - f(x_0)}{x - x_0} \cdot g(x) + f(x_0) \cdot \frac{g(x) - g(x_0)}{x - x_0}
$$
    4. Si valuta il limite per $x \to x_0$ dei singoli fattori:
        - $\frac{f(x) - f(x_0)}{x - x_0} \to f'(x_0)$ per l'ipotesi di derivabilità di $f$.
        - $g(x) \to g(x_0)$ per la **continuità** di $g$ in $x_0$ (conseguenza della sua derivabilità).
        - $f(x_0)$ è un fattore costante.
        - $\frac{g(x) - g(x_0)}{x - x_0} \to g'(x_0)$ per la derivabilità di $g$.
    5. Applicando i teoremi algebrici sui limiti di somme e prodotti: $$
\lim_{x \to x_0} \frac{(f \cdot g)(x) - (f \cdot g)(x_0)}{x - x_0} = f'(x_0)g(x_0) + f(x_0)g'(x_0)
$$

### 4. Derivata del Quoziente (Proprietà 4)

- **Enunciato**: Se $f$ e $g$ sono derivabili in $x_0$ con $g(x_0) \neq 0$, allora: $$
\left( \frac{f}{g} \right)'(x_0) = \frac{f'(x_0)g(x_0) - f(x_0)g'(x_0)}{[g(x_0)]^2}
$$
- Conseguenza diretta della combinazione della regola del prodotto con la derivata della reciproca $1/g$ (lasciata per esercizio).

### 5. Derivata della Funzione Composta (Proprietà 5)

- **Enunciato**: Sia $f$ derivabile nel punto $x_0$ e sia $g$ derivabile nel punto $y_0 = f(x_0)$. Allora la funzione composta $g \circ f$ è derivabile in $x_0$ e la sua derivata è data dal prodotto delle derivate delle componenti calcolate nei punti corrispondenti: $$
(g \circ f)'(x_0) = g'(f(x_0)) \cdot f'(x_0)
$$
- **Dimostrazione**:
    1. Si scriva il rapporto incrementale della funzione composta $g \circ f$ tra $x$ e $x_0$: $$
\frac{g(f(x)) - g(f(x_0))}{x - x_0}
$$
    2. Moltiplicando e dividendo l'espressione per l'incremento della funzione interna $f(x) - f(x_0)$: $$
\frac{g(f(x)) - g(f(x_0))}{f(x) - f(x_0)} \cdot \frac{f(x) - f(x_0)}{x - x_0}
$$
    3. Si effettui la sostituzione $y = f(x)$ e $y_0 = f(x_0)$.
    4. Poiché $f$ è derivabile in $x_0$, essa è anche continua in $x_0$, pertanto per $x \to x_0$ si ha che $y \to y_0$.
    5. Per il **teorema del limite della funzione composta** e il **teorema del limite del prodotto**:
        - Il primo fattore $\frac{g(y) - g(y_0)}{y - y_0} \to g'(y_0) = g'(f(x_0))$ per $y \to y_0$.
        - Il secondo fattore $\frac{f(x) - f(x_0)}{x - x_0} \to f'(x_0)$ per $x \to x_0$.
    6. Si conclude che: $$
\lim_{x \to x_0} \frac{g(f(x)) - g(f(x_0))}{x - x_0} = g'(f(x_0)) \cdot f'(x_0)
$$

---

## Derivata della Funzione Inversa e Dimostrazione Geometrica

### Enunciato del Teorema sulla Funzione Inversa (Proprietà 6)

- Sia $f$ una funzione invertibile e derivabile nel punto $x_0$ con $f'(x_0) \neq 0$.
- La funzione inversa $f^{-1}$ è derivabile nel punto corrispondente $y_0 = f(x_0)$ e la sua derivata è il reciproco della derivata della funzione di partenza: $$
(f^{-1})'(y_0) = \frac{1}{f'(x_0)} = \frac{1}{f'(f^{-1}(y_0))}
$$

### Dimostrazione Geometrica

1. **Rappresentazione grafica**: nel piano cartesiano, il grafico della funzione inversa $f^{-1}$ (in blu) si ottiene ribaltando simmetricamente il grafico della funzione $f$ (in rosso) rispetto alla **bisettrice del primo e terzo quadrante** ($y = x$).
2. **Proprietà dell'isometria**: la simmetria speculare rispetto alla bisettrice $y = x$ è un'**isometria** (conserva le distanze).
3. **Trasformazione della retta tangente**:
    - Essendo $f$ derivabile in $x_0$, il suo grafico ammette una retta tangente (in verde) nel punto $(x_0, f(x_0))$ con coefficiente angolare $m_1 = f'(x_0)$.
    - Riflettondo la retta tangente rispetto alla bisettrice $y = x$, si ottiene la retta tangente al grafico della funzione inversa $f^{-1}$ nel punto riflesso $(y_0, x_0) = (f(x_0), x_0)$, con coefficiente angolare $m_2 = (f^{-1})'(y_0)$.
    - Ciò garantisce l'esistenza della retta tangente per $f^{-1}$ e quindi la sua derivabilità in $y_0$.
4. **Relazione tra i coefficienti angolari**:
    - I coefficienti angolari $m_1$ e $m_2$ di due rette simmetriche rispetto alla bisettrice $y = x$ soddisfano la relazione algebrica fondamentale per cui il loro prodotto è unitario: $$
m_1 \cdot m_2 = 1
$$
    - Sostituendo $m_1 = f'(x_0)$ e $m_2 = (f^{-1})'(y_0)$: $$
f'(x_0) \cdot (f^{-1})'(y_0) = 1 \implies (f^{-1})'(y_0) = \frac{1}{f'(x_0)}
$$

---

## Calcolo di Derivate Elementari e di Funzioni Inverse

### Derivata della Funzione Tangente

- Sia $f(x) = \tan x = \frac{\sin x}{\cos x}$ per $x \neq \frac{\pi}{2} + k\pi$.
- Sapendo che $D(\sin x) = \cos x$ e $D(\cos x) = -\sin x$, si applica la regola di derivazione del quoziente: $$
D(\tan x) = \frac{(\sin x)' \cos x - \sin x (\cos x)'}{\cos^2 x} = \frac{\cos x \cdot \cos x - \sin x (-\sin x)}{\cos^2 x} = \frac{\cos^2 x + \sin^2 x}{\cos^2 x}
$$
- **Forme equivalenti del risultato**:
    1. Utilizzando la prima identità fondamentale della trigonometria $\cos^2 x + \sin^2 x = 1$: $$
D(\tan x) = \frac{1}{\cos^2 x}
$$
    2. Spezzando la frazione in due addendi: $$
D(\tan x) = \frac{\cos^2 x}{\cos^2 x} + \frac{\sin^2 x}{\cos^2 x} = 1 + \tan^2 x
$$

### Derivata della Funzione Arcotangente

- Sia $g(y) = \arctan y$ la funzione inversa della funzione tangente $f(x) = \tan x$ definita su $\left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$.
- Applicando il Teorema di derivazione della funzione inversa: $$
g'(y) = D(\arctan y) = \frac{1}{f'(x)} = \frac{1}{D(\tan x)}
$$
- Esprimendo la derivata della tangente nella forma $1 + \tan^2 x$: $$
g'(y) = \frac{1}{1 + \tan^2 x}
$$
- Poiché $x = \arctan y$, si ha che $\tan x = \tan(\arctan y) = y$. Sostituendo nell'espressione: $$
D(\arctan y) = \frac{1}{1 + y^2}
$$
- **Nota analitica**: sebbene l'arcotangente sia una funzione goniometrica inversa, la sua derivata è una funzione **razionale/polinomiale** ($\frac{1}{1+y^2}$), collegando due famiglie funzionali concettualmente distinte.

---

## Esempio Notevole di Studio di Derivata e Limiti

### Analisi della funzione $f(x) = \arctan x + \arctan\left(\frac{1}{x}\right)$

- **Dominio**: la funzione è definita per ogni $x \in \mathbb{R} \setminus {0}$ (a causa della presenza del termine $\frac{1}{x}$).

### Calcolo della derivata prima per $x \neq 0$

1. Applicando la regola della somma e la regola della funzione composta per il secondo addendo: $$
f'(x) = D(\arctan x) + D\left(\arctan\left(\frac{1}{x}\right)\right)
$$
2. Per il primo addendo: $D(\arctan x) = \frac{1}{1 + x^2}$.
3. Per il secondo addendo (composta dell'arcotangente con $\frac{1}{x}$): $$
D\left(\arctan\left(\frac{1}{x}\right)\right) = \frac{1}{1 + \left(\frac{1}{x}\right)^2} \cdot D\left(\frac{1}{x}\right) = \frac{1}{1 + \frac{1}{x^2}} \cdot \left(-\frac{1}{x^2}\right) = \frac{x^2}{x^2 + 1} \cdot \left(-\frac{1}{x^2}\right) = -\frac{1}{1 + x^2}
$$
4. Sommando i due contributi per $x \neq 0$: $$
f'(x) = \frac{1}{1 + x^2} - \frac{1}{1 + x^2} = 0 \quad \forall x \in \mathbb{R} \setminus {0}
$$

### Interpretazione geometrica ed esame dei limiti

- La derivata $f'(x) = 0$ in tutto il dominio $x \neq 0$.
- Poiché il dominio $\mathbb{R} \setminus {0}$ non è connesso ma è formato da due semirette separate (componenti connesse $(-\infty, 0)$ e $(0, +\infty)$), il fatto che la derivata sia nulla implica che la funzione è **costante a tratti** sulle singole componenti connesse, assumendo due valori diversi nei due semipiani.
- **Calcolo dei valori sui semiasse mediante i limiti**:
    1. Per $x \to +\infty$:
        - $\lim_{x \to +\infty} \frac{1}{x} = 0 \implies \arctan\left(\frac{1}{x}\right) \to \arctan(0) = 0$.
        - $\lim_{x \to +\infty} \arctan x = \frac{\pi}{2}$.
        - Quindi $\lim_{x \to +\infty} f(x) = \frac{\pi}{2} + 0 = \frac{\pi}{2}$.
        - Per tutti i punti $x > 0$, la funzione è la **semiretta orizzontale costante** $y = \frac{\pi}{2}$.
    2. Per $x \to -\infty$:
        - $\lim_{x \to -\infty} \frac{1}{x} = 0 \implies \arctan\left(\frac{1}{x}\right) \to 0$.
        - $\lim_{x \to -\infty} \arctan x = -\frac{\pi}{2}$.
        - Quindi $\lim_{x \to -\infty} f(x) = -\frac{\pi}{2} + 0 = -\frac{\pi}{2}$.
        - Per tutti i punti $x < 0$, la funzione è la **semiretta orizzontale costante** $y = -\frac{\pi}{2}$.