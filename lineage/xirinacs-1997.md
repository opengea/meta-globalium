---
title: Catàleg canònic de les 80 categories del Meta-Globàlium
source: Xirinacs LM (1997). Un model global de la realitat. Tesi doctoral UB.
url: https://www.bardina.org/globalium/lmx_tesi_1997_completa_1.pdf
date_extracted: 2026-05-02
license: CC BY-SA 4.0 (extracte amb fins de referència acadèmica)
references:
  - "Xirinacs 1997, Esquema XXXV (taula dels vuitanta termes), pàg. 142 (línies 4339-4421 del .txt extret)"
  - "Xirinacs 1997, §397 Índex analític de les vuitanta categories, pàg. 143 i ss. (línies 4424-5200)"
  - "Berenguer 2024, Globàlium petit manual, §8 Categories (línies 610-1019 del .txt extret)"
  - "Berenguer (s/d), Globàlium AI Trainer (línies 670-801 del .txt extret)"
---

# Catàleg canònic — 80 categories del Meta-Globàlium

Aquest document és la transcripció estructurada i comentada de les vuitanta categories del model global de la realitat tal com les fixa Lluís Maria Xirinacs Damians a la tesi doctoral *Un model global de la realitat* (UB, 1997). La taula nuclear és l'Esquema XXXV (símbol, dimensions i antiterme) i l'Índex analític (§397). S'hi afegeixen les definicions condensades posteriors del *Globàlium petit manual* (Berenguer 2024) i del *Globàlium AI Trainer* (en anglès) per a ús de l'agent Arkadium.

> **Estat**: **baseline canònic revisable**, no font definitiva. Les 80 categories de Xirinacs 1997 són una proposta històrica de cobertura de l'espectre de la realitat — qüestionables, ampliables i refinables. La seva funció és servir de **base d'on derivar els principis fonamentals** del Meta-Globàlium, no tancar el model. NO altera la base de dades; només documenta el punt de partida.

---

## 0. Glossari dimensional

Xirinacs estableix quatre dimensions ortogonals (Esquema XXXV i §11-§14, línies 4441 i ss.). Cadascuna té dos pols, codificats amb un signe a la quàdrupla `(k, p, t, v)`:

| Eix | Símbol | Pol negatiu (–) | Pol positiu (+) | Naturalesa |
|-----|--------|------------------|------------------|------------|
| D2 (Cernent) | **k** | PRA — Pràctica (concreció, fysis) | TEO — Teoria (abstracció, eídos) | cartesià |
| D3 (Parença) | **p** | NOU — Noümen (transcendència, en si) | FEN — Fenomen (aparença, esdevenir) | cartesià |
| D1 (Tensió) | **t** | SUB — Subjecte (intensió, vivència) | OBJ — Objecte (extensió, estructura) | cartesià |
| D4 (Voltant) | **v** | PLA — Plasma (involucionat, replegat) | MON — Món (evolucionat, desplegat) | radial |

**Convencions de Xirinacs** (línies 4441-4546):
- `k` = Cernent (pràctica/teoria)
- `p` = Parença (noümen/fenomen)
- `t` = Tensió (subjecte/objecte)
- `v` = Voltant (plasma/món)

**Numeració decimal** (sistema 4-base, §397.0): el primer dígit indica la *dialèctica* o ordre (1=primera, 2=segona, 3=tercera, 4=quarta), els següents el camí a la posició dimensional. La taula de la tesi usa `1xx`, `2xx`, `3xx`, `4xx` amb índex jeràrquic (subgrup k, p, t, v).

**Capes** del meta-Globàlium (mapping a la DB `kms_kb_categories`):
- **Generadors d'eix** (8 punts P1, ⟨k=p=t=v=0,159c⟩): generació 1 — codis 11x, 12x, 13x, 14x.
- **Dialèctica segona** (24 punts P2, ⟨0,113c⟩): combinacions binàries — codis 2xx.
- **Dialèctica tercera** (32 punts P3, ⟨0,092c⟩): combinacions ternàries — codis 3xx.
- **Dialèctica quarta** (16 punts P4, ⟨0,080c⟩): combinacions quaternàries — codis 4xx.

**Total**: 8 + 24 + 32 + 16 = **80 categories**.

> **Nota crítica**: la DB d'`opengea_kms` usa una taxonomia ortogonal a la dialèctica (Plasmàtica/Neutral/Mundana segons signe de `v`) que NO coincideix amb les "dialèctiques" de Xirinacs. La Plasmàtica DB conté entries amb `v=–` de qualsevol dialèctica; la Mundana, amb `v=+`; la Neutral, amb `v=0`. Vegi's la taula consolidada més avall.

---

## 1. Categories primàries (8 generadors d'eix — primera dialèctica)

| Codi | Label | Nom complet | Coords (k,p,t,v) | Antiterme | Nom EN | Pàg. tesi |
|------|-------|-------------|------------------|-----------|--------|-----------|
| 111 | **PRA** | PRÀCTICA | (–, 0, 0, 0) | TEORIA | PRACTICE | 46 |
| 112 | **TEO** | TEORIA | (+, 0, 0, 0) | PRÀCTICA | THEORY | 63 |
| 121 | **NOU** | NOÜMEN | (0, –, 0, 0) | FENOMEN | NOUMENON | 57 |
| 122 | **FEN** | FENOMEN | (0, +, 0, 0) | NOÜMEN | PHENOMENON | 51 |
| 131 | **SUB** | SUBJECTE | (0, 0, –, 0) | OBJECTE | SUBJECT | 50 |
| 132 | **OBJ** | OBJECTE | (0, 0, +, 0) | SUBJECTE | OBJECT | 54 |
| 141 | **PLA** | PLASMA | (0, 0, 0, –) | MÓN | PLASMA | 43 |
| 142 | **MON** | MÓN | (0, 0, 0, +) | PLASMA | WORLD | 43 |

### Definicions

**PRA — Pràctica** (§111, pàg. 144). *Concerniment: cernent replegat. Concreció, synolos. Naturalesa, fysis. Realitat-1: realitat en si, sat. Matèria, hylé. Força inercial. Inescrutabilitat de la referència (Quine). Autenticitat (Heidegger). Anarquia. Evidència. Intuïció (Kant). Espontaneïtat, primarietat. Praxi (Marx). Causa material concreta.* — Petit manual: «realitat concreta i dinàmica. Força. Autenticitat.»

