# biblia-content

Arquivo de conteúdo bíblico em Markdown — **7 peças por capítulo** da Bíblia
inteira, geradas para servirem de fonte/estudo. Repositório **público** e
**dormente** (um único commit, "Backup Inicial", desde a criação).

## O que tem aqui

```
biblia/<livro>/<capítulo NN>/<tipo>.md
```

| Tipo de arquivo | O que é |
|---|---|
| `devocional-01.md` | devocional |
| `estudo-tematico.md` | estudo temático |
| `exposicao-homiletica.md` | exposição homilética |
| `mensagem-pastoral.md` | mensagem pastoral |
| `oracao.md` | oração |
| `temas-controversos.md` | temas controversos |
| `terminologias.md` | terminologias |

Cobertura: **1.189 capítulos** (a contagem varia por tipo em 1–2 arquivos —
ver "Inconsistências conhecidas"). ~8.300 arquivos no total.

## Papel no ecossistema Portal Nascente

- É o item **"Bíblia — dados PT/EN"** do ecossistema (programa #6b nos
  documentos gerais). Tratado como **arquivo de conteúdo / backup**, não como
  um programa com frontend.
- **Não há consumidor de runtime confirmado** deste repositório. O site Penso
  Logo Creio consome a Bíblia dos **próprios** arquivos (`public/data/`,
  `src/content/biblia/`), não deste repo. Se algum dia este arquivo passar a
  ser consumido por URL (ex.: `raw.githubusercontent.com/...`), registrar aqui.

## Migração de organização (2026-08-29)

Este repositório foi transferido da conta pessoal
`nascente-pensologocreio/BIBLIA-CONTENT` para a organização GitHub
**`portal-nascente`** e renomeado para **`biblia-content`**
(`github.com/portal-nascente/biblia-content`). O endereço antigo redireciona.
Nenhum arquivo de conteúdo foi alterado — só a localização e o nome do
repositório. Parte da _Padronização e Migração do Ecossistema_ (Fase A).

## Inconsistências conhecidas (pré-existentes, não vieram da migração)

- Há pastas de livro com e sem espaço no nome: `biblia/1 timoteo/` (com
  espaço, contém só `devocional-01.md`) **e** `biblia/1timoteo/`. Provável
  erro na geração original. Não corrigido aqui — decidir se consolida quando
  o repo voltar a ser usado.

## Documentos relacionados

- Ecossistema: `PORTAL NASCENTE/ÍNDICE - Documentos do Portal Nascente.md` ·
  `PORTAL NASCENTE/Pasta Técnico do Portal Nascente/PORTAL NASCENTE - Documento Mestre do Ecossistema.md`
- Migração: `PORTAL NASCENTE/Pasta Técnico do Portal Nascente/URGENTE - PLANO DEFINITIVO - Padronização e Migração do Ecossistema.md`

## Registro de alterações

- **2026-08-29** — README criado (passo 4 do ciclo da Fase A da migração de
  organização). O repositório não tinha nenhum documento próprio; este arquivo
  dá contexto para quem chegar nele sem saber o que é. Conteúdo (`biblia/…`)
  não foi tocado.
- **~2026-01** — commit único "Backup Inicial: Conteudo Markdown Biblia".
