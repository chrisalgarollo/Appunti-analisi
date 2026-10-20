# **Modulo 1: Successioni e Proprietà Fondamentali di $\mathbb{R}$**

## **BLOCCO 4: Numeri Complessi e Teorema di De Moivre**

---

### **Teorema 1 (Preliminare): Prima Formula di De Moivre (Potenza $n$-esima in Forma Trigonometrica)**

#### **Enunciato Formale**

- **Ipotesi ($H$)**: Sia $z = \rho (\cos \theta + i \sin \theta) \in \mathbb{C}$ un numero complesso espresso in forma trigonometrica, con modulo $\rho = |z| \ge 0$ ed argomento $\theta = \text{arg}(z) \in \mathbb{R}$. Sia $n \in \mathbb{N}$ con $n \ge 1$.
- **Tesi ($T$)**: La potenza $n$-esima $z^n$ è un numero complesso avente come modulo la potenza $n$-esima del modulo $\rho^n$ e come argomento il multiplo $n\theta$: $$
z^n = \rho^n [\cos(n\theta) + i \sin(n\theta)]
$$

#### **Idea Chiave della Dimostrazione**

Si dimostra per **induzione su $n$** (sfruttando la regola del prodotto trigonometrico $z_1 z_2 = \rho_1 \rho_2 [\cos(\theta_1+\theta_2) + i \sin(\theta_1+\theta_2)]$). Nel passo induttivo si applicano le formule di addizione del seno e del coseno per raccogliere l'argomento $(n+1)\theta$.

#### **Dimostrazione Dettagliata**

1. **Base dell'induzione ($n = 1$)**: $$
z^1 = \rho^1 [\cos(1\cdot\theta) + i \sin(1\cdot\theta)] = \rho (\cos\theta + i\sin\theta) = z
$$ L'uguaglianza è chiaramente vera.
2. **Passo induttivo**: Si assume vera la formula per un generico $n \in \mathbb{N}$ (ipotesi induttiva): $$
z^n = \rho^n [\cos(n\theta) + i \sin(n\theta)]
$$ Si valuta la potenza $(n+1)$-esima $z^{n+1} = z^n \cdot z$: $$
z^{n+1} = \left( \rho^n [\cos(n\theta) + i \sin(n\theta)] \right) \cdot \left( \rho [\cos\theta + i \sin\theta] \right)
$$
3. Sviluppando il prodotto tra le parentesi tonde: $$
z^{n+1} = \rho^{n+1} \left[ (\cos(n\theta)\cos\theta - \sin(n\theta)\sin\theta) + i (\cos(n\theta)\sin\theta + \sin(n\theta)\cos\theta) \right]
$$
4. Applicando le **formule di addizione trigonometriche**: $$
\cos(n\theta)\cos\theta - \sin(n\theta)\sin\theta = \cos(n\theta + \theta) = \cos((n+1)\theta)
$$
$$
\cos(n\theta)\sin\theta + \sin(n\theta)\cos\theta = \sin(n\theta + \theta) = \sin((n+1)\theta)
$$
5. Sostituendo le identità trigonometriche nell'espressione al punto 3: $$
z^{n+1} = \rho^{n+1} [\cos((n+1)\theta) + i \sin((n+1)\theta)]
$$
6. La tesi è verificata per $n+1$. Per il Principio di Induzione, la formula vale per ogni $n \in \mathbb{N}^*$.

#### **Punti Critici / Errori Tipici all'Orale**

- **Incertezza sulle formule di addizione**: All'orale si richiede di saper scrivere esplicitamente le formule di addizione per $\cos(\alpha+\beta)$ e $\sin(\alpha+\beta)$.
- **Estensione agli esponenti interi negativi ($n \in \mathbb{Z}, n < 0$)**: Saper spiegare come si estende la formula ponendo $z^{-n} = (z^{-1})^n = \rho^{-n} [\cos(-n\theta) + i \sin(-n\theta)]$.

#### **Esercizio / Domanda di Verifica**

_Calcolare $(1+i)^{8}$ esprimendo prima $1+i$ in forma trigonometrica ed applicando la Prima Formula di De Moivre._

---

### **Teorema 2 (Principale): Teorema di De Moivre per le Radici $n$-esime di un Numero Complesso**

#### **Enunciato Formale**

