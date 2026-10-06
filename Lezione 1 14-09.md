## Organizzazione del Corso e Modalità d'Esame

### Struttura delle prove d'esame

- Prova scritta articolata in tre componenti:
    1. Prima parte con **tre domande secche** a risposta esatta su argomenti fondamentali, che non richiedono calcoli. Il superamento di queste tre domande è condizione necessaria e vincolante per accedere alla correzione della restante parte della prova.
    2. Parte di **teoria**: richiesta di definizioni, dimostrazioni ed enunciati di teoremi svolti a lezione (gli enunciati e le dimostrazioni obbligatorie vengono elencati esplicitamente durante il corso).
    3. Parte di **esercizi**.
- Messa a disposizione degli studenti degli appelli scritti e delle prove d'esame degli anni precedenti.

### Materiali didattici e libri di testo

- Informazioni sulla pagina del corso nei servizi online del Politecnico: descrizione dettagliata del programma suddiviso per sezioni e lista dei testi consigliati e degli eserciziari.
- Nessun testo di riferimento è obbligatorio: tutti i testi suggeriti sono idonei.
- Raccomandazione di consultare più testi in biblioteca per confrontare le spiegazioni con gli appunti presi a lezione.
- Nota sui contenuti: alcuni argomenti (ad esempio le **serie**) possono essere collocati nel primo o nel secondo volume a seconda della struttura adottata dall'autore.
- Invio settimanale dei link per la fruizione delle lezioni registrate.
- Pubblicazione di **dispense** brevi (circa due dispense di 2-3 pagine) per l'approfondimento di specifici argomenti teorici non dettagliati a lezione.

### Canali di comunicazione

- Email istituzionale del docente: `nome.cognome@polimi.it` per comunicazioni personali e urgenti.
- Email collettive inviate dal docente tramite la piattaforma dei servizi online del Politecnico per avvisi generali.
- Piattaforma **WeBeep**: utilizzata per l'inserimento di **avvisi** (pubblicazione esiti degli appelli) e la condivisione di **materiali** in formato PDF (dispense, locandine di eventi).

### Orari delle lezioni e variazioni calendariali

- Orario ordinario:
    - Lunedì: inizio alle ore 8:30 (2 ore di lezione con un intervallo).
    - Mercoledì: inizio alle ore 13:30 (3 ore di lezione con due intervalli).
    - Scansione oraria: moduli di lezione da 45 minuti alternati a pause di 15 minuti.
    - Esercitazioni: venerdì dalle ore 15:15 (o 15:30), per un monte ore totale di 40 ore gestite dal Prof. Angelici.
- Variazioni del calendario iniziale:
    - Venerdì della prima settimana: lezione teorica tenuta dal docente al posto dell'esercitazione.
    - Venerdì 18: lezione di 3 ore svolta da remoto sulla piattaforma **Webex** (causa occupazione dell'aula presso il Trifoglio per il Festival dell'Ingegneria e indisponibilità di altre aule).
    - Giornate di svolgimento delle lauree: sospensione delle lezioni in presenza con eventuale recupero mediante lezioni da remoto via **Webex**.

---

## Introduzione al Corso di Analisi Matematica 1

### Oggetto e finalità del corso

- Argomenti cardine: **calcolo differenziale** e **calcolo integrale**.
- Impostazione concettuale: sviluppo della materia a partire dai concetti base, definendo formalmente gli insiemi numerici ed i **simboli logici**.
- Trattazione iniziale focalizzata sulla costruzione rigorosa dell'insieme dei **numeri reali** ($\mathbb{R}$), con le relative leggi algebriche e proprietà operative.

### Motivazione teorica della costruzione dei numeri reali

- Né la struttura né le proprietà dei numeri reali vengono assunte come intuitive ("God given"): in matematica ogni ente deve essere costruito a partire da **enti primari**.
- La costruzione rigorosa dei numeri reali fornisce la base per introdurre le nozioni analitiche fondamentali:
    - Concetto di vicinanza e lontananza tra punti.
    - Concetto di **convergenza** e di **limite di una successione**.
    - Concetto di **continuità**.
    - Concetto di **integrale**.

---

## Simboli Logici e Notazioni Insiemistiche

### Simboli logici di base

I simboli logici vengono introdotti come abbreviazioni per sintetizzare le proposizioni matematiche:

