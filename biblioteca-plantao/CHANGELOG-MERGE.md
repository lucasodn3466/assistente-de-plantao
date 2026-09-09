[← Índice geral](00-INDICE-GERAL.md)

# CHANGELOG — merge das bibliotecas de plantão

Registro do trabalho de fusão entre as duas edições existentes. Cada fase é
**aditiva** sobre a espinha — nenhuma fase reescreve um protocolo da espinha por inteiro.

## Decisões fixadas

- **Espinha:** `biblioteca-generalista` v1.0 — **refatoração** da `biblioteca-plantao-pa-flat`
  feita com modelo Fable 5: mesma matéria-prima, reestruturada na arquitetura de 13 blocos
  (Esqueleto A), filosofia *ideal-first*, porta sindrômica, capítulo de procedimentos e
  camada `locais/`. O autor da espinha **viu todo o conteúdo do doador** e fez cortes
  editoriais deliberados — onde a espinha é mais curta, presume-se decisão, não esquecimento.
- **Doador:** `biblioteca-plantao-pa-flat` (ramo "BIC-atualizada", 27/08/2026). Fonte da
  refatoração. Entra explicitamente com **uma coisa** que a espinha ainda não tinha: a
  **seção de psiquiatria (05)** (na espinha, só nomes reservados).
- **Seção 05 (psiquiatria):** reformatação **completa** para o Esqueleto A (13 blocos),
  não port leve.
- **KB ≠ conteúdo.** Diferença de tamanho entre versões de um mesmo protocolo indica
  divergência, não qualidade — não é critério para reimportar nada.
- **Camada local** (perfil do serviço: laboratório e tempo de resultado, imagem,
  hemoderivados, retaguarda; BIC disponível): vai para `locais/`, **irmão** de
  `biblioteca-plantao/`, nunca no corpo dos protocolos.

## Fase 0 — Espinha fixada · 2026-08-31 · CONCLUÍDA

- `biblioteca-generalista/` copiada para `biblioteca-plantao/` (81 arquivos: 78 protocolos
  + `00-INDICE-GERAL` + `00-LEIA-PRIMEIRO` + `99-TEMPLATES`). Contagem conferida.
- Pasta de trabalho movida para `Assistente de Plantão/biblioteca-plantao/`, separada das
  doadoras, que ficam em `shiftAssistant/` (`biblioteca-generalista/`, `biblioteca-plantao-pa-flat/`).
- `biblioteca-generalista/` e `biblioteca-plantao-pa-flat/` marcadas somente-leitura
  (atributo ReadOnly em todos os arquivos) — passam a ser doadoras intocáveis.
- Este arquivo criado.

## Fase 1 — Port da psiquiatria (05) · 2026-08-31 · CONCLUÍDA

As 4 protocolos da seção 05 (doador `biblioteca-plantao-pa-flat`) foram reformatadas
para o Esqueleto A (13 blocos) e gravadas no working folder:

- `05-psiquiatria-urgencia__01-agitacao-contencao-aspectos-legais.md` — H1 🧠
- `05-psiquiatria-urgencia__02-risco-suicida.md` — H1 🆘
- `05-psiquiatria-urgencia__03-abstinencia-alcoolica-intoxicacoes.md` — H1 🍺
- `05-psiquiatria-urgencia__04-delirium-sindromes-hipertermicas.md` — H1 🌡️

Por arquivo:
- Linha 1 `[← Índice geral]` + emoji no H1 + intro no estilo da espinha (`>` com 📎 vizinhos
  inline + linha `**Tempo-alvo:**`).
- Blocos 1–7 preservados do doador.
- Bloco 8 retitulado `DESTINO: ALTA × OBSERVAÇÃO × ENFERMARIA × UTI/TRANSFERÊNCIA` e
  convertido para tabela `| Destino | Critérios |`.
- **Blocos 9 (🏨 ENFERMARIA — 9a prescrição, 9b plano 24–48h, 9c gatilhos de escalada) e
  10 (⚖️ DIVERGÊNCIAS) escritos do zero** — conteúdo clínico novo, PRECISA DE REVISÃO MÉDICA.
- Blocos renumerados: "O QUE NÃO FAZER" → 11 · "E SE EU NÃO TIVER X" → 12 (🔧 SEM RECURSO X) ·
  "MODELOS" → 13 (13a/13b/13c).
