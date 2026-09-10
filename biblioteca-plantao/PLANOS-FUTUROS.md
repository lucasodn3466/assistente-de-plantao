[← Índice geral](00-INDICE-GERAL.md)

# 🚀 PLANOS FUTUROS — Expansão e reestruturação da biblioteca

Documento para rastrear ideias de evolução, novos protocolos, melhorias e reestruturações planejadas para a **Assistente de Plantão**.

> **Como usar:** adicione itens conforme surgem. Organize por categoria. Quando começar trabalho em um item, mude o status para "em desenvolvimento". Quando concluir, mude para "✅ pronto".

---

## 🗺️ ÍNDICE PROJETADO (alvo)

> Estrutura-alvo fechada em 10/09/2026. **Documento de planejamento — não colar em `00-INDICE-GERAL.md`.** O índice geral só muda quando os arquivos forem de fato criados e movidos.

### 📁 Estrutura de pastas — DECIDIDO E EXECUTADO em 10/09/2026 (branch `restruturacao-pastas`)

A biblioteca **deixa de ser flat**. Motivo: com ~130 arquivos e uma seção 01 de ~57, a lista plana vira parede — pior de acessar no plantão, que é exatamente o que a estrutura deveria facilitar.

**Formato escolhido: um nível de pastas, sem aninhamento.** As 11 subseções de Emergências Clínicas viram pastas de primeiro nível (`01a-cardiologia/` … `01k-medicina-intensiva/`), não subpastas de uma pasta `01`. A ordenação alfabética mantém 01a–01k adjacentes, então a seção continua se lendo como um bloco.

```
biblioteca-plantao/
  00-INDICE-GERAL.md          ← arquivos de apoio ficam na raiz
  00-LEIA-PRIMEIRO.md
  99-TEMPLATES.md
  CHANGELOG-MERGE.md
  PLANOS-FUTUROS.md
  00-sindromico/            13
  01a-cardiologia/          11
  01b-pneumologia/           4
  01c-neurologia/            2
  01d-endocrinologia/        3
  01e-gastro-hepatologia/    5
  01f-nefrologia/            8
  01g-toxicologia/          11
  01h-infectologia-grave/    3
  01i-alergologia/           2
  01j-hematologia/           4
  01k-medicina-intensiva/    4
  02-cirurgia-trauma/        7
  03-go-obstetricia/         7
  04-pediatria/              4
  05-infectologia/          11
  06-ortopedia/              5
  07-oftalmo-orl/            2
  08-dermatologia/           2
  09-dor-cronica-queixas-recorrentes/   3
  10-psiquiatria-urgencia/   3
  11-paciente-retido/        2
  12-queixa-vaga-simulacao/  2
  13-regulacao/              1
  14-farmacologia-plantao/   1
  15-scores-calculadoras/    1
  16-procedimentos/          8
```

**Regras que continuam valendo:**
- **Um nível só.** Nada de subpasta dentro de subpasta.
- **Nome do arquivo = código da pasta + `__` + número + tema** (`01h__01-sepse-choque-septico.md`), com o número em dois dígitos. O código curto (`01h`, `05`, `16`) existe em uma única pasta, então os basenames seguem globalmente únicos — isso mata por construção o risco de basename duplicado que já quebrou os links relativos deste vault uma vez.
- **Links relativos.** O link do topo de cada protocolo é `../00-INDICE-GERAL.md`; os cruzados entre seções são `../pasta/arquivo.md`; no mesmo diretório, só o nome. A reescrita foi scriptada, não manual.
- **Fechar o Obsidian antes de mover.** Com `alwaysUpdateLinks: true` ele reescreve links sozinho durante a movimentação e briga com o script.

