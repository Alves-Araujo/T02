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

> **Do bit ao HTTP, em 70 questões.**

Simulado de estudo para **Redes 1**, montado a partir das questões da prova. Cada
questão tem o gabarito e um comentário explicando por que a resposta é aquela, e
por que as outras não são.

Sem back-end, sem login e sem build: é **um único `index.html`**, com HTML, CSS e
JavaScript puro, servido pelo GitHub Pages.

## O que tem dentro

| Parte | Assunto | Camada | Questões | Valor na prova |
| ---: | --- | --- | ---: | ---: |
| 1 | Endereçamento IP | 3 | 20 | 5 pts cada |
| 2 | Roteamento | 3 | 10 | 10 pts cada |
| 3 | Modelos OSI e TCP/IP | 1–7 | 10 | — |
| 4 | Ethernet e VLAN | 1–2 | 10 | 10 pts cada |
| 5 | Camada de aplicação | 7 | 10 | 10 pts cada |
| 6 | TCP e UDP | 4 | 10 | 10 pts cada |
| | **Total** | | **70** | |

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
| **📊&nbsp;Placar** | Acertos no topo e por parte, direto nas abas. Fica no `localStorage` do navegador; nada é enviado para lugar nenhum. |
| **↺&nbsp;Recomeçar** | **Refazer esta parte** ou **Recomeçar tudo**, sempre com confirmação antes de apagar. `Esc` cancela. |

O tema claro/escuro acompanha o sistema, e o layout funciona no celular.

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

Tudo fica no array `PARTS`, no `<script>` do `index.html`. Cada parte é um objeto
com as questões dentro:

```js
{ t:"Roteamento", layer:"Camada 3", pts:10, qs:[
  {q:"enunciado", o:["alt A","alt B","alt C"], a:2,
   e:"comentário do gabarito (aceita <b>negrito</b>)",
   flag:"Confira com o professor",   // opcional: selo amarelo
   code:"TD"},                       // opcional: tabela de rotas
]}
```

- `a` é o **índice** da alternativa certa, começando em `0`.
- `pts: null` esconde o valor da questão no cabeçalho da parte.
- `code` mostra uma tabela de rotas antes das alternativas: `"TD"` é a tabela com
  rota padrão e `"SEM"` a mesma tabela sem ela. As duas ficam em `TABLES`.
- Questões verdadeiro/falso são só múltipla escolha com `o:["Verdade","Falso"]`.

## Limites conhecidos

- **O total no cabeçalho é fixo** — o "70 questões · 6 partes" está escrito no
  HTML. Acrescentou questão, atualize ali também.
- **As respostas salvas são guardadas por posição** (`parte-índice`). Se você
  reordenar ou apagar questões, quem já respondeu vê as respostas nas questões
  erradas. Nesse caso, troque a chave `KEY` (`simulado-redes-v1` → `v2`) para
  zerar o progresso salvo.
- **Uma questão veio de foto cortada** — na parte 1, a opção "Camada 4" da questão
  sobre IPv4 foi deduzida. Ela está marcada no site.

## Aviso

O gabarito e os comentários **não são oficiais**. As questões marcadas em amarelo
dependem de como o professor encara o enunciado: confira com ele antes da prova.

Material de estudo pessoal, sem fins comerciais.