- Cross-refs internos convertidos para nomes flat com `📎 [texto](caminho)`.
- Rodapé unificado (`📚 **Fontes**:` / `**Revisado em 08/2026 · Revisar até 08/2027**`).
- File 02: nota de rodapé ao colega (CVV) preservada.

Fontes novas citadas nos blocos 9–10: Project BETA, ACEP Clinical Policy (psiquiátrico adulto),
TREC, NICE NG225, The Joint Commission NPSG 15.01.01, ASAM (alcohol withdrawal), SCCM PADIS 2018.

Wrap-up:
- `00-INDICE-GERAL.md`: seção 05 agora ativa com 4 links; contagem 78 → 82; +2 atalhos no
  "PLANTÃO RUIM" (agitação; risco suicida).

🔴 PENDÊNCIA: revisão clínica dos blocos 9 e 10 das 4 protocolos (conteúdo gerado, não portado).

## Fase 2 — Reconciliação da camada BIC · 2026-08-31 · CONCLUÍDA (sem alterações)

**Resultado: nenhuma edição necessária.** A espinha já é BIC-nativa por construção — o
próprio Esqueleto A exige "infusões tituláveis prescritas em BIC (droga, dose total,
diluente, volume final, concentração, dose inicial, mL/h, alvo, monitorização)".

Cada item concreto do `CHANGELOG-BIC.md` do doador foi verificado e **já está presente
na espinha**:

| Item do CHANGELOG-BIC | Onde já está na espinha |
|---|---|
| Checklist de segurança pré-infusão de alta vigilância | `14-farmacologia-plantao__01`, bloco 1 (com "dupla checagem: duas pessoas, conta refeita do zero") |
| Referência ISMP (smart infusion pumps) | `14-farmacologia-plantao__01`, rodapé |
| Adrenalina refratária 1 mg → 100 mL (10 mcg/mL), linha dedicada, mL/h, monitorização | `01-emergencias-clinicas__11-anafilaxia`, blocos 5, 6, 13a; divergência RCUK no bloco 10 |
| HNF 25.000 U → 250 mL (100 U/mL); 18 U/kg/h = 0,18 mL/kg/h | `01-emergencias-clinicas__15-tep`, blocos 6 e 13 |
| Alteplase 100 mg em 2h em BIC; fórmula mL/h = volume reconstituído ÷ 2 | `01-emergencias-clinicas__15-tep`, bloco 6 |
| Alteplase alternativa (bolus + fases em BIC) quando TNK indisponível | `01-emergencias-clinicas__03-iam-com-supra`, blocos 6 e 13 |
| Pantoprazol 0,8 mg/mL → 10 mL/h; fórmula geral mL/h = 8 ÷ concentração | `02-cirurgia-trauma__06-hemorragia-digestiva`, blocos 5.2, 6, 13 |
| Octreotida 500 mcg → 100 mL (5 mcg/mL) → 10 mL/h = 50 mcg/h | `02-cirurgia-trauma__06-hemorragia-digestiva`, blocos 5.2, 6, 13 |
| Checklist de transporte: BIC com bateria + volume de solução com margem | `13-regulacao__01`, bloco de transporte |

Verificação adicional: 9 dos 15 protocolos de emergências clínicas já prescrevem infusões
em BIC (sepse, crise hipertensiva, TEP, IAM, SCA, taqui/bradiarritmias, AVC, PCR, SRI).

Nenhum arquivo foi modificado nesta fase. Nenhuma tag `[BIC]` foi criada porque não houve
inserção.

## Fase 3 — Camada local (`locais/`) · PENDENTE (modelo rascunhado)

Estrutura escolhida: `locais/` como **irmão** de `biblioteca-plantao/` (a biblioteca fica
portável, sem nenhum fato local no corpo). Modelo rascunhado em
`Assistente de Plantão/locais/_MODELO/00-perfil.md` — 9 seções (identificação · laboratório
com TAT realista · imagem · hemoderivados · farmácia · retaguarda · linhas de cuidado ·
transporte/regulação · estrutura) + explicação do gancho no bloco 12. Aguardando avaliação
do usuário antes de instanciar um serviço real.

## Fase 4 — Checagem de regressão de fatos · 2026-08-31 · CONCLUÍDA (absorvida na Fase 5)