- $\forall$ : **per ogni**.
- $\exists$ : **esiste**.
- $\nexists$ : **non esiste** (simbolo di esistenza barrato).
- $\exists!$ : **esiste ed è unico** (simbolo di esistenza con punto esclamativo).
- $\implies$ : **implica** (implicazione logica: se vale la premessa $A$, allora vale la conseguenza $B$).
- $\nRightarrow$ : **non implica** (implicazione sbarrata).
- $\iff$ : **è equivalente** (doppia implicazione: l'affermazione a sinistra equivale a quella a destra).
- $\mid$ (oppure $/$) : **tale che**.

### Notazioni e relazioni sugli insiemi

- Denominazione: insiemi indicati con lettere maiuscole ($A, B, \dots$) ed elementi con lettere minuscole ($a, b, \dots$).
- $\in$ : **appartiene** ($a \in A$ indica che l'elemento $a$ è contenuto nell'insieme $A$; notazione con orientazione opposta: $A \ni a$).
- $=$ : **coincidono** ($A = B$ indica che i due insiemi contengono esattamente gli stessi elementi. Dimostrare che due insiemi definiti con procedure diverse coincidono richiede una verifica formale).
- $:=$ (o due puntini antecedenti al simbolo/uguale): **introduzione di un nuovo simbolo** per definire un insieme i cui elementi sono specificati tra parentesi graffe ${\dots}$. Non costituisce un'uguaglianza da dimostrare, ma una convenzione notazionale.
- $\neq$ : **diverso da** ($A \neq B$ indica che almeno uno dei due insiemi possiede un elemento non contenuto nell'altro).
- $\subset$ / $\subseteq$ : **sottoinsieme** o **contenuto in** ($A \subseteq B$ indica che ogni elemento di $A$ appartiene a $B$; la barra orizzontale indica che $A$ e $B$ possono eventualmente coincidere).
- $\supset$ / $\supseteq$ : **contiene** ($B \supseteq A$).

---

## Operazioni Fondamentali Insiemistiche

### Unione e Intersezione

- **Unione insiemistica** ($A \cup B$):
    - Definita come l'insieme degli elementi che appartengono ad $A$ oppure a $B$ (almeno ad uno dei due insiemi): $$
x \in A \cup B \iff x \in A \lor x \in B
$$
- **Intersezione insiemistica** ($A \cap B$):
    - Definita come l'insieme degli elementi appartenenti contemporaneamente sia ad $A$ sia a $B$: $$
x \in A \cap B \iff x \in A \land x \in B
$$
- Funzione metodologica: oltre ad essere operazioni binarie, servono in senso inverso per **decomporre** insiemi complessi in sottoinsiemi più semplici presi in cascata.
- Proprietà: commutative ($A \cup B = B \cup A$, $A \cap B = B \cap A$) e distributive.

### Insieme Vuoto

- **Insieme vuoto** ($\emptyset$): insieme privo di elementi.
- Proprietà algebriche: $$
A \cup \emptyset = A, \quad A \cap \emptyset = \emptyset
$$
- Analogia storica: concettualmente analogo all'introduzione dello **zero** nell'algebra (Alto Medioevo), necessario per definire il risultato di operazioni quali $3 - 3 = 0$. L'insieme vuoto garantisce rigore formale quando si sottraggono tutti gli elementi da un insieme.

### Prodotto Cartesiano, Complementare e Differenza

- **Prodotto cartesiano** ($A \times B$):
    - Insieme costituito dalle coppie ordinate il cui primo elemento appartiene ad $A$ ed il secondo appartiene a $B$: $$
A \times B := { (a, b) \mid a \in A \land b \in B }
$$
- **Insieme complementare** ($A^c$):
    - Dato un sottoinsieme $A \subseteq B$, il complementare di $A$ in $B$ è definito come: $$
A^c := { x \in B \mid x \notin A }
$$
- **Differenza tra insiemi** ($A \setminus B$ oppure $A - B$):
    - Insieme formato dagli elementi di $A$ che non appartengono a $B$: $$
A \setminus B := { x \in A \mid x \notin B }
$$
    - Esempio: l'insieme dei numeri naturali privo dello zero è indicato con $\mathbb{N}^* = \mathbb{N} \setminus {0}$.

---

## Insiemi Numerici ed Estensioni Algebrico-Analitiche

### Definizioni degli insiemi numerici

- **Numeri naturali** ($\mathbb{N}$): $$
\mathbb{N} = {0, 1, 2, 3, \dots}
$$
    - L'insieme privo dello zero si indica con $\mathbb{N}^* = \mathbb{N} \setminus {0} = {1, 2, 3, \dots}$.
- **Numeri interi** ($\mathbb{Z}$): $$
\mathbb{Z} = {0, \pm 1, \pm 2, \dots}
$$
- **Numeri razionali** ($\mathbb{Q}$): $$
\mathbb{Q} = \left{ \frac{m}{n} ;\middle|; m, n \in \mathbb{Z}, , n \neq 0 \right}
$$
- Catena di inclusione tra insiemi numerici: $$
\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R} \subset \mathbb{C}
$$

### Necessità ed evoluzione delle estensioni numeriche

1. **Da $\mathbb{N}$ a $\mathbb{Z}$**:
    - L'equazione $x + 2 = 3$ ammette l'unica soluzione $x = 1 \in \mathbb{N}$.
    - L'equazione $x + 3 = 2$ non possiede soluzioni in $\mathbb{N}$ (poiché sommando a 3 un numero naturale si ottiene un valore $\ge 3$). Per garantire la risolvibilità si estende l'insieme a $\mathbb{Z}$, ottenendo l'unica soluzione $x = -1 \in \mathbb{Z}$.
2. **Da $\mathbb{Z}$ a $\mathbb{Q}$**:
    - L'equazione $3x = -6$ possiede l'unica soluzione $x = -2 \in \mathbb{Z}$.
    - L'equazione $3x = 5$ non ha soluzioni negli interi $\mathbb{Z}$. Estendendo l'insieme ai numeri razionali $\mathbb{Q}$, l'equazione ammette l'unica soluzione $x = \frac{5}{3} \in \mathbb{Q}$.
3. **Da $\mathbb{Q}$ a $\mathbb{R}$**:
    - Problema geometrico della misura della diagonale di un quadrato di lato $1$. Per il teorema di Pitagora, la lunghezza della diagonale $x$ soddisfa $x^2 = 1^2 + 1^2 = 2$.
    - L'equazione $x^2 = 2$ è ben posta nell'insieme dei numeri razionali, ma non possiede alcuna soluzione in $\mathbb{Q}$. Per risolvere l'equazione occorre estendere $\mathbb{Q}$ ai **numeri reali** ($\mathbb{R}$), nei quali ammette due soluzioni ($\pm\sqrt{2}$).
    - Tale passaggio ha natura analitica e si basa sulla proprietà di **completezza**.
4. **Da $\mathbb{R}$ a $\mathbb{C}$**:
    - Ulteriore estensione ai **numeri complessi** ($\mathbb{C}$), rappresentabili graficamente mediante tutti i punti del piano cartesiano.

### Rappresentazione grafica dei prodotti cartesiani e sottoinsiemi

- Il prodotto cartesiano $\mathbb{Z} \times \mathbb{Z}$ è rappresentato dai punti appartenenti ai vertici della quadrettatura del piano.
- **Numeri primi**: sottoinsieme di $\mathbb{N}$ formato dai numeri maggiori di 1 divisibili solo per 1 e per se stessi $es. 3, 5, 7, 11...$. Rappresentano i mattoni fondamentali dell'aritmetica. Due numeri $m, n$ si dicono **primi tra loro** (o relativamente primi) se non hanno fattori primi in comune, permettendo la riduzione della frazione $\frac{m}{n}$ ai minimi termini.

---

## Dimostrazione dell'Inesistenza di Soluzioni di $x^2 = 2$ in $\mathbb{Q}$

### Enunciato del Teorema

L'equazione algebrica $x^2 = 2$ non ammette alcuna soluzione nell'insieme dei numeri razionali $\mathbb{Q}$ (l'insieme delle soluzioni in $\mathbb{Q}$ è l'**insieme vuoto** $\emptyset$).

### Dimostrazione per Assurdo

1. Si supponga per **assurdo** che esista un numero razionale $x \in \mathbb{Q}$ tale che $x^2 = 2$.
2. Per definizione di numero razionale, $x$ è esprimibile come frazione: $$
x = \frac{m}{n}, \quad m, n \in \mathbb{Z}, , n \neq 0
$$
3. Si assuma, senza perdita di generalità, che $m$ ed $n$ siano **primi tra loro** (frazione ridotta ai minimi termini, priva di fattori comuni).
4. Sostituendo $x = \frac{m}{n}$ nell'equazione $x^2 = 2$: $$
\left(\frac{m}{n}\right)^2 = 2 \implies \frac{m^2}{n^2} = 2 \implies m^2 = 2n^2
$$
5. Dall'uguaglianza $m^2 = 2n^2$ segue che $m^2$ è un numero **pari**.
6. Poiché il quadrato di un numero dispari è dispari, se $m^2$ è pari ne consegue che anche $m$ dev'essere **pari**.
7. Essendo $m$ pari, esiste un intero $k \in \mathbb{Z}$ tale che $m = 2k$.
8. Sostituendo $m = 2k$ nell'espressione $2n^2 = m^2$: $$
2n^2 = (2k)^2 = 4k^2 \implies n^2 = 2k^2
$$
9. Dall'uguaglianza $n^2 = 2k^2$ segue che $n^2$ è un numero **pari**, e di conseguenza anche $n$ dev'essere **pari**.
10. Risultando sia $m$ sia $n$ numeri pari, essi condividono il fattore comune $2$.
11. Ciò contraddice l'ipotesi iniziale secondo cui $m$ ed $n$ fossero **primi tra loro** (**assurdo**).
12. **Conclusione**: Non esiste alcun numero razionale $x \in \mathbb{Q}$ tale che $x^2 = 2$.