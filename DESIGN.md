---
name: Fabio Fiorucci — GitHub Profile README
description: Il profilo GitHub personale come landing page professionale
colors:
  navy-deep: "#0F172A"
  blue-royal: "#1E3A8A"
  blue-accent: "#2563EB"
  blue-mid: "#3B82F6"
  blue-light: "#60A5FA"
  blue-pale: "#93C5FD"
  ink-white: "#FFFFFF"
typography:
  display:
    fontFamily: "Segoe UI, Arial, sans-serif"
    fontSize: "52px"
    fontWeight: 700
    lineHeight: 1
    letterSpacing: "normal"
  label:
    fontFamily: "Segoe UI, Arial, sans-serif"
    fontSize: "22px"
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: "normal"
rounded:
  badge: "999px"
  banner: "0px"
spacing:
  sm: "8px"
  md: "16px"
  lg: "24px"
components:
  badge-brand:
    backgroundColor: "{colors.navy-deep}"
    textColor: "{colors.ink-white}"
    rounded: "{rounded.badge}"
    padding: "6px 16px"
  badge-stat:
    backgroundColor: "{colors.blue-royal}"
    textColor: "{colors.ink-white}"
    rounded: "{rounded.badge}"
    padding: "6px 16px"
  banner-header:
    backgroundColor: "{colors.navy-deep}"
    textColor: "{colors.ink-white}"
    rounded: "{rounded.banner}"
    padding: "0px"
---

# Design System: Fabio Fiorucci — GitHub Profile README

## 1. Overview

**Creative North Star: "Il Turno di Notte"**

