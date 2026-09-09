# 🏥 BIBLIOTECA GENERALISTA DE PLANTÃO — LEIA PRIMEIRO

**Referência clínica para o médico generalista de plantão · Versão 1.0 · Agosto de 2026**
**82 arquivos · 17 áreas · do PA à enfermaria**

---

> ## ⚠️ AVISO
> Este material é **referência de apoio à decisão** para uso por médico habilitado, construída a partir de diretrizes brasileiras e internacionais. **Não substitui julgamento clínico, protocolo institucional, treinamento supervisionado nem a bula do medicamento.** Confira as doses antes de administrar. Nos procedimentos, ler não substitui treinamento — o guia prepara e acompanha; a primeira vez ideal é com supervisão. A responsabilidade pela conduta é sempre do médico assistente.

---

## 🎯 A FILOSOFIA: IDEAL-FIRST

Esta biblioteca foi desenhada com uma separação deliberada:

1. **O corpo de cada protocolo ensina a medicina ideal** — o que um excelente generalista faz num hospital bem equipado. Válida em qualquer serviço, de qualquer porte.
2. **A adaptação a recursos limitados vive num bloco próprio no fim** (🔧 *Sem recurso X*), organizada **por capacidade faltante** — sem TC, sem laboratório em tempo hábil, sem hemoderivados, sem especialista — **nunca por local**. Não pedir imagem quando a regra de decisão é negativa é boa medicina; trombolisar sem TC não é adaptação, é erro. O bloco diz qual é qual.
3. **Nenhum serviço específico aparece no corpo.** Quando você mudar de plantão, a biblioteca continua valendo — só a camada local (futura, em `locais/`) muda.

E o arco vai até o fim: **reconhecer → estabilizar → tratar → decidir destino → internar e conduzir 24–48h → escalar**. O generalista de hospital pequeno também é o médico da enfermaria — o bloco 🏨 de cada protocolo existe para essa metade do plantão que as referências de emergência ignoram.

## 🚪 COMO USAR ÀS 3H DA MANHÃ

- **Sabe o diagnóstico?** Vá direto ao protocolo (índice → área).
- **Só tem a queixa?** Entre pela **porta sindrômica** (`00-sindromico__*`): ela discrimina os que matam dos comuns e aponta 📎 o protocolo certo. Roteadores não trazem tratamento — de propósito.
- **Vai fazer um procedimento?** Pasta 16: escrita como um preceptor do lado de fora do quarto — mãos, ângulos, sensações táteis, "o iniciante erra aqui".
- **Falta um recurso?** Bloco 12 (🔧) do protocolo em questão.
- **Precisa prescrever/documentar?** Bloco 13 (📝) — modelos prontos para copiar. Internação: bloco 9 (🏨). Paciente preso aguardando vaga: pasta 11, incluindo modelos de prescrição diária.

## 🗂️ A ESTRUTURA DE CADA PROTOCOLO (13 blocos)

| # | Bloco | |
|---|---|---|
| 1–3 | Definição · Reconhecer · ⚠️ Red flags | o que é, como se apresenta, o que não pode passar |
| 4–5 | Exames · Conduta | o cenário ideal, com tempos-alvo |
| 6–7 | 💊 Doses · Reavaliação | apresentações brasileiras; infusões tituláveis prescritas em BIC |
| 8 | Destino | alta × observação × enfermaria × UTI/transferência, com critérios |
| 9 | 🏨 **Enfermaria** | prescrição de internação modelo, plano 24–48h, gatilhos de escalada |
| 10 | ⚖️ **Divergências** | Europa × EUA × Brasil — só divergências reais, com a recomendação prática |
| 11 | ❌ O que não fazer | erros frequentes, com o porquê |
| 12 | 🔧 **Sem recurso X** | adaptação genérica por capacidade faltante |
| 13 | 📝 Modelos | prescrição e evolução prontas para copiar |

Exceções deliberadas (folhas de consulta, não protocolos): doses pediátricas por peso, vasoativas/sedação, antibióticos empíricos, escores, prescrição diária do retido. O parto de emergência tem bloco extra de reanimação neonatal.

### Legenda de símbolos

🔴 ação imediata/risco de morte · ⚠️ red flag · 💊 dose · 📝 texto pronto para prontuário · 🚑 gatilho de transferência/regulação · 🔧 adaptação a recurso limitado · ⚖️ divergência entre diretrizes · 🏨 enfermaria · ✅/❌ fazer/não fazer · 📎 link para outro arquivo · 🚪 roteador sindrômico · 🛠️ procedimento

## 📚 SOBRE AS FONTES — NOTA DE HONESTIDADE

As diretrizes citadas são as **edições vigentes verificáveis até o início de 2026** (AHA 2025, ERC 2025, ATLS 11ª, ESC por tema, SSC 2021, ADA 2024, ASH 2020, FEBRASGO, SBC, PCDTs do MS, resoluções do CFM, entre outras). Onde a edição exata não pôde ser confirmada, o rodapé marca **`(verificar edição vigente)`** — confira antes de citar em documento formal. Doses cuja apresentação varia entre farmácias trazem **`(conferir)`**. Cada arquivo tem rodapé `Revisado em / Revisar até` — a biblioteca inteira deve ser reauditada até **08/2027**.

## 🧱 O QUE AINDA NÃO EXISTE (por decisão)

- **Camada local (`locais/`)** — o perfil de um serviço específico (laboratório e tempo de resultado, imagem, hemoderivados, retaguarda, estoques, telefones) e suas adaptações. Fica como pasta **irmã** desta biblioteca; o bloco 12 de cada protocolo é o gancho onde ela se pluga. Um modelo em branco está em `locais/_MODELO/00-perfil.md`. Adaptar a biblioteca a um novo plantão = preencher um perfil, nunca reescrever protocolo.
- **Urgências menores** — área reservada para expansão futura.

## 🛠️ MANUTENÇÃO

Novo protocolo: copie o esqueleto de `99-TEMPLATES.md`, nomeie `NN-area__NN-tema.md` (minúsculas, sem acento, hífens), preencha os 13 blocos e o rodapé. Revisão: confira os rodapés a cada semestre. Funciona em Obsidian, Logseq, Drive, ou numa pasta no celular — Markdown puro, sem dependências.

---
**Versão 1.0 · Revisado em 08/2026 · Revisar até 08/2027**