- **Ipotesi ($H$)**: Dato un numero complesso non nullo $w \in \mathbb{C} \setminus {0}$ espresso in forma trigonometrica $w = \rho (\cos \theta + i \sin \theta)$, con modulo $\rho = |w| > 0$ ed argomento $\theta = \text{arg}(w) \in \mathbb{R}$, e dato un numero intero $n \ge 1$.
- **Tesi ($T$)**: L'equazione algebrica $z^n = w$ ammette **esattamente $n$ soluzioni complesse distinte e non nulle** $z_0, z_1, \dots, z_{n-1} \in \mathbb{C}$ (dette radici $n$-esime di $w$). Ciascuna radice $z_k$ (per $k = 0, 1, \dots, n-1$) ha la seguente espressione in forma trigonometrica: $$
z_k = r \left( \cos \theta_k + i \sin \theta_k \right)
$$ con:
    1. **Modulo unico** $r = \sqrt[n]{\rho} = \sqrt[n]{|w|}$ (radice $n$-esima reale aritmetica del modulo $\rho$).
    2. **Argomenti distinti**: $$
\theta_k = \frac{\theta + 2k\pi}{n} = \frac{\theta}{n} + k \frac{2\pi}{n} \quad \text{per } k = 0, 1, \dots, n-1
$$

#### **Idea Chiave della Dimostrazione**

Si pone la generica incognita in forma trigonometrica $z = r (\cos \alpha + i \sin \alpha)$ e si impone l'uguaglianza $z^n = w$. Applicando la Prima Formula di De Moivre a $z^n$, l'equazione complessa si scinde in un sistema reale per il modulo ($r^n = \rho$) e per l'argomento ($n\alpha = \theta + 2k\pi$). Si dimostra infine che i valori dell'indice $k \in {0, 1, \dots, n-1}$ producono esattamente $n$ angoli geometricamente distinti nel piano di Gauss, mentre per $k \ge n$ o $k < 0$ le radici si ripetono per la periodicità $2\pi$.

#### **Dimostrazione Dettagliata**

##### **Passo 1: Derivazione delle formule per il modulo e gli argomenti**

1. Si cerchi la soluzione $z \in \mathbb{C}$ espressa in forma trigonometrica generica: $$
z = r (\cos \alpha + i \sin \alpha) \quad \text{con } r \ge 0 \text{ e } \alpha \in \mathbb{R}
$$
2. Elevando $z$ alla potenza $n$-esima tramite la Prima Formula di De Moivre: $$
z^n = r^n [\cos(n\alpha) + i \sin(n\alpha)]
$$
3. Si imponga l'uguaglianza con il numero complesso dato $w = \rho (\cos \theta + i \sin \theta)$: $$
r^n [\cos(n\alpha) + i \sin(n\alpha)] = \rho (\cos \theta + i \sin \theta)
$$
4. Due numeri complessi scritti in forma trigonometrica sono uguali se e solo se:
    - Hanno lo **stesso modulo**: $r^n = \rho$
    - Gli **argomenti differiscono per un multiplo intero di $2\pi$**: $n\alpha = \theta + 2k\pi$ per qualche $k \in \mathbb{Z}$
5. Risolvendo le due equazioni reali:
    - Poiché $r \ge 0$ e $\rho > 0$, l'equazione $r^n = \rho$ ammette un'unica soluzione reale positiva: $$
r = \sqrt[n]{\rho} = \sqrt[n]{|w|}
$$
    - Dividendo l'equazione angolare per $n$: $$
\alpha_k = \frac{\theta + 2k\pi}{n} = \frac{\theta}{n} + k \frac{2\pi}{n} \quad (k \in \mathbb{Z})
$$

##### **Passo 2: Dimostrazione dell'esistenza di esattamente $n$ soluzioni distinte**

6. Si valutino i valori degli argomenti $\alpha_k$ al variare dell'indice intero $k \in \mathbb{Z}$:
    - Per $k = 0, 1, \dots, n-1$, i valori dell'angolo sono: $$
\alpha_0 = \frac{\theta}{n}, \quad \alpha_1 = \frac{\theta}{n} + \frac{2\pi}{n}, \quad \dots, \quad \alpha_{n-1} = \frac{\theta}{n} + (n-1)\frac{2\pi}{n}
$$
    - La differenza tra due angoli generici $\alpha_j$ e $\alpha_i$ (con $0 \le i < j \le n-1$) vale: $$