Il sistema visivo del README è un cielo notturno che schiarisce verso l'alba: si parte dal navy quasi-nero (#0F172A) dell'header e si sale, passo dopo passo, verso l'azzurro chiaro (#93C5FD) dei dettagli e degli accenti. Non è decorazione: è la stessa progressione del percorso professionale raccontato nella timeline — un ingegnere che lavora quotidianamente su sistemi enterprise solidi (il navy, il fondamento) e che al tempo stesso sta esplorando territori nuovi come l'AI-assisted development (l'azzurro che schiarisce, la direzione verso cui si muove).

Il sistema rifiuta esplicitamente l'estetica "da tutorial GitHub": badge ammassati senza gerarchia, emoji usate come riempitivo invece che come indice visivo, sezioni scaffolding numerate identiche (`01 · / 02 · / 03 ·`) ripetute meccanicamente. Ogni elemento — badge, tabella, riga di icone — ha un ruolo informativo preciso all'interno di un'unica famiglia cromatica blu/navy, mai un colore aggiunto per riempire spazio.

**Key Characteristics:**
- Un'unica famiglia cromatica (navy → blu → azzurro chiaro), nessun colore fuori palette
- Struttura ordinata: sezioni con gerarchia chiara, non un accumulo di badge
- Voce tecnica ma calda: solidità enterprise + curiosità verso l'AI, mai hype vuoto
- Densità informativa alta ma leggibile: ogni riga conta

## 2. Colors

Palette monocromatica blu/navy a scala di luminosità, letta come una progressione dal fondamento (scuro, stabile) alla direzione di crescita (chiaro, aperto).

### Primary
- **Notte Profonda** (`#0F172A`): sfondo dell'header banner, badge del portfolio. È il colore "casa": enterprise, stabile, il fondamento su cui tutto il resto si costruisce.
- **Blu Reale** (`#1E3A8A`): estremità chiara del gradiente del banner, badge follower. Il passo intermedio tra il fondamento e l'accento.

### Secondary
- **Blu Accento** (`#2563EB`): badge stelle GitHub e riga "Mobile" del Tech Stack. Usato con parsimonia per marcare un secondo raggruppamento distinto da quello primario.

### Neutral
- **Blu Medio** (`#3B82F6`): badge "last commit", puntini decorativi del banner. Colore di supporto, non protagonista.
- **Blu Chiaro** (`#60A5FA`) e **Azzurro Pallido** (`#93C5FD`): sottotitolo del banner, puntini decorativi finali. Segnano il punto più "aperto" della scala — dove il navy si è schiarito del tutto.
- **Bianco** (`#FFFFFF`): testo su sfondo scuro (nome nel banner, testo dei badge navy/blu).

### Named Rules
**La Regola del Cielo Unico.** Ogni colore del sistema appartiene alla stessa scala navy→azzurro. Nessun colore estraneo (verde, arancio, rosso) entra nella palette propria, a eccezione dei colori di marchio fissi imposti da terze parti (vedi sotto).
**La Regola dei Colori di Marchio Esterni.** I badge LinkedIn (`#0A66C2`), GitHub (`#181717`) e Gmail (`#D14836`) sono fissati dalla convenzione shields.io/brand del servizio collegato, non fanno parte della palette propria e non vanno mai estesi ad altri elementi del README.

## 3. Typography

**Display Font:** Segoe UI (fallback: Arial, sans-serif) — usato solo nel banner SVG
**Corpo del testo:** governato dal renderer Markdown di GitHub (stack di sistema, non controllabile a livello di font-family)

**Character:** Un unico punto di peso tipografico deliberato — il nome nel banner (sans-serif bold, 52px) — che ancora l'identità senza competere con il resto della pagina, rimasta nel font di sistema di GitHub.

### Hierarchy
- **Display** (700, 52px, line-height 1): nome "Fabio Fiorucci" nel banner. Unico punto dove compare un peso da titolo.
- **Label** (400, 22px, line-height 1.2): sottotitolo ruolo nel banner ("Frontend Developer • Vue & TypeScript Specialist").
- **Body** (default GitHub markdown): tutto il testo delle sezioni. Paragrafi brevi, mai oltre 2-3 righe consecutive senza un elenco o un'intestazione a spezzare il ritmo.
- **Heading** (default GitHub `##`/`###`): un'emoji + titolo breve per sezione, mai più di 3-4 parole.

### Named Rules
**La Regola della Famiglia Unica.** Il sistema usa esattamente una famiglia tipografica propria (Segoe UI), confinata al banner SVG. Il corpo del README resta nel font di sistema di GitHub: non si introduce una seconda famiglia via immagini o SVG aggiuntivi (rimosso, ad esempio, l'effetto "typing" in Fira Code: ripeteva informazioni già presenti altrove senza aggiungere gerarchia).

## 4. Elevation

Il sistema è completamente flat: markdown renderizzato da GitHub non supporta ombre reali, e il banner SVG stesso non usa `box-shadow` o `filter: drop-shadow`. La profondità, dove esiste, è simulata nel banner tramite due `path` semi-trasparenti (opacità 0.06 e 0.1) che suggeriscono onde/strati sullo sfondo navy — un effetto di texture, non di elevazione.

### Named Rules
**La Regola della Piattezza Voluta.** Nessun elemento del README deve simulare elevazione con ombre, bordi sfumati o gradienti decorativi fuori dal banner. La profondità, quando serve, si ottiene solo con variazione di opacità sullo stesso colore (come nel banner), non con nuovi livelli di grigio o shadow CSS (che GitHub markdown ignorerebbe comunque).

## 5. Components

### Banner Header
- **Forma:** rettangolo pieno 1200×260, nessun arrotondamento (`0px`)
- **Sfondo:** gradiente lineare diagonale da Notte Profonda (`#0F172A`) a Blu Reale (`#1E3A8A`)
- **Contenuto:** nome in Display bianco, sottotitolo in Label azzurro pallido, tre puntini decorativi (blu medio→chiaro→pallido) in alto a destra come firma visiva discreta

### Badge / Pill (shields.io)
- **Forma:** pillola (`border-radius: 999px` visivamente, gestito da shields.io con `style=for-the-badge` o `flat-square`)
- **Contenuto:** icona del servizio + etichetta, sempre in maiuscolo per lo stile `for-the-badge`
- **Colore:** badge di marchio esterno mantengono il colore ufficiale del servizio, ed è un'eccezione nominata solo per LinkedIn, GitHub e Gmail (vedi "La Regola dei Colori di Marchio Esterni"); ogni altro badge — statistiche, Tech Stack, Integrazioni & Servizi — usa esclusivamente la scala navy→blu propria, incluse le icone dei singoli linguaggi/tool (`logoColor=white` su sfondo della scala, mai il colore ufficiale del logo)
- **Stato:** statico (nessun hover in markdown); il colore stesso comunica la categoria (identità vs. metriche vs. stack tecnico)

### Tabelle informative
- **Stile:** tabella markdown nativa, senza bordi colorati o sfondo custom
- **Uso:** "Progetti in evidenza" (2 colonne: nome progetto con emoji + descrizione) — è l'unica tabella della pagina; non se ne aggiungono altre che ripetano le stesse informazioni in una forma diversa
- **Regola:** ogni cella inizia con un'emoji-indice seguita da testo breve; mai più di 3 righe per cella

### Timeline (Mermaid)
- **Stile:** diagramma `timeline` nativo Mermaid, tema di default GitHub (non personalizzato con colori custom)
- **Uso:** percorso professionale in ordine cronologico, un evento per anno
- **Regola:** un solo evento per riga, testo conciso (ruolo + azienda, opzionalmente contesto tra em-dash)

### Riga di contatti (footer)
- **Stile:** link testuali inline separati da `•`, ciascuno con un'emoji-icona (🌐 💼 💻 📧)
- **Uso:** ripetizione compatta dei link già presenti nei badge in alto, per chi arriva in fondo alla pagina senza dover risalire

## 6. Do's and Don'ts

### Do:
- **Do** mantenere ogni colore all'interno della scala navy→blu→azzurro pallido (`#0F172A` → `#1E3A8A` → `#2563EB` → `#3B82F6` → `#60A5FA` → `#93C5FD`).
- **Do** usare i colori di marchio ufficiali (LinkedIn `#0A66C2`, GitHub `#181717`, Gmail `#D14836`) solo sui badge che rappresentano quel servizio specifico, mai altrove.
- **Do** far iniziare ogni riga di tabella o elenco con un'unica emoji-indice coerente per sezione.
- **Do** tenere i paragrafi di corpo a 2-3 righe massimo prima di una rottura visiva (elenco, tabella, heading).

### Don't:
- **Don't** aggiungere colori fuori dalla scala navy/blu (niente verde, arancio, viola, rosso) per badge o testo propri — incluse le icone dei singoli linguaggi/tool nel Tech Stack, che vanno sempre ricolorate in scala e non lasciate nel colore ufficiale del logo.
- **Don't** usare eyebrow numerati (`01 ·`, `02 ·`, `03 ·`) come scaffolding ripetuto sopra ogni sezione — non è mai stato usato in questo README e non va introdotto come pattern di default.
- **Don't** ammassare badge senza raggruppamento logico: ogni riga di badge deve rappresentare una sola categoria (identità/contatti, metriche, oppure stack tecnico, non un mix).
- **Don't** introdurre ombre, gradienti decorativi o glassmorphism fuori dal banner: il sistema è flat by design.
- **Don't** aggiungere una seconda famiglia tipografica: il corpo resta nel font di sistema GitHub, Segoe UI resta confinato al banner SVG.
- **Don't** ripetere le stesse 3-4 informazioni (stack, focus, progetti) in più contenitori diversi (tabelle, badge, testo animato): ogni sezione deve dire qualcosa che nessun'altra sezione dice già.