| Seção | Nome | Hoje | Alvo | Mudança |
|---|---|---|---|---|
| 00 | Porta sindrômica | 13 | 13 | sem mudança |
| — | **Semiologia** | — | a definir | seção nova; local no índice ainda em aberto |
| 01 | Emergências clínicas | 15 | ~57 | subdividida em 11 subseções (01a–01k) |
| 02 | Cirurgia e trauma | 7 | 7 | sem mudança |
| 03 | GO e obstetrícia | 7 | 7 | sem mudança |
| 04 | Pediatria | 4 | 4 | sem mudança |
| 05 | **Infectologia** | — | 11 | seção nova; número reaproveitado (era psiquiatria) |
| 06 | Ortopedia | 5 | 5 | sem mudança |
| 07 | Oftalmo e ORL | 2 | 2 | sem mudança |
| 08 | Dermatologia | 2 | 2 | sem mudança |
| 09 | Dor crônica e queixas recorrentes | 4 | 3 | perde crise falcêmica para 01j |
| 10 | Psiquiatria de urgência | 4 (hoje em 05) | 3 | movida de 05; perde abstinência/intoxicações para 01g |
| ~~10~~ | ~~Acidentes peçonhentos~~ | 4 | — | absorvida por 01g; é o que libera o número 10 |
| 11 | Paciente retido | 2 | 2 | sem mudança |
| 12 | Queixa vaga e documentação | 2 | 2 | sem mudança |
| 13 | Regulação | 1 | 1 | sem mudança |
| 14 | Farmacologia de plantão | 2 | 1 | perde ATB empírico por foco para 05 |
| 15 | Scores e calculadoras | 1 | 1 | sem mudança |
| 16 | Procedimentos | 7 | 8 | + paracentese |

### Seção 01 — subseções

| Sub | Nome | Conteúdo | Qtd |
|---|---|---|---|
| 01a | Cardiologia | IAM com supra, SCA sem supra, taquiarritmias, bradiarritmias, crise hipertensiva, EAP/IC descompensada, tamponamento cardíaco, miocardite, pericardite, síndrome aórtica aguda, QT longo | 11 |
| 01b | Pneumologia | asma/DPOC, TEP, derrame pleural, PAC | 4 |
| 01c | Neurologia | AVC agudo, crise convulsiva/EME | 2 |
| 01d | Endocrinologia | CAD/EHH/hipoglicemia, crise tireotóxica/coma mixedematoso, insuficiência adrenal aguda | 3 |
| 01e | Gastro/Hepatologia | encefalopatia hepática, PBE, ascite/cirrose, síndrome hepatorrenal, hepatite alcoólica | 5 |
| 01f | Nefrologia | LRA, rabdomiólise, sódio, potássio + ECG, cálcio, magnésio, fósforo, ácido-base | 8 |
| 01g | Toxicologia | abstinência alcoólica/intoxicações, paracetamol, tricíclicos, lítio, carbamazepina, organofosforados, digitálicos, ofídico, escorpiônico, aranhas, mordeduras/raiva/tétano | 11 |
| 01h | Infectologia grave | sepse/choque séptico, meningite aguda, encefalite viral | 3 |
| 01i | Alergologia | anafilaxia, angioedema | 2 |
| 01j | Hematologia | crise falcêmica, reversão de varfarina, reversão de DOAC, reações transfusionais | 4 |
| 01k | Medicina intensiva | PCR/ACLS, via aérea/SRI, choque circulatório, ventilação mecânica | 4 |

> Sobreposição entre 01h (sepse) e 01k (choque) é esperada e ok — coesão > pureza taxonômica.

---

## 📋 NOVOS PROTOCOLOS