**TEO — Teoria** (§112, pàg. 144). *Discerniment: cernent desplegat. Abstracció, afaíresis (Plató, Arist.). Ment. Realitat-2: ment en si, cit. Forma, morfé, eídos. Causa formal abstracta. Especulació. Filosofia. Globalitat. Integració. Estat (Plató…Hegel). Episteme. Cultura. Llenguatge.* — Petit manual: «realitat mentalitzada i abstracta. Enteniment.»

**NOU — Noümen** (§121, pàg. 144). *Desparença: parent replegat. Transcendència. Causa eficient transcendent. Déu. Brahman. Eternitat, "tota simul". Misteri de la vida. Unitat. Monisme. Nirvana. Contemplació, samadhi. Ànima del món. Causa sui. Categoria màxima. Etern retorn. Anihilació.* — Petit manual: «transcendència. Esperit universal. Eternitat. Unitat.»

**FEN — Fenomen** (§122, pàg. 144). *Aparença: parent desplegat. Esdeveniment. Fluència, samsara, panta rei. Multiplicitat. Acte. Moviment. Diacronia. Esdevenir. Temps físic, khrónos. Història. Maia. Manifestació. Causa formal aparent. Dualitat. Present puntual. Conflicte. Diàleg. Mercat. Relació, pròs tí. Intersubjectivitat. Erscheinung (Kant).* — Petit manual: «moment present; l'ara aquí. Realitat aparent.»

**SUB — Subjecte** (§131, pàg. 145). *Intensió: tens replegat. Vivència. Erlebnis. Vida, bíos. Agent. Jo. Atman. Hypokeímenon. Lloc dels qualia. Interior, intimitat. Solipsisme. Concentració, dharana. Emancipació. Autonomia. Causa final intencional. Liberum arbitrium. Angoixa (Kierkegaard, Heidegger, Sartre).* — Petit manual: «jo pur. Vivència despullada d'identitat. Voluntat.»

**OBJ — Objecte** (§132, pàg. 145). *Extensió: tens desplegat. Estructura, Gestalt. Causa material estructural. Cohesió. Xarxa. Trama. Text (Gadamer). Espai físic. On, ubi. Sincronia. Heteronomia. Alienació (Hegel, Marx). Institució. Cos. Cosa. Element, stoikheion. Lloc dels quanta. Exterior, publicitat.* — Petit manual: «estructura constant i coherent. Cos. Objectiu.»

**PLA — Plasma** (§141, pàg. 146). *Involucionat: voltant replegat. Radicalitat. Alfa i omega. Big-bang. Virtualitat. Implicatio (Nicolau de Cusa). Opacitat. Fonament. Lloc "ciclònic". Compressió. Forat blanc/negre. Etern retorn. Genuïnitat. Originalitat. Causa eficient física. Potència. Interior "ple" de les partícules reals.* — Petit manual: «Origen i fi (Alfa/Omega). Llavor radical de la realitat.»

**MON — Món** (§142, pàg. 146). *Evolucionat: voltant desplegat. Plenitud, pléroma, purxa. Actualitat al mig de la història general. Explicatio (Nicolau de Cusa). Transparència. Desenvolupament. Lloc "anticiclònic". Expansió. Maduració. Acte, enérgeia. Perfecció, entelékheia. Futur. Causa final utòpica.* — Petit manual: «Realitat desplegada i madura. Plenitud dels temps.»

---

## 2. Categories segon nivell — segona dialèctica (24 categories P2)

Combinacions de dos eixos. Distribuïdes en 6 sub-grups segons quins eixos estan actius.

### 2.1 (k, p) — Cernent + Parença [4]

| Codi | Label | Nom | Coords | Antiterme | Definició condensada (Xirinacs §211-§214) | Pàg. |
|------|-------|-----|--------|-----------|--------------------------------------------|------|
| 211 | **AMO** | AMOR | (–, –, 0, 0) | ANÀLISI | *Realitat transcendent: concerniment desparent. Bé / Mal. Bé comú. Bona voluntat (Kant). Compassió, karuna. Filotes (Empèdocles). To agathón (Plató). Cáritas. Fraternitat. Élan vital (Bergson).* | 47 |
| 212 | **EXP** | EXPERIÈNCIA | (–, +, 0, 0) | SÍNTESI | *Realitat manifesta: concerniment aparent. Concurrència. Possessió, èkhein. Existència (Heidegger). Prakriti. Empiria. Acte perlocucionari. Conducta. Lebenswelt (Husserl). Judicis sintètics a posteriori.* | 46 |
| 213 | **ANA** | ANÀLISI | (+, +, 0, 0) | AMOR | *Ment manifesta: discerniment aparent. Crítica. Dissonància. Apófansis. Exposició. Verb. Narració. Discurs (Foucault). Analogia. Diaíresis. Discriminació. Retòrica. Llenguatge universal. Judicis analítics a priori.* | 63 |
| 214 | **SIN** | SÍNTESI | (+, –, 0, 0) | EXPERIÈNCIA | *Ment transcendent: discerniment desparent. Saviesa. Oracle, profecia. Aforisme. Nyana yoga. Teosofia. Aufhebung (Hegel). Mestre, guru. Docta ignorantia. Trinitat. Trimurti. Logos.* | 68 |

### 2.2 (k, t) — Cernent + Tensió [4]

| Codi | Label | Nom | Coords | Antiterme | Definició condensada (§221-§224) | Pàg. |
|------|-------|-----|--------|-----------|-----------------------------------|------|
| 221 | **STM** | SENTIMENT | (–, 0, –, 0) | SIGNIFICAT | *Realitat vivencial: concerniment intens. Força interior. Tremp, Stimmung (Heidegger). To vital. Kundalini. Libido, angoixa (Freud). Orgasme (W. Reich). Exaltació/depressió. Naixement i mort místics. Reencarnació.* | 47 |
| 222 | **SGE** | SIGNE | (–, 0, +, 0) | SENTIT | *Realitat estructural: concerniment extens. Valor (Scheler). Infraestructura. Senyal. Semiòtica. Símbol. Empremta. Hàbit. Virtut, areté. Energia física. Tradició. Significant. Denotació. Bedeutung (Frege). Naixement i mort físics.* | 48 |
| 223 | **SGT** | SIGNIFICAT | (+, 0, +, 0) | SENTIMENT | *Ment estructural: discerniment extens. Sinn (Frege). Veritat / error. Raó (Kant). Superestructura. Geometria. Dret. Definició. Comprensió. Connotació. Sistema. Darsana. Coherència. Compatibilitat. Univocitat. Sinònim. Hermenèutica al peu de la lletra.* | 66 |
| 224 | **STT** | SENTIT | (+, 0, –, 0) | SIGNE | *Ment vivencial: discerniment intens. Gràcia. Intel·ligència. Veracitat / mentida. Idiolecte. Paradoxa, paralogisme. Irracionalitat. Non sens. Equivocitat. Humor. Hermenèutica al peu de l'esperit. Principi de participació (Lévy-Bruhl).* | 63 |

