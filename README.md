<p align="center">
  <img src="./assets/banner.svg" width="100%" alt="Simulado de Redes" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-0D1117?style=for-the-badge&logo=javascript&logoColor=F7DF1E" alt="JavaScript" />
  <img src="https://img.shields.io/badge/HTML5-0D1117?style=for-the-badge&logo=html5&logoColor=E34F26" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-0D1117?style=for-the-badge&logo=css&logoColor=1572B6" alt="CSS3" />
</p>

<p align="center">
  <a href="https://alves-araujo.github.io/T02/">
    <img src="https://img.shields.io/badge/%E2%86%92_Acessar_o_site-ff3ee0?style=for-the-badge&labelColor=0D1117" alt="Acessar o site" />
  </a>
</p>

> **Do bit ao IPv6, em 410 questões e dois resumos.**

Simulado de estudo para **Redes de Dados I** (T02/T202 · Inatel), montado a partir
das questões das provas, das listas de exercícios, das atividades do Teams e do relato
de quem fez a PV1 e a PV2. Cada
questão tem o gabarito e um comentário explicando por que a resposta é aquela, e
por que as outras não são.

Sem back-end, sem login e sem build: é **um único `index.html`**, com HTML, CSS e
JavaScript puro, servido pelo GitHub Pages.

## O que tem dentro

O site tem cinco seções no topo: **Resumo**, **Tabela de rotas**, **Por assunto**, **Prova PV1** e **Prova PV2**, que abre por padrão.

### Resumo

Duas abas. **Resumo PV1**: toda a matéria da PV1 em 10 seções: modelos OSI e TCP/IP, endereçamento IPv4 (tabela de máscaras e o passo a passo de rede/broadcast), gateway, roteamento, comandos do roteador e do switch, Ethernet, VLAN, TCP e UDP, camada de aplicação e dicas para a hora da prova. Tem índice clicável e um botão “Li” em cada seção.

**Resumo PV2**: sub-redes, VLSM, binário, cabeçalho IPv4, fragmentação (com a tabela de deslocamentos), ICMP, IPv6 (abreviação, prefixos, IPv4 × IPv6), transição v4/v6, cibersegurança e dicas para a prova.

### Tabela de rotas

Treino de leitura do `show ip route`: cada rodada gera uma tabela nova (C, L, S, R, O, rota padrão e rotas sobrepostas /22, /23, /24, como na prova) e um IP de destino. Você escolhe o que o roteador faz (sai por qual interface, usa a rota padrão, descarta ou é para o próprio roteador) e vê a análise rota por rota: a faixa de cada uma, se contém o destino e qual ganha pelo maior prefixo, com a linha vencedora destacada na tabela. Dá para testar qualquer outro destino na mesma tabela.

Embaixo do treino ficam os **24 exercícios de tabela de rotas** que já existem nas provas, nas listas, no simulado e no Relatório 5, em quatro blocos: para onde vai o pacote, lendo a tabela, rota padrão e rota estática, e interfaces e redes conectadas. São as mesmas questões das outras abas, então a resposta dada num lugar aparece no outro.

### Prova PV1

| Aba | O que tem |
| --- | --- |
| **O que caiu** | O relato de quem fez a PV1, organizado em 11 tópicos que dá para marcar como estudados, com atalhos para as questões que caíram iguais ou parecidas. |
| **Treino de contas** | Uma conta nova a cada clique (máscara, rede, broadcast, total de endereços e hosts), corrigida campo a campo com a resolução passo a passo. Tem também uma calculadora para conferir qualquer IP. |
| **Simulado PV1** | 40 questões novas no formato da prova (2,5 pontos cada), com o peso do que caiu: contas, MQTT, gateway, comandos do roteador, cabeçalho TCP/UDP, tabela de rotas, VLAN, CSMA/CD e o desenho com a configuração do roteador. |
| **Prova anterior** | A prova da T02-B de 01/10/25 (40 questões), com o gabarito da correção. Selo rosa nas seis que caíram iguais. |
| **Lista PV1** | As 91 questões da lista, com o gabarito oficial e um comentário em cada. |
| **Relatório 5** | 11 questões sobre o laboratório: router-on-a-stick, `encapsulation dot1q`, OSPF com wildcard, `passive-interface` e rota estática. |

### Prova PV2

