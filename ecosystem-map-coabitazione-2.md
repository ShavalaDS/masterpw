# Ecosystem map — Coabitazione e nuove forme dell’abitare

## Tesi

> La casa non è più progettata soltanto per una famiglia, ma per una pluralità di persone e relazioni temporanee.

I dati Istat mostrano famiglie più piccole, più persone sole e una riduzione delle coppie con figli. La coabitazione tra persone non imparentate va letta dentro questo cambiamento, anche se le statistiche ufficiali non isolano sempre i coinquilini non parenti. [web:18][web:19]

## Evidenze quantitative

| Indicatore | 2002-2003 | 2023-2024 | Evoluzione |
|---|---:|---:|---|
| Famiglie unipersonali | 25,5% | 36,2% | Forte aumento |
| Coppie con figli | 42,2% | 29,2% | Forte diminuzione |
| Coppie senza figli | 20,9% | 20,2% | Quasi stabile |
| Famiglie monogenitore | 8,2% | 10,8% | Aumento |
| Altra tipologia* | 3,2% | 3,6% | Lieve aumento |

\* “Altra tipologia” comprende famiglie senza nucleo diverse dalle persone sole e famiglie formate da due o più nuclei; non coincide esclusivamente con i coinquilini non parenti. [web:19]

La dimensione media della famiglia è scesa da circa 2,6 a circa 2,2 persone. [web:18][web:19]

## Ecosystem map

```mermaid
flowchart LR
    A["MACROTREND<br/>Famiglie più piccole<br/>Invecchiamento<br/>Affitti elevati<br/>Mobilità"]
    B["PERSONE NON IMPARENTATE<br/>SOTTO LO STESSO TETTO"]
    C["Studenti"]
    D["Lavoratori fuori sede"]
    E["Amici e coinquilini"]
    F["Anziani"]
    G["Migranti"]
    H["Proprietari"]
    I["Agenzie immobiliari"]
    J["Piattaforme digitali"]
    K["Università e aziende"]
    L["Comune e servizi sociali"]
    M["Famiglia d'origine"]
    N["Quartiere e vicinato"]
    O["Privacy e confini"]
    P["Pulizie e responsabilità"]
    Q["Spese e utenze"]
    R["Contratti e garanzie"]
    S["Rumore e conflitti"]
    T["Transitorietà e instabilità"]
    U["OPPORTUNITÀ DI DESIGN<br/>Spazi flessibili<br/>Regole condivise<br/>Gestione spese<br/>Mediazione"]
    A --> B
    B --> C & D & E & F & G
    H --> B
    I --> B
    J --> B
    K --> B
    L --> B
    M --> B
    N --> B
    B --> O & P & Q & R & S & T
    O & P & Q & R & S & T --> U
    classDef trend fill:#E8F1F8,stroke:#39739D,stroke-width:2px,color:#17324D
    classDef central fill:#F4B942,stroke:#9A6B00,stroke-width:3px,color:#241A00
    classDef people fill:#E8F5E9,stroke:#4F8A53,color:#173B1B
    classDef actors fill:#F3E8FF,stroke:#7C4D99,color:#30163E
    classDef problems fill:#FFE8E6,stroke:#B64B42,color:#4A1713
    classDef opportunities fill:#E4F7F5,stroke:#198F88,color:#123E3B
    class A trend
    class B central
    class C,D,E,F,G people
    class H,I,J,K,L,M,N actors
    class O,P,Q,R,S,T problems
    class U opportunities
```

## Forme di coabitazione

```mermaid
flowchart TB
    A["COABITAZIONE"]
    A --> B["Familiare"]
    A --> C["Non familiare"]
    B --> B1["Coppia con figli"]
    B --> B2["Coppia senza figli"]
    B --> B3["Monogenitore"]
    B --> B4["Fratelli o parenti"]
    C --> C1["Studenti"]
    C --> C2["Lavoratori fuori sede"]
    C --> C3["Amici"]
    C --> C4["Coinquilini"]
    C --> C5["Coabitazione temporanea"]
```

## Attori e relazioni

```mermaid
flowchart LR
    A["ABITANTE"]
    B["Coinquilini"]
    C["Proprietario"]
    D["Piattaforma digitale"]
    E["Università / azienda"]
    F["Comune"]
    G["Quartiere"]
    H["Famiglia d'origine"]
    I["Servizi sociali"]
    A <--> B
    A --> C
    D --> A
    E --> A
    F --> A
    G <--> A
    H --> A
    I --> A
```

## Problemi e opportunità

```mermaid
flowchart LR
    A["COABITAZIONE"]
    B["Privacy"]
    C["Pulizie"]
    D["Spese"]
    E["Contratti"]
    F["Conflitti"]
    G["Instabilità"]
    H["Spazi flessibili"]
    I["Regole condivise"]
    J["Gestione digitale"]
    K["Contratti modulari"]
    L["Mediazione"]
    M["Servizi di matching"]
    A --> B & C & D & E & F & G
    B --> H
    C --> I
    D --> J
    E --> K
    F --> L
    G --> M
```

## Nota metodologica

I dati Istat descrivono la struttura delle famiglie, non tutti i casi di semplice condivisione dell’abitazione. “Altra tipologia” può comprendere due fratelli conviventi, ma non identifica separatamente tutti i coinquilini non parenti. Per documentare il fenomeno specifico servono anche interviste, osservazione e dati su studenti, lavoratori mobili, migranti e abitazioni condivise. [web:18][web:19]

## Riferimenti

- Istat, [Indicatori demografici — Anno 2024](https://www.istat.it/comunicato-stampa/indicatori-demografici-anno-2024/). [web:18]
- Istat, [Indicatori demografici — Anno 2024, PDF](https://www.istat.it/wp-content/uploads/2025/03/indicatori_demografici_2024.pdf). [web:19]
- Istat, [I nuclei familiari nei censimenti della popolazione](https://www.istat.it/comunicato-stampa/i-nuclei-familiari-nei-censimenti-della-popolazione/). [web:17]
- Istat, [Previsioni della popolazione e delle famiglie](https://www.istat.it/wp-content/uploads/2024/07/Previsioni-popolazione-famiglie_2023.pdf). [web:25]
- Visual Studio Code, [Markdown](https://code.visualstudio.com/docs/languages/markdown). Supporto ai blocchi Mermaid nella preview. [web:27]
- Mermaid, [Flowcharts](https://mermaid.ai/open-source/syntax/flowchart.html). Sintassi per diagrammi. [web:28]