### 2.3 (k, v) — Cernent + Voltant [4]

| Codi | Label | Nom | Coords | Antiterme | Definició condensada (§231-§234) | Pàg. |
|------|-------|-----|--------|-----------|-----------------------------------|------|
| 231 | **CAS** | CAOS | (–, 0, 0, –) | COSMOVISIÓ | *Realitat plàsmica: concerniment involutiu. Microcosmos. Univers plegat. Matriu universal. Aigües primordials. Tenebra. Abisme, la Terra (Heidegger). Revolució. Catàstrofe. "L'altre món".* | (no indicat) |
| 232 | **COS** | COSMOS | (–, 0, 0, +) | CAOVISIÓ | *Realitat mundana: concerniment evolutiu. Macrocosmos. Univers desplegat. La creació. Les criatures, el Món (Heidegger). "Aquest món".* | 46 |
| 233 | **COV** | COSMOVISIÓ | (+, 0, 0, +) | CAOS | *Ment mundana: discerniment evolutiu. Paradigma (Kuhn). Model global. Patró general. Tall epistemològic (Bachelard). Concepció del món, Weltanschauung (Dilthey).* | 63 |
| 234 | **CAV** | CAOVISIÓ | (+, 0, 0, –) | COSMOS | *Ment plàsmica: discerniment involutiu. Enigma. Gnosi. Esoterisme. Ocultisme. Hermetisme.* | 63 |

### 2.4 (p, t) — Parença + Tensió [4]

| Codi | Label | Nom | Coords | Antiterme | Definició condensada (§241-§244) | Pàg. |
|------|-------|-----|--------|-----------|-----------------------------------|------|
| 241 | **MTP** | METAPSÍQUICA | (0, –, –, 0) | CIÈNCIA | *Transcendència vivencial: desparença intensa. Esperit, Geist (Hegel). Ànima. Persona, hypóstasis. Consciència (Hegel). Inconscient (Freud). Èxtasi. Meditació, dhyana. Il·luminació. Llibertat. Holicitat (Wilber). Immortalitat.* | 59 |
| 242 | **MTF** | METAFÍSICA | (0, –, +, 0) | ART | *Transcendència estructural: desparença extensa. Creença, fe. Ontologia. Essència, ousía. Particular, singular. Substància individual. Quidditat. Espècie. Eidètica (Husserl). Judicis apodíctics. Holisme. Cosa en si (Kant). Realisme.* | 56 |
| 243 | **CIE** | CIÈNCIA | (0, +, +, 0) | METAPSÍQUICA | *Manifestació estructural: aparença extensa. Coneixement, Erkenntnis. Il·lustració. Verificació/falsació (Popper). Ciència experimental. Mesura. Variable. Llei. Computadora. Judicis assertòrics. Demostració. Fórmula física. Ciència unificada.* | 53 |
| 244 | **ART** | ART | (0, +, –, 0) | METAFÍSICA | *Manifestació vivencial: aparença intensa. Creació. Poesia. Tacte. Encert. "Ull clínic". Anderswerden (Hegel). Somni, Traum (Nietzsche). Educació. Medicina. Política. Periodisme. Màscara, persona, prósopon.* | 51 |

### 2.5 (p, v) — Parença + Voltant [4]

| Codi | Label | Nom | Coords | Antiterme | Definició condensada (§251-§254) | Pàg. |
|------|-------|-----|--------|-----------|-----------------------------------|------|
| 251 | **CFN** | CONFINAMENT | (0, –, 0, –) | EXACTITUD | *Transcendència plàsmica: desparença involutiva. Tancament. Implosió, remolí. Quark. Subleptó. Clausura, reclusió. Membrana. Agorafòbia. Heràclit el fosc. L'encobriment del ser (Heidegger). Destí, eimarméne, fatum.* | 57 |
| 252 | **CMN** | COMUNIÓ | (0, –, 0, +) | ATZAR | *Transcendència mundana: desparença evolutiva. Obertura. Lliurament, donació de si. Magnanimitat. Explosió. Compartir. Comunicació. Claustrofòbia. La patència del ser (Heidegger).* | 57 |
| 253 | **EXC** | EXACTITUD | (0, +, 0, +) | CONFINAMENT | *Manifestació mundana: aparença evolutiva. Acribologia. Ex actis. Ocasió. Neguentropia. Informació. Conformitat. Confirmació. Contrastació (Carnap, Popper). Validació. Puntualitat. Document. Distinció fenomènica. Classe social (Marx).* | 51 |
| 254 | **ATZ** | ATZAR | (0, +, 0, –) | COMUNIÓ | *Manifestació plàsmica: aparença involutiva. Amfibologia. Confusió, embull, vaguetat. Entropia. Soroll. Exiguum clinamen (Lucreci). Caos estocàstic, caos quàntic. Tiquisme, týkhe (Bergson, James, Peirce).* | 51 |

### 2.6 (t, v) — Tensió + Voltant [4]

| Codi | Label | Nom | Coords | Antiterme | Definició condensada (§261-§264) | Pàg. |
|------|-------|-----|--------|-----------|-----------------------------------|------|
| 261 | **FEL** | FELICITAT | (0, 0, –, –) | AFINITAT | *Vivència plàsmica: intensió involutiva. Ananda. Confiança/desconfiança. Bonhomia. Encantament. Por, fascinació (Otto). Goig/terror (Nietzsche). Temor pànic. Alegria, Freude, eudaimonia, laetitia. Joia/tristesa.* | 50 |
| 262 | **INT** | INTENCIÓ | (0, 0, –, +) | BOSÓ | *Vivència mundana: intensió evolutiva. Cura, epiméleia (Sòcrates). Preocupació. Inquietud del cor (Agustí). Propòsit. Interès. Motivació. Esperança. Selecció. Atenció (Husserl). Vigilància, téresis. Sorge (Heidegger). Reflexió.* | 50 |
| 263 | **AFI** | AFINITAT | (0, 0, +, +) | FELICITAT | *Estructura mundana: extensió evolutiva. Extensió externa. Enllaç. Unió. Mescla, mîxis. Nexe, symploké. Articulació. Coordinació. Composició. Anatomia. Connectives. Disjunció. Aparellament. València. Atracció mecànica. Parentiu. Fidelitat. Exclusió (Pauli).* | 54 |
| 264 | **BOS** | BOSÓ | (0, 0, +, –) | INTENCIÓ | *Estructura plàsmica: extensió involutiva. Condensació (Bose-Einstein). Extensió interna. "Àtom" (Demòcrit). Mònades (Leibniz). Quantum (Planck). Inclusió (Bose). Fusió. Làser.* | 54 |

