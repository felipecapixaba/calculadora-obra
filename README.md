# Calculadora de estouro de obra

**No ar em https://felipecapixaba.github.io/calculadora-obra/**

Marque o que já está pronto na obra, informe o orçamento e o quanto já foi gasto,
e a página projeta quanto a obra vai custar no final. Sem cadastro e sem conta.

A conta roda inteira no aparelho de quem acessa — nada do que a pessoa digita é
enviado para lugar nenhum.

## Para quem serve

A página pergunta primeiro quem está usando, porque cada um tem um pedaço
diferente do dado:

| Perfil | O que informa | O que recebe |
|---|---|---|
| Dono da obra | etapas + dinheiro | Estouro em reais, custo final projetado |
| Engenheiro ou arquiteto | etapas + dinheiro + prazo | O mesmo, mais projeção de prazo e memória de cálculo |
| Mestre de obras | só as etapas | Avanço da obra e um resumo pronto para o WhatsApp |
| Quem trabalha na obra | só as etapas | O mesmo, em linguagem mais direta |

O mestre gera o resumo e manda para o dono no WhatsApp. O dono clica, cai aqui e
completa com os números. A distribuição está embutida no produto.

## A conta

Método de valor agregado:

| Sigla | Nome | Fórmula |
|---|---|---|
| VA | Valor agregado | orçamento × % executado |
| CR | Custo real | o que já saiu do caixa |
| IDC | Índice de desempenho de custo | VA ÷ CR |
| ENT | Custo final projetado | orçamento ÷ IDC |
| VNT | Diferença contra o orçamento | orçamento − ENT (negativo = estouro) |

Os pesos das etapas são de uma obra comum de alvenaria e estão declarados na
própria tela. É estimativa, não parecer técnico — a página diz isso ao usuário.

## Esta pasta

Gerada por `ferramentas/gerar-app.js` a partir do `index.html` do projeto. Não
editar à mão: rodar o gerador de novo sobrescreve tudo daqui.

| Arquivo | O que é |
|---|---|
| `index.html` | A página inteira, sem dependência externa |
| `manifest.webmanifest` | Instalação como aplicativo |
| `sw.js` | Abre sem internet depois da primeira visita |
| `icone.svg`, `icone-192.png`, `icone-512.png` | Ícone na tela de início |

## Ligação com o resto

É a isca de topo de funil do **Painel de Obras**
(https://felipecapixaba.github.io/painel-obras/), que faz esta mesma conta toda
semana a partir da planilha da construtora, obra por obra e fornecedor por
fornecedor. O botão no fim da página leva o contato direto para o WhatsApp, com o
diagnóstico da pessoa já escrito na mensagem.

---

Capixaba Shop — Trabalha e Confia