| Aba | O que tem |
| --- | --- |
| **O que caiu** | O relato de quem fez a PV2 da outra turma, em 11 tópicos: formato da prova (4 abertas, V/F, fechadas), cabeçalho IPv4, deslocamento de fragmento, divisão de rede, binário, ICMP/ping, IPv6, transição, cibersegurança, tabela de rotas e a prova do lab. Com atalhos para as questões parecidas. |
| **Treino de contas** | Cinco tipos de conta gerados na hora: fragmentação (nº de fragmentos, dados, deslocamento e MF), divisão em N sub-redes, VLSM, binário/máscaras e abreviação de IPv6. Corrige campo a campo e mostra a resolução. |
| **Simulado PV2** | 40 questões novas no formato relatado (2,5 pontos cada): começa pelo cabeçalho IPv4, fragmentação, sub-redes, IPv6, transição, ICMP, 3 de tabela de rotas, V/F de cibersegurança e as 4 abertas. |
| **Lista PV2** | As 37 questões da lista de PV2 (passadas), com o gabarito oficial e um comentário em cada. |
| **Lista de sub-redes** | Os 10 exercícios da lista de sub-redes da aula 07, resolvidos (a lista não tem gabarito), mais a Atividade 7 da aula. |
| **Atividades 9 e 10** | As atividades do Teams de Protocolos IP (20) e Cibersegurança (15). |
| **Prova do lab** | Roteiro da Atividade Integradora II: topologia, endereços e os comandos de cada etapa (OSPF, pfSense, Apache com TLS). |
| **Questões do lab** | 17 questões sobre os relatórios do laboratório (VMs, redes do VirtualBox, Docker, MQTT, TLS, pfSense, OSPF). |

As **questões abertas** têm uma caixa para escrever a resposta e o botão **Ver gabarito e corrigir**: depois de comparar, você marca se acertou, e isso entra no placar.

As figuras (topologias e os cabeçalhos IPv4 e de camada 4) são desenhadas em SVG dentro do
próprio HTML e acompanham o tema claro/escuro.

### Por assunto

| Parte | Assunto | Camada | Questões | Valor na prova |
| ---: | --- | --- | ---: | ---: |
| 1 | Endereçamento IP | 3 | 20 | 5 pts cada |
| 2 | Roteamento | 3 | 10 | 10 pts cada |
| 3 | Modelos OSI e TCP/IP | 1–7 | 10 | — |
| 4 | Ethernet e VLAN | 1–2 | 10 | 10 pts cada |
| 5 | Camada de aplicação | 7 | 10 | 10 pts cada |
| 6 | TCP e UDP | 4 | 10 | 10 pts cada |
| | **Total** | | **70** | |

Com a PV2, o site soma **410 questões**.

As questões de roteamento trazem a **tabela de rotas no formato do roteador Cisco**
(`show ip route`), uma com rota padrão e outra sem, para comparar o que acontece
com o pacote em cada caso.

## Como se estuda nele

| Recurso | O que faz |
| --- | --- |
| **✅&nbsp;Correção&nbsp;imediata** | Marcou, corrigiu: a alternativa certa fica verde, a errada vermelha, e o comentário aparece logo abaixo. A resposta trava para não dar para "chutar de novo". |
| **📝&nbsp;Modo&nbsp;prova** | Responde a parte inteira sem ver nada e só corrige no fim, com o botão **Corrigir parte**. O seletor de modo fica no topo de cada lista de questões, e dá para trocar a qualquer momento. |
| **💬&nbsp;Comentários** | Toda questão tem explicação. As de conta (máscara, broadcast, binário) mostram a conta passo a passo. |
| **🔎&nbsp;Filtros** | **Todas**, **Sem resposta** ou **Erradas**. O filtro de erradas é o jeito rápido de revisar antes da prova. |
| **⚠️&nbsp;Questões&nbsp;marcadas** | Cinco questões têm um selo amarelo: redação ambígua, foto cortada ou pegadinha. O comentário diz qual é a resposta mais provável e qual seria a alternativa se o professor ler de outro jeito. |
| **📊&nbsp;Placar&nbsp;por&nbsp;aba** | O anel no topo mostra a aba aberta: acertos, respondidas, questões a corrigir e a nota (nas abas de prova). Cada aba tem a própria barra de progresso. Fica no `localStorage` do navegador; nada é enviado para lugar nenhum. |
| **⬇️&nbsp;Próxima&nbsp;sem&nbsp;resposta** | Botão flutuante que desce até a próxima questão em branco. |
| **↺&nbsp;Recomeçar** | Abre uma janela para escolher o que apagar: cada aba aparece com o seu progresso, e a aba atual já vem marcada. Depois de apagar, um aviso oferece **Desfazer** por alguns segundos. Nas abas de questões também há o **Refazer esta aba**. `Esc` fecha. |

