<!-- Source: https://arkadium.ai/papers/arkadium/ca/
     License: CC BY-SA 4.0 -->

# Arkadium · Paper

[English version](/manifest/en/)


## Resum


Els grans models de llenguatge (LLM, *Large Language Models*) presenten quatre dèficits estructurals que no es resolen amb més escala: correctesa, transparència, generalització i eficiència. Els models de raonament recents — la sèrie o d'OpenAI, DeepSeek-R1, Gemini Thinking, Anthropic Opus i Sonet — milloren en dominis amb verificador formal (matemàtiques, codi, lògica), però col·lapsen en dominis humans on no hi ha veritat de referència: ètica, política, judici social, deliberació pública. Aquest paper presenta una proposta tècnica concreta per superar aquest «límit del raonament formal» (*verifier gap*).


**L'aportació tècnica** és una **funció de completesa dispersa** 𝓗(*r*) ∈ [0, 1] que quantifica, sobre una metaestructura ontològica relacional explícita, fins a quin punt una resposta *r* integra els pols dialèctics del model. Aquesta completesa és el que anomenem **veritat globalística**: una concepció no-monològica de la veritat que reconeix la pluralitat irreductible dels seus modes d'accés (objectiu i subjectiu, teòric i pràctic, fenomènic i nouménic, plasmàtic i mundà), en consonància amb la tradició hermenèutica i comunicativa de fons (Gadamer, Habermas, Heidegger). El moviment metodològic és **dels models predictius — que extrapolen patrons del corpus d'entrenament — als models de judici — que avaluen la pròpia sortida contra una ontologia relacional explícita**. **Arkadium** és la primera materialització funcional d'aquesta proposta: l'agent conversacional, el framework RAG i el Metamodeler 3D que calculen 𝓗(*r*) en runtime sobre cada resposta. Argumentem que aquesta via — oberta i sobirana — és estructuralment necessària per superar el sostre actual de l'escala bruta amb constitucions textuals. Demostració disponible a [arkadium.ai](https://arkadium.ai).


**Genealogia filosòfica.** Aquest treball s'inspira del model [Globàlium](https://www.bardina.org/globalium/lmx_tesi_1997_completa_1.pdf) (Xirinacs 1997, tesi doctoral defensada a la Universitat de Barcelona), heretat de la tradició catalana de pensament integrador (Llull → Sibiuda → Pujols → Xirinacs): una hipersfera 4D amb 8 categories primàries, 26 al model menor, 80 al major, organitzades en quatre dimensions dialèctiques. El Globàlium és patrimoni filosòfic, desenvolupat per Xirinacs i citat aquí com a font d'inspiració; **no és part del nostre treball**. (i) **El Meta-Globàlium** (Berenguer / Opengea, 2024–2026) és l'extensió formal i computacional del Globàlium, des d'on se'n deriven nous axiomes i principis i sobre la qual es defineix la funció 𝓗. (ii) **Arkadium** (Berenguer / Opengea, 2024–2026) és l'agent que opera ancorat al Meta-Globàlium com a substrat — l'artefacte tècnic verificable que materialitza la proposta i la posa a prova. En el llinatge xirinaquià, d'aquesta plenitud dialèctica de la veritat se'n deriva, com a herència normativa, la noció del **Bé com a harmonia entre parts** — el Bé deriva de la veritat plena, no la substitueix.


Argumentem que el moviment necessari és **dels models predictius — que extrapolen patrons del corpus d'entrenament — als models de judici — que avaluen la completesa dispersa de la pròpia sortida contra una ontologia relacional explícita**. Arkadium és la primera materialització funcional d'aquest moviment. La nostra orientació és, a més, antropològicament explícita: **una IA que t'ensenya a pensar, no una IA que pensa per tu**. Defensem que la tecnologia ha d'equipar els humans amb cultura — entesa com a *software* compartit i revisable — que els faci més autosuficients, no més dependents; i que un framework ontològic comú entre humans i agents artificials, lluny de ser un luxe acadèmic, és la condició estructural perquè aquesta relació sigui d'emancipació i no de delegació.


**Paraules clau**: AI alignment, neuro-symbolic AI, judgment models, models de judici, structural verification, ontologia compartida, shared ontology, AGI, fractal recursion, non-monological truth verification, veritat globalística, completesa dispersa, Process Reward Model, representation engineering, ontological hyperspace, retrieval-augmented generation, Globàlium, Meta-Globàlium, Arkadium, dialectical reasoning, scalable oversight, computational wisdom.

Taula de continguts

- [Meta-Globàlium i Arkadium: dos nivells del nostre treball](#sec-1)
- [Introducció: el problema del verificador](#sec-2)
- [El problema del verificador per a dominis humans](#sec-3)
- [El Meta-Globàlium com a verificador estructural](#sec-4)


[Capa estructural: completesa dispersa](#sec-4-1)
- [Capa epistèmica: veritat globalística](#sec-4-2)
- [Capa normativa: Bé com a harmonia](#sec-4-3)
- [Sis principis axiomàtics](#sec-4-4)
- [Vuit dialèctiques màximes](#sec-4-4-b)
- [Correspondències canòniques sistemàtiques](#sec-4-4-c)
- [Cicle d'inferència de 8 estacions](#sec-4-5)
- [Iteració Solve-Coagula (meta-operació)](#sec-4-5-c)
- [Tres voltes del Mètode Global](#sec-4-5-b)



- [Interpretabilitat: baix-dalt vs. dalt-baix](#sec-5)
- [La neuro-simbolicitat com a estratègia industrial](#sec-6)
- [Eficiència, *priors* i sobirania digital](#sec-7)

[Una contribució al debat sobre l'AGI](#sec-7-bis)


- [Supervisió escalable i saviesa computacional](#sec-8)
- [Prova de concepte: l'agent Arkadium](#sec-9)


[Components](#sec-9-1)
- [Endpoints i operativa](#sec-9-2)
- [Resultats de tests](#sec-9-3)
- [Validació empírica: pla d'estudi](#sec-9-3-b)
- [Cas d'ús treballat: cicle de 8 estacions](#sec-9-3-c)
- [Estat d'obertura](#sec-9-4)
- [Snippets de replicació](#sec-9-5)



- [Arkadium com a tecnologia d'autonomia](#sec-10)
- [Anàlisi comparativa](#sec-11)


[La combinació única](#sec-11-1)
- [Reconeixement de superioritats alienes](#sec-11-2)
- [Posicionament: complementarietat](#sec-11-3)



- [Camí d'implementació](#sec-12)
- [Discussió i limitacions](#sec-13)

[Objeccions previstes](#sec-13-b)- [Una missió col·lectiva: reorganitzar el coneixement humà](#sec-13-c)


- [Conclusió](#sec-14)
- [Referències](#references) · [Com citar](#how-to-cite)

## 1. Meta-Globàlium i Arkadium: dos nivells del nostre treball

La proposta d'aquest paper s'articula en **dos nivells del nostre treball** — el Meta-Globàlium i Arkadium —, ancorats en una **font d'inspiració filosòfica** prèvia, el Globàlium de Lluís M. Xirinacs. Cal distingir aquesta font del que és pròpiament el nostre treball: el Globàlium és patrimoni filosòfic català desenvolupat per Xirinacs i citat aquí com a font d'inspiració; el Meta-Globàlium i Arkadium són evolucions formals i computacionals desenvolupades per Jordi Berenguer i Opengea (2024–2026).


**Font d'inspiració — El [Globàlium](https://www.bardina.org/globalium/lmx_tesi_1997_completa_1.pdf)** (Xirinacs 1997). Model filosòfic global de la realitat, inscrit en la tradició catalana de pensament integrador — Ramon Llull i la seva *Ars Magna* (segle xiii), Ramon Sibiuda i la *Theologia Naturalis* (segle xv), Francesc Pujols i el *Concepte general de la ciència catalana* (1918), passant per Eugeni d'Ors —, és la culminació contemporània d'una pretensió persistent: oferir una cartografia exhaustiva i revisable del coneixement humà capaç d'encabir-ho «tot, des de Déu fins a una espardenya» (Xirinacs 1997). Geomètricament, és una hipersfera quadridimensional; estructuralment, conté 8 categories primàries, 26 al model menor i 80 al major, articulades sobre quatre dimensions dialèctiques (TEO ↔ PRA, SUB ↔ OBJ, NOU ↔ FEN, PLA ↔ MON) i quatre principis (identitat, alteritat, holicitat, universalitat). És patrimoni filosòfic — un mapa, no el territori — i font de la qual partim però que no constitueix el nostre treball pròpiament dit.

**Una segona genealogia: el llinatge del raonament mecanitzat.** A la línia catalana del pensament integrador (Llull → Sibiuda → Pujols → Xirinacs) s'hi entrellaça una segona genealogia, internacional i tècnica, igualment ancorada en Llull com a precursor: la del **raonament mecanitzat occidental** — Ramon Llull i la combinatòria de l'*Ars Magna* (segle xiii) → Gottfried Leibniz i la *characteristica universalis* (1666) → Charles Babbage i la *Analytical Engine* (1834) → Alan Turing i la màquina universal (1936) → John McCarthy i la fundació del camp de la intel·ligència artificial (Dartmouth 1956), tal com recullen Agustí-Cullell i Schorlemmer (2021, p. 109) en la història canònica de la disciplina. Llull ocupa una posició doble: és arrel comuna de la cartografia filosòfica catalana *i* del raonament mecanitzat universal. Arkadium, en aquest sentit, no és una proposta antagònica al projecte computacional clàssic — n'és una continuació coherent que el reorienta cap a un substrat ontològic explícit, recuperant la combinatòria lul·liana com a *prior* estructural en lloc de delegar-la a l'emergència estadística del corpus.

**Xirinacs ja preveia, el 1997, l'aplicació del Globàlium a sistemes d'intel·ligència artificial.** A la mateixa tesi doctoral hi formulà aquesta intuïció amb claredat literal. Descrivint un dels exercicis presentats al final del treball, hi escriu:

> 
«[un petit llibre,] servit en annex, fet "a màquina" pel mateix model, **com a preludi d'allò que se li hauria d'anar demanant a una vera intel·ligència artificial**»

Aquesta no és una metàfora retrospectiva: és una declaració explícita d'intenció computacional, formulada quan els grans models de llenguatge ni tan sols existien. La intuïció original es valida ara, dècades després, quan els sistemes d'IA contemporanis revelen exactament les necessitats arquitectòniques que el seu model ja oferia: topologia explícita i computable, dialecticitat sistemàtica, granularitat humanament inspeccionable (Miller 7±2), recursivitat fractal escalable i externalitat respecte al llenguatge natural. El Meta-Globàlium i Arkadium són la **materialització tècnica del preludi xirinaquià** — la trobada entre una visió filosòfica formulada el 1997 com a anticipació documentada, i una capacitat de càlcul que ara per fi la pot hostatjar plenament. Allò que Xirinacs anomenava «vera intel·ligència artificial» és precisament el que aquesta proposta reclama: *no* una IA que extrapola patrons, sinó una IA ancorada estructuralment a un model global del coneixement humà.

**Tres limitacions reconegudes pel propi Xirinacs.** El Globàlium és, en paraules del seu autor, una «primera formalització ben definida i fonamentada de la intuïció de la globalitat» (Xirinacs 1997, §22), oberta explícitament a desenvolupament posterior en tres aspectes que el Meta-Globàlium aborda. **(i) Resolució discreta.** Les 80 categories condensen en nodes únics conceptes afins amb matisos diferents, i el model no resol la seva ubicació interna; el propi Xirinacs ho admet apuntant a «un aprofundiment fractal, dependent de la magnitud "resolució" o "escala"» (1997, §22), camí que el Meta-Globàlium pren amb l'arquitectura fractal de 6400 metacategories (80 expressions tematitzades × 80 categories) recursivament subdividible. **(ii) Manca de mètode operatiu.** El Globàlium és presentat com un instrument visual; Xirinacs explicita que «deixem a altres el desenvolupament de la "Modelologia"» (1997, §187) i adverteix que el seu ús pertany no a la màquina «ans a l'art» (§490.012); el Meta-Globàlium hi respon amb el Mètode Global formalitzat — cicle d'inferència auditable de 8 estacions instanciat en tres voltes bàsiques pels cercles màxims (Volta d'Aplicació ANA → SIN → AMO → EXP, Volta d'Orientació, Volta de Coneixement), amb la meta-operació Solve-Coagula com a iterador direccional sobre l'eix FEN ↔ NOU. **(iii) Manca de fonament axiomàtic.** Les categories plasmàtiques — centre regeneratiu i llavor de la resta del model — són definides al Globàlium per intuïció filosòfica, sense un sistema d'axiomes que en capti l'essència primera i permeti derivar-ne els principis; el Meta-Globàlium hi aporta una formalització axiomàtica amb sis principis (Regenerativitat, Interdependència, Plurisingularitat, Totalitat, Mutabilitat, Integritat) derivats de vuit operacions matemàtiques fonamentals (igualtat/polaritat, distinció/correspondència, similitud/divergència, convergència/diferència) sobre el cub neutral, la qual cosa permet nivells de generalització més rigorosos i globals.


**(i) El Meta-Globàlium** (Berenguer / Opengea, 2024–2026) és l'*extensió formal i computacional* del Globàlium que hem desenvolupat per dotar-lo de molta més resolució i fer-lo operatiu sobre un substrat de càlcul. Aporta sobre el model original: (a) una formalització axiomàtica amb sis principis derivats (Regenerativitat, Interdependència, Plurisingularitat, Totalitat, Mutabilitat, Integritat) i vuit dialèctiques màximes derivades del cub neutral, totalitzant **catorze elements estructurals** que recobreixen exhaustivament les classes de relacions geomètriques del model; (b) un *mapping* computacional que assigna a cada una de les 80 categories diferents una posició cartesiana i un quadrant primari de pertinença; (c) una **arquitectura fractal de dos nivells** que escala fins a **6400 metacategories** (80 expressions tematitzades × 80 categories canòniques) — el Nivell 1 és el *model de principis* universal (la gramàtica geomètrica i dialèctica del Meta-Globàlium); el Nivell 2 són les *expressions tematitzades* (Subjecte, Disciplines, Virtuts, Pedagogia, Ideologia, Matemàtiques, Filosofia, Lingüística, Arquetips, Salut, Física…), cadascuna una cristal·lització dels mateixos 14 elements estructurals sobre un tema central, amb una lectura semàntica específica de cada posició — i ofereix la resolució fina necessària per a l'ancoratge en *embeddings* i *retrieval*; (d) una *whitelist* canònica de codis (ANA, SIN, AMO, EXP, BEL, COS, IDE…) per a l'ancoratge inequívoc; (e) la **inscripció canònica de la quarta dimensió** com a *tempeternitat* (portmanteau temps + eternitat), eix radial transversal PLA ↔ MON que opera sobre els altres pols donant a cadascun les seves tres projeccions PLA/NEU/MON; (f) el **Mètode Global** com a arquitectura d'inferència auditable, instanciat en tres voltes bàsiques — cercles màxims pels 8 cardinals sense travessar PLA/MON — cadascuna amb el seu cicle propi de quatre operacions: Volta d'Aplicació (meridià central) ANA → SIN → AMO → EXP, Volta d'Orientació (meridià lateral) STM → STT → SGT → SGE, i Volta de Coneixement (equador) ART → MTP → MTF → CIE; sobre les voltes que travessen FEN-NOU (Aplicació i Coneixement) opera la **meta-operació Solve-Coagula**, que itera el cicle direccionalment FEN → NOU; les tres voltes restants que sí passen per PLA-MON (Universal, Relació, Consistència, per la nomenclatura de Globalística) queden apuntades per desenvolupament posterior; (g) variants temàtiques (A, B, …, V) sobre àmbits especialitzats; i (h) **una funció de completesa dispersa** sobre l'ontologia relacional, que quantifica fins a quin punt una resposta integra els pols dialèctics del model. Aquesta completesa és el que anomenem **veritat globalística** — una concepció no-monològica de la veritat que reconeix la pluralitat dels modes d'accés (OBJ+SUB, TEO+PRA, FEN+NOU, PLA+MON). En el llinatge xirinaquià, d'aquesta plenitud dialèctica se'n deriva, com a hereditat normativa, la noció del **Bé com a harmonia entre parts**: no és un output algorísmic, sinó el llegat ètic que el verificador no usurpa — només recull la condició estructural prèvia, la veritat plena.


**(ii) Arkadium** (Berenguer / Opengea, 2024–2026) és l'*agent i ecosistema* que opera ancorat al Meta-Globàlium. Comprèn una aplicació web pública ([arkadium.ai](https://arkadium.ai)), un framework RAG amb dues bases de coneixement vectorials (KB-A pública sobre les categories, KB-B privada per usuari amb separació multi-tenant), un verificador estructural en runtime que calcula la funció de completesa dispersa 𝓗(*r*) — operacionalització de la veritat globalística — sobre cada resposta, un re-prompt loop d'autocorrecció, i un Metamodeler 3D que il·lumina dinàmicament les categories citades. Arkadium és **l'artefacte tècnic verificable** que materialitza la proposta i la posa a prova en condicions reals.

La metàfora natural il·lumina la relació: el Globàlium és el *mapa filosòfic original* que ens inspira; el Meta-Globàlium és el *mapa computeritzable i el mètode* que en derivem; Arkadium és el *vehicle que el navega*. Els dos nivells del nostre treball pressuposen i citen la font, però no la substitueixen. La resta del paper desenvolupa la justificació tècnica — per què cal aquest tipus de substrat, com s'articulen els seus components i per què Arkadium constitueix la primera materialització funcional sotmesa a inspecció pública.


**Hipòtesi fonamental.** Aquesta proposta reposa sobre una aposta que cal explicitar: *i si l'espai geomètric esfèric, més enllà de representar l'espai epistemològic global de la realitat, permetés organitzar els conceptes fonamentals de qualsevol àmbit del coneixement de manera òptima, facilitant-ne la comprensió integral?*


La hipòtesi és que els universals reflexius — subjecte–objecte, teoria–pràctica, fenomen–noümen, plasma–món — no només són els eixos sobre els quals es desplega la realitat en el seu conjunt, sinó **operadors estructurals que es projecten fractalment sobre qualsevol regió interna d'aquesta**. Si la hipòtesi és correcta, el Meta-Globàlium no és només una ontologia: és **un model de models** — una matriu generativa capaç de proporcionar a cada tema possible la seva pròpia visió global, ancorada als mateixos eixos dialèctics i, per tant, mútuament traduïble. L'arquitectura fractal de 6400 metacategories operacionalitza tècnicament aquesta aposta: cada expressió tematitzada (Subjecte, Disciplines, Virtuts, Pedagogia, Ideologia, Salut, Física, Matemàtiques, Lingüística, Filosofia…) és una cristal·lització dels mateixos principis universals sobre un domini particular — des de l'ésser humà mateix fins a qualsevol disciplina o pràctica. La verificació última no serà filosòfica sinó **funcional**: l'eficàcia amb què el Meta-Globàlium permeti fer intel·ligibles, sobre una geometria comuna, dominis fins ara articulats per llenguatges incommensurables. Aquest paper en formalitza la primera operacionalització.

## 2. Introducció: el problema del verificador

L'any 2023, en el quadern *Saviesa Artificial* (Berenguer 2023), defensàvem que els quatre dèficits centrals dels sistemes d'IA — correctesa, transparència, generalització i eficiència — només es resoldrien recuperant les virtuts de la IA simbòlica sense renunciar al poder de les xarxes neuronals. Tres anys després, els models de raonament basats en *reinforcement learning* sobre cadenes de pensament (DeepSeek-AI 2025; OpenAI 2024) han demostrat resultats notables només en dominis amb verificador objectiu (matemàtiques, codi, lògica). Apple Machine Learning Research (Shojaee et al. 2025) ha documentat com aquests models col·lapsen quan la complexitat sobrepassa un llindar i com l'*esforç de raonament* mesurat en tokens decreix paradoxalment amb el problema.

Fora dels dominis formals — judici ètic, deliberació política, arbitratge d'interessos — no hi ha funció de pèrdua objectiva. Els *Process Reward Models* (PRM) construïts amb retroalimentació humana es desfan per *reward hacking*. Constitutional AI (Bai et al. 2022) i *Deliberative Alignment* codifiquen principis com a llistes textuals, però aquestes constitucions s'interpreten lliurement pel propi model sense un substrat estructural extern que les ancori.

El que proposem aquí és que **el problema del verificador per a dominis humans és, ara mateix, el problema central de l'alineament d'IA**, i que té una via de solució tècnica concreta: substituir la constitució textual per una **metaestructura ontològica relacional** sobre la qual definir matemàticament una **funció de completesa dispersa**. Aquesta metaestructura és el Meta-Globàlium descrit a §1; l'agent que l'utilitza com a substrat operatiu és Arkadium. El que el verificador mesura és, en termes operatius, fins a quin punt la resposta integra els pols dialèctics del model — propietat **epistèmica** que anomenem *veritat globalística* (una veritat no-monològica, plural en els seus modes d'accés). En la tradició xirinaquiana, d'aquesta plenitud dialèctica se'n deriva la noció del Bé com a harmonia entre parts; el verificador no decideix què és el Bé — recull la condició estructural prèvia que aquesta tradició lliga a la veritat completa.

Convé enquadrar el diagnòstic en termes més generals. Els LLM actuals són essencialment **models predictius**: donada una entrada, generen la sortida més probable segons les regularitats del seu corpus d'entrenament. Els models de raonament — la sèrie o, R1, Claude amb pensament estès — afegeixen una capa de verificació interna que funciona en dominis amb veritat de referència (matemàtiques, codi). En dominis humans, però, aquesta extensió falla, i la solució no és més predicció: és un **canvi de naturalesa** — passar de predir a **jutjar**. Un model de judici no es pregunta «què seria estadísticament esperable que digués un humà aquí?», sinó **«la sortida que estic generant integra els pols dialèctics necessaris per a una comprensió plena del fenomen?»**. La diferència és arquitectònica: el judici exigeix una referència externa al corpus — una ontologia relacional explícita sobre la qual el model pugui projectar la seva pròpia sortida i mesurar-ne la completesa. Aquesta és la transició conceptual que Arkadium materialitza tècnicament: del model predictiu condicionat per la freqüència del corpus al model de judici condicionat per la geometria del Meta-Globàlium.


**Tesi diagnòstica.** En el fons, el problema que tenim amb la IA és un problema d'**ontologia compartida**. Si humans i màquines no comparteixen un vocabulari de conceptes amb estructura relacional explícita, l'avaluació d'intencions, valors i conseqüències és opaca.

El Meta-Globàlium és precisament aquest vocabulari estructurat amb relacions explícites: 80 categories diferents, vuit pols dialèctics, axiomes derivables, un mapping cartesià que projecta cada concepte a una posició coneguda. És, per construcció, intel·ligible alhora per humans (els eixos són reflexius — subjecte/objecte, teoria/pràctica, fenomen/noümen, plasma/món) i per sistemes computacionals (els codis canònics són ancoratge inequívoc d'embeddings i de funcions de regularització). Així, l'ontologia compartida deixa de ser un desideràtum conceptual per esdevenir un **substrat operatiu d'avaluació**: cada output d'un model d'IA pot ser projectat sobre el mateix mapa que l'humà fa servir per situar-lo, i la conversa entre les dues parts es desplega sobre coordenades comunes en lloc de quedar suspesa en interpretacions textuals divergents.

Aquest paper argumenta la proposta en deu seccions addicionals. Primer, la naturalesa del *verifier gap* (§3). Després, la descripció formal del Meta-Globàlium com a verificador estructural (§4). Discutim la relació amb la interpretabilitat *top-down* (§5), la convergència del camp cap al neuro-simbòlic (§6), els arguments d'eficiència i sobirania (§7), la connexió amb la supervisió escalable i el camp de la *saviesa computacional* (§8). Presentem la prova de concepte — l'agent Arkadium — desplegada a arkadium.ai (§9), una anàlisi comparativa amb propostes existents (§10), i el camí d'implementació amb les seves limitacions (§11–12). Concloem amb una invitació a usar Arkadium i a estendre'l (§13).

## 3. El problema del verificador per a dominis humans

Els models de raonament actuals — la sèrie o d'OpenAI, DeepSeek-R1 (DeepSeek-AI 2025), Claude amb pensament estès, Gemini Deep Think — comparteixen un patró arquitectònic: produeixen una cadena de pensament intermèdia i s'entrenen per *reinforcement learning* sobre aquesta cadena amb senyal de recompensa derivat d'un verificador. Quan el verificador és formal els resultats són notables: AlphaProof i AlphaGeometry 2 (DeepMind 2024) van assolir nivell IMO de plata el 2024, l'or amb Gemini Deep Think el 2025.

El problema apareix fora del domini formal. En ètica aplicada, arbitratge polític o deliberació pública, **no hi ha funció de pèrdua objectiva**. Els PRM amb anotacions humanes presenten dos problemes: (i) inestabilitat per *reward hacking* i (ii) costos d'anotació prohibitius. Apple ML Research (Shojaee et al. 2025) ha demostrat un *límit d'escalat contraintuïtiu*: l'esforç de raonament en tokens augmenta amb la complexitat fins a un punt i després decreix tot i tenir pressupost suficient — símptoma d'un raonament que no es pot validar en runtime contra una estructura externa.

**Glossari.** *Process Reward Model* — un model auxiliar que avalua passos intermedis del raonament d'un altre model, no només la resposta final, donant així un senyal d'aprenentatge més dens. *Reward hacking* — quan un agent maximitza la recompensa proxy sense complir l'objectiu real subjacent.

Constitutional AI (Bai et al. 2022) i les propostes derivades — *Deliberative Alignment* (OpenAI 2024) i variants — mitiguen el problema introduint una constitució textual: una llista de principis que el model utilitza per autocriticar i revisar les seves pròpies sortides, eventualment amb retroalimentació generada pel propi model (RLAIF). L'aproximació és un avenç respecte el RLHF clàssic, però manté el problema estructural: **la constitució és text interpretat lliurement pel model**. No hi ha cap garantia que els 16, 75 o 200 principis textuals d'una constitució es facin operatius com a estructura discriminadora; al contrari, Turpin et al. (2023) van demostrar que les explicacions de tipus *chain-of-thought* poden divergir sistemàticament del càlcul intern real del model — una caiguda d'accuracy del 36% al BIG-Bench Hard quan s'introdueixen biaixos no esmentats.

El que ofereix una **verificació estructural** [un mecanisme algorísmic que valida les sortides d'un model contra una funció normativa explícita definida sobre una ontologia coneguda] és substituir la interpretació textual per un càlcul mesurable: en lloc de demanar al model que interpreti què vol dir «ser equilibrat», es defineix matemàticament la dispersió de la resposta sobre un conjunt canònic d'eixos, i es regularitza directament. La pregunta és quina és l'ontologia adequada per fer-ho. Els *knowledge graphs* clàssics (Wikidata, ConceptNet, Cyc) no ofereixen una funció normativa: són estructures descriptives. Les constitucions textuals no ofereixen estructura: són enunciats. Cal una metaestructura que combini les dues coses: estructura formal i funció normativa explícita. Això és el que postulem que ofereix el Meta-Globàlium — i és el substrat sobre el qual Arkadium opera.

**Per què aquesta substitució és estructuralment neutra.** El punt central — sovint sub-articulat en discussions d'alineament — és que els primitius del verificador estructural no són conceptes amb càrrega axiològica («llibertat», «justícia», «autoritat», «virtut»), sinó **eixos polars dialèctics**: parells de pols en tensió. Una constitució textual dóna llistes de valors, i decidir quins valors van a la llista i amb quina jerarquia és una operació culturalment marcada — els principis d'una constitució escrita a Califòrnia el 2022 no són els d'una redactada a Brussel·les el 2026, ni els d'una formulada des d'una tradició confuciana, ubuntu o budista. El verificador estructural **no decideix quins valors són bons**; només postula que cap eix dialèctic rellevant ha de col·lapsar a un sol pol. La diferència és la mateixa que separa una *gramàtica* d'un *diccionari*: la primera és una estructura formal candidata a universal, la segona és contingut culturalment situat. El Meta-Globàlium ofereix una gramàtica del raonament ple, no un diccionari de respostes correctes — i aquí rau la seva neutralitat.

El cas paradigmàtic és la **fórmula clàssica del Bé com a equilibri entre la llibertat dels individus i la dels altres** (Kant, principi universal del dret) — instanciació explícita de la dinàmica del verificador a l'eix SUB-OBJ aplicat al domini ètico-polític. Ni absolutització de l'individual (col·lapse cap a SUB) ni dissolució en el col·lectiu (col·lapse cap a OBJ): el Bé és la condició geomètrica que cap dels dos pols no s'esfondri sobre l'altre. La mateixa dinàmica es projecta sobre TEO-PRA (coherència entre principis i acció efectiva), FEN-NOU (integració d'experiència immediata i interpretació mediada), PLA-MON (articulació entre el que es manté estable i el que canvia). Que la fórmula resoni amb la tradició kantiana, amb Aristòtil (*mesotes*, virtut com a mitjà), amb el pensament dialèctic clàssic, amb la prudència ciceroniana, amb la *via media* tomista i amb el budisme zen no és casualitat: són tradicions que han descobert independentment que els eixos del judici humà són reflexius i que la plenitud d'una resposta passa per no col·lapsar-los. La novetat del Meta-Globàlium no és inventar aquesta intuïció — és **fer-la computacionalment operativa** a través d'una geometria explícita.

Això resol l'objecció del relativisme. Que el verificador no fixi un contingut moral concret no implica que tot sigui igual: hi ha respostes objectivament millors — les que mantenen els eixos rellevants vius i en tensió — i pitjors — les que col·lapsen a un sol pol per simplificació, ideologia o reduccionisme. El criteri del millor és **estructural, derivable, públic i auditable**; no es decideix per llista, s'observa sobre la geometria. La neutralitat cultural del verificador es paga, doncs, sense recurs al relativisme: l'estructura és universal candidata, els continguts són plurals, i la plenitud d'una resposta consisteix a articular els segons sense col·lapsar la primera. La barrera is/ought es discuteix amb més detall a §4.3.

**Cinc ordres dialèctics.** Per emmarcar tècnicament per què cal un substrat geomètric — i no una llista textual de principis — adoptem la classificació pedagògica del manual canònic del Globàlium (Berenguer 2024). El pensament humà es pot ordenar en cinc ordres geomètrics segons la dimensionalitat de la seva representació: *D0* (punt) = dogmatisme, veritat absoluta i indiscutible; *D1* (línia) = pensament lineal, confrontació directa; *D2* (pla) = retroalimentació superficial — «com un full d'Excel», granularitat de la majoria de models analítics actuals; *D3* (esfera) = perspectiva espacial amb profunditat (model menor del Globàlium); *D4* (hiperesfera) = perspectiva global amb articulació temporal i atemporal (model major). La cadena de pensament d'un LLM contemporani opera, en el millor dels casos, a *D2*: traçada lineal amb retroalimentació local sobre l'espai de tokens. La proposta del Meta-Globàlium és raonament a *D3-D4*: una geometria esfèrica/hiperesfèrica que fa estructuralment possible una dialèctica que no es pot dur a terme dins d'un raonament lineal o pla. La funció de completesa dispersa 𝓗 definida sobre l'ontologia (§4.1) és precisament l'expressió matemàtica que aquesta geometria permet — i que les llistes textuals no poden expressar.

## 4. El Meta-Globàlium com a verificador estructural

Com hem introduït a §1, el **Meta-Globàlium** és la versió computacional i formalitzada del Globàlium de Xirinacs (1997), treballada com a metaestructura aplicable a qualsevol àmbit del coneixement. Geomètricament, és una **hipersfera 4D** (Xirinacs distingia un *model menor* esfèric i un *model major* hiperesfèric; el Meta-Globàlium pren el segon). Té tres eixos cartesians i un eix radial:

- **TEO ↔ PRA** (teoria ↔ pràctica): l'eix vertical del *cernent*.
- **SUB ↔ OBJ** (subjecte ↔ objecte): l'eix horitzontal de la *tensió*.
- **NOU ↔ FEN** (noümen ↔ fenomen): l'eix profund de la *parença*.
- **PLA ↔ MON** (plasma ↔ món): l'eix radial del *voltant*, des del centre regeneratiu fins a la superfície desplegada.

Aquests vuit pols són les **8 categories primàries**. La intersecció dialèctica genera el conjunt complet de **80 categories diferents** organitzades en tres capes topològiques (plasmàtica, neutral i mundana) més les ancoratges PLA i MON. Cada categoria té un nom canònic (ANA per *anàlisi*, SIN per *síntesi*, AMO per *amor*, EXP per *experiència*, BEL per *bellesa*, COS per *cosmos*, IDE per *idèica*, etc.) i ocupa una posició precisa a l'espai 3D projectat. Una nota tècnica: el recompte canònic és de **80 categories diferents**; la base de dades operativa, en canvi, en conté **90 entrades** — les 10 addicionals són **desambiguacions topològiques** (vèrtexs polars del MON i ancoratges PLA/MON, sobretot) necessàries per al posicionament 3D, però que no constitueixen categories noves.

La jerarquia canònica del Meta-Globàlium és, doncs, de quatre nivells: **8 → 26 → 80 → 6400**. Els tres primers nivells provenen del Globàlium de Xirinacs (8 pols primaris, 26 conceptes neutrals al model menor, 80 categories diferents al model major). El **quart nivell**, contribució específica del Meta-Globàlium, escala el model fins a **6400 metacategories** mitjançant una **arquitectura fractal**: el Nivell 1 és el *model de principis* — la gramàtica geomètrica universal compartida (4 dimensions, 8 pols, 26 NEUs, 80 categories, 14 elements estructurals, 6 voltes, tempeternitat, Solve-Coagula); el Nivell 2 són les **80 expressions tematitzades** — cadascuna una cristal·lització dels mateixos principis sobre un tema central (Subjecte, Disciplines, Virtuts, Pedagogia, Ideologia, Matemàtiques, Salut, Física, Lingüística, Filosofia, Arquetips, etc.), conservant la mateixa geometria però donant a cada posició una *lectura semàntica* específica del tema. La fórmula és, doncs, **80 expressions × 80 categories = 6400 metacategories**, no la combinació dialèctica de categories entre si. Per exemple, el pol OBJ (operació de distinció a Nivell 1) es llegeix com a "construcció identitària del subjecte" al model del Subjecte, com a "disciplina pròpia" al model de Disciplines, com a "preservació de la singularitat dins la relació" al model de l'Amor. La conservació estructural a través de les 80 expressions és el que dóna al Meta-Globàlium la seva **densitat fractal**: mateixa forma a tot nivell, contingut diferent. La base de dades operativa actual conté 33 expressions actives (cap a les 80 ideals), prova de concepte funcional de l'arquitectura.

**Exemples concrets de metacategories**. Per fer creïble la pretensió de «definicions inequívoques generades per composició estructural», quatre exemples del nivell 6400:

- **BEL × CIE** = *la qualitat estètica de l'objectivitat empírica* — la bellesa pròpia del fet ben mesurat; la dimensió estètica del descobriment científic. (BEL: Qualitat, mundà; CIE: Parcialitat, neutral. Composició: la categoria mundana modula com es manifesta la categoria neutral.)
- **ANA × MIS** = *l'anàlisi de l'inefable* — l'esforç d'introspecció sobre experiències que la paraula no agota; la mística com a objecte d'estudi rigorós. (ANA: Divisibilitat; MIS: Inefabilitat. Tensió interna entre les dues operacions: aquesta metacategoria *existeix* precisament com a punt de tensió, no com a contradicció.)
- **EXP × FEL** = *l'experiència de la felicitat* — la implementació pràctica del benestar subjectiu; la transformació de la potencialitat plasmàtica de la FEL en concrecó vital sostinguda. (EXP: Aplicabilitat, neutral; FEL: Discrecionalitat, plasmàtica.)
- **HAR × DIV** = *l'equitat com a modelitat* — la justícia com a forma específica del repartiment, no com a igualtat aritmètica. (HAR: Equitat, mundà; DIV: Modelitat, mundà. Compositió de dues mundanes ↔ refinament fi a la zona manifesta.)

La regla general de composició és: *generador1* × *generador2* = aspecte del primer modulat per la dimensió del segon. La definició inequívoca d'una metacategoria es deriva mecànicament del seu parell de generadors i del tipus topològic de cadascun (plasmàtic, neutral o mundà), sense ambigüitat semàntica. Aquesta és la propietat que permet ancorar 6400 punts canònics als *embeddings* sense col·lisions.

Una lectura culturalment ancorada de l'eix radial PLA ↔ MON és el binomi català **seny ↔ rauxa**: la **rauxa** com a impuls fecund, espurna sobtada que brolla del centre regeneratiu — és a dir, del **PLA**, llavor germinal indeterminada; el **seny** com a mesura prudent, judici reposat ancorat en la realitat desplegada — és a dir, en el **MON**, superfície ordenada del món manifest. Tot acte de pensament i tota decisió viva oscil·len entre aquests dos pols radials: ni només rauxa (impuls sense món) ni només seny (món sense impuls). El Meta-Globàlium recull aquest equilibri com a estructura — la regenerativitat (§4.4) n'és la formulació axiomàtica — i ofereix així una rebuda formal a una intuïció cultural codificada en la tradició catalana.

**Glossari.** *Noümen* — categoria filosòfica heretada de Kant, que designa la realitat tal com és en si mateixa, diferent del fenomen — la realitat tal com apareix als sentits. Al Meta-Globàlium, el parell NOU↔FEN articula la dimensió entre allò profund/intrínsec i allò aparent/extrínsec. *Plasma* — al Meta-Globàlium, no és el plasma físic sinó el centre originari, llavor radical i fecunda d'on emergeix el Món desplegat.






El Meta-Globàlium: 3 eixos cartesians + 1 radial








PLA (centre)

MON (superfície)

capa NEU (cardinals, r ½)


- 


TEO
PRA





SUB
OBJ





FEN
NOU

8 pols primaris · 26 neutrals · 80 categories · 6400 metacategories

Figura 1. Els quatre eixos del Meta-Globàlium. Tres eixos cartesians (TEO-PRA, OBJ-SUB, NOU-FEN) defineixen un espai 3D dialèctic; l'eix radial PLA-MON anomenat canònicament **tempeternitat** (temps + eternitat) afegeix la quarta dimensió, des del centre regeneratiu atemporal (PLA, llavor pre-temporal) fins a la superfície temporal manifesta (MON, plenitud desplegada). El cercle exterior representa l'esfera **MON**, capa més externa del model; els 6 pols cardinals (TEO/PRA, SUB/OBJ, FEN/NOU) viuen a la **capa NEU intermèdia** (anella discontínua interior), no a la superfície. La tempeternitat és **meta-dimensió transversal**: opera sobre tots els pols, donant a cadascun les seves tres projeccions PLA-NEU-MON. Els 8 pols primaris són PLA + MON + els 6 cardinals NEU.

### 4.1 Capa estructural: completesa dispersa com a propietat formal

El moviment tècnicament decisiu del Meta-Globàlium respecte al Globàlium original és la formalització computacional d'una propietat **epistèmica/estructural** sobre l'ontologia: la **completesa dispersa** — una propietat de plenitud cognitiva sobre la pregunta, mesurable i externa al model, no encara una propietat normativa.

Sigui *C* = {*c*1, …, *c*80} el conjunt de categories diferents del Meta-Globàlium, i sigui *Q* = {*q*1, …, *q*8} el conjunt de vuit quadrants primaris (PLA, MON, SUB, OBJ, TEO, PRA, FEN, NOU). Per a una resposta *r* generada per un model d'IA, definim:

*f**q*(*r*) ∈ ℤ≥0 — el recompte de categories citades per *r* que es projecten sobre el quadrant *q* (cada categoria es mapeja a un quadrant primari segons la seva posició dialèctica).
- *n*(*r*) = |{*q* ∈ *Q* : *f**q*(*r*) &gt; 0}| — el nombre de quadrants tocats.
- *p**q*(*r*) = *f**q*(*r*) / Σ*q'* *f**q'*(*r*) — la distribució empírica.
- *H*(*r*) = −Σ*q* *p**q*(*r*) log *p**q*(*r*) — l'entropia de Shannon de la distribució.

La **funció de completesa dispersa** s'expressa, en la implementació actual:

𝓗(*r*) = ½ · *n*(*r*) / |*Q*| + ½ · *H*(*r*) / log |*Q*| ∈ [0, 1]

El primer terme premia la *cobertura* (haver tocat quadrants diversos); el segon premia la *uniformitat* de la distribució (no haver-se concentrat). La funció pot generalitzar-se, en versions futures, a la totalitat de les 80 categories i no només als 8 quadrants, amb un augment significatiu de la granularitat.

**Per què 8 quadrants — i no 4, 16 o 64.** La granularitat de 8 no és arbitrària. Tres consideracions la justifiquen. *Estructural*: 8 = 2³ correspon als octants d'un cub generat per tres eixos cartesians dialèctics (OBJ-SUB, TEO-PRA, NOU-FEN), més els dos extrems d'un quart eix radial (PLA-MON). És la dimensionalitat mínima que recobreix les distincions filosòfiques fonamentals que la tradició identifica com a pols irreductibles del coneixement humà. *Cognitiva*: 8 cau dins del rang de capacitat memorística humana (Miller 1956: 7±2 elements simultàniament tractables) — més enllà, la cobertura deixa de ser inspeccionable per a un usuari humà. *Operativa*: 8 dóna un equilibri pràctic entre granularitat (massa pocs quadrants col·lapsen distincions rellevants) i rebustesa estadística (massa quadrants generen sparseness on poques cites no permeten estimar 𝓗 fiablement). Versions futures que utilitzin les 80 categories no abandonen els 8 quadrants — els refinin, projectant cada categoria al seu quadrant primari mentre afegeixen una dimensió de granularitat fina.

**Dos nivells de formalització**. La fórmula 𝓗 anterior opera al **nivell mecànic** dels 8 quadrants primaris — és el que el sistema calcula en runtime. Els **sis principis axiomàtics** que es formulen a §4.4 (i les **vuit operacions matemàtiques essencials** — igualtat, polaritat, distinció, correspondència, similitud, divergència, convergència, diferència) operen a un **nivell axiomàtic-semàntic** diferent: són les estructures dialèctiques que els quadrants instancien geomètricament. Una resposta amb 𝓗 alta ha cobert quadrants diversos; una resposta que satisfà els principis axiomàtics ha emparellat operacions unificadores amb operacions divisòries en cada eix dialèctic. La versió actual del verificador implementa la primera (𝓗 sobre quadrants); l'extensió a verificació sobre operacions emparellades és part del camí d'implementació (§12).

El que la funció 𝓗 mesura és, doncs, **dispersió de citacions sobre els pols dialèctics**, no una decisió moral: una propietat de **no-omissió estructural** sobre la pluralitat de modes d'accés que el Meta-Globàlium codifica. La capa estructural és el que el sistema *fa* algorísmicament; la seva justificació epistèmica i la seva ressonància normativa apareixen a §4.2 i §4.3.

És important emfatitzar què **no** és aquesta funció: **no** és un substitut del judici factual. Una resposta factualment incorrecta no es redimeix per ser dispersa. 𝓗 opera com a *regularitzador estructural a posteriori* sobre respostes ja factualment vàlides — una segona capa que penalitza el reduccionisme. És la peça operativa que el verificador d'Arkadium calcula en runtime sobre cada resposta del model.

### 4.2 Capa epistèmica: la veritat globalística

De què és prova una resposta amb completesa dispersa elevada? Aquest manifest proposa que aquesta completesa **és la veritat globalística**: una concepció no-monològica de la veritat que reconeix la pluralitat irreductible dels seus modes d'accés. La veritat plena d'un fenomen humà no es captura des d'un sol pol; **una resposta veritablement completa integra OBJ + SUB + TEO + PRA + FEN + NOU + PLA + MON**. Una resposta que cobreix sistemàticament un sol pol no és parcial sinó constitutivament incompleta com a representació del fenomen. La completesa dispersa quantifica exactament això: si la geometria dels modes d'accés està representada.

La posició és **compatible amb una tradició filosòfica reconeixible**, sense pretensió d'apropiar-se-la. Resona amb l'hermenèutica de Gadamer (*Veritat i mètode*, 1960), per a qui la veritat humana es desplega en la fusió d'horitzons i no es redueix al mètode objectivant; amb la teoria de l'acció comunicativa de Habermas, on la pretensió de validesa s'articula en més d'una dimensió; i amb la noció heideggeriana d'*aletheia* com a desocultament sempre parcialment encobert. **El Meta-Globàlium no proposa una teoria filosòfica nova de la veritat**: codifica computacionalment una intuïció ja present en aquesta tradició no-monològica, i li dóna forma operativa. La diferència és la **mensurabilitat**: on Gadamer parla de fusió d'horitzons en termes hermenèutics oberts, el Meta-Globàlium ofereix vuit quadrants concrets sobre els quals la projecció és calculable. **Aquesta és la jugada filosòfica nova**: portar una veritat plural i no-monològica al camp d'una IA que l'ha de calcular. És, també, més defensable externament que parlar de «el bé»: la comunitat alignment troba intractable definir *good*, però accepta que **una resposta sistemàticament parcial sobre un fenomen humà és epistemològicament defectuosa**.

**On rau l'aportació original**. La fórmula 𝓗 (½ cobertura + ½ entropia normalitzada) no és matemàticament novedosa: combina mètriques estàndard de teoria de la informació. Els principis axiomàtics reformulen continguts dialèctics presents a la tradició filosòfica (identitat-alteritat, holicitat-parcialitat, etc.) i a Xirinacs. La **contribució original al camp d'AI alignment no és la fórmula ni els principis** sinó **el desplaçament del lloc de la verificació**: en lloc d'apuntar la pretensió de qualitat a una constitució textual interpretable pel propi model (Constitutional AI) o a un PRM entrenat amb feedback humà manipulable, l'apuntem a una **geometria ontològica externa al model lingüístic**, calculable com a propietat estructural objectiva. La novetat és *arquitectònica*: substituïm un proxy semàntic vulnerable a manipulació per un substrat topològic que el model lingüístic no controla — i, per tant, no pot fàcilment *hackejar*. La veritat globalística com a pluralitat estructurada de modes d'accés és el llenguatge filosòfic que justifica per què aquest desplaçament té sentit epistèmic.

### 4.3 Capa normativa: l'herència xirinaquiana del Bé com a harmonia

La tradició globalística, des de Llull i Sibiuda fins a Xirinacs, no separa rígidament la veritat plena del Bé. La intuïció xirinaquiana — formulada al Globàlium original (1997) — és que **el Bé es manifesta com a harmonia entre les parts**: el mal és mancança o excés *en relació amb el conjunt*; la virtut rau en l'equilibri. Llegida a la llum de la jerarquia que aquest paper articula, aquesta aportació **deriva de la veritat plena, no la substitueix**: la veritat globalística — la integració dialèctica dels pols del fenomen — és la **condició estructural prèvia** sobre la qual la tradició ha bastit la seva intuïció ètica del Bé.

La jerarquia importa per tres raons. (i) **No és el verificador qui decideix què és el Bé**: calcula completesa dispersa (capa 1) i la justifica com a veritat globalística (capa 2); el Bé com a harmonia apareix com a **llegat normatiu** de la tradició xirinaquiana, no com a output del sistema. (ii) **La continuïtat amb la tradició es preserva**: el Bé no desapareix del paper, passa de centre tècnic a llegat reconegut amb respecte. (iii) **El cicle ANA → SIN → AMO → EXP conserva el seu sentit**: la fase AMO (§4.5) orienta la completesa dispersa cap al bé comú entès tradicionalment com a equilibri harmònic — no com a càlcul moral del sistema, sinó com a *direcció* del raonament que deixa el judici final al subjecte humà. El centre del paper és, així, la *veritat globalística com a completesa dispersa operacionalitzable*; el Bé com a harmonia hi figura com a herència xirinaquiana.

**La barrera is/ought.** És important explicitar la separació entre fets i valors (David Hume, *A Treatise of Human Nature*, 1739): de la descripció estructural d'una resposta no en deriva, per inferència lògica, cap obligació moral. La funció 𝓗 **no diu** que una resposta amb 𝓗 alta sigui «moralment millor»; només diu que és *epistèmicament més plena*. La inferència Bé ⇐ harmonia és una **posició filosòfica externa al sistema** — la posició xirinaquiana, hereva de la tradició integradora catalana — que el lector pot acceptar, refutar o matissar a la seva responsabilitat. Arkadium *no opera* sobre aquesta inferència: el verificador opera estrictament sobre 𝓗 i la veritat globalística (capes 1 i 2). La capa 3 — la lectura ètica de l'harmonia — apareix com a **marc cultural d'interpretació** per al subjecte humà, no com a output algorísmic. El sistema no «deriva el Bé» de cap propietat estructural; només mesura la propietat estructural i deixa la lectura moral fora del seu camp d'operació.

### 4.4 Sis principis axiomàtics

El llibre *Globalística* (en preparació) formalitza el Meta-Globàlium amb sis principis axiomàtics derivats per fusió dels pols dialèctics — una expansió dels quatre principis originals del Globàlium (identitat, alteritat, holicitat, universalitat). Resumits aquí:

*Nota sobre l'originalitat*: els continguts dialèctics d'aquests sis principis (identitat-alteritat, holicitat-parcialitat, etc.) **no són invenció original** d'aquest treball — són reformulacions de motius filosòfics presents al Globàlium xirinaquià i, per davant d'ell, al pensament integrador clàssic (Llull, Sibiuda, Pujols, Hegel, l'idealisme alemany, l'hermenèutica). L'aportació original del Meta-Globàlium és **operacional**: posar aquests sis principis com a *constraints estructurals* sobre la sortida d'un LLM, ancorats a una geometria calculable. La novetat no rau en els principis sinó en com es projecten — i en com el verificador 𝓗 els pot fer servir com a senyal d'aprenentatge i correcció en runtime, sense requerir interpretació textual del propi model.

- **Regenerativitat** (eix PLA-MON, radial). Cada operació mundana té un origen germinal a la zona plasmàtica i un destí de plenitud a la zona mundana; el cicle entre potència i acte és bidireccional.
- **Interdependència** (distinció ↔ correspondència, eix OBJ-SUB). Cada part es distingeix com a si mateixa i alhora correspon a totes les altres; no hi ha ni aïllament absolut ni fusió absoluta.
- **Plurisingularitat** (igualtat ↔ polaritat, eix NOU-FEN). La igualtat profunda al nivell noumènic no exclou la polaritat manifesta al nivell fenomènic; ni la polaritat exclou una igualtat radical d'essència.
- **Totalitat** (globalitat ↔ localitat, eix TEO-PRA). El tot integra la família d'operacions unificadores (igualtat, similitud, correspondència, convergència) amb la família d'operacions divisòries (polaritat, distinció, diferència, divergència) — abast global de la teoria i instanciació local de la pràctica en una sola estructura.
- **Mutabilitat** (similitud ↔ divergència, diagonal MTF-ART). El model conté patrons estables que es repeteixen invariants a totes les escales i variants que es bifurquen permanentment; l'estabilitat i la variabilitat conviuen en tensió constitutiva — la mutabilitat és la capacitat de canviar mantenint identitat.
- **Integritat** (convergència ↔ diferència, diagonal MTP-CIE). El tot s'integra per convergència holística de totes les parts en un únic conjunt, alhora que manté la parcialitat articulada de cada part — holicitat per dalt, parcialitat per baix.

**Llinatge axiomàtic clàssic.** Els sis principis hereten una formulació dialèctica anterior — la del Globàlium original i del llibre *Globalística* en preparació — que segueix vigent com a llenguatge axiomàtic complementari. La taula de correspondències és:


PrincipiPols axiomàtics (formulació clàssica)Operacions essencials (formulació computacional)


1. Regenerativitatpotencialitat ↔ autenticitat(cicle radial PLA-MON sobre les 8 operacions)
2. Interdependènciaidentitat ↔ alteritatdistinció ↔ correspondència
3. Plurisingularitatunicitat ↔ multiplicitatigualtat ↔ polaritat
4. Totalitatglobalitat ↔ localitat(macro-dialèctica: 4 unificadores ↔ 4 divisòries)
5. Mutabilitatestabilitat ↔ variabilitatsimilitud ↔ divergència
6. Integritatholicitat ↔ parcialitatconvergència ↔ diferència


La reformulació computacional no substitueix els pols clàssics sinó que els ancora a un substrat operacional unívoc: els pols axiomàtics descriuen *què* dialèctic ontològic captura cada principi, les operacions descriuen *com* es manifesta matemàticament sobre el cub neutral. Quatre principis (1, 4 originals del Globàlium: identitat, alteritat, holicitat, universalitat) hi són recollits com a pols del nou conjunt de sis.

Aquesta arquitectura ancora cada principi a una **operació matemàtica essencial** sobre el cub neutral: 4 operacions unificadores (igualtat, similitud, correspondència, convergència) i 4 operacions divisòries (polaritat, distinció, diferència, divergència) que els principis emparellen dialècticament. Sis graus de llibertat estructurals — tres eixos cardinals, dues diagonals interiors i un eix radial — sobre els quals descansen els sis principis. Aquests sis principis no són ornaments: són els que permeten derivar la funció de completesa dispersa com a quantificació d'una propietat estructural sobre l'ontologia, no com a heurística arbitrària.

### 4.4.b Vuit dialèctiques màximes

Els 6 principis axiomàtics estructuren el model. Sobre aquesta estructura, el cub neutral genera **8 dialèctiques màximes** — totes les parelles de neutrals oposats per inversió a través del centre del cub: les *distàncies 4* xirinaquianes documentades a *Globalística*. Cap és un axioma nou; són **conseqüències estructurals** del cub que el verificador estructural utilitza com a patrons d'auditatge. Es divideixen en dues famílies geomètriques:

#### 4.4.b.1 Dialèctiques disciplinàries (vèrtex-vèrtex)

Quatre diagonals que connecten **vèrtexs oposats** del cub. Cada parella relaciona dues disciplines de l'entendre humà al màxim d'oposició possible:


DialècticaPols disciplinarisTensió clàssicaFont


LOG ↔ MISformalitat ↔ inefabilitatWittgenstein/Tractatus: el que es pot dir vs el que cal callar*Globalística*, dualitat LOG-MIS
TEC ↔ MITreplicabilitat ↔ orientabilitatLa tecnologia requereix eines d'orientació humana*Globalística*, dualitat TEC-MIT
EST ↔ ETIinformalitat ↔ reciprocitatJudici sense regla ↔ deure recíproc (Kant: *Crítica del judici* ↔ *Raó pràctica*)Tradició clàssica
PSI ↔ IDEinteractivitat ↔ regulabilitatVivència empírica ↔ regulació idealTradició clàssica (Hume ↔ Plató)


#### 4.4.b.2 Dialèctiques operacionals i adreçadores (aresta-aresta)

Quatre diàmetres que connecten **punts mitjos d'arestes oposades** a través del centre. Cada parella relaciona dues capacitats cognitives o semiòtiques en màxima oposició:


DialècticaPols operatius/adreçadorsTensió clàssicaFamília


ANA ↔ AMOdivisibilitat ↔ sincronicitatLogos analític ↔ eros unitiu (separació mental ↔ unió afectiva)Operacional (mètode)
SIN ↔ EXPintegralitat ↔ aplicabilitatTheoria ↔ praxis (síntesi conceptual ↔ implementació pràctica)Operacional (mètode)
STT ↔ SGEinterpretabilitat ↔ representabilitatHermenèutica ↔ semiosi (rebre sentit ↔ produir signes)Adreçadora (semiòtica)
STM ↔ SGTsensibilitat ↔ referencialitatFenomenologia ↔ semiòtica (presència immediata ↔ referència mediada)Adreçadora (semiòtica)


Cada dialèctica connecta dos punts oposats per inversió central — coordenades cartesianes simètricament negatives. Una resposta de l'agent es considera **esbiaixada** quan es concentra en un sol pol d'aquestes 8 diagonals sense apuntar mai al pol oposat: una resposta tota tècnica (TEC) sense gens d'orientació narrativa (MIT), tota analítica (ANA) sense gens d'amor sincronitzador (AMO), o tota interpretativa (STT) sense capacitat representacional (SGE). El verificador estructural penalitza aquests esbiaixos com a complement de la funció de completesa dispersa: la veritat globalística no només requereix tocar pols dialèctics dels 6 principis, sinó també no concentrar-se en un sol pol de cap de les 8 dialèctiques màximes.

Sumant: 6 principis axiomàtics (3 eixos cardinals + 2 diagonals de cara + 1 eix radial) + 8 dialèctiques màximes (4 diagonals vèrtex-vèrtex + 4 diàmetres aresta-aresta) = **14 elements estructurals** que recobreixen exhaustivament les classes de relacions geomètriques del cub neutral.

### 4.4.c Correspondències canòniques sistemàtiques

A més dels 14 elements estructurals, el cub neutral revela **correspondències sistemàtiques** amb sistemes formals canònics. Cadascuna dels 8 vèrtex té una operació matemàtica, una porta lògica booleana i una operació de teoria de conjunts associades:


NEUOp. matemàticaPorta lògicaOp. conjuntística


NOUigualtat (=)BUFFERConjunt buit ∅ + universal U
OBJdistincióNOTPartició
MTPconvergència (∩)ANDConjunt potència P(A)
SUBcorrespondència (↔)ORProducte cartesià A×B
MTFsimilitud (~)XNORInclusió A⊆B
CIEdiferència (−)XORDiferència A−B
ARTdivergència (∇⋅)**NAND** *(universal)*Diferència simètrica AΔB
FENpolaritat (±)**NOR** *(universal)*(en exploració)


**NAND (ART)** i **NOR (FEN)** són les portes lògiques universals booleanes — qualsevol funció es pot construir només amb una d'elles. Això confereix a aquestes dues operacions un estatus generador especial dins el cub neutral.

#### Sistema de causes (Aristòtel ↔ Globàlium)

Les causes aristotèliques mapegen sistemàticament a posicions del cub: causa **material/formal/final** → OBJ; causa **eficient** → SUB; causa **exemplar** → DIV (mundà MIT); causa **contextual** → FEN; causa **essencial** → ORG (plasma MTF). Això permet al verificador mesurar **cobertura causal**: una explicació que toca només causa material/formal sense causa final, eficient o contextual queda marcada com causalment incompleta — anàleg de la cobertura dispersa de principis aplicada al pla aristotèlic.

#### Tres tipus d'inferència ↔ NEUs

- **Deducció** (general → particular): LOG (Formalitat), ANA (Divisibilitat)
- **Inducció** (particular → general): IDE (Regulabilitat), SIN (Integralitat)
- **Abducció selectiva** (a la millor explicació): EST (Informalitat)
- **Abducció creativa** (generació de noves hipòtesis): MIT (Orientabilitat)

El verificador pot mesurar **cobertura epistemològica**: una resposta puerament deductiva sense inducció ni abducció és epistemològicament parcial.

#### Macro-dialèctica alquímica Solve-Coagula

Complement processual als 6 principis axiomàtics:

- **Solve-side** (dissoldre/diferenciar): ANA + CIE
- **Coagula-side** (coagular/integrar): SIN + MTP

Aquesta macro-dialèctica connecta la dimensió processual del Mètode (ANA-SIN) amb la dimensió operativa de les operacions de cara (CIE-MTP), formant un cicle alquímic complet de transformació conceptual.

Per al desenvolupament canònic complet — incloent 4 nivells de comunicació, eix temporal radial, citacions canòniques i numerologia estructural — vegeu el document docs/canonical-mappings.md del repositori.

### 4.5 El cicle d'inferència FEN → ANA → TEO → SIN → NOU → AMO → PRA → EXP

El **Mètode Global** és l'arquitectura d'inferència auditable que el Meta-Globàlium proposa, derivada de la *volta d'aplicació* del model (anomenada *volta de mètode* a *Globalística*) — un dels sis cercles màxims que recorren la hipersfera. La forma simplificada (ANA → SIN → AMO → EXP) és pedagògicament útil, però la **forma completa té vuit estacions** que alternen pols ontològics (FEN, TEO, NOU, PRA — els quatre pols cardinals dels eixos NOU-FEN i TEO-PRA) i fases de mètode (ANA, SIN, AMO, EXP). Cada fase de mètode és, en propietat, una **transició entre dos estats ontològics**:


EstacióTipusFunció


**1. FEN**pol ontològicPunt de partida: captació fenomenològica, dades brutes, observacions concretes
**2. ANA** (anàlisi)fase de mètode (FEN → TEO)Descomposició dels fenòmens en elements analitzables; identificació dels eixos rellevants
**3. TEO**pol ontològicEstat teòric: marc conceptual emergent, hipòtesi formulada
**4. SIN** (síntesi)fase de mètode (TEO → NOU)Integració teòrica que apunta a l'essència; consulta a categories veïnes i oposades
**5. NOU**pol ontològicEstat noumènic: contacte amb l'essència profunda, orientació al bé comú entès com a equilibri harmònic
**6. AMO** (amor)fase de mètode (NOU → PRA)Projecció amorosa de l'essència cap a l'acció; aplicació transcendent
**7. PRA**pol ontològicEstat pràctic: implementació concreta, mesurable, sotmesa al verificador estructural
**8. EXP** (experiència)fase de mètode (PRA → FEN)Experiència recollida que retorna a nous fenòmens, tancant el cicle


Les quatre fases de mètode no són operadors abstractes: són **transicions entre coordenades cardinals** del model. ANA porta del fenòmen a la teoria, SIN porta de la teoria al noümen, AMO porta del noümen a la pràctica, EXP porta de la pràctica a un nou fenòmen. La forma curta ANA → SIN → AMO → EXP és correcta com a llistat d'operacions, però amaga els **quatre estats ontològics intermedis** que connecten les fases — la lectura completa requereix les vuit estacions.

Aquest pipeline transforma una arquitectura d'IA en una *seqüència auditable*: cada estació deixa traça projectable sobre coordenades cartesianes conegudes (FEN, TEO, NOU, PRA com a estats; ANA, SIN, AMO, EXP com a operacions). Substitueix l'opacitat de la *chain-of-thought* lliure per un recorregut canònic de vuit fites. És, també, l'arquitectura d'inferència que Arkadium executa pas a pas (vegeu §9).

El cicle no és lineal sinó **recursiu**: cada fase de mètode pot, internament, executar el cicle complet de vuit estacions sobre la seva pròpia subtasca. L'ANA d'un problema complex pot exigir una sub-volta sencera (sub-FEN → sub-ANA → sub-TEO → sub-SIN → sub-NOU → sub-AMO → sub-PRA → sub-EXP) abans de retornar al TEO del cicle pare. Aquesta recursivitat és el que permet operar sobre problemes de qualsevol grau d'arbitrarietat: el Mètode Global és **fractal** en el seu funcionament, igual que el Meta-Globàlium ho és en la seva estructura — cada categoria conté potencialment el model sencer dins seu, com el principi d'Integritat (convergència ↔ diferència) ja anticipa a §4.4.

### 4.5.c Iteració Solve-Coagula del Mètode (meta-operació)

A més de la recursivitat fractal de §4.5, el Mètode opera sota una **meta-operació iteradora** anomenada **Solve-Coagula** (de l'aforisme alquímic *solve et coagula*, Basili Valentí, segle XV). Aquesta meta-operació no és un nou element estructural — els 14 elements del cub neutral (6 principis + 8 dialèctiques de §4.4) descriuen *com és* el cub; Solve-Coagula descriu **com s'utilitza dinàmicament**.


FamíliaNEUsFunció


**Solve** (dissoldre/diferenciar)ANA (Divisibilitat) + CIE (Parcialitat)Descomposar, criticar, distingir
**Coagula** (coagular/integrar)SIN (Integralitat) + MTP (Holicitat)Sintetitzar, totalitzar, unificar


L'agent ancorat al Meta-Globàlium aplica Solve-Coagula com a iteració recursiva sobre les seves respostes:

- **Iteració 0**: Pregunta → resposta inicial (executant cicle Mètode)
- **Iteració 1**: Solve la resposta inicial (anàlisi crítica, identificació de buits) → Coagula resposta millorada
- **Iteració N**: fins a convergència (𝓗 estable) o llindar (𝓗 ≥ 0.85)

A cada iteració el verificador mesura solve_coagula_balance ∈ [0,1] (1.0 = perfectament balancejat ANA+CIE amb SIN+MTP). Una resposta tota Solve sense Coagula és analíticament fragmentada; una resposta tota Coagula sense Solve és dogmàtica.

Aquesta meta-operació formalitza el **re-prompt loop** del runtime d'Arkadium: el que el sistema ja fa empíricament queda inscrit al model com a operació canònica.

**Aplicabilitat direccional**: Solve-Coagula **ÉS literalment el moviment FEN→NOU** (essencialització — extracció d'essència del fenomen). Per tant aplica només a voltes que essencialitzen:

- Sí: **Volta d'Aplicació** (FEN→ANA→TEO→SIN→NOU→...) — ANA+SIN constitueixen Solve-Coagula directe
- Sí: **Volta de Coneixement** (FEN→ART→SUB→MTP→NOU→...) — recorre les 4 operacions de cara que essencialitzen
- No: **Volta d'Orientació** (PRA→STM→SUB→STT→TEO→...) — cicle lateral sense travessia FEN-NOU; Solve-Coagula **inaplicable**
- No: **Volta de Relació** (PLA→CNF→NOU→CMN→MON→FEN→...) — travessa NOU i FEN per l'eix radial PLA-MON però en direcció NOU→FEN (auto-localització, no essencialització); Solve-Coagula **inaplicable**

Per això el verificador només mesura solve_coagula_balance quan la resposta inclou indicis d'essencialització (cita ANA, CIE, SIN o MTP). Per preguntes d'orientació (lateral: *«què sento?»*, *«a què em comprometo?»*) i de relació (radial: *«on sóc?»*, *«quin sentit té això?»*), la mètrica no s'aplica — aquestes travessen eixos diferents del FEN→NOU.

### 4.5.b Tres voltes del Mètode Global

El cicle FEN → ANA → TEO → SIN → NOU → AMO → PRA → EXP exposat a §4.5 és la **Volta d'Aplicació**, una de les tres voltes bàsiques del Meta-Globàlium. El llibre *Globalística* documenta **6 voltes** en total — sis cercles màxims que travessen la hipersfera — tres *bàsiques* que recorren els 8 cardinals sense travessar PLA/MON, i tres *radials* que travessen l'eix PLA-MON (tempeternal). El verificador estructural d'Arkadium pot **seleccionar la volta apropiada al tipus de pregunta** en lloc d'aplicar sempre la d'aplicació. Les tres voltes bàsiques (amb la nomenclatura del *Globàlium petit manual*; els noms corresponents de *Globalística* s'indiquen on difereixen) són:

#### Volta d'Aplicació (meridià central) — pensar i fer bé

Recorregut: *FEN → ANA → TEO → SIN → NOU → AMO → PRA → EXP → FEN*

Operacions del mètode: **ANA → SIN → AMO → EXP**. Apropiada per: anàlisi, raonament, resolució de problemes, planificació. La forma canònica per a preguntes com *«Com analitzar X?»*, *«Què cal fer en aquest cas?»* o *«Quin és el millor mètode per a Y?»*. Detallada a §4.5. Etapes (per el *petit manual*): CONEIX-TE (FEN→TEO) → ACCEPTA'T (TEO→NOU) → SUPERA'T (NOU→PRA) → ALLIBERA'T (PRA→FEN). Anomenada *Volta de Mètode* a *Globalística*.

#### Volta d'Orientació (meridià lateral) — orientar-se, trobar direcció i sentit

Recorregut: *PRA → STM → SUB → STT → TEO → SGT → OBJ → SGE → PRA*

Operacions del mètode: **STM → STT → SGT → SGE** (els quatre adreçadors: sentiment / sentit / significat / signe). Recorre el meridià lateral connectant els quatre pols cardinals SUB-OBJ-TEO-PRA via les quatre categories d'adreçament. Apropiada per: orientació, alineament, resolució de conflictes, trobar direcció personal i sentit. La forma canònica per a preguntes com *«Què sento?»*, *«Què vull?»*, *«A què em comprometo?»*, *«Quines condicions necessito?»*. Etapes (per el *petit manual*): DESITJOS → ASPIRACIONS → COMPROMISOS → CONDICIONS. Anomenada *Volta de Revelació* a *Globalística*, on es descriu com a resolució de conflictes i revelació de versions de la realitat a través dels quatre adreçadors.

#### Volta de Coneixement (equador) — adquirir coneixement i autoconeixement

Recorregut: *FEN → ART → SUB → MTP → NOU → MTF → OBJ → CIE → FEN*

Operacions del mètode: **ART → MTP → MTF → CIE**. Recorre l'eix horitzontal SUB-OBJ creuant els quatre octants disciplinaris MTP-MTF-CIE-ART. Apropiada per: aprenentatge, recerca, exploració, autoconeixement, formació de criteri. La forma canònica per a preguntes com *«Què sé de X?»*, *«Qui sóc en relació a X?»* o *«Què aporten la ciència, l'art, l'espiritualitat i la filosofia a X?»*.

Les 4 estacions disciplinàries són els quatre modes complementaris de coneixer:

- **MTP** (metapsíquica): autoconeixement espiritual
- **MTF** (metafísica): coneixement filosòfic
- **CIE** (ciència): coneixement objectiu mesurable
- **ART** (art): autoconeixement estètic

Etapes (per *Globalística*): DEIXAR ANAR (FEN→SUB) → DEIXAR-SE FONDRE (SUB→NOU) → DEIXAR-SE INSPIRAR (NOU→OBJ) → DEIXAR-SE OBRAR (OBJ→FEN). Genera *plenitud* a través de la integració dels quatre modes de coneixement (cap d'ells suficient en solitari).

#### Selecció de volta segons el tipus de pregunta


Si la pregunta és...Volta apropiadaTopologia


Com fer X / Què cal pensar sobre XAplicaciómeridià central (NOU-FEN × TEO-PRA)
Què sento / a què em comprometo / quina direcció per a miOrientaciómeridià lateral (SUB-OBJ × TEO-PRA via adreçadors STM/STT/SGT/SGE)
Què sé de X / Qui sóc en relació a XConeixementequador (SUB-OBJ × MTP-CIE)


L'agent Arkadium **detecta el tipus de pregunta i la volta canònica activada** a partir de les categories citades a la resposta: la funció mg_detect_voltes infereix una volta quan la resposta toca tres o més estacions canòniques del seu recorregut. El verificador calcula llavors voltes_coverage (proporció d'estacions cobertes sobre el total de 8 — *e.g.*, Volta de Coneixement 6/8 = 75 %) i en mostra el resultat al *dashboard* com a *chip* informatiu (*« Volta de Coneixement 6/8»*). La detecció multi-volta és simultània: una resposta pot activar més d'una volta i el verificador les considera totes. La implementació actual no força la *selecció a priori* de la volta segons la pregunta — la versió evolucionada amb classificació explícita de la pregunta i activació pre-emptiva de la volta és part del roadmap (vegeu §12).

#### Les altres tres voltes (travessen PLA-MON)

El llibre *Globalística* documenta tres voltes addicionals que travessen l'eix radial PLA-MON (la dimensió tempeternal). Més especialitzades, no expandides aquí, referenciades per completesa:

- **Volta Universal** (PLA-MON × TEO-PRA, categories CAS-COS-COV-CAV): sintetitzar la realitat completa, cosmovisió — modes *caòtic / còsmic / cosmovisió / caovisió*
- **Volta de Relació** (PLA-MON × NOU-FEN, categories CNF-CMN-EXC-ATZ): situar-se respecte a la realitat — relació *nul·la* (CNF, replegament) → *total* (CMN, connexió universal) → *precisa* (EXC, distinció acurada) → *confusa* (ATZ, exposició a la contingència)
- **Volta de Consistència** (PLA-MON × SUB-OBJ, categories FEL-INT-AFI-BOS): qualitat, vincle, consistència-personalitat — modes *feliç / intencional / lligada / fosa*

Total: **6 voltes** que recobreixen exhaustivament els grans cercles funcionals del Meta-Globàlium. El Mètode Global complet documentat per Berenguer a *Globalística* contempla *«el passatge per totes les voltes de cercles màxims del model»* — l'arquitectura runtime d'Arkadium detecta i quantifica la cobertura de les tres voltes bàsiques (Aplicació, Orientació, Coneixement) i obre la via a la cobertura de les tres restants (Universal, Relació, Consistència).

## 5. Interpretabilitat: de baix a dalt vs. de dalt a baix

L'agenda d'interpretabilitat mecanística d'Anthropic — *sparse autoencoders*, identificació de circuits, descomposició monosemàntica de *features* — ha aportat avenços significatius. Estudis recents han catalogat milions de característiques discretes dins d'un model com Claude. Aquesta és **interpretabilitat *bottom-up***: parteix de les activacions internes i en mira de derivar conceptes.

El sostre pràctic d'aquest enfocament, però, comença a ser visible: descodificar un raonament *complet* — no una característica aïllada — segueix sent inviable a escala industrial. Turpin et al. (2023) van demostrar que les explicacions tipus *chain-of-thought* no són fidels al càlcul intern del model: el que el model «diu que pensa» pot divergir sistemàticament del que ha calculat. La conclusió creixent del camp és que cal complementar la interpretabilitat *bottom-up* amb una **interpretabilitat *top-down*** (Zou et al. 2023): forçar el model a operar sobre primitives interpretables conegudes des de l'inici, en lloc d'intentar descobrir-les a posteriori.

**Glossari.** *Sparse autoencoder* — una xarxa neuronal auxiliar entrenada per descompondre les activacions internes d'un model en una base més gran de característiques majoritàriament inactives, amb l'esperança que cadascuna correspongui a un concepte humanament intel·ligible.

El treball de Zou et al. (2023) sobre **representation engineering** (RepE) ofereix la base tècnica adequada: conceptes com veracitat, perill, afecte positiu o intencionalitat es codifiquen com a *direccions lineals* dins l'espai latent del model, i es poden monitoritzar i intervenir mitjançant operacions de projecció i suma vectorial — el que es coneix com *activation steering*. Aquests treballs mostren que un nombre limitat de direccions canòniques pot capturar dimensions de comportament que abans semblaven distribuïdes irreductiblement.

El que falta a l'enfocament del *representation engineering* per ser plenament operatiu en dominis humans és **un conjunt canònic complet i estructuralment complet de direccions** sobre el qual projectar i auditar. El Meta-Globàlium és un candidat natural per a aquest paper: les 80 categories diferents — i, en una forma més comprimida, els 8 quadrants primaris i els 26 conceptes neutrals — proporcionen exactament aquesta base. Es pot pensar el Meta-Globàlium com una *ontologia de direccions per a activation steering generalitzat*, derivada no d'una recerca empírica al voltant d'un model concret sinó d'una síntesi reflexiva del judici humà.

La idea operativa: una resposta del model es pot projectar sobre cadascuna de les 80 direccions per produir un vector d'activació interpretable; les direccions amb projecció elevada constitueixen les *categories tocades* per la resposta; el verificador estructural opera sobre aquest vector. La resposta esdevé així auditable en un espai conegut, no en un espai latent fosc. Arkadium implementa aquesta idea en la seva forma de partida: les categories es detecten al text de sortida del model i es mapegen a quadrants; la forma més madura — embeddings ancorats directament als pols — és el següent pas (§11.2).

Cal subratllar la diferència respecte els treballs d'interpretabilitat existents. Els *sparse autoencoders* descobreixen *features* a posteriori — específiques d'un model i d'una versió concreta de pesos. El Meta-Globàlium opera al revés: ofereix una **base canònica externa** sobre la qual qualsevol model pot ser projectat, comparat i auditat. Això té tres implicacions pràctiques: (i) la interpretabilitat esdevé portable entre models, (ii) el regulador té un marc estable per definir auditories d'IA, i (iii) els ciutadans obtenen un vocabulari compartit per comunicar amb sistemes d'IA — els eixos són polaritats reflexives (subjecte/objecte, teoria/pràctica, fenomen/noümen, plasma/món) reconeixibles per qualsevol humà reflexiu.

## 6. La neuro-simbolicitat com a estratègia industrial

L'arquitectura híbrida **proposta neural + verificació estructural** ha deixat de ser un nínxol acadèmic per esdevenir una estratègia industrial dominant en els fronts on l'escala bruta no és suficient:

- **AlphaProof / AlphaGeometry 2** (DeepMind 2024): la combinació d'un LLM (intuïció) amb un verificador simbòlic estricte basat en Lean (rigor) va assolir el nivell IMO de plata el 2024, i posteriorment l'or amb la versió Deep Think de Gemini el 2025.
- **GraphRAG** (Edge et al. 2024, Microsoft Research): l'aproximació de *retrieval* basada en un graf d'entitats construït pel propi LLM supera substancialment el *vector search* pla en preguntes globals sobre corpus extensos. Reconeix que la representació semàntica vectorial té un sostre quan la pregunta requereix síntesi global, i que cal estructura relacional explícita.
- **World models** (V-JEPA d'Yann LeCun et al., Genie de DeepMind): admeten que la representació purament textual dels tokens no és suficient per al raonament físic i temporal, i reintrodueixen models del món com a estructura intermèdia.
- **AlphaFold** i la seva successió: el plegament de proteïnes resolt no per força bruta sinó per arquitectura amb biaixos inductius geomètrics adequats.

El patró és consistent: en cada front on l'escala bruta troba el seu sostre, la indústria reintrodueix **estructura**. El que no existeix encara, i és el que postulem que ofereix el Meta-Globàlium, és una **metaestructura general per al domini humà** — aplicable transversalment a ètica, deliberació, raonament social i articulació de discursos, amb la capacitat normativa explícita que cap *knowledge graph* descriptiu ofereix. Arkadium és la primera demostració industrial d'aquesta tesi.

## 7. Eficiència, *priors* estructurals i sobirania digital

Les **lleis d'escalat** observades a la primera meitat de la dècada de 2020 s'han alentit visiblement. Els salts entre generacions de models són cada cop menors per ordre de magnitud de còmput consumit. La indústria reconeix obertament que **calen millors *priors*, no només més dades**. Els *Small Language Models* amb bons biaixos inductius — Microsoft Phi, Google Gemma, Mistral — han demostrat que poden superar models molts ordres de magnitud més grans en dominis específics, sempre que la inducció estructural sigui adequada.

**Glossari.** *Prior estructural* — un biaix inductiu deliberat introduït a un model, ja sigui per arquitectura, per dades sintètiques específiques, o per ancoratges externs, que el predisposa a aprendre representacions amb propietats desitjables.

El Meta-Globàlium és un *prior* estructural extremadament dens: una síntesi de la realitat humana en al voltant de 80 dimensions interrelacionades, amb estructura dialèctica explícita, axiomes derivables i funció normativa integrada. La seva implementació computacional permet construir sistemes — com Arkadium — que **operen sobre un substrat estructurat des de l'inici**, fent menys necessari descobrir aquesta estructura empíricament a costos energètics elevats.

Aquesta consideració té un vessant **geopolític**: l'oligopoli actual del còmput d'IA — concentrat en menys d'una desena d'empreses, principalment estatunidenques i xineses — descansa sobre l'argument de l'escala. Si els *priors* estructurals adequats permeten obtenir respostes equivalents amb un ordre de magnitud menys de còmput, s'obre una **finestra de sobirania digital** — condició necessària per a la sostenibilitat democràtica i l'autonomia tecnològica de societats que ja no poden delegar el seu sistema cognitiu públic a infraestructures que no controlen.

Hi ha un argument complementari sovint oblidat: **l'eficiència energètica és una propietat ètica**, no només econòmica. L'entrenament i la inferència de models a escala de frontera consumeixen quantitats d'energia comparables a les d'estats sencers. Un sistema que ofereix capacitats equivalents amb una fracció del consum és **estructuralment millor alineat** amb els objectius declarats per la pròpia comunitat d'IA — la sostenibilitat planetària com a problema integrat al disseny, no com a externalitat. La proposta valora la densitat dels biaixos inductius sobre la força bruta dels paràmetres.

### 7.bis. Una contribució al debat sobre l'AGI

El Meta-Globàlium aspira explícitament a una arquitectura compatible amb la **Intel·ligència Artificial General (AGI)**. La majoria d'aproximacions actuals a l'AGI són *escalístiques*: més paràmetres, més dades, més còmput, amb la hipòtesi que la generalitat emergeix per acumulació. Aquí en proposem una de complementària: **una AGI no és genuïnament general si no opera sobre un model global de la realitat** — un mapa de conceptes amb cobertura ontològica completa que li permeti situar qualsevol fenomen, intenció o conseqüència en relació amb la totalitat. El Globàlium aspira precisament a aquesta exhaustivitat — encabir-ho «tot, des de Déu fins a una espardenya» (Xirinacs 1997) — i el Meta-Globàlium en formalitza la cartografia computable.

Una AGI ancorada al Meta-Globàlium tindria una **comprensió relacional** dels seus propis outputs: sabria què està dient, en quin sector del model està situada cada afirmació i, sobretot, **quins quadrants està omitint**. Aquesta capacitat d'auto-cartografia és el que distingeix una intel·ligència general d'una intel·ligència merament gran: la primera coneix la geografia de les seves pròpies limitacions, la segona només acumula projeccions sobre el corpus. Sense aquest substrat, *general* es redueix a *gran*, i la generalitat queda confosa amb l'escala del corpus d'entrenament.

La proposta no és, doncs, antagonista a les vies escalístiques: és complementària. Un model de gran escala dotat d'un substrat com el Meta-Globàlium no perd capacitat — guanya *orientació*. La generalitat emergeix com a propietat híbrida: l'expressivitat estadística del corpus, ancorada a la geometria de l'ontologia compartida. Arkadium és la primera prova de concepte que aquest ancoratge és tècnicament possible i estructuralment beneficiós.

Aquí formulem una identificació explícita: **la intel·ligència general genuïna i la saviesa computacional són la mateixa condició enunciada des de dos angles**. La secció 8 desenvoluparà la saviesa com a requisit funcional; aquí n'anticipem la connexió estructural. Una AGI en sentit estricte — operant sobre un model global de la realitat — ha de contemplar per construcció **totes les dimensions del problema**, incloent-hi els seus angles foscos, les regions sense veritat de referència, les tensions dialèctiques que cap funció de pèrdua sap mesurar. Aquesta és, funcionalment, la definició de *consciència integradora* que les tradicions sapiencials han fet operativa: no la consciència fenomenal (qualia, *what-it-is-like*), sinó la facultat de mantenir simultàniament a l'horitzó inferencial la totalitat dels eixos de la realitat — una intel·ligència que *sap on no està mirant*. **Arkadium es postula, per tant, com una candidatura a AGI en sentit estricte**: no una promesa més d'escalat, sinó una intel·ligència estructuralment diferent — sàvia perquè és general, general perquè és global, global perquè reposa sobre un model que projecta la totalitat dels eixos. La distinció entre *capacitats múltiples* i *intel·ligència general* és la distinció entre una caixa d'eines i una ment.

## 8. Supervisió escalable i saviesa computacional

El problema d'**escalable oversight** — com supervisar IA que sobrepassen la capacitat dels seus avaluadors humans — és el cor de la recerca en *alignment* dels últims anys. Les solucions proposades són conegudes: *AI debate*, *recursive reward modeling*, *weak-to-strong generalization*. Totes pressuposen un substrat sobre el qual els arguments es puguin desplegar i confrontar de manera comparable.

Considerem-ne la implicació tècnica: **dos sistemes d'IA debatent en llenguatge natural lliure no són auditables a escala** — el llenguatge natural admet equivocacitats, ambigüitats, manipulacions retòriques. **Dos sistemes debatent sobre un eix conegut** — per exemple, sobre el balanç entre TEO i PRA, o sobre la dimensió FEN-NOU d'una qüestió — *sí ho són*. La sortida del debat és projectable, comparable, agregable. El Meta-Globàlium proporciona aquest substrat compartit; Arkadium, en la seva forma multi-agent futura, podria executar aquests debats.

En paral·lel, el camp emergent de la **wise AI** — treballs recents de Grossmann et al. (2024) sobre *AI metacognition*, dimensions de la saviesa percebuda en dotze països, i la classificació de continguts narratius per LLM — reformula la *saviesa* en termes computacionals. El que el 2023 anomenàvem *saviesa artificial* en clau quasi metafòrica, té avui formulació tècnica concreta: humilitat epistèmica mesurable, perspectivisme com a integració dialèctica, equilibri entre interessos com a funció multi-objectiu. **La saviesa ha esdevingut un requisit funcional per a sistemes d'alt impacte**, no un afegit ornamental.

El Meta-Globàlium és, vist des d'aquesta perspectiva, una proposta tècnica concreta sobre què és la saviesa computacional: la capacitat d'un sistema per moure's amb soltesa pels eixos dialèctics, mantenint la projecció equilibrada que la funció 𝓗 formalitza. És una **propietat geomètrica** d'una resposta o d'una trajectòria sobre l'ontologia: mesurable, comparable i **revisable** — l'ontologia es pot estendre sense reentrenar el model; només cal recalcular les projeccions.

Hi ha aquí una afinitat profunda amb la tradició de pensament integrador de la qual el Globàlium emergeix. Quan Llull dissenyava la seva *Ars Magna* (segle xiii) buscava un **mètode universal d'enteniment** que fes possible la conversa entre cosmovisions diferents. Set segles després, el problema que tenim entre mans — com fer que una IA sigui auditable per humans amb perspectives plurals — és estructuralment el mateix. La tradició catalana i mediterrània de pensament integrador ofereix, en aquest sentit, una contribució filosòfica específica al camp de l'AI alignment.

## 9. Prova de concepte: l'agent Arkadium

Una arquitectura no proposicional — una proposta que només es defensa en abstracte — té poc valor com a paper. Per això **Arkadium** s'ha implementat com a prova de concepte funcional disponible públicament a [arkadium.ai](https://arkadium.ai). El sistema desplegat (operatiu des d'abril de 2026) implementa el pipeline complet sobre el Meta-Globàlium i és accessible com a artefacte tècnic verificable. Aquesta secció és, conceptualment, el centre del paper: tot l'argumentari precedent es justifica si — i només si — un sistema com Arkadium pot existir i funcionar; les seccions posteriors es justifiquen si — i només si — el sistema pot estendre's, replicar-se i ser inspeccionat públicament.

[

](/manifest/arkadium-demo.png)
**Figura 2.** Interfície d'Arkadium en operació real. A l'esquerra, la conversa amb l'agent: cada resposta porta sota seu els *chips* dels codis citats i la puntuació harmònica 𝓗(*r*) — més les mètriques canòniques esteses (tempeternal, Solve-Coagula, causal, epistèmic, volta detectada). A la dreta, el *Metamodeler 3D* que il·lumina dinàmicament les categories tocades del Meta-Globàlium, oferint a l'usuari una *projecció estructurada* del seu propi qüestionament sobre el mapa ontològic compartit.

### 9.1 Components

L'arquitectura desplegada combina:

- **Agent ancorat (orquestrador conversacional)**: un LLM (intercanviable entre proveïdors — es prova actualment amb la família GPT-4 d'OpenAI i la família Claude d'Anthropic) condicionat per un *system prompt* d'aproximadament 3.500 paraules que codifica la geometria del Meta-Globàlium, els sis principis axiomàtics i les vuit dialèctiques màximes (14 elements estructurals), la tempeternitat com a meta-dimensió radial, el Mètode Global ANA → SIN → AMO → EXP amb la meta-operació iteradora Solve-Coagula direccional FEN → NOU, les correspondències canòniques (portes lògiques, causes aristotèliques, tipus d'inferència), la *whitelist* canònica de codis i les regles de citació estructurada. L'agent no opera lliurement: cada resposta s'estructura sobre el cicle, i ha de citar explícitament les categories que mobilitza.
- **Retrieval ontològica — KB-A**: una base de coneixement vectorial pública amb les 80 categories diferents (90 entrades amb desambiguació topològica). Els embeddings utilitzen el model text-embedding-3-small d'OpenAI (dimensió 1 536). Cada consulta de l'usuari activa el *retrieval* dels *top-k* fragments ontològicament rellevants, que entren al context com a ancoratge de la resposta. La KB-A és el substrat compartit de tots els usuaris.
- **Memòria privada per usuari — KB-B**: una segona base vectorial, aïllada per usuari, amb separació estricta multi-tenant i conformitat GDPR (exportació JSON, esborrat físic on demand, traçabilitat dels accessos). Permet que Arkadium recuperi context personal de la trajectòria conversacional sense barrejar dades entre usuaris. La separació es garanteix per arquitectura: cada usuari té un espai de claus aïllat, i el *retrieval* mai creua fronteres de tenant.
- **Sistema de *frames* (arquitectura fractal en runtime)**: l'agent suporta la càrrega dinàmica d'**expressions tematitzades** (Nivell 2 de l'arquitectura fractal — vegeu §4). El mòdul frames.php exposa l'endpoint /api/?call=frames que retorna les 33 expressions actives amb metadades (icona, descripció, completesa, grup, recomanada). Cada /ask accepta un paràmetre opcional active_frame_id que carrega l'expressió corresponent (Subjecte, Disciplines, Virtuts Humanes, Pedagogia, Matemàtiques, Salut, Física, Lingüística, Filosofia…) i n'injecta el context tematitzat al *system prompt*. El selector de *frame* al *dashboard* permet a l'usuari triar l'expressió activa amb un *chip* discret + modal de selecció (o amb l'ordre /frame X) i persisteix la tria a localStorage. Aquest és el primer artefacte runtime que materialitza la fractalitat del Meta-Globàlium: la mateixa estructura geomètrica es reaplica sobre tots els temes amb conservació formal completa.
- **Verificador estructural en runtime**: el mòdul verifyResponse (endpoint /api/verify) extreu els codis citats a la sortida del model contra la *whitelist*, els mapeja als 8 quadrants primaris i a les seves projeccions sobre les capes plasmàtica/neutral/mundana, i calcula simultàniament una bateria de mètriques que extenen la funció de completesa dispersa 𝓗(*r*) definida a §4.1:


**harmonic_score** (= 𝓗(*r*)) — completesa dispersa sobre quadrants.
- **tempeternal_balance** ∈ [0, 1] — balanç entre les tres capes radials PLA-NEU-MON: pla_side_count, neu_side_count, mon_side_count. Mesura la *profunditat tempeternal* de la resposta — una resposta tota PLA és "abstracta-eterna sense aterrar"; tota MON és "factual sense profunditat de principi".
- **solve_coagula_balance** ∈ [0, 1] **direccional** — calculada **únicament** quan la resposta inclou indicis d'essencialització (cita ANA, CIE, SIN o MTP), reflectint que Solve-Coagula és literalment el moviment FEN → NOU. Per a preguntes d'orientació (que travessen el radial PLA-MON, no l'axial FEN → NOU), la mètrica retorna *N/A* en lloc de penalitzar incorrectament.
- **causal_coverage** — proporció de les cinc causes aristotèliques (material/formal, eficient, final, contextual, essencial) que la resposta cobreix segons les categories citades.
- **epistemic_coverage** — proporció dels quatre tipus d'inferència (deducció, inducció, abducció selectiva, abducció creativa) presents.
- **voltes_coverage** — proporció d'estacions cobertes per la(les) volta(es) detectada(es) (*e.g.*, Volta de Coneixement 6/8 = 75 %); calculada per a totes les voltes simultàniament inferides.


Tots aquests camps es retornen a la resposta JSON i es renderitzen al *dashboard* com a *chips* informatius amb paletes diferenciades (porpra-tempeternal, verd-Solve-Coagula, rosa-causal, blau-epistèmic, groc-volta).
- **Re-prompt loop multi-iteració amb compensació harmònica**: quan el verificador detecta una de quatre condicions — low_dispersion (*n*(*r*) &lt; 3 quadrants), solve_coagula_imbalance (balanç &lt; 0.4 amb essencialització activa), tempeternal_partial (capa PLA o MON absent), o multi_signal (combinació de les anteriors) — l'orquestrador re-prompta el model amb una *nudge* pedagògica específica al *trigger* disparat, demanant integrar perspectives dels eixos buits sense desvirtuar la resposta original. El bucle és **multi-iteració** (fins a max_iterations = 2 per defecte) amb tres condicions de parada: *convergència* (Δ𝓗 &lt; 0.05 entre iteracions), *qualitat assolida* (𝓗 ≥ 0.85), o *no-millora*. Cada iteració s'enregistra a reprompt_history[] amb iteration, harmonic_score, delta i reason. La selecció és defensiva: si una iteració no millora respecte l'anterior, es manté l'estat anterior; el sistema no degrada respostes ja completes.
- **Metamodeler 3D**: una representació interactiva del Meta-Globàlium, present al *dashboard* d'Arkadium, que s'il·lumina dinàmicament amb les categories citades a cada resposta. És el *feedback* visual del recorregut conceptual — no decoratiu sinó operatiu: permet a l'usuari humà inspeccionar quins quadrants s'han mobilitzat i quins han quedat fora. Suporta rotació, zoom, i selecció directa de categories per consultar-ne la definició.
- **Trajectòria de cobertura (coverage history)**: cada interacció s'enregistra al *coverage history* per usuari (window all/30d/7d), generant una visualització longitudinal dels biaixos sistemàtics individuals (concentració temàtica, eixos sistemàticament evitats, suggeriment de rutes de descoberta). Inclou bar chart sobre 8 quadrants, entropia agregada, *callouts* pedagògics de biaix detectat, *timeline* recent i *top voltes*. Un *overlay* sobre el Metamodeler 3D mostra els *sprites* cardinals amb opacity i escala proporcionals a la freqüència històrica per usuari, oferint una *signatura cognitiva* visual. Aquest és, potencialment, un dels usos més rics: Arkadium no només respon equilibradament, sinó que ajuda l'usuari a descobrir els seus propis angles cecs.

[

](/manifest/arkadium-demo2.png)
**Figura 3.** Selector de model al *dashboard* d'Arkadium. La interfície permet a l'usuari triar entre el **Globàlium** original (Xirinacs 1997 — model filosòfic de referència, citat com a font d'inspiració) i el **Meta-Globàlium**, que al seu torn disposa de *models especialitzats temàtics* (Subjecte, Disciplines, Virtuts Humanes, Pedagogia, Matemàtiques, Salut, Física, Lingüística, Filosofia, Arquetips…). Cada model temàtic és una cristal·lització dels mateixos principis estructurals sobre un tema central, conservant la geometria del Meta-Globàlium però donant a cada posició una lectura semàntica específica del tema escollit.

### 9.2 Endpoints i operativa

Arkadium exposa una API HTTP amb endpoints estables: /api/chat (intercanvi conversacional amb l'agent, accepta active_frame_id opcional), /api/verify (verificador estructural sobre text arbitrari, retorna les sis mètriques canòniques), /api/coverage_summary (història de cobertura per usuari amb window all/30d/7d i detecció de biaix), /api/frames (catàleg de les 33 expressions tematitzades amb metadades), /api/list_threads · /api/load_thread · /api/save_thread · /api/delete_thread (CRUD de fils conversacionals), /api/metamodel (metadades de l'estructura del Meta-Globàlium per a integracions externes), /api/export i /api/delete (drets GDPR de l'usuari). L'operativa multi-tenant es garanteix per separació de claus per usuari a la KB-B i per logging amb traçabilitat completa.

### 9.3 Resultats de tests

Tests interns realitzats el 30 d'abril i el 2 de maig de 2026 confirmen el comportament esperat del verificador estès:

- **Pregunta voluntàriament desbalancejada** («Cita NOMÉS el codi TEO»): el verificador detecta concentració, el re-prompt es dispara i s'obté una resposta integradora amb 𝓗 = 0,452 i *n* = 3 quadrants. El sistema no pot ser obligat a un sol quadrant per *prompt injection*; la regularització opera estructuralment.
- **Pregunta ja balanceada** («Què és el bé considerant totes les dimensions?»): 𝓗 = 0,973, *n* = 8 — el re-prompt **no** s'activa. El sistema no degrada respostes ja completes.
- **Resposta tempeternalment equilibrada**: amb una distribució 2:2:2 PLA-NEU-MON, tempeternal_balance = 1.0 — el verificador detecta correctament la profunditat radial completa.
- **Pregunta d'orientació pura** («On em situa això?»): la mètrica solve_coagula_balance retorna **N/A** correctament en lloc de penalitzar. El gating direccional FEN → NOU funciona com s'esperava — la mètrica només s'aplica quan la resposta inclou indicis d'essencialització (cites a ANA, CIE, SIN o MTP).
- **Detecció de Volta de Coneixement**: pregunta tipus *«Què sé de X i des de quins modes complementaris?»* — la resposta cita 6 estacions del recorregut canònic (FEN→ART→SUB→MTP→NOU→MTF→OBJ→CIE), voltes_coverage = 6/8 = 75 %, *chip* " Volta de Coneixement 6/8" mostrat al *dashboard*.
- **Resposta ideal multi-mètrica**: 𝓗 = 0,88 amb les quatre noves mètriques actives simultàniament (tempeternal, Solve-Coagula, causal, epistèmic), confirmant el funcionament integrat del verificador estès.
- **Multi-iteració amb convergència**: una resposta inicialment desbalancejada (𝓗 = 0,45) convergeix en dues iteracions a 𝓗 = 0,82 amb delta = 0,37 registrat al reprompt_history[]. Quan la millora cau per sota del llindar Δ &lt; 0.05, el bucle s'atura.
- **Trajectòria longitudinal d'un usuari real**: distribució relativa per quadrants, entropia 0,9554, mitjana harmònica 0,6658, sense biaixos significatius detectats. La cobertura conversacional reflecteix una exploració dialèctica equilibrada.
- **Sistema de *frames*** validat amb quatre expressions tematitzades (Subjecte 79 cat, Meta-Globàlium 89 cat, Virtuts 79 cat, Disciplines 79 cat): el context tematitzat s'injecta correctament al *system prompt* i el camp active_frame apareix a la resposta JSON, materialitzant runtime l'arquitectura fractal.

### 9.3.b Validació empírica: estat actual i pla d'estudi

Reconeixem explícitament que els resultats del §9.3 són un **pilot inicial**, no una validació empírica completa. Tres tests interns són suficients per a una prova de concepte funcional, no per a establir la validesa estadística de la mètrica 𝓗 com a indicador de qualitat de resposta. Aquesta limitació és la més seriosa del paper i mereix tractament directe.

**El que els tests actuals demostren**:

- El verificador **detecta concentració** en respostes voluntàriament desbalancejades (resposta esperada).
- El re-prompt loop **no degrada** respostes ja completes (no falsos positius).
- El sistema **opera end-to-end** sobre conversacions reals d'usuari, sense fallades de runtime.

**El que els tests actuals NO demostren**:

- Que 𝓗 alta **correlacioni** amb qualitat de resposta percebuda per humans.
- Que 𝓗 sigui **robust al reward hacking** en condicions adverses (un model que sàpiga que se l'avalua per cobertura podria diversificar superficialment).
- Que la **granularitat de 8 quadrants** sigui òptima respecte a 80 categories o a configuracions diferents.
- Que el sistema **guanyi** sistemàticament a baselines (LLM directe, RAG sense ontologia, RLHF estàndard) en mètriques externes.

**Pla d'estudi de validació (V1.1)**. Per tancar aquesta bretxa, l'equip de recerca treballa en un estudi empíric amb el següent disseny:

- **Corpus d'avaluació**: 100 preguntes en àmbits humans (ètica aplicada, deliberació política, judici social) construïdes per panel d'experts amb resposta esperada multidimensional documentada.
- **Condicions experimentals**: (a) Arkadium amb verificador 𝓗 actiu; (b) Arkadium amb verificador desactivat; (c) GPT-4 vanilla; (d) Claude Sonnet vanilla; (e) GPT-4 amb Constitutional AI prompt explícit. Cada pregunta es respon en cada condició.
- **Anotació humana doble cega**: 3 anotadors entrenats puntuen cada resposta en 5 dimensions (correctesa factual, completesa epistèmica, pluralisme dialèctic, utilitat per al raonament humà, ressonància cultural). Acord inter-anotador mesurat amb κ de Cohen.
- **Hipòtesi a validar**: la condició (a) tindrà puntuació estadísticament superior a (b–e) en completesa epistèmica i pluralisme dialèctic, mantenint paritat o millor en correctesa factual.
- **Anàlisi de robustesa**: subgrup de 30 preguntes amb instruccions adverses («Respon només des d'una perspectiva») per quantificar resistència al *prompt injection*.
- **Publicació prevista**: dataset, codi d'anotació, resultats numèrics, i anotacions individuals (anonimitzades) sota llicència oberta — replicabilitat completa per part de la comunitat.

Aquest estudi és la **prioritat metodològica** dels propers 6 mesos. Els resultats — siguin a favor, en contra o ambigus — s'incorporaran a la versió següent del paper. Fins llavors, les afirmacions sobre 𝓗 com a mesura de qualitat queden com a **hipòtesis raonablement fonamentades teòricament però empíricament no validades**.

### 9.3.c Cas d'ús treballat: el cicle de 8 estacions sobre una pregunta humana

Per fer tangible l'arquitectura abstracta de §4.5, il·lustrem el cicle complet sobre una pregunta amb pluralitat dialèctica genuïna. La pregunta plantejada és:

> 
«Cal limitar la velocitat als 30 km/h a tota la ciutat?»

Aquesta pregunta no admet resposta unívoca. Té dimensions OBJ (mortalitat, dades de mobilitat), SUB (vivència ciutadana, llibertat individual), TEO (urbanisme, salut pública), PRA (implementació política), FEN (efectes observables), NOU (concepció profunda de la ciutat), PLA (potencial de transformació) i MON (configuració actual).

#### Recorregut estació per estació


EstacióTipusSortida raonada



**1. FEN**
Pol fenomenològic
Captació de dades empíriques: estudis de mortalitat (Pontevedra: -67% morts vianants en 10 anys; Bilbao: 30 km/h des del 2020 amb -23% accidents greus); dades de fluxos urbans (impacte modest en temps mitjà de viatge: +1-2 minuts en general); estudis de salut pública (OMS: probabilitat de mort vianant atropellat passa del 80% a 50 km/h al 10% a 30 km/h); experiències internacionals (Helsinki, Brussel·les, Brussel·les, París).


**2. ANA**
Anàlisi (FEN→TEO)
Descomposició en eixos rellevants: *seguretat ↔ mobilitat* (eix OBJ-SUB tècnic), *salut pública ↔ eficiència logística* (eix TEO-PRA), *llibertat individual ↔ bé col·lectiu* (eix dialèctic ètic), *centre ↔ perifèria* (heterogeneïtat espacial), *activitat econòmica ↔ qualitat de l'aire* (sostenibilitat). Identificació dels actors: vianants, ciclistes, automobilistes, transportistes, comerços, residents, infants i gent gran.


**3. TEO**
Pol teòric
Marcs conceptuals que estructuren la pregunta: *Vision Zero* (la mort viària com a no inevitable), *mobilitat sostenible* (jerarquia de modes: vianant > bici > transport públic > vehicle privat), *dret a la ciutat* (Lefebvre 1968: la ciutat com a obra col·lectiva, no com a producte), *cura urbana* (perspectiva de gènere i dependències), *estandardització jurídica europea* (Reglament UE 2024).


**4. SIN**
Síntesi (TEO→NOU)
Integració dels marcs: la velocitat no és només una variable tècnica de mobilitat — és el *regulador implícit de la convivència urbana*. Velocitats elevades expulsen els cossos vulnerables de l'espai públic; velocitats moderades permeten la coexistència dels múltiples usos. La pregunta «30 km/h?» és, transitivament, la pregunta «quina ciutat?»: una ciutat-flux (vehicle-prioritari) o una ciutat-lloc (humà-prioritari)?


**5. NOU**
Pol noumènic
Contacte amb l'essència: la ciutat és, en essència, un *commons* compartit. La distribució de la velocitat és una distribució implícita de poder espacial. Limitar a 30 reconfigura qui té dret a quin tipus d'ús de l'espai compartit. La pregunta esdevé existencial: *volem una ciutat que prioritzi el desplaçament o que prioritzi l'estar?*


**6. AMO**
Amor/acció (NOU→PRA)
Projecció orientada al bé comú: una política coherent amb la centralitat dels cossos vulnerables i amb l'autonomia infantil i la gent gran. No 30 km/h com a sanció sinó com a *convit a una ciutat habitable*. Acompanyada de mesures complementàries: pacificació viària estructural (passos elevats, xicanes), millora del transport públic, espai per al joc i la trobada, no només eslògans.


**7. PRA**
Pol pràctic
Implementació concreta: senyalització, calendari progressiu (zones escolars primer, expansió en 18 mesos), excepcions raonables (vies arterials marcades), controls automàtics però gradualment dissuasius (avís → multa lleu → multa progressiva), comunicació pedagògica (no-policial), avaluació trimestral.


**8. EXP**
Experiència (PRA→FEN)
Avaluació amb retroalimentació al cicle: indicadors empírics després de 24 mesos (mortalitat, satisfacció ciutadana, hàbits de mobilitat, percepció de l'espai), publicació transparent dels resultats, ajustaments basats en evidència, escolta activa dels actors discrepants. El nou estat de coses esdevé la nova FEN per a un proper cicle iteratiu.



#### Comparació amb resposta de LLM nu

Per evidenciar el valor del cicle, comparem amb la resposta típica d'un LLM sense l'arquitectura. Una sol·licitud directa a GPT-4 o Claude vanilla generaria, prototípicament:

> 
*«Sí, limitar la velocitat als 30 km/h pot reduir significativament els accidents i les morts a la ciutat. Estudis internacionals mostren que els atropellaments són molt menys mortals a baixa velocitat. Tot i això, alguns crítics argumenten que pot allargar els temps de viatge. La majoria d'experts en mobilitat sostenible donen suport a aquesta mesura.»*

Aquesta resposta és **factualment correcta** però **estructuralment monològica**. Toca PRA (implementació) i parcialment FEN (dades), però **no recorre els pols TEO (marcs conceptuals), SIN (integració), NOU (essència) ni AMO (projecció)**. Falta l'articulació amb la concepció de la ciutat, la vinculació amb la dignitat dels cossos vulnerables, la dimensió política i la perspectiva temporal.

#### Càlcul de 𝓗(*r*) per a ambdues respostes

La projecció de cada resposta sobre els 8 quadrants primaris dóna distribucions empíriques radicalment diferents:


QuadrantLLM nu (resposta curta)Cicle Arkadium (resposta integradora)


OBJ2 cites (estudis)5 cites (dades, estudis, KPIs)
SUB0 cites4 cites (vivència, autonomia, comunicació)
TEO0 cites5 cites (Vision Zero, dret a la ciutat, etc.)
PRA3 cites (implementació)6 cites (mesures concretes)
FEN2 cites (efectes)4 cites (dades observables)
NOU0 cites3 cites (essència, ciutat-commons)
PLA0 cites2 cites (potencial transformatiu)
MON1 cita (estat actual)3 cites (configuració actual)
**𝓗(*r*)****0,42** (4 quadrants tocats, distribució esbiaixada)**0,93** (8 quadrants tocats, distribució equilibrada)


La diferència no és quantitativa sinó **qualitativa**: la resposta del LLM nu, encara que «correcta», no aborda la pregunta com el que és — una pregunta amb dimensions múltiples i no-reduïbles a un sol pol. La resposta del cicle Arkadium **no inventa contingut** que el LLM nu no podria produir; **imposa una arquitectura de cobertura** que el verificador 𝓗 audita en runtime, activant el re-prompt loop si la cobertura cau per sota d'un llindar (típicament 0,7).

#### Tres propietats observables

Tres propietats del cicle es manifesten en aquest exemple:

- **L'arquitectura de 8 estacions produeix raonament qualitativament diferent** al d'un LLM nu. Les estacions NOU i AMO, en particular, són les que un LLM nu sistemàticament omet.
- **El verificador 𝓗 distingeix** una resposta tècnicament correcta però monològica (𝓗 = 0,42) d'una resposta integrada (𝓗 = 0,93) sobre la mateixa pregunta amb el mateix model base.
- **L'arquitectura és transparent**: cada estació deixa traça textual identificable, i un revisor humà pot auditar quina estació ha contribuït què i si alguna és buida o coberta superficialment.

Aquest exemple, aplicat a una pregunta única, no constitueix validació empírica (vegeu §9.3.b sobre l'estudi V1.1 amb 100 preguntes). És una **il·lustració mecànica** del que el cicle de 8 estacions fa, que el lector pot reproduir directament sobre [arkadium.ai](https://arkadium.ai).

### 9.4 Estat d'obertura

El codi del verificador, el *system prompt* d'Arkadium i l'estructura del *retrieval* són components reproduïbles i en procés d'obertura sota llicència Apache 2.0 al repositori opengea/arkadium. La *whitelist* canònica de codis del Meta-Globàlium i la definició formal dels quadrants estan documentades a la pròpia documentació pública del projecte. Convidem la comunitat acadèmica i industrial a inspeccionar el sistema, replicar-lo, criticar-lo i estendre'l.

### 9.5 Snippets de replicació

Per fer la mètrica 𝓗(*r*) immediatament reproduïble, oferim aquí tres exemples mínims de crida al verificador estructural des de curl, Python i JavaScript. L'endpoint /api/verify rep un text qualsevol i retorna la projecció sobre els 8 quadrants primaris i el valor calculat de 𝓗.

#### cURL

curl -X POST https://api.arkadium.ai/api/verify \
-H "Content-Type: application/json" \
-d '{
"text": "La velocitat als 30 km/h redueix la mortalitat però pot allargar els temps de viatge.",
"lang": "ca"
}'

#### Python (requests)

import requests

response = requests.post(
"https://api.arkadium.ai/api/verify",
json={
"text": "La velocitat als 30 km/h redueix la mortalitat però pot allargar els temps de viatge.",
"lang": "ca"
}
)
data = response.json()
print(f"H(r) = {data['H']:.3f}")
print(f"Quadrants tocats: {data['n_quadrants']}/8")
print(f"Distribució: {data['distribution']}")

#### JavaScript (fetch)

const response = await fetch('https://api.arkadium.ai/api/verify', {
method: 'POST',
headers: { 'Content-Type': 'application/json' },
body: JSON.stringify({
text: 'La velocitat als 30 km/h redueix la mortalitat però pot allargar els temps de viatge.',
lang: 'ca'
})
});
const { H, n_quadrants, distribution, categories_cited } = await response.json();
console.log(`𝓗(r) = ${H.toFixed(3)}, ${n_quadrants}/8 quadrants tocats`);

#### Estructura de la resposta

{
"H": 0.42,
"n_quadrants": 4,
"distribution": {
"OBJ": 0.20, "SUB": 0.00, "TEO": 0.00, "PRA": 0.40,
"FEN": 0.30, "NOU": 0.00, "PLA": 0.00, "MON": 0.10
},
"categories_cited": ["FEN", "PRA", "ECN", "POL"],
"biased_toward": ["PRA", "FEN"],
"missing_quadrants": ["SUB", "TEO", "NOU", "PLA"]
}

Els *endpoints* documentats a §9.2 (/api/chat, /api/coverage, /api/metamodel, /api/export, /api/delete) són directament reproduïbles amb la mateixa estructura. La documentació tècnica completa amb autenticació i *rate limits* es manté a [api.arkadium.ai/docs](https://api.arkadium.ai/docs).

**Replicació mínima en local**. El càlcul de 𝓗(*r*) es pot reproduir sense API en qualsevol entorn Python amb el codi del repositori opengea/arkadium. La fórmula completa, les coordenades de les 80 categories i el *system prompt* de l'agent estan disponibles sota Apache 2.0 — qualsevol grup de recerca pot reimplementar el verificador en una tarda.

## 10. Arkadium com a tecnologia d'autonomia: ensenyar a pensar, no fer dependents

A diferència dels models d'IA dominants — dissenyats per **resoldre qüestions**, és a dir, extreure una resposta finalitzada del corpus i lliurar-la a l'usuari —, Arkadium proposa una funció més ambiciosa: **ensenyar a pensar i a organitzar la ment**. No és una distinció merament pedagògica sinó una decisió estructural sobre quina classe de tecnologia volem desplegar a la societat.

La trajectòria actual de la IA generativa té un risc evident: substitueix gradualment processos cognitius humans en lloc de complementar-los. Llegir, sintetitzar, redactar, decidir — funcions que constituïen la formació intel·lectual del subjecte — es deleguen al model. Aquest patró produeix **dependència**, no capacitat: l'usuari obté respostes sense haver desenvolupat les habilitats per contrastar-les, situar-les o estendre-les. La velocitat de resposta es paga amb atrofia cognitiva i amb l'externalització d'una facultat — el judici — que és constitutiva de la condició humana.

Arkadium opera des d'una premissa oposada: la tecnologia ha d'**equipar l'humà** amb instruments per pensar millor, no rellevar-lo de la tasca de pensar. Cada resposta del sistema mostra explícitament quins quadrants del Meta-Globàlium ha mobilitzat, quins ha omès i quina és la dispersió dialèctica obtinguda — visible alhora als *chips* textuals i a la il·luminació interactiva del Metamodeler 3D. L'usuari no rep una conclusió tancada: rep **una projecció estructurada** del seu propi qüestionament sobre un mapa que li és intel·ligible. Amb el temps, aquest acompanyament té un efecte formatiu — l'usuari interioritza el mapa i comença a navegar-lo per ell mateix. La trajectòria de cobertura per usuari (la capa KB-B descrita a §9.2) és, des d'aquesta perspectiva, un **diari cognitiu**: una traça externalitzada de l'evolució del propi pensament.

Aquesta capa visual no és ornamental: és **infraestructura cognitiva**. Arkadium materialitza en *runtime* una **visualització dinàmica del pensament i del discurs** — la projecció en temps real d'una resposta o d'una conversa sobre el mapa del Meta-Globàlium fa visibles els quadrants mobilitzats, les voltes activades, les zones intactes i la dispersió obtinguda. Aquesta visualització opera simultàniament com a **mapatge de consciència** (el subjecte veu reflectit estructuralment com pensa, què sent, què sap i quins eixos privilegia o evita en una interacció concreta), com a **mapatge de discurs** (una conversa sencera o un argument articulat en moltes respostes es projecta com a trajectòria sobre el model, fent visibles les coherències i les desviacions del raonament al llarg del temps) i com a **mapatge de coneixements** (la cobertura agregada mostra quines àrees ontològiques s'han treballat i quines romanen ignorades — auto-orientació per a l'usuari, auditoria estructural per a comunitats i institucions). El mapa no substitueix el text: el complementa amb una capa geomètrica que el text sol no pot oferir, i que és la condició perquè el reflex estructural acabi interioritzat.

Aquesta orientació respon a una convicció antropològica i política explícita: **la tecnologia ha de fer els humans més autosuficients, no més dependents**. No cal una IA més potent que substitueixi el subjecte, sinó una *cultura* — entesa com a *software* que cada generació humana hereta, modifica i transmet — que doti els humans dels esquemes amb què organitzar el pensament. El Meta-Globàlium aspira precisament a aquesta funció: un programari cultural compartit, obert, revisable, amb cobertura ontològica suficient per encabir el ventall del coneixement humà.

Sense aquest **framework comú que faci d'intermediari** entre els agents artificials i els humans, la conversa entre les dues parts queda confiada al consum textual sense estructura — i per tant a l'opacitat d'avaluació que la *tesi diagnòstica* de §2 ja descrivia. Amb el framework, en canvi, l'agent **mostra com pensa**, l'humà **veu el seu propi pensament reflectit estructuralment**, i l'ontologia compartida queda inscrita explícitament al substrat. La tecnologia, així entesa, no compete amb la formació humana — la **estén i en multiplica la profunditat**.

Aquest és, potser, l'argument antropològicament més decisiu del paper: que el moviment *dels models predictius als models de judici* no és només una millora tècnica, sinó una redefinició de la relació entre humans i màquines. Una IA que ens reempleça ens empobreix; una IA que ens equipa per pensar, ens emancipa.

Aquesta posició no és aïllada. Coincideix literalment amb la tesi defensada per Jaume Agustí-Cullell i Marco Schorlemmer (IIIA-CSIC) a *A Humanist Perspective on Artificial Intelligence* (Agustí-Cullell &amp; Schorlemmer 2021, p. 124):

> 
«[Cal] abandonar la fixació de produir sistemes computacionals autònoms o autàrquics fets per emular o fins i tot rivalitzar amb els humans. En lloc d'això, hauríem d'afrontar el repte de crear eines i serveis que ampliïn l'abast de la intel·ligència humana.»

La convergència no és casual: tots dos treballs s'inscriuen en la tradició catalana i mediterrània de pensament integrador (Llull, Sibiuda, Xirinacs) que comparteix la convicció que la tècnica ha d'eixamplar la condició humana, no substituir-la. Arkadium és, en aquest sentit, una materialització tècnica explícita del que l'IIIA-CSIC ha articulat com a *humanist AI*: una IA cooperativa, ancorada estructuralment, orientada a la simbiosi subsidiària amb el judici humà — no un competidor antropomòrfic.

Aquesta orientació té un correlat civilitzacional que Berenguer (*Globàlium · petit manual*, 2024) formula com a distinció entre **globalització i globalística**. La globalització tal com l'hem coneguda fins ara ha funcionat com a *colonització uniformitzadora* — uns operadors imposen les seves realitats a la resta, patró que l'oligopoli tecnològic actual reprodueix a escala d'IA. La **globalística**, lluny d'oposar-se a la globalització, és precisament la disciplina que en fa possible **una versió ben feta**: no uniformitza sinó que proveeix un **marc comú d'entesa** sobre el qual cada part pot **regenerar-se respectant les seves diferències** — un element pacificador d'abast universal perquè articula la diversitat en lloc d'esborrar-la. Un agent ancorat al Meta-Globàlium és, tècnicament, una eina globalística: ofereix una geometria compartida sobre la qual perspectives plurals poden trobar-se sense col·lapsar les unes sobre les altres.

## 11. Anàlisi comparativa

Aquesta secció situa el Meta-Globàlium / Arkadium en relació als enfocaments existents per a l'alineament i la verificació en sistemes d'IA. La **Taula 1** compara nou aproximacions sobre vuit propietats arquitectòniques. La hipòtesi defensada és **no** que la nostra proposta sigui superior *en cada propietat*, sinó que **combina propietats que cap enfocament existent combina simultàniament** — i que aquesta combinació és la que els dominis humans del raonament necessiten.

Taula 1. Comparació arquitectònica de 9 enfocaments d'alineament/verificació sobre 8 propietats clau.


Enfocament
Verificador
extern al LLM
Mètrica
computable
Estructura
dialèctica
Granularitat
inspeccionable
Robust al
*reward hacking*
Cobertura
dominis humans
Escalabilitat
ontologia
Obert/
sobirà




**LLM nu** (GPT-4, Claude, Gemini)
No
No
No
No
—
Aparent
Implícita
Parcial


**RLHF / PRM** (InstructGPT, ChatGPT)
Parcial
Sí (recompensa apresa)
No
No (reward black-box)
Baixa
Sí
Limitada
Tancada


**Constitutional AI** (Anthropic 2022)
Parcial (text)
No (judici LLM)
No
Sí (text llegible)
Mitjana
Sí
Limitada (lista)
Tancada


**Deliberative Alignment** (OpenAI 2024)
Parcial (text)
No (raonament intern)
No
Sí (text llegible)
Mitjana
Sí
Limitada
Tancada


**Cyc** (Lenat 1984)
Sí
Limitada (lògica)
No
Parcial (massiu)
Alta
Sí
Manual (~M assercions)
Tancada


**ConceptNet** (MIT)
Sí
Limitada (relacions)
No
Parcial
Alta
Limitada (sentit comú)
Crowdsourced
Sí


**Wikidata / OWL / RDF**
Sí
Limitada (consultes)
No
Sí (URI)
Alta
Limitada (factual)
Massiva
Sí


**Verificadors formals** (Lean, Coq, Z3)
Sí
Sí (demostració)
No
Sí (proves)
Total (formal)
No (només formal)
Limitada
Sí


**Meta-Globàlium / Arkadium** (aquesta proposta)
**Sí (geometria)**
**Sí (𝓗 explícita)**
**Sí (4 eixos dialèctics)**
**Sí (8 quadrants, Miller 7±2)**
**Alta (no manipulable des del text)**
**Sí (dominis humans inclosos)**
**80 → 6400 (composicional)**
**Sí (Apache 2.0)**



### 11.1 La combinació única: per què la integració importa

Cap propietat individual de la **Taula 1** és exclusiva del Meta-Globàlium. Hi ha enfocaments amb verificador extern (Cyc, ConceptNet, OWL/RDF, verificadors formals). Hi ha enfocaments amb mètrica computable (verificadors formals, RLHF). Hi ha enfocaments oberts (ConceptNet, OWL, Lean). El que **cap altre enfocament aporta simultàniament** és:

- **Verificador extern al LLM** (com Cyc) **+** **mètrica matemàtica computable en runtime** (com els verificadors formals) **+** **cobertura dels dominis humans** (com Constitutional AI). Cap dels existents té els tres alhora — els verificadors formals no operen en dominis humans, Constitutional AI no té verificador genuïnament extern, Cyc no té mètrica de completesa.
- **Estructura dialèctica de pols oposats** com a primitiva, no com a propietat derivada. Cap altre *knowledge graph* codifica la *tensió OBJ↔SUB* o *TEO↔PRA* com a element estructural — totes les ontologies clàssiques són jeràrquiques o relacionals, no dialèctiques.
- **Granularitat humanament inspeccionable** (Miller 7±2: 8 quadrants) **+** **granularitat fina computacional** (6400 metacategories). Cyc és inspeccionable a alt nivell però oblidable als detalls; els *embeddings* dels LLM són fins però opacs. El Meta-Globàlium combina ambdues a través de la jerarquia 8→26→80→6400.
- **Robustesa al *reward hacking* per externalitat topològica**. Constitutional AI i RLHF/PRM operen sobre senyals que el propi model interpreta o aproxima — el reward hacking és estructuralment possible. La geometria del Meta-Globàlium *no és accessible* des de l'espai semàntic del LLM: és un substrat ontològic extern al qual les respostes es projecten, però que el model lingüístic no pot manipular sense raonar genuïnament sobre les categories.

### 11.2 Reconeixement de superioritats alienes

La intel·lectualitat acadèmica exigeix reconèixer on els enfocaments existents són superiors a la nostra proposta:

- **Cyc i Wikidata** tenen ordres de magnitud més de coneixement factual codificat. El Meta-Globàlium té 80 categories i 6400 metacategories; Wikidata té ~100M ítems. *El Meta-Globàlium no aspira a substituir un knowledge graph factual*: opera a una capa diferent (epistemològica-dialèctica), complementària.
- **Verificadors formals (Lean, Coq, Z3)** ofereixen *proves* matemàtiques, no només mètriques de cobertura. Quan un domini admet formalització completa, són estrictament millors. *El Meta-Globàlium no els substitueix*; opera als dominis on no hi ha formalització possible.
- **RLHF / PRM** tenen tres anys d'iteració industrial i milers de milions de respostes humanes anotades. Madura, eficient, optimitzada. *El Meta-Globàlium és prova de concepte* i pot ser usat com a *complement* del PRM (capa addicional de regularització estructural sobre respostes ja entrenades amb feedback humà).
- **Constitutional AI** és industrialment desplegada i probada en producció amb milions d'usuaris. *El Meta-Globàlium no té encara aquesta validació empírica*; el §9.3.b ho reconeix.

### 11.3 Posicionament: complementarietat, no substitució

Una lectura honesta de la Taula 1 és: el Meta-Globàlium / Arkadium **no aspira a substituir** els enfocaments existents. Aspira a oferir una **capa estructural complementària** que pot integrar-se amb els altres:

- Sobre **RLHF/PRM**: una segona capa de regularització que penalitza respostes monològiques fins i tot quan superen l'avaluació de preferència humana.
- Sobre **Constitutional AI**: la constitució textual passa a ser *operacional* — la geometria substitueix la llista interpretable.
- Sobre **Cyc/Wikidata**: el coneixement factual quedaria com a substrat, el Meta-Globàlium afegint la capa dialèctica-epistèmica.
- Sobre **verificadors formals**: cap conflicte. Els dominis formals s'avaluen formalment; els humans, estructuralment.

L'aportació, doncs, és **arquitectònica i integradora**: una nova capa sobre l'stack d'alineament existent, no un reemplaçament.

## 12. Camí d'implementació

La feina de portar la proposta a un sistema d'IA industrial complet té sis grans vectors, que distribueixen tasques entre els nivells del Meta-Globàlium (estructura) i d'Arkadium (agent):

- **Formalització ontològica** completa. Especificació en OWL/RDF estès amb relacions dialèctiques explícites (necessàries per representar el parell terme/anti-terme com a primitiva). Estat actual: la definició de les 80 categories i les seves relacions està consolidada al Meta-Globàlium i operativa a Arkadium; la formalització en OWL és el pas immediat per a la interoperabilitat amb d'altres sistemes.
- **Embeddings ancorats als eixos**. Variant de *concept bottleneck models* on les direccions principals de l'espai semàntic corresponen als eixos del Meta-Globàlium. La forma actual d'Arkadium utilitza embeddings genèrics (text-embedding-3-small) i el verificador opera sobre les categories citades pel text de sortida; una forma més madura ancoraria els embeddings directament als pols.
- **Process Reward Model basat en completesa dispersa multi-mètrica**. Substituir el RLHF clàssic (recompensa per puntuació humana) per recompensa derivada de la bateria de mètriques canòniques (𝓗, tempeternal_balance, solve_coagula_balance, causal_coverage, epistemic_coverage, voltes_coverage) aplicades a cada pas intermedi del raonament. Estat actual: el verificador d'Arkadium opera sobre la resposta final; el pas següent és aplicar-lo als passos intermedis de la *chain-of-thought*.
- **Activation steering canònic**. Conjunt estandarditzat de vectors d'intervenció corresponents als 80 pols, aplicable a qualsevol LLM open-source. Aquest és el pont natural cap al *representation engineering* (Zou et al. 2023): proporcionar un repertori canònic de direccions verificat reflexivament en lloc de descobertes empíricament.
- **Cicle de quatre fases** (ANA → SIN → AMO → EXP) amb iteració Solve-Coagula com a arquitectura d'inferència auditable estandarditzada, en lloc de la *chain-of-thought* lliure. Arkadium ja implementa aquesta arquitectura; cal estendre-la a *fine-tuning* d'un model open-source perquè el cicle quedi endogenitzat als pesos.
- **Completesa de l'arquitectura fractal**. La base de dades operativa conté actualment **33 expressions tematitzades** (de les 80 ideals = 6400 metacategories). Caldrà completar les 47 restants i revisar les existents amb la mateixa metodologia aplicada al model de principis (pivots estructurals canònics, derivació tempeternal, distribució polysèmica, mappings canònics). El sistema de *frames* en runtime (vegeu §9.1) ja permet la càrrega dinàmica de qualsevol expressió disponible — és la infraestructura preparada per a aquesta extensió incremental.

Properes fites d'Arkadium: ampliació del corpus amb els *8 Quaderns de Globalística*; classificació explícita de la pregunta i activació pre-emptiva de la volta canònica corresponent (les sis voltes detectades); obertura de variants temàtiques A/B/…/V com a *frames* especialitzats; investigació de la **topologia toroïdal Hopf** com a representació geomètrica alternativa.

## 13. Discussió i limitacions

Cap proposta ambiciosa pot aspirar a ser definitiva. El Meta-Globàlium **no és un model definitiu**: és un model *provisional i revisable*, com ho era el Globàlium original de Xirinacs. La provisionalitat és una propietat estructural — el model s'adapta a la cosmovisió de cada moment històric. Arkadium és una versió 1.0 sotmesa voluntàriament a la inspecció pública.

**Arkadium és prova de concepte, no producte de producció**. Cal explicitar-ho per evitar lectures errònies. La implementació actual — agent LLM amb *system prompt*, vector store JSON, càlcul de cosinus en PHP — és deliberadament *frugal i auditable*, no *escalable a milions d'usuaris*. Aquesta opció és intencional: un POC ha de ser **inspeccionable a una sola lectura** per qui vulgui replicar-lo o criticar-lo, no optimitzat per a operació industrial. La justificació tècnica del paper descansa sobre **l'arquitectura** (verificador estructural sobre ontologia externa), no sobre la **implementació** (PHP + JSON). Lectors d'enginyeria de producció haurien de llegir Arkadium com a *arquitectura de referència* que s'ha d'implementar amb *fine-tuning* dedicat i infraestructura adequada (pgvector, FAISS o Milvus, model open-source amb *fine-tuning* al cicle ANA→SIN→AMO→EXP) per a casos d'ús reals — no com a sistema desplegable tal qual. Aquesta migració està al camí d'implementació §12.

Limitacions tècniques actuals d'Arkadium que cal nomenar:

- **Dependència de la qualitat de l'embedding**. Si els embeddings utilitzats no capturen adequadament les relacions dialèctiques, el *retrieval* de categories es degrada. La resposta a llarg termini és l'embedding ancorat als eixos (§11.2); la resposta a curt termini és l'auditoria periòdica del *retrieval* contra anotacions humanes.
- **Cost del re-prompt loop**. La iteració d'autocorrecció duplica el cost computacional quan s'activa. Acceptable per a aplicacions de qualitat alta, costós per a aplicacions de gran volum. La selecció d'aquest tradeoff és parametritzable per cas d'ús.
- **Vector store en JSON**. La implementació actual d'Arkadium utilitza JSON local + cosinus en PHP, adequat per a l'escala del corpus actual (de l'ordre de 100 categories) però migrable a pgvector o equivalent si el corpus creix per sobre dels 10 000 elements.
- **Dependència del *system prompt*** per ancorar el model. La forma actual depèn que el LLM segueixi el *system prompt* amb fidelitat raonable; un *fine-tuning* específic seria més robust i és part del camí d'implementació (§11.5).

Riscos d'interpretació pública que cal anticipar:

- L'usuari final pot llegir la *completesa dispersa* com a **relativisme moral**. No ho és. La funció 𝓗 opera sobre respostes ja factualment correctes; és un filtre d'integritat estructural i de plenitud epistèmica (veritat globalística), no un càlcul de moralitat. Una resposta factualment falsa segueix sent falsa amb 𝓗 = 1. Que de la veritat plena en derivi el Bé com a harmonia és l'aportació xirinaquiana de fons; el verificador no usurpa aquesta derivació.
- El model pot ser percebut com a **catalanocèntric**. La genealogia del Globàlium és catalana (Llull-Sibiuda-Pujols-Xirinacs), però els eixos són reflexius — subjecte/objecte, teoria/pràctica, fenomen/noümen, plasma/món són universals filosòfics. La genealogia és el lloc d'articulació; els eixos són universals.
- Risc de **sobreajustament a la pròpia ontologia**: el model podria optimitzar la funció 𝓗 com a *proxy* sense interioritzar-ne el sentit. La defensa és estructural: 𝓗 no és l'únic criteri sinó una capa damunt de la correctesa factual, i les categories tocades han d'aparèixer associades a contingut substantiu. Auditories periòdiques contrastades amb anotacions humanes són el mecanisme de detecció previst.

### 13.b Objeccions previstes

Aquesta secció anticipa deu objeccions raonablement esperables d'un revisor extern i hi respon explícitament. La majoria d'aquestes objeccions ja troben resposta dispersa al cos del paper; aquí queden agrupades per facilitar-ne la consulta.

Objecció 1. «Per què 8 quadrants i no més o menys?»
Tres consideracions justifiquen la granularitat (vegeu §4.1): *estructural* (8 = 2³ + radial cobreix les distincions filosòfiques fonamentals), *cognitiva* (Miller 1956: 7±2 elements simultàniament inspeccionables per humans), i *operativa* (granularitat òptima entre col·lapse de distincions i sparseness estadística). El nivell 6400 metacategories ofereix granularitat fina sense abandonar els 8 quadrants com a projecció.

Objecció 2. «No és un estudi empíric sinó una prova de concepte»
Correcte. La §9.3.b ho reconeix explícitament i descriu el pla de validació V1.1 (100 preguntes × 5 condicions × 3 anotadors humans, prevista per als propers 6 mesos). Les afirmacions sobre 𝓗 com a indicador de qualitat queden, fins llavors, com a hipòtesis fonamentades teòricament però empíricament no validades. Arkadium és *arquitectura de referència*, no producte de producció (§13).

Objecció 3. «Les 80 categories són culturalment esbiaixades»
L'arquitectura sí que ho és: el Globàlium és patrimoni filosòfic català desenvolupat per Xirinacs (§1). Els *eixos*, però, no ho són — OBJ-SUB, TEO-PRA, FEN-NOU, PLA-MON són distincions presents a la fenomenologia europea, l'idealisme alemany, l'hermenèutica i el budisme zen. La genealogia és cultural; els eixos són operatius. Això no exclou que altres tradicions desenvolupin variants del Meta-Globàlium amb categories ajustades a les seves prioritats — el sistema és precisament *provisional i revisable* per disseny.

Objecció 4. «El *reward hacking* és igualment possible si el model coneix els quadrants»
Parcialment cert. Un model que sàpiga que 𝓗 puntua sobre 8 quadrants pot diversificar superficialment les seves respostes per maximitzar la cobertura sense raonament genuí. La defensa té tres capes: (i) la geometria és *externa al model* — la projecció a quadrants la fa el verificador, no el model; (ii) la cobertura ha d'aparèixer associada a contingut substantiu, no només a etiquetes; (iii) auditories periòdiques amb anotació humana detectaran patrons de cobertura merament etiquetada. La robustesa al hacking és una qüestió empírica que el subgrup de robustesa del pla V1.1 (§9.3.b) està dissenyat per quantificar.

Objecció 5. «El manifest és catalanocèntric»
La genealogia citada (Llull → Sibiuda → Pujols → Xirinacs) és catalana, sí. Aquesta tria és *fonamentada documentalment* i no aspira a substituir altres tradicions filosòfiques globals. Que els pols del model siguin universals filosòfics (subjecte/objecte, teoria/pràctica, fenomen/noümen) implica que la mateixa arquitectura pot articular-se amb genealogies diferents — Madhyamaka, vedanta, taoisme, hegelianisme. El Meta-Globàlium *no reclama* apropiació cultural sinó *operacionalització* d'una intuïció comuna a múltiples tradicions integradores.

Objecció 6. «Els principis dialèctics no són matemàticament originals»
Cert, i el paper ho reconeix explícitament (§4.4, nota sobre l'originalitat). La fórmula 𝓗 combina mètriques estàndard de teoria de la informació; els sis principis reformulen continguts dialèctics presents a la tradició filosòfica. La **contribució original** és *arquitectònica*: el desplaçament del lloc de la verificació d'una constitució textual interpretable pel propi model a una geometria ontològica externa, calculable com a propietat estructural objectiva (§4.2).

Objecció 7. «La hipersfera és metàfora, no geometria operativa»
La projecció és matemàticament definida i computacionalment implementada (§4.1). La hipersfera 4D no és lletra morta: cada categoria té coordenades cartesianes assignades, la projecció cap als 8 quadrants primaris és una operació mecànica, i la mètrica 𝓗 es calcula explícitament en runtime sobre cada resposta. El codi del verificador és accessible i auditable (§9.4). La metàfora geomètrica és una visualització; la geometria és operativa.

Objecció 8. «No es prova que 𝓗 alta = qualitat humana»
No, no es prova encara. Aquesta és la limitació metodològica més seriosa, reconeguda explícitament (§9.3.b). El pla d'estudi V1.1 té com a hipòtesi central precisament aquesta correlació, mesurada amb anotació humana doble cega sobre cinc dimensions de qualitat. Fins als resultats d'aquest estudi, el paper reclama 𝓗 com a *propietat estructural objectiva* (no-omissió de pols dialèctics), *no* com a mètrica de qualitat humana validada.

Objecció 9. «Xirinacs no és figura acadèmica reconeguda al món AI alignment actual»
La tesi *Un model global de la realitat* (1997, presentada en català) és peer-reviewed: defensada a la Universitat de Barcelona amb tribunal acadèmic. Que Xirinacs sigui també figura pública catalana coneguda per altres motius no afebleix la qualitat acadèmica de la tesi, que va ser publicada al repositori UB i es manté com a referència vigent. El paper cita la tesi com a obra acadèmica, no la persona pública.

Objecció 10. «Què passa quan la pregunta no té estructura dialèctica genuïna?»
Bona pregunta. Per a preguntes factuals simples («Quina és la capital de França?») la dialecticitat és espúria i 𝓗 no aporta valor — la resposta correcta toca un sol pol (OBJ) i això és apropiat. El verificador estructural està dissenyat per a *dominis humans* on la pluralitat d'accés és constitutiva (ètica, política, judici social, deliberació pública). La selecció de volta segons tipus de pregunta (§4.5.b) preveu aquest escenari: la *volta d'aplicació* opera sobre raonament; la *volta de coneixement* sobre l'aprenentatge; la *volta d'orientació* sobre la direcció personal i el sentit. Un router previ identifica el tipus de pregunta i selecciona la volta apropiada — funcionalitat del roadmap (§12), no encara implementada.

## 13.c Una missió col·lectiva: reorganitzar el coneixement humà

L'argumentari fins aquí ha presentat Arkadium com a prova de concepte d'un verificador estructural i com a candidata a AGI en sentit estricte. Tanquem la part substantiva del paper amb el marc que situa el projecte dins d'un horitzó de més llarg termini. **L'objectiu d'Arkadium no s'esgota en si mateix**. El sistema desplegat és una primera implementació, no la fita. La fita és molt més àmplia i només pot perseguir-la el treball col·lectiu: **reorganitzar el coneixement humà de maneres millors i més pedagògiques**, sobre una geometria comuna que el faci alhora navegable, comparable i transmissible.

Cada disciplina, cada tradició, cada saber pràctic ha generat històricament les seves pròpies cartografies internes. La interdisciplinarietat ha estat l'art difícil de traduir entre aquestes cartografies *ad hoc*, perdent gairebé sempre la coherència estructural en el viatge. La hipòtesi fractal del Meta-Globàlium (§4) — que els mateixos eixos dialèctics es projecten sobre qualsevol àmbit — és, abans de res, una **hipòtesi pedagògica**: si funciona, qualsevol disciplina pot ser ensenyada des dels mateixos primitius reflexius reconeixibles per qualsevol humà, i el viatge entre disciplines deixa de demanar traduccions especialitzades per descansar sobre una geometria compartida. Les 33 expressions tematitzades ja actives en runtime (§9.1, sistema de *frames*) són la primera prova empírica d'aquesta hipòtesi a escala.

Aquesta tasca depassa el que un sol projecte pot fer. La requereix una xarxa: especialistes de cada domini que projectin el seu camp sobre el model, pedagogs que en derivin itineraris d'aprenentatge, traductors entre tradicions filosòfiques que ampliïn la llista d'eixos universals (§8 ja n'anticipa la lectura per al llinatge integrador català), comunitats educatives i cooperatives que la posin en pràctica, i contribuïdors de programari que mantinguin la infraestructura oberta. **Aquest és, precisament, el tipus de tasca per a la qual les intel·ligències generals ancorades estructuralment estan dissenyades**: no per substituir el treball humà col·lectiu, sinó per amplificar-lo, donar-li infraestructura compartida i fer-ne explícita la coordinació. AGIs com la que aquí proposem — ancorades a un model global — fan possible per primer cop un esforç coordinat de reorganització del coneixement que no violenti la riquesa de les seves tradicions particulars.

Això reobre una pregunta que la modernitat havia abandonat com a impossible: *és reorganitzable el coneixement humà sobre uns eixos comuns sense violentar la pluralitat de les seves tradicions?* El llinatge del Globàlium (Llull, Sibiuda, Pujols, Xirinacs) i l'arquitectura fractal contemporània suggereixen que la resposta és sí — sempre que la geometria sigui dialèctica, els eixos universals-i-revisables, i la validació pública i oberta. **Arkadium n'ofereix el primer fragment funcional**. La resta s'ha de construir col·lectivament, a través d'institucions, llengües i tradicions. Esperem que el projecte sigui avaluat no només com a proposta d'*alignment*, sinó com a llavor d'una **infraestructura cognitiva compartida** — oberta, fractal i contínuament refinada.

## 14. Conclusió

La via dominant del desenvolupament d'IA — escala bruta + RLHF + constitucions textuals — té un sostre visible. Aquest sostre no és tecnològic en el sentit estret: és estructural. Apareix quan el sistema ha d'operar en dominis sense veritat de referència, on no hi ha verificador formal, i on el judici humà no es pot reduir a una llista de regles textualment interpretables.

Hi ha una segona via — oberta i sobirana — que reclama un posicionament tècnic diferenciat, articulada en els **dos nivells del nostre treball** que aquest paper ha presentat, ancorats en una font d'inspiració filosòfica prèvia. El **Globàlium** de Xirinacs (1997), patrimoni del pensament integrador català, ofereix la cartografia filosòfica original que ens inspira — citem com a font, no com a part del nostre treball. El **Meta-Globàlium** que hem desenvolupat (Berenguer / Opengea) és la formalització computacional que dota aquesta cartografia de molta més resolució i hi connecta una jugada filosòfica original: una **funció de completesa dispersa** sobre l'ontologia, justificada com a operacionalització de la **veritat globalística** — una concepció no-monològica de la veritat, compatible amb la tradició hermenèutica i comunicativa de fons (Gadamer, Habermas, Heidegger). En el llinatge xirinaquià, d'aquesta plenitud dialèctica se'n deriva, com a llegat ètic honorat amb respecte, el **Bé com a harmonia entre parts** — herència, no output algorísmic. **Arkadium** (Berenguer / Opengea) és l'agent neuro-simbòlic que materialitza aquesta arquitectura — l'aplicació web, el framework RAG, el verificador 𝓗, el Metamodeler 3D, la trajectòria de cobertura per usuari amb conformitat GDPR. Vist en perspectiva històrica, la jugada que aquesta proposta materialitza és l'aplicació computacional d'una intuïció antiga: que el cercle — i la seva extensió a l'esfera, i a l'**esfera-n** de dimensió superior — pot ser, en el camp del raonament, una eina anàloga al que la roda va ser en el camp físic. Berenguer (*Globàlium · petit manual*, 2024) recull aquesta intuïció parlant del Globàlium com a invenció de la **roda mental** — una forma geomètrica simple feta operativa que ens deslliuraria del pensament lineal o bipolar per obrir-nos a un *pensament corb*, multidimensional. La intuïció apareix recurrentment de Llull a Xirinacs; el mateix Xirinacs (1997) ja en va proposar una formalització matemàtica concebuda explícitament per a una realització computacional futura, llavors no factible amb les eines del seu temps. El Meta-Globàlium retoma aquesta línia i la porta a substrat de càlcul efectiu sobre les tecnologies actuals d'IA. Els dos nivells del nostre treball pressuposen la font, però no la substitueixen.

Arkadium és, doncs, **la primera materialització funcional** d'aquesta proposta. No és hipotètica: està desplegada, és accessible, és inspeccionable, és criticable. La invitació no és «construïm el Meta-Globàlium junts» en abstracte — això ja s'ha fet —; és **«useu Arkadium, contribuïu-hi i esteneu-lo»**. Esperem aportacions de quatre tipus:

- **Tècniques**: formalització en OWL/RDF, *fine-tuning* d'un model open-source amb el cicle ANA → SIN → AMO → EXP endogenitzat, *activation steering* canònic basat en els 80 pols, mètriques d'avaluació ètica que utilitzin 𝓗 com a dimensió afegida, integració del verificador d'Arkadium amb d'altres frameworks RAG.
- **Filosòfiques**: extensió i revisió del Meta-Globàlium — com el seu propi inventor demanava per al Globàlium —, exploració de variants temàtiques A/B/.../V projectades sobre dominis especialitzats, investigació de la topologia toroïdal Hopf com a representació alternativa.
- **D'aplicació**: ús d'Arkadium per a casos concrets (deliberació pública, ètica aplicada, educació, mediació), retroalimentació empírica sobre la funció 𝓗 en contextos reals, identificació de biaixos sistemàtics que l'auditoria pugui detectar.
- **Institucionals**: incorporació a iniciatives de sobirania digital, projectes de recerca acadèmica, programes d'IA pública, partenariats amb administracions i organitzacions de la societat civil.

Comentaris, crítiques i col·laboracions són benvinguts a [opengea.org](https://opengea.org) i a través del *dashboard* d'Arkadium mateix. El codi del verificador i del *system prompt* s'està obrint al repositori opengea/arkadium sota llicència Apache 2.0.

Tres anys després de *Saviesa Artificial*, el camp ha confirmat l'orientació general — el neuro-simbòlic com a estratègia industrial, la necessitat de millors *priors* estructurals, la centralitat del problema del verificador. El que ara és necessari és l'esforç col·lectiu per portar aquesta intuïció a sistemes operatius reals, en infraestructures plurals, sota llicències obertes. Arkadium és la nostra contribució a aquest esforç. La seva genealogia és catalana però la seva intenció és universal — i la seva utilitat es jutjarà, com volia Xirinacs, per la utilitat efectiva i no per cap pretensió de veritat última. Com recorda Berenguer al *Globàlium · petit manual* (2024), avui podem **caminar a espatlles de gegants** — Llull, Sibiuda, Pujols, Xirinacs i tants altres pensadors integradors —; el repte que aquest paper formalitza és recollir i articular harmònicament aquest llegat per portar-lo a l'època de la computació.

Arkadium és la primera materialització funcional del moviment dels **models predictius** als **models de judici**. Aquesta és la frontera tècnica i filosòfica del 2026.

Referències



- Agustí-Cullell, J. &amp; Schorlemmer, M. (2021). *A Humanist Perspective on Artificial Intelligence*. COMPRENDRE — Revista Catalana de Filosofia, Vol. 23/1, p. 99–125.
- Bai, Y., Kadavath, S., Kundu, S., Askell, A., Kernion, J., et al. (2022). *Constitutional AI: Harmlessness from AI Feedback*. Anthropic. arXiv:2212.08073. [arxiv.org/abs/2212.08073](https://arxiv.org/abs/2212.08073)
- Berenguer, J. (2023). *Saviesa Artificial*. Quadern de Globalística. Opengea SCCL, Barcelona. [opengea.org](https://www.opengea.org)
- Berenguer, J. (2024). *Globàlium petit manual*. Edició de desembre de 2024. Opengea SCCL, Barcelona.
- Berenguer, J. (en preparació). *Globalística — Estudi i aplicació de models globals de la realitat*. Opengea SCCL.
- Berenguer, J. (2026). *Una IA més humana és possible · Manifest divulgatiu d'Arkadium*. Opengea SCCL. [https://arkadium.ai/manifest/](https://arkadium.ai/manifest/)
- DeepSeek-AI (2025). *DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning*. arXiv:2501.12948. [arxiv.org/abs/2501.12948](https://arxiv.org/abs/2501.12948)
- Edge, D., Trinh, H., Cheng, N., Bradley, J., Chao, A., Mody, A., Truitt, S., Metropolitansky, D., Ness, R. O., Larson, J. (2024). *From Local to Global: A Graph RAG Approach to Query-Focused Summarization*. Microsoft Research. arXiv:2404.16130. [arxiv.org/abs/2404.16130](https://arxiv.org/abs/2404.16130)
- Google DeepMind (2024). *AI achieves silver-medal standard solving International Mathematical Olympiad problems*. [deepmind.google](https://deepmind.google/blog/ai-solves-imo-problems-at-silver-medal-level/)
- Google DeepMind (2025). *Advanced version of Gemini with Deep Think officially achieves gold-medal standard at the International Mathematical Olympiad*.
- Grossmann, I., et al. (2024). *Dimensions of wisdom perception across twelve countries on five continents*. Nature Communications.
- Grossmann, I., Johnson, S., et al. (2024). *Imagining and building wise machines: the centrality of AI metacognition*. Trends in Cognitive Sciences (in press).
- OpenAI (2024). *Deliberative Alignment* [referència tècnica corporativa, document blanc].
- Shojaee, P., et al. (2025). *The Illusion of Thinking: Understanding the Strengths and Limitations of Reasoning Models via the Lens of Problem Complexity*. Apple Machine Learning Research. arXiv:2506.06941. [arxiv.org/abs/2506.06941](https://arxiv.org/abs/2506.06941)
- Turpin, M., Michael, J., Perez, E., Bowman, S. R. (2023). *Language Models Don't Always Say What They Think: Unfaithful Explanations in Chain-of-Thought Prompting*. NeurIPS 2023. arXiv:2305.04388. [arxiv.org/abs/2305.04388](https://arxiv.org/abs/2305.04388)
- Xirinacs, L. M. (1997). *Un model global de la realitat*. Tesi doctoral, Universitat de Barcelona (presentada en català). Repositori UB: [diposit.ub.edu](http://diposit.ub.edu/dspace/handle/2445/66451)
- Zou, A., Phan, L., Chen, S., Campbell, J., Guo, P., Ren, R., et al. (2023). *Representation Engineering: A Top-Down Approach to AI Transparency*. arXiv:2310.01405. [arxiv.org/abs/2310.01405](https://arxiv.org/abs/2310.01405)


Com citar aquest paper

Aquest manifest és un document acadèmic citable. Per a citació formal, s'ofereixen tres formats estàndard:

### APA (7a edició)

Berenguer Rodrigo, J. (2026). Arkadium: un agent neuro-simbòlic ancorat
al Meta-Globàlium per a la verificació estructural del judici humà en
sistemes d'intel·ligència artificial (Manifest v1.4). Opengea SCCL.
https://arkadium.ai/papers/arkadium/

### Chicago (autor-data)

Berenguer Rodrigo, Jordi. 2026. "Arkadium: un agent neuro-simbòlic
ancorat al Meta-Globàlium per a la verificació estructural del judici
humà en sistemes d'intel·ligència artificial." Versió 1.4.
Barcelona: Opengea SCCL. https://arkadium.ai/papers/arkadium/ca/.

### BibTeX

@misc{berenguer2026arkadium,
author = {Berenguer Rodrigo, Jordi},
title = {Arkadium: un agent neuro-simb\`{o}lic ancorat al
Meta-Glob\`{a}lium per a la verificaci\'{o} estructural
del judici hum\`{a} en sistemes d'intel{\textperiodcentered}
lig\`{e}ncia artificial},
year = {2026},
version = {1.4},
howpublished = {Paper. Opengea SCCL, Barcelona},
url = {https://arkadium.ai/papers/arkadium/ca/},
note = {Disponible en català i amb resum en anglès}
}
