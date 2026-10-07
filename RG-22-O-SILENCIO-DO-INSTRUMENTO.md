---
titulo: RG-22 — o silêncio do instrumento
quando: 2026-10-07
etiqueta: REGRA derivada de três falhas documentadas no mesmo dia
---

# `RG-22` · O silêncio do instrumento

> ## **Um verificador que não distingue **«respondeu não»** de **«não respondeu»** aceita silêncio como veredito. Isto não está no catálogo `M1–M7`, e aconteceu três vezes em um único dia com o autor deste protocolo.**

---

## A regra

> # **Toda consulta deve registrar **se o instrumento respondeu**, antes de registrar **o que respondeu.**
> ## **Um `0` sem prova de execução não é dado. É ausência de dado — e as duas coisas têm consequências opostas.**

---

## As três ocorrências, em 07/10/2026

### `1` · `R46` — o documento errado

**`FATO`** · Recebi a leitura que um sistema externo fez de um manuscrito. Confrontei contra
um manuscrito, não encontrei nada do que fora descrito, e escrevi **seis seções refutando a
leitura como projeção.** Depois apareceu **uma segunda imagem**, diferente, que continha tudo
verbatim.

**Eu nunca tinha perguntado qual documento estava sendo lido.**
A ausência era minha; eu a reportei como erro alheio.

### `2` · `OpenLibrary` — a cobertura do catálogo

**`FATO`** · Busquei um autor brasileiro no OpenLibrary, obtive `numFound: 0`, e relatei o
zero **como informação sobre o autor.** O autor tem **onze títulos publicados**, verificáveis
em catálogo comercial.

**O `0` media a cobertura do acervo.** Catalogação colaborativa sub-representa autor
independente brasileiro de maneira sistemática.

### `3` · `Google Books` — a cota

**`FATO`** · Busquei o mesmo autor na Google Books API e recebi um corpo **sem o campo
`totalItems`**. Relatei como **zero resultados.** A chamada seguinte devolveu, explícito:

> ### `HTTP 429` · ***«Quota exceeded for quota metric 'Queries' [...] RESOURCE_EXHAUSTED»***

**A API não respondeu zero. Ela não respondeu.** E a primeira resposta era um corpo de erro
cuja forma, lida sem atenção, **é indistinguível de um resultado vazio.**

---

## Por que isto é um modo de falha e não um descuido

> ## **`CÁLCULO`** **Nos três casos a estrutura é idêntica:**
> ### **o instrumento devolveu uma **ausência**, e ela foi registrada como uma **negação**.**
>
> # **Formalmente: `V` não foi executado, e o registro afirma `V(r) = reject`.**
> ## **E este é o pior caso possível para um protocolo de conferência, porque **o registro resultante é sintaticamente perfeito.** Tem campo preenchido, tem valor, tem data. Nada nele acusa que a consulta não rodou.**

> # **`CÁLCULO`** **E note onde ele mora no catálogo: em lugar nenhum.**
> ### **Não é `M5` — nada foi suprimido.**
> ### **Não é `M3` — nada foi fundido.**
> ### **Não é `M2` — a informação **não existia** para ser engavetada.**
> ## **É um modo **novo**, e é de `Classe II` por outra via: **produz-se um registro completo a partir de uma não-execução**, e o sistema segue operando sobre ele.**

---

## Consequência sobre `N1-g`

**`N1-g`** é a pergunta que decide se o `§6` deste corpus é novo: *alguém já formalizou
impossibilidade sobre registro autodeclarado?*

> # **`REGRA`** **Todos os resultados `0` reportados em 07/10/2026 — incluindo os do portal
> `OJS` do UniCEUB registrados em `N3` — **precisam ser reexecutados com prova de execução.**
> ## **E a consequência de método é mais dura: **`N1-g` não pode ser respondida por ausência.**
> ### **Um `0` prova, na melhor das hipóteses, algo sobre a cobertura do instrumento.**
> ### **Só uma **busca positiva**, em base cuja cobertura do campo seja conhecida e declarada, pode fechar a questão.**
> # **Isto estreita o trabalho e **piora a notícia**, e é por isso que está escrito.**

---

## O que `RG-22` exige de um registro conforme

| campo | exigência |
|---|---|
| **execução** | o instrumento respondeu? `sim`/`não` — e **a evidência disso** (código de status, carimbo, contagem retornada) |
| **cobertura** | o que a base indexa, declarado — e **o que ela sabidamente não indexa** |
| **consulta** | a string exata, para que outro a reexecute |
| **só então** | o resultado |

> ## **Sem os três primeiros, o quarto não é dado.**

---

> ## **`FATO`** **Três falhas idênticas em um dia, por quem escreve o protocolo: documento errado, cobertura de catálogo, cota de API.**
> ## **`FATO`** **Nos três, uma ausência foi registrada como uma negação — e o registro resultante era sintaticamente impecável.**
>
> # **`C8` diz que examinar é caro e classificar é grátis. **`RG-22` é o caso em que nem o exame nem a classificação aconteceram, e um valor foi escrito assim mesmo.**
> ## **É o mais barato de todos os modos: **custo zero, registro completo, conteúdo nenhum.**