| Protocolo | Destino | Status | Notas |
|-----------|---------|--------|-------|
| Tamponamento cardíaco | 01a Cardiologia | ⏳ planejado | |
| Miocardite | 01a Cardiologia | ⏳ planejado | |
| Pericardite | 01a Cardiologia | ⏳ planejado | |
| Síndrome aórtica aguda | 01a Cardiologia | ⏳ planejado | |
| QT longo | 01a Cardiologia | ⏳ planejado | |
| Derrame pleural | 01b Pneumologia | ⏳ planejado | |
| Pneumonia adquirida na comunidade | 01b Pneumologia | ⏳ planejado | Destino mudou: era Infectologia, agora Pneumologia |
| Crise tireotóxica e coma mixedematoso | 01d Endocrinologia | ⏳ planejado | |
| Insuficiência adrenal aguda | 01d Endocrinologia | ⏳ planejado | |
| Encefalopatia hepática | 01e Gastro/Hepatologia | ⏳ planejado | |
| Peritonite bacteriana espontânea | 01e Gastro/Hepatologia | ⏳ planejado | |
| Ascite e cirrose descompensada | 01e Gastro/Hepatologia | ⏳ planejado | Escrever junto com paracentese (seção 16) |
| Síndrome hepatorrenal | 01e Gastro/Hepatologia | ⏳ planejado | |
| Hepatite alcoólica | 01e Gastro/Hepatologia | ⏳ planejado | |
| Lesão renal aguda | 01f Nefrologia | ⏳ planejado | Causas pré e pós-renal, indicação de diálise de urgência |
| Rabdomiólise | 01f Nefrologia | ⏳ planejado | |
| Distúrbios do sódio | 01f Nefrologia | ⏳ planejado | Hiponatremia e hipernatremia. Hoje fragmentado dentro de outros protocolos |
| Distúrbios do potássio + ECG | 01f Nefrologia | ⏳ planejado | Hipercalemia e hipocalemia. Hoje fragmentado dentro de PCR |
| Distúrbios do cálcio | 01f Nefrologia | ⏳ planejado | |
| Distúrbios do magnésio | 01f Nefrologia | ⏳ planejado | |
| Distúrbios do fósforo | 01f Nefrologia | ⏳ planejado | |
| Distúrbios ácido-base | 01f Nefrologia | ⏳ planejado | |
| Intoxicação por paracetamol | 01g Toxicologia | ⏳ planejado | |
| Intoxicação por tricíclicos | 01g Toxicologia | ⏳ planejado | |
| Intoxicação por lítio | 01g Toxicologia | ⏳ planejado | |
| Intoxicação por carbamazepina | 01g Toxicologia | ⏳ planejado | |
| Intoxicação por organofosforados | 01g Toxicologia | ⏳ planejado | |
| Intoxicação digitálica | 01g Toxicologia | ⏳ planejado | |
| Meningite aguda | 01h Infectologia grave | ⏳ planejado | |
| Encefalite viral | 01h Infectologia grave | ⏳ planejado | |
| Angioedema | 01i Alergologia | ⏳ planejado | |
| Reversão de varfarina | 01j Hematologia | ⏳ planejado | |
| Reversão de DOAC | 01j Hematologia | ⏳ planejado | |
| Reações transfusionais | 01j Hematologia | ⏳ planejado | |
| Choque circulatório | 01k Medicina intensiva | ⏳ planejado | Sobreposição esperada com sepse (01h) |
| Ventilação mecânica | 01k Medicina intensiva | ⏳ planejado | |
| ITU baixa e pielonefrite | 05 Infectologia | ⏳ planejado | |
| Celulite e erisipela | 05 Infectologia | ⏳ planejado | ⚠️ Checar sobreposição com `08-dermatologia__02-infeccoes-pele-partes-moles.md` ao escrever |
| Faringoamigdalite, sinusite e otite | 05 Infectologia | ⏳ planejado | |
| Gastroenterite e infecções entéricas | 05 Infectologia | ⏳ planejado | |
| Infecções sexualmente transmissíveis | 05 Infectologia | ⏳ planejado | Cobrir decisão de tratar e ambulatorial × internar |
| Arboviroses e febre maculosa | 05 Infectologia | ⏳ planejado | Dengue, chikungunya, zika, febre amarela |
| Malária e leishmaniose visceral | 05 Infectologia | ⏳ planejado | |
| Leishmaniose cutânea, hanseníase e paracoccidioidomicose | 05 Infectologia | ⏳ planejado | |
| Tuberculose | 05 Infectologia | ⏳ planejado | |
| Doença de Chagas | 05 Infectologia | ⏳ planejado | |
| Paracentese | 16 Procedimentos | ⏳ planejado | Procedimento próprio no livro de Ribeirão Preto; escrever junto com 01e |
| Semiologia (conteúdo a definir) | Semiologia | ⏳ planejado | Esqueleto de arquivo e local no índice ainda em aberto |

---

## 🏗️ REESTRUTURAÇÃO / MELHORIAS NA BIBLIOTECA

| Item | Escopo | Status | Notas |
|------|--------|--------|-------|
| **Migrar de flat para pastas de um nível** | Toda a biblioteca | 🟢 feito | 82 arquivos → 25 pastas na branch `restruturacao-pastas`, esquema D. 1235 links verificados, 0 quebrados |
| Subdividir Emergências clínicas em subseções | Seção 01 | 🟢 feito | Os 15 arquivos atuais foram para 01a/01b/01c/01d/01g/01h/01i/01j/01k. 01e Gastro-Hepato e 01f Nefrologia nascem com o primeiro arquivo |
| Criar seção 05 · Infectologia | Nova seção | 🟢 feito | Pasta criada com o ATB empírico. Estrutura interna sindrômica ainda em aberto |
| Mover Psiquiatria de urgência de 05 para 10 | 3 arquivos | 🟢 feito | |
| Absorver Acidentes peçonhentos (10) em 01g Toxicologia | 4 arquivos | 🟢 feito | Ficaram em 01g__08 a 01g__11; 01g__02 a 01g__07 reservados para as intoxicações planejadas |
| Migrar ATB empírico por foco de 14 para 05 | 1 arquivo | 🟢 feito | Virou `05__01-antibioticos-empiricos-por-foco.md`. A 14 ficou só com vasoativas/sedação/analgesia |
| Mover crise falcêmica de 09 para 01j | 1 arquivo | 🟢 feito | A 09 ficou com 3 arquivos |
| Mover abstinência alcoólica e intoxicações de 05 para 01g | 1 arquivo | 🟢 feito | Virou `01g__01` |
| Criar seção Semiologia | Nova seção | ⏳ planejado | Local dentro do índice em aberto; não necessariamente na porta sindrômica |
| Atualizar índice geral e links internos | Toda a biblioteca | 🟢 feito | `00-INDICE-GERAL.md` reagrupado nas subseções novas; todos os links relativos reescritos e verificados |

