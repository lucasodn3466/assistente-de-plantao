# 🏥 Assistente de Plantão

Biblioteca clínica de apoio à decisão para o médico generalista de plantão — do pronto atendimento à enfermaria. Markdown puro, sem dependências: funciona em Obsidian, Logseq, Drive ou numa pasta no celular.

> ⚠️ **Referência de apoio à decisão para uso por médico habilitado.** Não substitui julgamento clínico, protocolo institucional, treinamento supervisionado nem a bula do medicamento. A responsabilidade pela conduta é sempre do médico assistente.

## Por onde começar

👉 **[`biblioteca-plantao/00-LEIA-PRIMEIRO.md`](biblioteca-plantao/00-LEIA-PRIMEIRO.md)** — filosofia, avisos e como usar às 3h da manhã.
📖 **[`biblioteca-plantao/00-INDICE-GERAL.md`](biblioteca-plantao/00-INDICE-GERAL.md)** — índice completo por área.

## Estrutura

| Onde | O que é |
|---|---|
| `biblioteca-plantao/` | O conteúdo. 82 protocolos + índice, guia de uso, templates e changelog. Portátil: nenhum fato de serviço específico no corpo. |
| `locais/` | Camada de adaptação por serviço (laboratório, imagem, hemoderivados, retaguarda). Pluga no bloco 12 de cada protocolo. Hoje só o modelo em branco. |
| [`biblioteca-plantao/PLANOS-FUTUROS.md`](biblioteca-plantao/PLANOS-FUTUROS.md) | O roadmap. Índice projetado, protocolos na fila, reestruturações planejadas e decisões em aberto. |

## Estado

**Versão 2.0 · Revisado em 08/2026 · Revisar até 08/2027**
Biblioteca pronta para uso. Camada local (`locais/`) ainda não instanciada.
O que vem a seguir está em [`PLANOS-FUTUROS.md`](biblioteca-plantao/PLANOS-FUTUROS.md).

<details>
<summary>Notas de manutenção</summary>

- **`main` é a branch canônica.**
- **Fechar o Obsidian antes de mover arquivos.** Ele reescreve links ao mover; o vault usa links relativos de propósito.
- **Backup byte-idêntico** parado em `Downloads/Assistente de Plantão Hierarquizado/`.
- **Um nível de pastas.** Nome do arquivo = código da pasta + `__` + número + tema (`01h__01-sepse-choque-septico.md`). O código curto só existe numa pasta, então nenhum basename se repete.
- **Links relativos.** Topo de cada protocolo: `../00-INDICE-GERAL.md`. Entre seções: `../pasta/arquivo.md`.

</details>