> **Nota dialèctica P2**: La tesi de Xirinacs documenta 24 categories P2 (no 26). Les categories addicionals que apareixen al `glob_petit` o a la DB com a "Neutral" més enllà d'aquestes 24 (e.g. LOG, EST, MIS, PSI, CIE, ART, etc.) són en realitat **categories P3** (terceres) que la lectura pedagògica posterior tracta com a "disciplines neutres". Vegi's la secció 3 i la nota a la secció final sobre discrepàncies.

---

## 3. Categories tercer nivell — tercera dialèctica (32 categories P3)

Combinacions ternàries (els tres eixos `k, p, t` tots simultàniament actius, o un d'aquests amb `v`). 4 sub-grups × 8 cantons = 32.

### 3.1 (k, p, t) — Cernent + Parença + Tensió [8] — *les 8 disciplines*

Aquest sub-grup conté el que tradicionalment es coneix com a "8 disciplines del coneixement". Tots tenen `v=0` (estan al pla equatorial radial).

| Codi | Label | Nom | Coords | Antiterme | Definició condensada (§311-§318) | Pàg. |
|------|-------|-----|--------|-----------|-----------------------------------|------|
| 311 | **MIS** | MÍSTICA | (–, –, –, 0) | LÒGICA | *Realitat transcendent vivencial. Daimon. Orfisme. Misteri (G. Marcel). Musa. Experiència interior. Impuls dionisíac (Nietzsche). Misteris iniciàtics. Indicibilitat. Inefabilitat. Sacralitat. Sadhana.* | 47 |
| 312 | **ETI** | ÈTICA | (–, –, +, 0) | ESTÈTICA | *Realitat transcendent estructurada. Necessitat. Ent, on. Deure. Instint. Conservació. Memòria. Patrimoni. Protecció. Dret natural. Jusnaturalisme. Corresponsabilitat. Fatalitat, dharma, moira.* | 48 |
| 313 | **TEC** | TÈCNICA | (–, +, +, 0) | MÍTICA | *Realitat manifesta estructurada. Física. Tenir. Possessió. Utilitat. Tekhne. Procediment. Mètode. Màquina. Eina. Experiment. Qualitat, poión.* | 46 |
| 314 | **PSI** | PSÍQUICA | (–, +, –, 0) | IDEICA | *Realitat manifesta vivencial. Sensibilitat (Kant). Psikhe, Eros (Plató). Afecte. Sensacions. Percepció. Imatges. Pensaments. Decisions. Accions. Educació. Maièutica (Sòcrates). Introspecció. Joc.* | 47 |
| 315 | **MIT** | MÍTICA | (+, –, –, 0) | TÈCNICA | *Ment transcendent vivencial. Deliri. Heroïcitat. Epopeia. Litúrgia. Jerarquia. Festa. Carnaval. Glossolàlia. L'imaginari. Vidència. Tragèdia (Nietzsche).* | 71 |
| 316 | **IDE** | IDEICA | (+, –, +, 0) | PSÍQUICA | *Ment transcendent estructurada. Concepte. Einai. Idea. Pensament. Gènere. Classe lògica. Conjunt. Dogma. Tesi/hipòtesi. Doxa. Predicat. Categoria. Teleologia. Finalitat. Idealisme. Universal, kathólon.* | 68 |
| 317 | **LOG** | LÒGICA | (+, +, +, 0) | MÍSTICA | *Ment manifesta estructurada. Matemàtica. Aritmètica (Peano). Sintaxi. Judici. Proposició. Sistema formal. Axiomàtica. Càlcul. Quantitat, posón. Algoritme (Leibniz). Inducció. Deducció. Inferència. Bivalència.* | 65 |
| 318 | **EST** | ESTÈTICA | (+, +, –, 0) | ÈTICA | *Ment manifesta vivencial. Simulacre. Ídols, eídola (F. Bacon). Prejudici. Miratge. Fantasia. Imaginació. Mímesis. Còpula. Ficció. Comèdia. Ironia. Metàfora. Apol·lini (Nietzsche). Polaritat. Complementarietat (Bohr).* | 62 |

### 3.2 (k, p, v) — Cernent + Parença + Voltant [8]

| Codi | Label | Nom | Coords | Antiterme | Definició condensada (§321-§328) | Pàg. |
|------|-------|-----|--------|-----------|-----------------------------------|------|
| 321 | **MGM** | MAGMA | (–, –, 0, –) | PRECISIÓ | *Realitat transcendent plàsmica. Ctònic. Plutònic. "Volcànic". Hades. Xeol. Ebullició. Infern. Avern.* | 47 |
| 322 | **RGN** | REGNE | (–, –, 0, +) | PROBABILITAT | *Realitat transcendent mundana. Paradís terrenal. Cel a la terra. Civitas Dei terrena (Agustí). Edèn. Pàtria. Terra promesa. Utopia realitzada. Comunitat d'amor.* | 47 |
| 323 | **POL** | POLIDESA | (–, +, 0, +) | SUBLIM (SLM) | *Realitat manifesta mundana. Habilitat. Rigor tècnic. Ben fer. Manualitat. Manufactura. Pulcritud. Cortesia. Existenz (Jaspers). Dasein (Heidegger). Deconstrucció (Derrida).* | 46 |
| 324 | **TRB** | TURBULÈNCIA | (–, +, 0, –) | HARMONIA | *Realitat manifesta plàsmica. Agitació. Pressa. Tumult. Baralla. Aldarull. Pertorbació. Crisi. Neptú.* | 46 |
| 325 | **SLM** | SUBLIMITAT | (+, –, 0, –) | POLIDESA | *Ment transcendent plàsmica. Glòria. Fama. Altesa. Excel·lència. Olimp. Walhalla. Magnificència. Sobirania. Supèrbia. Orgull. Júpiter-Zeus. "El tercer cel". Santedat. Corpus Hermeticum.* | 68 |
| 326 | **HAR** | HARMONIA | (+, –, 0, +) | TURBULÈNCIA | *Ment transcendent mundana. Perfecció. Harmonia (Pitàgores, Leibniz). Cel. Empiri. Civitas Dei coelestis. Equilibri. Utopia ideal. Urà. Doctrina exotèrica.* | 68 |
| 327 | **PCS** | PRECISIÓ | (+, +, 0, +) | MAGMA | *Ment manifesta mundana. Matisació. Modificació. Mode. Compte. Computació. Informàtica. Nitidesa. Teoria de tipus. Anticipació, prolepsis.* | 63 |
| 328 | **PRB** | PROBABILITAT | (+, +, 0, –) | REGNE | *Ment manifesta plàsmica. Contingència. Eventualitat. Estimació. Versemblança. Judicis problemàtics o contingents (Kant). Atzar degut a la ignorància. Lleis probabilístiques.* | 63 |

### 3.3 (k, t, v) — Cernent + Tensió + Voltant [8]

| Codi | Label | Nom | Coords | Antiterme | Definició condensada (§331-§338) | Pàg. |
|------|-------|-----|--------|-----------|-----------------------------------|------|
| 331 | **EBR** | EMBRIAGUESA | (–, 0, –, –) | CONVENCIÓ | *Realitat vivencial plàsmica. Entusiasme. "Sentiment oceànic". Ebrietat. Excés, hýbris. Rauxa. Inconscient (Freud). Atordiment. Rausch (Nietzsche).* | 47 |
| 332 | **DSG** | DESIG | (–, 0, –, +) | RARESA | *Realitat vivencial mundana. Voluntat. Sentiment mundà. Afany. Apetit, órexis (Arist.). Anhel. Pruïja.* | 47 |
| 333 | **OBL** | OBLIGACIÓ | (–, 0, +, +) | FOLLIA | *Realitat estructurada mundana. Coacció. Coerció. Imposició. Religió. Exigència. Karma. Objecte desideratiu d'obligació (Meinong).* | 48 |
| 334 | **PRD** | PRODIGI | (–, 0, +, –) | ASTÚCIA | *Realitat estructurada plàsmica. Poders. Meravella. Miracle. Admiració, thauma. Taumatúrgia. Naufragi, Scheitern (Jaspers). Fracàs, échec (Sartre).* | 48 |
| 335 | **FOL** | FOLLIA | (+, 0, –, –) | OBLIGACIÓ | *Ment vivencial plàsmica. Mania (Plató). Bogeria (Foucault), morïa (Erasmus). Extravagància. Absurd (Kierkegaard, Sartre, Camus, Beckett).* | 63 |
| 336 | **AST** | ASTÚCIA | (+, 0, –, +) | PRODIGI | *Ment vivencial mundana. Prudència, frónesis (Plató). Sagacitat. Enginy. "Mà esquerra". Diplomàcia. Picardia. Capacitat de maniobra. Die List der Vernunft (Hegel).* | 63 |
| 337 | **CNV** | CONVENCIÓ | (+, 0, +, +) | EMBRIAGUESA | *Ment estructurada mundana. Capteniment. Sistematicitat. Normalitat. Sobrietat. Concordat. Pacte. Conveni. Persuasió. Convencionalisme (Duhem-Quine, Lakatos, Feyerabend, Kuhn). Continu (Leibniz, Newton).* | 66 |
| 338 | **RAR** | RARESA | (+, 0, +, –) | DESIG | *Ment estructurada plàsmica. Anomalia. Anormalitat. Irregularitat. Sorpresa. Estranyesa (Quark). Una sola vegada, ápax legómena. Excentricitat. Marginalitat. Reminiscència, anámnesis (Plató).* | 66 |

### 3.4 (p, t, v) — Parença + Tensió + Voltant [8]

| Codi | Label | Nom | Coords | Antiterme | Definició condensada (§341-§348) | Pàg. |
|------|-------|-----|--------|-----------|-----------------------------------|------|
| 341 | **LET** | LETARGIA | (0, –, –, –) | FUNCIÓ | *Transcendència vivencial plàsmica. Ataraxía (estoics). Aponía (epicuris). Pau d'esperit. Impassibilitat. Estat inert. Indiferència (Kant, Schelling), adiaforá. Catalèpsia. Son. Hipnosi. Narcosi. Geni adormit.* | 59 |
| 342 | **GEN** | GENI | (0, –, –, +) | ONA | *Transcendència vivencial mundana. Talent. Personalitat. Generativitat. Singularitat. Personalitat. Elf.* | 59 |
| 343 | **OGN** | ÒRGAN | (0, –, +, +) | TRÀNSIT | *Transcendència estructurada mundana. Autoconstruït. Autopoïètic (Luhmann). Compromís ontològic (Quine). Organisme. Organització. Estructuralisme. Zoé.* | 56 |
| 344 | **ORG** | ORGÓ | (0, –, +, –) | AGUDESA | *Transcendència estructurada plàsmica. Autoconstructor. Autogeneració. Llavor. Homeomeries (Anaxàgoras). Ou. Embrió. Germen. Causa. Origen. Autopoïesi (Luhmann). Prana. Energia orgònica (W. Reich). Genètica.* | 56 |
| 345 | **TRS** | TRÀNSIT | (0, +, –, –) | ÒRGAN | *Manifestació vivencial plàsmica. Paroxisme. Mèdium. Accés. Histèria. Eufòria. Inspiració.* | 51 |
| 346 | **AGU** | AGUDESA | (0, +, –, +) | ORGÓ | *Manifestació vivencial mundana. Perspicàcia. Clarividència. Llestesa. Vivacitat. Alerta. Acuïtat. Penetració. Subtilesa. Finor. Minuciositat.* | 51 |
| 347 | **FUN** | FUNCIÓ | (0, +, +, +) | LETARGIA | *Manifestació estructurada mundana. Macrofísica. Biologia. Previsió. Funcionalitat. Funcionament. Fisiologia. Llei macrofísica o determinista. Sanció.* | 53 |
| 348 | **ONA** | ONA | (0, +, +, –) | GENI | *Manifestació estructurada plàsmica. Microfísica (equació d'ona de Schrödinger, fórmula del camp unitari). Ona de probabilitat. Imprevisió. Llei estadística.* | 53 |

---

## 4. Categories quart nivell — quarta dialèctica (16 categories P4)

Combinacions quaternàries — els quatre eixos `k, p, t, v` simultàniament actius. Aquestes són les 16 hiperdiagonals (vèrtexs de l'hipercub 4D).

| Codi | Label | Nom | Coords | Antiterme | Definició condensada (§411-§41G) | Pàg. |
|------|-------|-----|--------|-----------|-----------------------------------|------|
| 411 | **AKA** | AKAIXA | (–, –, –, –) | DETERMINACIÓ | *Realitat transcendent vivencial plàsmica. Abandó. Matèria causal (budisme theravada). Mística de la matèria. Mística plàsmica.* | 47 |
| 412 | **ECU** | ECUMENE | (–, –, –, +) | INDETERMINACIÓ | *Realitat transcendent vivencial mundana. Universalitat concreta. Simbiosi. Altruisme (Comte, Spencer). Comunió dels sants (crist.). Cos místic de Crist. Espiritisme. Mística mundana. Fraternité (Revol. Fr.). Tolerància. Consens.* | 47 |
| 413 | **ECL** | ECOLOGIA | (–, –, +, +) | GLÒRIA | *Realitat transcendent estructurada mundana. Solidaritat. Univers conjuntat. Justesa. Responsabilitat. Reciclatge. Retroacció, feed-back. Impenetrabilitat fermiònica. Ètica mundana.* | 48 |
| 414 | **APE** | ÀPEIRON | (–, –, +, –) | BELLESA | *Realitat transcendent estructurada plàsmica (Anaximandre, Demòcrit, Plató, Epicur). Anòmia (Guyau). "Tot us és permès". "Tot lliga amb tot". Prostitució universal (A. Breton). Ahimsa. Home de frontera. Amoralitat (Nietzsche). Penetrabilitat bosònica. Ètica plàsmica.* | 48 |
| 415 | **PAS** | PASSIÓ | (–, +, –, –) | ARQUETIP | *Realitat manifesta vivencial plàsmica. Pathos, páskhein (Arist.). Emoció. Ira. Plaer/dolor. Concupiscència. Agitació còsmica de base. Patiment. Apassionament. Empatia. Endopatia, Einfühlung. Passivitat. Psíquica plàsmica.* | 47 |
| 416 | **COM** | COMUNITAT | (–, +, –, +) | ARKHÉ | *Realitat manifesta vivencial mundana. Convivència. Col·lectivitat. Col·legi. Societat. Poble. Informació, opinió, decisió, voluntat, acció públiques. Ajuntament. Germania. Confraria. Psíquica mundana.* | 47 |
| 417 | **ECN** | ECONOMIA | (–, +, +, +) | TIÀMAT | *Realitat manifesta estructurada mundana. Empresa. Mínim esforç (Avenarius). Producció, poiesis. Contracte social (Rousseau). Ofici. Mecànica. Fabricació. Tècnica mundana.* | 46 |
| 418 | **ACC** | ACCIÓ | (–, +, +, –) | DIVINITAT | *Realitat manifesta estructurada plàsmica. Profetisme. Praxis (Arist.). Empenta. Iniciativa. Activitat. Agència. Sonambulisme. Automatisme. Acció absoluta, Tathandlung (Fichte), hazaña (Ortega). Tècnica plàsmica.* | 46 |
| 419 | **TIA** | TIÀMAT | (+, –, –, –) | ECONOMIA | *Ment transcendent vivencial plàsmica. Mare universal ideal. Principi femení. Confiança cega. "Les aigües primordials" (Babilònia). Providència. Mítica plàsmica. Consciència pura o transcendental, epokhé (Husserl).* | 71 |
| 41A | **DIV** | DIVINITAT | (+, –, –, +) | ACCIÓ | *Ment transcendent vivencial mundana. Demiürg. Sant, numinós (Otto). Déus. Àngels. Principi masculí. Superhome. Vida sobrenatural. Gràcia. Teogonia. Teofania. Revelació. Carisma. Heroi. Mítica mundana. Deisme (Kant).* | 71 |
| 41B | **ARQ** | ARQUETIP | (+, –, +, +) | PASSIÓ | *Ment transcendent estructurada mundana (Plató, K. Jung). Cosmologia. Cercle, circularitat (Plotí, Procle, Cusa, Hegel). Mandala. Esfera. I-Txing. Càbala. Organon. Ars (R. Llull). Predestinació. Mathesis (Descartes, Leibniz). Tectologia. Camp morfogenètic (Sheldrake). Ordre explicat (Bohm). Ideica mundana. Pattern.* | 68 |
| 41C | **ARK** | ARKHÉ | (+, –, +, –) | COMUNITAT | *Ment transcendent estructurada plàsmica. Cosmogonia. Elements fonamentals (pre-socràtics), bhutas, xandhas, yin-yang. Quintaessència. Arcà. Misteri de fe. Primers principis (Spencer). Causa última. Idea innata. Innatisme. Variables ocultes (Einstein). "Pasta subquàntica". Ordre implicat (Bohm). Ideica plàsmica.* | 68 |
| 41D | **GLO** | GLÒRIA | (+, +, –, –) | ECOLOGIA | *Ment manifesta vivencial plàsmica. Caprici. Antull. Preferència/repugnància (Scheler). Nàusea (Sartre). Atracció estètica. Hedonisme. Gurmanderia. Sensualisme. Erotisme. Refinament. Sibaritisme. Estètica plàsmica.* | 62 |
| 41E | **BEL** | BELLESA | (+, +, –, +) | ÀPEIRON | *Ment manifesta vivencial mundana (Hippies Major de Plató, Scheler, N. Hartmann). Elegància. Esclat. Classe estètica. Estil. Distinció estètica. Proporció. Ornament. Decoració. Estètica mundana.* | 62 |
| 41F | **DET** | DETERMINACIÓ | (+, +, +, +) | AKAIXA | *Ment manifesta estructurada mundana. Claredat. Distinció lògica. Certesa. Tautologia. Principis d'identitat, no contradicció, terç exclòs. Seguretat. Computabilitat. Numerabilitat. Ordre. Cibernètica. Cientifisme. Reduccionisme. Cognoscible (Spencer).* | 65 |
| 41G | **IDT** | INDETERMINACIÓ | (+, +, +, –) | ECUMENE | *Ment manifesta estructurada plàsmica (Heisenberg). Borrositat. Implícit. Desordre. Incertesa. Principis de no identitat, contradicció, terç inclòs (Lupasco). Infinit. Il·limitat. Imprevisibilitat. Incognoscible (Spencer). Dubte. Epokhé (Nova Acadèmia). Interpretació de Copenhaguen.* | 65 |

---

## 5. Resum — comptatge i taxonomia

| Dialèctica | Codis | # | Capa DB resultant (segons signe v) |
|-------------|--------|---|--------------------------------------|
| 1ª (P1, generadors) | 11x, 12x, 13x, 14x | 8 | Eixos cardinals (PRA/TEO/NOU/FEN/SUB/OBJ Neutral; PLA/MON Plasmàtic/Mundà polars) |
| 2ª (P2, parelles) | 21x..26x | 24 | 8 amb v=– (Plasmàtica), 8 amb v=+ (Mundana), 8 amb v=0 (Neutral) |
| 3ª (P3, ternàries) | 31x..34x | 32 | 8 amb v=0 (Neutral, "disciplines"), 12 amb v=+ (Mundana), 12 amb v=– (Plasmàtica) |
| 4ª (P4, quaternàries) | 411..41G | 16 | 8 amb v=– (Plasmàtica), 8 amb v=+ (Mundana) |
| **Total** |  | **80** | |

Distribució DB (independent dialèctica):
- **Plasmàtiques** (`v=–`): 1 + 8 + 12 + 8 = **29 entries** (PLA + 8 P2 + 12 P3 + 8 P4)
- **Mundanes** (`v=+`): 1 + 8 + 12 + 8 = **29 entries** (MON + 8 P2 + 12 P3 + 8 P4)
- **Neutrals equatorials** (`v=0`): 6 + 8 + 8 = **22 entries** (PRA, TEO, NOU, FEN, SUB, OBJ + 8 P2 amb v=0 + 8 P3 disciplines)

Total: 80 categories pures + (PLA, MON ja comptats al primer grup) = 80.

> **Discrepància amb la DB actual** (90 entries): el surplus respecte de 80 prové d'entries duplicades als generadors entre capes (e.g. PLA com a id=1 a (0,0,0) i una segona ocurrència a la capa Plasmàtica), de vèrtexs polars `MONp1..MONpt4` (12 entries) i de l'entrada `AZO` placeholder. Vegi's nota AZO més avall.

---

## 6. Nota sobre AZO

**`AZO` no apareix a la tesi de Xirinacs ni a cap dels documents canònics posteriors** (`glob_petit`, `glob_trainer`, `globalium-manifest`, `saviesa-artificial`, `globalistica`, `arkadium-project`).

Recerca exhaustiva a `xirinacs-tesi-1997.txt`: les úniques aparicions del trigrama "AZO" són com a substring de `metazoa`/`metazous` (zoologia, lectura biològica de la jerarquia r=0,40c MET). No hi ha cap categoria amb label AZO al corpus canònic.

A la DB `opengea_kms.kms_kb_categories` existeix una entrada `AZO` amb `id=93` i `name_en="cc"` (placeholder), i a `kms_kb_metacategories` amb `parent=28 id=2815` apareix amb `nom="Accidentalitat"`.

**Aclariment de Jordi (2026-05-02)**: "Accidentalitat" és **un terme afí d'Atzar**, no un duplicat sense sentit. AZO és, doncs, una **lectura plasmàtica complementària de l'eix ATZ** — sigui com a sinònim plasmàtic ("atzar com a accident pur"), sigui com a inflexió específica del concepte d'atzar a la capa interior. ATZ continua essent la categoria canònica de Xirinacs (codi 254, coords `0,+p,0,–v`, antiterme COMUNIÓ); AZO és afegit post-canònic que captura un matís semàntic afí.

**Implicació per al meta-de-PLA (parent=28)**: les dues entrades (2245 ATZ "Aleatorietat", 2815 AZO "Accidentalitat") són **lectures complementàries** del mateix pol radial (atzar plasmàtic). No cal eliminar AZO; cal documentar la relació de sinonímia/afinitat entre les dues. Resta pendent decidir si es manté com a doblet semàntic o es consolida.

---

## 7. Discrepàncies trobades entre documents

### 7.1 Grafia del label CONFINAMENT

- **Tesi 1997** (Xirinacs, línies 4364, 4716): `CFN`
- **Glob_trainer (anglès)** (línia 723): `CNF`
- **Glob_petit (català)**: no apareix label explícitament
- **CLAUDE.md del projecte**: `CNF`
- **DB `opengea_kms`**: per verificar — probablement `CFN` (canònic) o `CNF` (post-canònic)

**Recomanació**: adoptar `CFN` per coherència amb la tesi. Documentar el sinònim `CNF` al manifest si la DB l'usa.

### 7.2 Grafia de SUBLIM/SUBLIMITAT

- **Tesi 1997 — Esquema XXXV** (línia 4382): label `SUBLIM` com a antiterme de POL — escrit `SUBLIM` (forma curta).
- **Tesi 1997 — Esquema XXXV** (línia 4384): nom de categoria `SUBLIMITAT (SLM)`.
- A línia 3180 apareix la sigla `SBL`, però no com a label oficial sinó com a referència informal al §325.
- **Glob_petit, glob_trainer, manifest**: tots usen `SLM` (Sublimitat).

**Conclusió**: el label canònic és `SLM`. `SBL` és una referència informal puntual; `SUBLIM` (sense suffix) és la forma curta del nom.

### 7.3 Disciplines com a "Neutrals" (categories P3 amb v=0)

- **Tesi 1997**: les 8 disciplines (MIS, ETI, TEC, PSI, MIT, IDE, LOG, EST) són **categories P3 (terceres)**, no segones.
- **Glob_petit (Berenguer 2024)**: les llista junt amb les P2 (AMO, EXP, ANA, SIN, STM, SGE, SGT, STT, MTP, MTF, CIE, ART) sota la rúbrica pedagògica "Neutrals" sense distingir entre P2 i P3.
- **DB `opengea_kms`**: les 26 entries Neutrals barregen P2 i P3 (8 binàries r=100 + 12 ternàries r≈85·√3 + 6 generadors r=100).

**Implicació**: la lectura pedagògica del Manifest 2026 i del CLAUDE.md ("8 generadors + 12 disciplines + 8 P2 binàries", `r` diferenciats) és correcta operativament però **trenca la classificació original** de Xirinacs. No és una contradicció: és una *vista de presentació* sobre el catàleg subjacent. Cal documentar-ho explícitament al manifest.

### 7.4 Ordenació dels eixos D1-D2-D3

Xirinacs usa l'ordre `(k, p, t, v)` → `(Cernent, Parença, Tensió, Voltant)` → conceptualment `(TEO-PRA, FEN-NOU, OBJ-SUB, MON-PLA)`.

El CLAUDE.md d'Arkadium llista les dimensions en ordre `D1=SUB-OBJ, D2=TEO-PRA, D3=NOU-FEN, D4=PLA-MON`. **No coincideix** amb l'ordre canònic de Xirinacs (que seria D1=Cernent, D2=Parença, D3=Tensió, D4=Voltant).

**Cap implicació matemàtica** (els eixos són ortogonals, l'ordre és convencional), però per coherència de cita acadèmica i per claredat als nous documents recomano:
- Mantenir ordre Xirinacs (k, p, t, v) per tot el que es refereixi a la tesi.
- Documentar al CLAUDE.md la convenció emprada al codi i al manifest, amb el mapping explícit a (k, p, t, v).

### 7.5 Categoria 41A vs. label DIV

A la taula original (línia 4413): `41A. DIVINITAT (DIV)`. La numeració hexadecimal s'utilitza perquè els 16 vèrtexs d'una dialèctica quarta requereixen 16 valors (1..G en base hexa+G estesa). Cal que la DB i el manifest preservin aquesta numeració extensa: 411, 412, ..., 419, 41A, 41B, 41C, 41D, 41E, 41F, 41G. Si la DB usa codis decimals diferents (e.g. 4110, 4111…) hi ha una conversió necessària.

### 7.6 Antiterme de PRD

A la tesi (línia 4391): `334. PRODIGI (PRD) –k, 0, +t, –v. ASTÚCIA`. Antiterme **ASTÚCIA**.
A glob_petit (línia 931): "PRD (Prodigi): característica o fet sorprenent. Meravella. → SGE" (apunta a SGE, signe). Aquesta fletxa `→ SGE` indica la *categoria neutra cap a la qual recula PRD per anular el seu desplaçament v* (PRD té `–v` i SGE té `v=0` amb mateixa firma `(–k, 0, +t)`). No és l'antiterme; és el "neutralitzador radial". El petit manual no contradiu Xirinacs en cap cas a la tesi: complementa la lectura amb una segona relació útil per a la praxi.

---

## 8. Implicacions per al meta-de-PLA (parent=28 a la DB)

Aquest catàleg permet enquadrar la revisió pendent de coherència PLA-NEU-MON (vegi's `docs/coherence-review-meta-PLA-2026-05-01.md`) sobre bases canòniques fortes:

1. **Cada categoria Mundana té una contrapart Plasmàtica única** definida per inversió del signe `v`. Les 29 plasmàtiques que canònicament hi ha al model són exactament aquelles que tenen `v=–`. La taula d'inversions ha de ser bijectiva.

2. **Els 12 parells P3 (k,p,v=0)+(k,p,t,v)+(k,p,t,–v)** que el CLAUDE.md anomena «12 ternàries Neutrals + Mundanes + Plasmàtiques» són en realitat:
   - 8 Neutrals P3 disciplines (MIS, ETI, TEC, PSI, MIT, IDE, LOG, EST) — totes amb `v=0`
   - 12 Mundanes (les 12 P3 amb `v=+`: RGN, POL, HAR, PCS, DSG, OBL, AST, CNV, GEN, OGN, AGU, FUN)
   - 12 Plasmàtiques (les 12 P3 amb `v=–`: MGM, TRB, SLM, PRB, EBR, PRD, FOL, RAR, LET, ORG, TRS, ONA)

3. **Les 8 P4 Mundanes vs. 8 P4 Plasmàtiques** són hiperdiagonals i constitueixen el nivell més extern del model en la lectura radial. Els seus parells per inversió de `v` són:
   - PAS↔COM, ECN↔ACC, TIA↔DIV, ARK↔ARQ, GLO↔BEL, DET↔IDT, AKA↔ECU, APE↔ECL.

   Aquests 8 parells haurien de constituir l'esquelet del meta-de-PLA al nivell més profund de la dialèctica.

4. **La distinció Plasmàtica/Mundana NO s'aplica als P3 disciplines (v=0) ni als generadors transversals (PRA, TEO, NOU, FEN, SUB, OBJ — tots amb v=0)**. PLA i MON són els únics generadors que estan a la dimensió radial.

---

## 9. Resum executiu (≤200 paraules)

S'han transcrit **80 categories canòniques** a partir de l'Esquema XXXV (línies 4339-4421) i de l'Índex analític §397 (línies 4424-5200) de la tesi de Xirinacs (1997). Distribució: 8 generadors P1 + 24 P2 + 32 P3 + 16 P4 = 80. Cap categoria addicional documentada al corpus canònic.

**Naturalesa del catàleg (clarificació de Jordi 2026-05-02)**: les 80 categories no són definitives. Són una proposta històrica de cobertura de l'espectre de la realitat, qüestionable i revisable, que serveix de base per derivar els principis fonamentals del Meta-Globàlium. El doc és **baseline**, no font de veritat tancada.

**Aclariment AZO**: AZO no apareix als documents canònics, però el seu `nom` "Accidentalitat" a `kms_kb_metacategories` parent=28 id=2815 és un **terme afí d'Atzar** (no un placeholder buit). Funciona com a doblet semàntic d'ATZ a la lectura plasmàtica. La hipòtesi inicial `AZO == ATZ` queda matisada: no és el mateix label, però sí termes afins d'un mateix pol radial.

**Divergències més rellevants Tesi vs glob_petit/CLAUDE.md**:
1. Label `CFN` (tesi) vs `CNF` (manifest+glob_trainer). Recomanació: adoptar `CFN`.
2. Les 8 disciplines (MIS, ETI, TEC, PSI, MIT, IDE, LOG, EST) són P3 (no P2). El CLAUDE.md i la DB les barregen amb les P2 sota la rúbrica «Neutral»: és una vista pedagògica vàlida, però cal documentar-la com a tal.
3. Numeració hexadecimal (41A..41G) als 16 vèrtexs P4: si la DB no la preserva, cal mapping.

Les definicions citades vénen totes de la tesi i del glob_petit (català) + glob_trainer (anglès). No s'ha inventat cap definició.
