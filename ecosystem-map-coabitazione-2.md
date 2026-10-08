# Documentazione di Progetto: Delivery GDO per Nuove Forme dell'Abitare
**Progetto:** Ottimizzazione dei servizi di e-grocery (Esselunga / Penny Market) per nuclei di coabitazione non familiare.
**Metodologia:** Strategic UX Research & Service Design.

---

# PART 1: Ecosystem Map & Validazione dei Dati

##  Verifica della Tesi alla luce delle evidenze incrociate

**Tesi Iniziale:** 
*La casa non è più progettata soltanto per una famiglia, ma per una pluralità di persone e relazioni temporanee. Le app di spesa online della GDO (es. Esselunga, Penny) ignorano questo segmento collettivo, trattandolo erroneamente tramite account singoli.*

###  Il Fact-Checking Metodologico: Cosa è vero e cosa no?

1. **L'invisibilità anagrafica vs La realtà dei fatti:** L'intuizione di partenza è **parzialmente smentita** dal solo dato demografico Istat sulle famiglie, dove le coabitazioni non parentali faticano a emergere in modo pulito nella voce "Altra tipologia", ferma al 3,6%.
2. **La prova regina (I dati OMI):** La tesi viene **pienamente confermata** quando si incrocia la demografia con la contabilità dei contratti reali dell'Agenzia delle Entrate (OMI). La serie storica sul numero di contratti per **"Immobili in porzione"** (affitto di singole stanze) mostra un balzo netto da 265.277 a **349.028 contratti registrati**, certificando che circa il 35% delle locazioni urbane attive nei capoluoghi è ormai a stanze.
3. **Il Verdetto per il Design:** Il fenomeno non è una nicchia transitoria di studenti, ma un'infrastruttura macroeconomica consolidata. Oltre 1,5 milioni di individui in Italia coabitano legalmente condividendo la logistica dello stesso frigorifero, ma rimangono "nascosti" all'anagrafe come nuclei unipersonali separati. C'è un gap evidente tra il modello operativo della GDO e l'infrastruttura abitativa reale.

---

##  Ecosystem Map Strutturata

```mermaid
flowchart TD
    %% Definizione dei Nodi Macro e Connessioni Principali
    subgraph Macro_Context ["Scenario e Driver di Mercato"]
        A1["Macrotrend Istat<br/>Singoli al 36.2%<br/>Diminuzione coppie"] 
        A2["Mercato Immobiliare OMI<br/>349.028 Immobili in porzione<br/>34.9% Affitti a stanze nei capoluoghi"]
    end

    subgraph Core_Target ["Il Nucleo Collettivo Coinvolto"]
        B["COABITAZIONE NON FAMILIARE<br/>(Co-living / Inquilini non parenti)"]
    end

    subgraph Stakeholders ["Attori ed Ecosistema Esterno"]
        H["Proprietari Privati"]
        I["Società di Gestione Property"]
        J["Piattaforme di Delivery GDO<br/>(Esselunga / Penny)"]
    end

    subgraph Pain_Points ["Frizioni Interne ed Economiche (As-Is)"]
        O["Privacy e Confini Spaziali"]
        P["Gestione Turni e Pulizie"]
        Q["Economia Domestica<br/>(Split spese e Anticipi soldi)"]
        R["Transitorietà Contrattuale"]
    end

    subgraph Opportunities ["Opportunità del Servizio Digitale (To-Be)"]
        U1["Carrello Multi-utente Condiviso"]
        U2["Split-Payment Nativo al Checkout"]
        U3["Abbonamenti Ricorrenti di Casa"]
    end

    %% Flussi di relazione e impatto
    A1 & A2 --> B
    B <--> H & I
    J -.-> |Ignora l'unità collettiva| B
    B --> O & P & Q & R
    Q & O --> U1
    Q --> U2
    R & P --> U3

    %% Classi di Stile Ottimizzate per Leggibilità
    classDef trend fill:#EAF2F8,stroke:#2980B9,stroke-width:2px,color:#1B4F72;
    classDef central fill:#FCF3CF,stroke:#F39C12,stroke-width:3px,color:#7E5109;
    classDef actors fill:#EBDEF0,stroke:#8E44AD,stroke-width:2px,color:#4A235A;
    classDef problems fill:#FDEDEC,stroke:#C0392B,stroke-width:2px,color:#641E16;
    classDef opps fill:#E8F8F5,stroke:#16A085,stroke-width:2px,color:#0E6251;

    class A1,A2 trend;
    class B central;
    class H,I,J actors;
    class O,P,Q,R problems;
    class U1,U2,U3 opps;
```

---

##  Tassonomia delle Forme di Coabitazione

```mermaid
graph TD
    A["MODELLI DI ABITAZIONE CELLULARE"] --> B["Coabitazione Familiare<br/>(Rilevata accuratamente da Istat)"]
    A --> C["Coabitazione Non Familiare<br/>(La zona d'ombra quantitativa)"]

    B --> B1["Coppie con figli (29,2%)"]
    B --> B2["Coppie senza figli (20,2%)"]
    B --> B3["Monogenitori (10,8%)"]

    C --> C1["Studentato Spontaneo<br/>(Focus: Penny Market / Budget)"]
    C --> C2["Young Professionals / Fuori Sede<br/>(Focus: Esselunga / Time-saving)"]
    C --> C3["Modelli Istituzionali / Co-housing"]

    classDef fam fill:#EAFAF1,stroke:#27AE60,color:#145A32;
    classDef nonFam fill:#FEF9E7,stroke:#D35400,color:#6E2C00;
    class B,B1,B2,B3 fam;
    class C,C1,C2,C3 nonFam;
```

---

