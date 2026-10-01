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

> **Do bit ao HTTP, em 252 questões.**

Simulado de estudo para **Redes de Dados I** (T02/T202 · Inatel), montado a partir
das questões das provas, da lista de exercícios e do relato de quem fez a PV1. Cada
questão tem o gabarito e um comentário explicando por que a resposta é aquela, e
por que as outras não são.

Sem back-end, sem login e sem build: é **um único `index.html`**, com HTML, CSS e
JavaScript puro, servido pelo GitHub Pages.

## O que tem dentro

O site tem duas seções: **Prova PV1**, que abre por padrão, e **Por assunto**.

### Prova PV1

| Aba | O que tem |
| --- | --- |
| **O que caiu** | O relato de quem fez a PV1, organizado em 11 tópicos que dá para marcar como estudados, com atalhos para as questões que caíram iguais ou parecidas. |
| **Treino de contas** | Uma conta nova a cada clique (máscara, rede, broadcast, total de endereços e hosts), corrigida campo a campo com a resolução passo a passo. Tem também uma calculadora para conferir qualquer IP. |
| **Simulado PV1** | 40 questões novas no formato da prova (2,5 pontos cada), com o peso do que caiu: contas, MQTT, gateway, comandos do roteador, cabeçalho TCP/UDP, tabela de rotas, VLAN, CSMA/CD e o desenho com a configuração do roteador. |
| **Prova anterior** | A prova da T02-B de 01/10/25 (40 questões), com o gabarito da correção. Selo rosa nas seis que caíram iguais. |
| **Lista PV1** | As 91 questões da lista, com o gabarito oficial e um comentário em cada. |
| **Relatório 5** | 11 questões sobre o laboratório: router-on-a-stick, `encapsulation dot1q`, OSPF com wildcard, `passive-interface` e rota estática. |

As figuras (topologias e o cabeçalho de camada 4) são desenhadas em SVG dentro do
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

As duas seções somam **252 questões**.

As questões de roteamento trazem a **tabela de rotas no formato do roteador Cisco**
(`show ip route`), uma com rota padrão e outra sem, para comparar o que acontece
com o pacote em cada caso.

## Como se estuda nele

| Recurso | O que faz |
| --- | --- |
| **✅&nbsp;Correção&nbsp;imediata** | Marcou, corrigiu: a alternativa certa fica verde, a errada vermelha, e o comentário aparece logo abaixo. A resposta trava para não dar para "chutar de novo". |
| **📝&nbsp;Modo&nbsp;prova** | Responde a parte inteira sem ver nada e só corrige no fim, com o botão **Corrigir parte**. Dá para trocar de modo a qualquer momento. |
| **💬&nbsp;Comentários** | Toda questão tem explicação. As de conta (máscara, broadcast, binário) mostram a conta passo a passo. |
| **🔎&nbsp;Filtros** | **Todas**, **Sem resposta** ou **Erradas**. O filtro de erradas é o jeito rápido de revisar antes da prova. |
| **⚠️&nbsp;Questões&nbsp;marcadas** | Cinco questões têm um selo amarelo: redação ambígua, foto cortada ou pegadinha. O comentário diz qual é a resposta mais provável e qual seria a alternativa se o professor ler de outro jeito. |
| **📊&nbsp;Placar&nbsp;por&nbsp;aba** | O anel no topo mostra a aba aberta: acertos, respondidas, questões a corrigir e a nota (nas abas de prova). Cada aba tem a própria barra de progresso. Fica no `localStorage` do navegador; nada é enviado para lugar nenhum. |
| **⬇️&nbsp;Próxima&nbsp;sem&nbsp;resposta** | Botão flutuante que desce até a próxima questão em branco. |
| **↺&nbsp;Recomeçar** | **Refazer esta aba** ou **Recomeçar tudo**, sempre com confirmação antes de apagar. `Esc` cancela. |

Acertar dá um brilho verde no card, e errar faz a alternativa tremer. As abas entram
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
as abas da PV1 em `PV1_SIM`, `PV1_PROVA`, `PV1_LISTA` e `PV1_REL`. O guia está em
`TOPICS` e `JUMPS`. Cada aba é um objeto com as questões dentro:

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

## Limites conhecidos

- **As respostas salvas são guardadas por posição** (`aba-índice`). Se você
  reordenar ou apagar questões, quem já respondeu vê as respostas nas questões
  erradas. Nesse caso, troque a chave `KEY` (`simulado-redes-v2` → `v3`) para
  zerar o progresso salvo. O progresso da versão antiga (`v1`) é migrado
  automaticamente na primeira visita.
- **O relato da PV1 é de memória** — de quem saiu da prova e foi lembrando em
  áudios. Serve para priorizar o estudo, não como gabarito.
- **Uma questão veio de foto cortada** — na parte 1, a opção "Camada 4" da questão
  sobre IPv4 foi deduzida. Ela está marcada no site.

## Aviso

O gabarito e os comentários **não são oficiais**. As questões marcadas em amarelo
dependem de como o professor encara o enunciado: confira com ele antes da prova.

Material de estudo pessoal, sem fins comerciais.