No fundo, uma rede animada: nós, links e pacotes trafegando nas laterais, bem fraca atrás do conteúdo. Ela reage às respostas: acertar solta pacotes verdes dos dois lados do card, e errar solta pacotes vermelhos. O card também brilha no acerto, e a alternativa treme no erro. As abas entram
com uma animação curta, e tudo isso é desligado se o sistema estiver com
`prefers-reduced-motion`. O tema claro/escuro acompanha o sistema, e o layout funciona no celular.

Cada aba tem endereço próprio (`#pv1-sim`, `#pv1-treino`…), então dá para mandar o
link direto de uma aba.

## Rodar localmente

Basta abrir o `index.html` no navegador. Sem internet, as fontes caem para as do
sistema e o resto funciona igual.

Para servir por HTTP:

```bash
python3 -m http.server 8000
```

E acessar <http://localhost:8000>.

## Publicar sua própria cópia

O site é estático, então basta apontar o GitHub Pages para a raiz do repositório:
**Settings → Pages → Source: Deploy from a branch → Branch `main` / `(root)`**.

> O arquivo `.nojekyll` já vem incluso para o GitHub não processar nada com o Jekyll.

## Estrutura

```
.
├── index.html          → tudo: estilo, questões e lógica do simulado
├── assets/banner.svg   → banner deste README
└── .nojekyll
```

## Onde mexer nas questões

Tudo fica no `<script>` do `index.html`: as partes por assunto no array `PARTS`, e
as abas da PV1 em `PV1_SIM`, `PV1_PROVA`, `PV1_LISTA` e `PV1_REL`, e as da PV2 em
`PV2_SIM`, `PV2_LISTA`, `PV2_SUB`, `PV2_ATIV` (que junta `A9_QS` e `A10_QS`) e
`PV2_LABQ`. Os guias estão em `TOPICS`/`JUMPS` (PV1), `TOPICS2`/`JUMPS2` (PV2) e
`LAB_TOPICS` (prova do lab); os resumos em `SUMMARY` e `SUMMARY2`. O treino de contas
da PV2 fica em `T2G` (um gerador por tipo de conta). Cada aba é um objeto com as
questões dentro:

```js
{ t:"Roteamento", layer:"Camada 3", pts:10, qs:[
  {q:"enunciado", o:["alt A","alt B","alt C"], a:2,
   e:"comentário do gabarito (aceita <b>negrito</b>)",
   flag:"Confira com o professor",   // opcional: selo amarelo
   code:"TD",                        // opcional: tabela de rotas fixa
   fig:FIG_LANS, pre:"texto",        // opcional: figura SVG e bloco de texto
   tag:"igual"},                     // opcional: selo rosa "caiu igual/parecida"
]}
```

- `a` é o **índice** da alternativa certa, começando em `0`.
- `pts: null` esconde o valor da questão no cabeçalho da parte.
- `code` mostra uma tabela de rotas antes das alternativas: `"TD"` é a tabela com
  rota padrão e `"SEM"` a mesma tabela sem ela. As duas ficam em `TABLES`.
- Questões verdadeiro/falso são só múltipla escolha com `o:["Verdade","Falso"]`.
- Questão aberta: `open:"gabarito em HTML"`, com `o:OPEN_O, a:0, e:OPEN_E`. Ela
  mostra a caixa de resposta e só exibe o gabarito e as opções “Acertei/Errei”
  depois do clique em **Ver gabarito e corrigir**.

## Limites conhecidos

- **As respostas salvas são guardadas por posição** (`aba-índice`). Se você
  reordenar ou apagar questões, quem já respondeu vê as respostas nas questões
  erradas. Nesse caso, troque a chave `KEY` (`simulado-redes-v2` → `v3`) para
  zerar o progresso salvo. O progresso da versão antiga (`v1`) é migrado
  automaticamente na primeira visita.
- **Os relatos da PV1 e da PV2 são de memória**, de quem saiu da prova e foi
  lembrando em áudios e mensagens. Servem para priorizar o estudo, não como gabarito.
- **A lista de sub-redes não tem gabarito oficial**: as respostas foram calculadas.
  No exercício 6 (“até 32 hosts”), a resposta é /26, porque 32 hosts não cabem numa
  /27; a questão está marcada.
- **Uma questão veio de foto cortada** — na parte 1, a opção "Camada 4" da questão
  sobre IPv4 foi deduzida. Ela está marcada no site.

## Aviso

O gabarito e os comentários **não são oficiais**. As questões marcadas em amarelo
dependem de como o professor encara o enunciado: confira com ele antes da prova.

Material de estudo pessoal, sem fins comerciais.