\alpha_j - \alpha_i = (j - i)\frac{2\pi}{n}
$$ Poiché $1 \le j - i \le n - 1$, si ha $0 < \alpha_j - \alpha_i < 2\pi$. Angoli che differiscono per una quantità strettamente compresa tra $0$ e $2\pi$ individuano posizioni angolari **distinte** nel piano di Gauss. Dunque $z_0, z_1, \dots, z_{n-1}$ sono $n$ numeri complessi distinti.
7. **Verifica della periodicità (nessuna ulteriore soluzione)**:
    - Per un qualsiasi altro valore intero $k \in \mathbb{Z}$, per la divisione euclidea tra interi si può scrivere $k = q \cdot n + r_0$, dove $q \in \mathbb{Z}$ è il quoziente e $r_0 \in {0, 1, \dots, n-1}$ è il resto.
    - L'argomento $\alpha_k$ diventa: $$
\alpha_k = \frac{\theta + 2(qn + r_0)\pi}{n} = \frac{\theta + 2r_0\pi + 2qn\pi}{n} = \frac{\theta + 2r_0\pi}{n} + 2q\pi = \alpha_{r_0} + 2q\pi
$$
    - Poiché le funzioni trigonometriche $\cos$ e $\sin$ sono periodiche di periodo $2\pi$, si ha: $$
\cos(\alpha_k) = \cos(\alpha_{r_0} + 2q\pi) = \cos(\alpha_{r_0}) \quad \text{e} \quad \sin(\alpha_k) = \sin(\alpha_{r_0})
$$
    - Pertanto $z_k = z_{r_0}$. Ciò dimostra che al variare di $k \in \mathbb{Z}$ non si generano nuovi numeri complessi, ma si riottengono ciclicamente le medesime $n$ radici $z_0, z_1, \dots, z_{n-1}$.

#### **Punti Critici / Errori Tipici all'Orale**

- **Interpretazione geometrica**: All'orale si richiede sempre l'interpretazione geometrica delle radici $n$-esime nel piano di Gauss:
    - Le $n$ radici $z_0, z_1, \dots, z_{n-1}$ si trovano tutte sulla circonferenza centrata nell'origine con raggio $r = \sqrt[n]{|w|}$.
    - Congiungendo i punti $z_0, z_1, \dots, z_{n-1}$ nel piano di Gauss si ottiene un **poligono regolare di $n$ lati** inscritto nella circonferenza (es. $n=3$ triangolo equilatero, $n=4$ quadrato, $n=5$ pentagono regolare).
    - Il primo vertice $z_0$ ha argomento $\theta_0 = \frac{\theta}{n}$ e ciascun vertice successivo si ottiene ruotando il precedente di un angolo costante pari al passo angolare $\Delta \theta = \frac{2\pi}{n}$.
- **Uso improprio del simbolo di radice nel piano complesso**: Sottolineare che in $\mathbb{C}$ la notazione $\sqrt[n]{w}$ indica **l'insieme di tutte le $n$ radici complesse**, a differenza di quanto avviene in $\mathbb{R}$ dove $\sqrt[n]{x}$ (con $x \ge 0$) indica unicamente l'unica radice reale non negativa (radice aritmetica).

#### **Esercizio / Domanda di Verifica**

_Risolvere in $\mathbb{C}$ l'equazione $z^4 + 1 = 0$, trovando le 4 radici quarte di $-1$ in forma algebrica e rappresentandole geometricamente nel piano di Gauss._

---

### **Fonti maggiormente utilizzate per questo Blocco**

Per la stesura e la verifica delle dimostrazioni del **BLOCCO 4**, le fonti del notebook maggiormente consultate ed utilizzate sono state:

1. **`Lezione 9 07-10.md`**: Fonte principale per la trattazione teorica della Prima e Seconda Formula di De Moivre, la dimostrazione per il modulo e gli argomenti e l'inesistenza di ulteriori soluzioni oltre alle $n$ radici.
2. **`Lezione 10 12-10.md`**: Utilizzata per l'interpretazione geometrica delle radici $n$-esime come vertici di poligoni regolari nel piano di Gauss e per le proprietà di rotazione e trasformazione.
3. **`2026-10-09.pdf`**: Utilizzata per la verifica degli esercizi pratici sullo sviluppo delle radici n-esime e le equazioni nei complessi.
4. **`AMI 2026-27 Programma Teoremi Dimostarzioni.pdf`**: Utilizzato per garantire l'allineamento con i punti 11, 12, 13 e 14 del programma ufficiale d'esame.

---

Dimmi pure se la trattazione del **BLOCCO 4** (che chiude il Modulo 1) è chiara e se possiamo passare al **Modulo 2: Limiti e Funzioni Continue (BLOCCO 5: Continuità e Teoremi Globali)**.