Diff dirigido espinha × doador nos 4 arquivos de maior divergência
(`12-...__02-atestado-recusa-evasao`, `09-...__03-dor-cronica-paciente-que-retorna`,
`09-...__02-crise-falcemica`, `08-dermatologia__02-infeccoes-pele-partes-moles`), procurando
apenas **fatos discretos** (doses, red flags, prazos legais, contraindicações) perdidos na
refatoração.

**Resultado — 1 fato readicionado:**
- `08-dermatologia__02-infeccoes-pele-partes-moles.md`: a ressalva **"doxiciclina ❌ em
  <8 anos e gestante"** (tetraciclina) estava no doador e sumiu na espinha, que recomenda
  doxiciclina em 3 pontos. Readicionada nos 3 (linha do MRSA-CA purulenta, linha *Vibrio*/água
  salgada, tabela de doses). `[FATO-08]`

**Sem regressão (diferenças eram relocação ou escolha editorial, não perda):**
- Critérios de cefaleia por uso excessivo (MOH: ≥15 dias/mês simples, ≥10 combinação) —
  relocados de `09-...__03` para o protocolo de cefaleia (`09-...__01`).
- Red flag "primeira cefaleia > 50 anos" — está no protocolo de cefaleia (mnemônica SNOOP +
  seção de arterite temporal), mais completo que no doador.
- Doses de profilaxia de migrânea (propranolol, topiramato) — omitidas por decisão: a espinha
  é explícita que profilaxia é ambulatorial ("a carta, não a receita").
- Conteúdo legal de `12-...__02` — espinha igual ou mais rica (cita STF Temas 952/1069 2024).

## Fase 5 — Consistência e fechamento · 2026-08-31 · CONCLUÍDA

**Varredura de consistência (working folder, 86 `.md`):**
- **Links:** 100% dos alvos `.md` relativos resolvem. Nenhum link quebrado.
- **Rodapés:** 85/85 protocolos com `**Revisado em 08/2026 · Revisar até 08/2027**` e
  `📚 **Fontes**:` — zero variante `**Fonte:**` / `**Revisado em:**` do doador (as 4 de
  psiquiatria já tinham sido unificadas na Fase 1).
- **Linha 1 `[← Índice geral]`:** presente em todos os protocolos.
- Corrigido um `Ok` acidental colado no início de `CHANGELOG-MERGE.md`.

**Edições:**
- `00-INDICE-GERAL.md` — já feito na Fase 1 (seção 05 ativa, contagem 78→82, +2 atalhos).
- `00-LEIA-PRIMEIRO.md` — contagem `78 arquivos` → `82 arquivos`; removido o item
  "05-psiquiatria-urgencia … área planejada" de "O QUE AINDA NÃO EXISTE" (agora existe);
  item "Camada local" atualizado (pasta irmã, lista de eixos, aponta para `locais/_MODELO/`).
- `08-dermatologia__02` — `[FATO-08]` (ver Fase 4).

**Decisões adiadas (não bloqueiam a entrega):**
- Identidade da biblioteca: título ainda diz "BIBLIOTECA GENERALISTA DE PLANTÃO" / "Versão 1.0".
  Renomear para "BIBLIOTECA DE PLANTÃO" e/ou bumpar versão é decisão do usuário.
- `99-TEMPLATES.md`: acrescentar um Esqueleto D (camada local) e a convenção de nome
  `<serviço>__<protocolo>.md` — melhor fazer quando a Fase 3 for instanciada.
- Índices por seção (`NN-area__00-indice.md`, estilo do doador) — não adotados; o índice
  mestre basta.
- Fase 3 (camada local) segue pendente — só o modelo foi rascunhado.

## Estado final

- `biblioteca-plantao/` — 82 protocolos (78 da espinha + 4 de psiquiatria) + `00-INDICE-GERAL`
  + `00-LEIA-PRIMEIRO` + `99-TEMPLATES` + este changelog.
- `locais/_MODELO/00-perfil.md` — modelo da camada local, aguardando avaliação.
- Doadoras (`shiftAssistant/biblioteca-generalista/`, `.../biblioteca-plantao-pa-flat/`)
  intocadas e somente-leitura.

🔴 PENDÊNCIA CLÍNICA (herdada da Fase 1): revisão médica dos blocos 9 (🏨 ENFERMARIA) e
10 (⚖️ DIVERGÊNCIAS) das 4 protocolos de psiquiatria — conteúdo gerado, não portado.

---
**Revisado em 08/2026 · Revisar até 08/2027**