---

## ⚠️ DECISÕES EM ABERTO

1. **Nome "Infectologia grave" (01h) × "Infectologia" (05)** — parecidos, conteúdo bem diferente. Talvez renomear um dos dois.
2. **Estrutura sindrômica interna da seção 05 (Infectologia)** — como agrupar os protocolos ainda não definido.
3. **Semiologia** — local dentro do índice e esqueleto de arquivo ainda não fechados. Conteúdo listado em conversa anterior.
4. **Desmembrar a biblioteca em duas** (Emergências × Urgências/Pequenas emergências) — decisão futura, sem ação agora.

---

## 🌐 FASE 3 — CAMADA LOCAL (locais/)

| Serviço | Status | Perfil pronto? | Observações |
|---------|--------|----------------|-------------|
| | ⏳ planejado | [ ] | |

---

## 💡 IDEIAS E FEEDBACK

Observações gerais, sugestões de colegas, ou melhorias menores que ainda não têm espaço próprio:

- **Infectologia por síndrome**: nova aba organizada por síndrome infecciosa (não por decisão terapêutica isolada), no mesmo espírito generalista do resto da biblioteca — funciona em qualquer PA, não amarrado a um serviço específico.

- **Guia Prático de Emergências Clínicas** (Unidade de Emergência, HC-FMRP-USP, Ribeirão Preto) — 14 capítulos, 141 subcapítulos. ✅ **Já consultado (10/09/2026).** Sumário cruzado capítulo a capítulo com o índice atual; o resultado é a estrutura-alvo registrada em [Índice projetado](#️-índice-projetado-alvo), incluindo as 11 subseções de Emergências Clínicas e a paracentese na seção 16.

- **Minor Emergencies** (Buttaravoli, Leffler & Herrington, 4ª edição) — usar como espinha para o futuro módulo de baixa acuidade (fichas verde e amarela). Já organizado por sistema (neurológico e psiquiátrico, oftalmológico, otorrino etc.), cobre ~200 apresentações no formato "o que fazer / o que não fazer" — formato compatível com o estilo enxuto já usado na biblioteca.

---

## ✅ PRÓXIMAS TAREFAS

> Só o que vem a seguir. A fila completa está nas tabelas acima.

**Estrutura**
- [x] Migrar a biblioteca para pastas de um nível — branch `restruturacao-pastas`
- [x] Atualizar `00-INDICE-GERAL.md` e os links internos
- [x] Bump de versão para 2.0 (Setembro de 2026)

**Decisões em aberto**
- [ ] Nome: 01h Infectologia grave × 05 Infectologia
- [ ] Estrutura interna da seção 05
- [ ] Onde entra Semiologia
- [ ] Dividir a biblioteca em duas?

**Escrita — primeiros da fila**
- [ ] 01f Nefrologia — distúrbios do sódio, distúrbios do potássio + ECG
- [ ] 01e Gastro/Hepatologia — encefalopatia hepática, PBE
- [ ] 16 Procedimentos — paracentese, junto com ascite/cirrose

**Camada local**
- [ ] Instanciar o primeiro perfil de serviço em `locais/`

---

## 🔄 HISTÓRICO DE MUDANÇAS

| Data | Item | Status anterior | Status novo | Responsável |
|------|------|-----------------|-------------|-------------|
| 2026-09-10 | Índice projetado e plano de reestruturação | — | ⏳ planejado | Lucas |
| 2026-09-10 | Estrutura de pastas (flat → um nível, esquema D) | em aberto | ✅ decidido | Lucas |
| 2026-09-10 | Migração executada: 82 arquivos → 25 pastas, índice reagrupado, 1235 links OK | ⏳ planejado | 🟢 feito na branch `restruturacao-pastas` | Claude + Lucas |

---

**Última atualização:** 2026-09-10  
**Revisar regularmente** — a cada trimestre ou sempre que novas ideias surjam