##  Il Modello delle Frizioni e Mappatura delle Soluzioni

```mermaid
flowchart LR
    %% Area Problemi
    subgraph Frizioni_Utente ["Pain Points Rilevati"]
        P1["Mancanza di spazio comune nel frigo"]
        P2["Anticipo economico del singolo per tutti"]
        P3["Rincorsa dei micro-debiti (Splitwise/Contanti)"]
        P4["Frammentazione degli ordini singoli (Più consegne)"]
    end

    %% Area Soluzioni
    subgraph Soluzioni_GDO ["Opportunità nell'App Delivery"]
        S1["Tag o Sub-Carrelli personali per singolo ripiano"]
        S2["Divisione automatica del conto alla cassa"]
        S3["Integrazione sistemi P2P (Satispay/Bancomat Pay)"]
        S4["Unificazione Logistica con sconti sul volume della Casa"]
    end

    %% Collegamenti diretti causali
    P1 --> S1
    P2 --> S2
    P3 --> S3
    P4 --> S4

    classDef prob fill:#FDF2E9,stroke:#E67E22,color:#7E5109;
    classDef sol fill:#EBF5FB,stroke:#3498DB,color:#1B4F72;
    class P1,P2,P3,P4 prob;
    class S1,S2,S3,S4 sol;
```

---

# PART 2:  UX Research Plan

## 1. Background & Context
Le attuali piattaforme di e-grocery e delivery dei grandi player della GDO (es. Esselunga, Penny Market) sono storicamente progettate su modelli familiari tradizionali o sul profilo del consumatore singolo. 

I dati demografici correnti evidenziano tuttavia una trasformazione strutturale della società: il crollo dei nuclei familiari con figli e la crescita esponenziale di famiglie unipersonali. Parallelamente, i dati OMI dell'Agenzia delle Entrate certificano l'esplosione dei contratti per "immobili in porzione" (stanze singole), passati a quota 349.028 unità attive.

Esiste un segmento di mercato emergente — composto da coinquilini non parenti — le cui dinamiche di economia domestica, logistica e condivisione delle spese alimentari non sono attualmente intercettate dall'offerta digitale della GDO.

## 2. Business Objectives & Design Opportunity
* **Dimostrare l'esistenza e il valore** di un cluster di utenti "collettivo" (il nucleo di coabitazione) attualmente ignorato dai sistemi di carrello e pagamento unici.
* **Identificare nuove feature di servizio** (es. carrelli condivisi, split-payment nativo, gestione delle macro-scorte comuni) in grado di posizionare il brand come abilitatore di nuove forme di convivenza, aumentando la fidelizzazione e lo scontrino medio della casa.

## 3. Research Goals (Obiettivi di Ricerca)
* **Goal 1:** Comprendere i modelli mentali e le dinamiche di collaborazione/frizione tra coinquilini nella gestione della spesa e della dispensa.
* **Goal 2:** Mappare l'attuale ecosistema di strumenti "accrocchiati" dagli utenti (es. WhatsApp + Splitwise + Excel) per compensare i limiti delle attuali app di delivery.
* **Goal 3:** Isolare i comportamenti d'acquisto comunitari (beni condivisi) da quelli individuali (spesa personale) all'interno dello stesso nucleo abitativo.
* **Goal 4:** Indagare la percezione e il posizionamento dei brand GDO (Premium vs Discount) all'interno delle economie di coabitazione.

## 4. Key Research Questions (Domande di Ricerca)
* *In che modo i coinquilini negoziano la lista della spesa comune e bilanciano le preferenze alimentari individuali?*
* *Quali sono i punti di attrito principali nella catena logistica della spesa in casa (dall'ordine, al momento del pagamento, fino allo stoccaggio in frigo)?*
* *Come viene vissuto l'impatto economico della spesa e come vengono gestiti i micro-debiti interni?*

## 5. Methodology & Research Tools
Per rispondere agli obiettivi utilizzeremo un approccio qualitativo ed esplorativo, ideale per mappare comportamenti complessi:

* **Interviste Qualitative Semi-strutturate (In-depth Interviews):** Interviste di 60 minuti condotte a coppie di coinquilini appartenenti allo stesso nucleo. Il focus sarà il racconto di episodi reali e la ricostruzione dell'ultima spesa effettuata.
* **Osservazione Contestuale / Contextual Inquiry (Disamina della Dispensa):** Durante le interviste, chiederemo ai partecipanti di mostrarci (anche via webcam o foto) l'organizzazione fisica del frigorifero e della dispensa, per validare sul campo le regole invisibili di gestione degli spazi condivisi.

## 6. Target & Sampling Plan (Criteri di Reclutamento)
Il campione complessivo sarà di **12-15 partecipanti** (suddivisi in circa 6-7 nuclei abitativi), profilati secondo i seguenti cluster estratti dall'Ecosystem Map:

* **Cluster 1: Lo "Studentato" spontaneo (3-4 coinquilini, focus budget):** Alta transitorietà, spesa frammentata, uso intensivo di digital tools per lo split dei costi. Target affine a Penny Market.
* **Cluster 2: Young Professionals in Co-housing (2-3 lavoratori fuori sede, focus time-saving):** Maggiore potere d'acquisto, alta penetrazione dei servizi di delivery, l'app serve a ottimizzare i tempi. Target affine a Esselunga.
* **Cluster 3: Il Lead Buyer (Profilo trasversale):** L'inquilino che storicamente si fa carico dell'ordine logistico per tutti e che sperimenta la massima frizione nel "rincorrere" gli altri per i rimborsi.

## 7. Expected Outputs (I Deliverable della Ricerca)
I dati qualitativi raccolti verranno sintetizzati e modellati nei seguenti artifact di design:
