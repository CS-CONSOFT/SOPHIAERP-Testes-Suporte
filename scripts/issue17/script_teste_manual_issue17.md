# 🧪 Script de Teste Manual — Lei Complementar (AA143)
**Issue:** #17 — Teste Caixa Preta - Lei Complementar - Reforma Tributária
**Tela (Resource):** `LeiComplementar`
**URL:** https://dsv17.sophiaerp.cloud/LeiComplementar
**Módulo:** Faturamento > Regras Fiscais
**Action:** READ (Consulta e Pesquisa)
**Tabela:** AA143 — `IAa143LeiComplementar`
**Ambiente:** Desenvolvimento (dsv17)
**Responsáveis:** @MatheusAutranAndrade | @WaldsonBrelaz
**Elaborado por:** @AgnaldoBarros com auxílio GitHub Copilot
**Release:** 2026.05.015

---

## 🔐 1. Configuração do Ambiente (Executar antes de iniciar)

### 1.1 Acesso ao Sistema
```
1. Abrir o navegador (preferencialmente Google Chrome ou Edge, versão atualizada)
2. Acessar: https://dsv17.sophiaerp.cloud
3. Realizar login com usuário que possua permissão no módulo Faturamento > Regras Fiscais
4. Confirmar que o login foi realizado com sucesso — verificar nome do usuário no canto superior
5. Anotar a versão do ERP exibida na tela: _______________
```

### 1.2 Verificação de Dados no Ambiente
```
1. Confirmar que existem registros de Lei Complementar cadastrados no ambiente dsv17
2. Confirmar que há ao menos 15 artigos cadastrados (para validar paginação)
3. Anotar ao menos 2 artigos e suas redações para uso nos testes de pesquisa:
   - Artigo 1: _______________  |  Redação: _______________
   - Artigo 2: _______________  |  Redação: _______________
   - Palavra-chave para busca: _______________
```

---

## 🧪 Script — Cenário 1: READ (Listagem / Consulta)

**Objetivo:** Verificar se a tela carrega corretamente com todas as colunas e dados.

```
PASSO 1
  Ação:      Acessar https://dsv17.sophiaerp.cloud/LeiComplementar
  Esperado:  A tela é carregada sem mensagens de erro
             URL muda para /LeiComplementar
             Título da tela exibido corretamente
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 2
  Ação:      Observar as colunas exibidas na listagem
  Esperado:  Coluna "Artigo" visível e populada com dados
             Coluna "Redação da Lei Complementar" visível e populada
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 3
  Ação:      Comparar os dados exibidos com os artigos anotados no item 1.2
  Esperado:  Os artigos cadastrados aparecem corretamente na listagem
             Dados íntegros, sem truncamento ou caracteres estranhos
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 4
  Ação:      Verificar se há botões/ações disponíveis na tela
  Esperado:  Apenas consulta disponível (sem botões de Adicionar/Editar/Excluir)
             Confirmando que é tela somente leitura (READ only)
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente
```

**📸 Evidência Cenário 1:** _(anexar print da tela com listagem carregada)_

---

## 🧪 Script — Cenário 2: Pesquisa por Artigo

**Objetivo:** Validar o filtro de pesquisa pelo número/nome do artigo.

```
PASSO 1
  Ação:      Localizar o campo "Pesquisar por artigo ou redação da lei complementar"
  Esperado:  Campo de pesquisa visível no topo ou no cabeçalho da listagem
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 2
  Ação:      Digitar no campo o artigo anotado no item 1.2 (ex: "Art. 15")
  Esperado:  Listagem filtra em tempo real ou ao pressionar Enter
             Exibe apenas registros que contêm o termo no campo Artigo
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 3
  Ação:      Verificar os registros retornados
  Esperado:  Todos os registros visíveis contêm o termo pesquisado
             Nenhum registro fora do filtro é exibido
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 4
  Ação:      Digitar um artigo parcial (ex: apenas "15" ou "Art")
  Esperado:  Busca parcial funciona, retornando todos artigos que contêm o fragmento
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 5
  Ação:      Limpar o campo de pesquisa (apagar o texto ou clicar no "X")
  Esperado:  Listagem retorna com TODOS os artigos
             Nenhum filtro residual aplicado
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente
```

**📸 Evidência Cenário 2:** _(anexar print com filtro aplicado e sem filtro)_

---

## 🧪 Script — Cenário 3: Pesquisa por Redação

**Objetivo:** Validar o filtro de pesquisa pelo texto da redação da lei.

```
PASSO 1
  Ação:      No campo de pesquisa, digitar "imposto"
  Esperado:  Listagem exibe apenas artigos cuja redação contém "imposto"
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 2
  Ação:      Limpar e digitar "reforma"
  Esperado:  Listagem exibe artigos com "reforma" na redação
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 3
  Ação:      Limpar e digitar "tributária" (minúsculas)
  Esperado:  Retorna artigos com "tributária" na redação
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 4
  Ação:      Limpar e digitar "TRIBUTÁRIA" (maiúsculas)
  Esperado:  Retorna os MESMOS resultados que no PASSO 3 (busca case-insensitive)
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 5
  Ação:      Testar com palavra do meio da redação (não início)
  Esperado:  Busca encontra o termo em qualquer posição do texto
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 6
  Ação:      Limpar o campo
  Esperado:  Todos os registros retornam
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente
```

**📸 Evidência Cenário 3:** _(anexar print comparando busca maiúscula x minúscula)_

---

## 🧪 Script — Cenário 4: Paginação

**Objetivo:** Validar o controle de paginação da listagem.

```
PASSO 1
  Ação:      Observar a quantidade padrão de itens exibidos por página
  Esperado:  Quantidade padrão claramente visível (ex: 10, 15 ou 25 itens)
             Anotar quantidade padrão: ___
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 2
  Ação:      Localizar o seletor de "itens por página" e selecionar 10
  Esperado:  Lista exibe exatamente 10 registros
             Total de páginas recalculado corretamente
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 3
  Ação:      Alterar para 25 itens por página
  Esperado:  Lista exibe até 25 registros
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 4
  Ação:      Alterar para 50 itens por página
  Esperado:  Lista exibe até 50 registros
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 5
  Ação:      Voltar para 10 itens por página e clicar em "Próxima Página" (→)
  Esperado:  Página 2 carregada com os próximos 10 registros
             Indicador de página atual atualizado (ex: "Página 2 de X")
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 6
  Ação:      Clicar em "Página Anterior" (←)
  Esperado:  Retorna à página 1 com os mesmos 10 primeiros registros
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 7
  Ação:      Navegar até a última página disponível
  Esperado:  Última página exibe apenas os registros restantes (pode ser menos de 10)
             Botão "Próxima" desabilitado ou oculto na última página
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente
```

**📸 Evidência Cenário 4:** _(anexar print da paginação em diferentes páginas)_

---

## 🧪 Script — Cenário 5: Ordenação de Colunas

**Objetivo:** Validar a ordenação da listagem ao clicar nos cabeçalhos das colunas.

```
PASSO 1
  Ação:      Clicar no cabeçalho da coluna "Artigo" (1º clique)
  Esperado:  Listagem reordenada em ordem CRESCENTE (A→Z ou 1→N)
             Ícone de seta para cima (↑) exibido no cabeçalho
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 2
  Ação:      Clicar novamente no cabeçalho "Artigo" (2º clique)
  Esperado:  Listagem reordenada em ordem DECRESCENTE (Z→A ou N→1)
             Ícone de seta para baixo (↓) exibido no cabeçalho
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 3
  Ação:      Clicar no cabeçalho "Redação da Lei Complementar" (1º clique)
  Esperado:  Listagem reordenada em ordem crescente pela redação
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 4
  Ação:      Clicar novamente no cabeçalho "Redação" (2º clique)
  Esperado:  Listagem reordenada em ordem decrescente pela redação
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 5
  Ação:      Verificar se ao trocar de coluna a ordenação anterior é cancelada
  Esperado:  Apenas a coluna clicada por último fica marcada como ordenada
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente
```

**📸 Evidência Cenário 5:** _(anexar print com ordenação crescente e decrescente)_

---

## 🧪 Script — Cenário 6: Carregamento de Dados

**Objetivo:** Validar o comportamento de loading durante o carregamento da tela.

```
PASSO 1
  Ação:      Limpar o cache do navegador (Ctrl+Shift+Del > Limpar dados)
             Acessar novamente: https://dsv17.sophiaerp.cloud/LeiComplementar
  Esperado:  Um indicador de carregamento (spinner/loading) é visível enquanto
             os dados são buscados da API
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 2
  Ação:      Aguardar o carregamento completo
  Esperado:  O indicador de loading desaparece após carregamento
             Dados aparecem na listagem corretamente
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 3
  Ação:      Verificar integridade dos dados carregados
  Esperado:  Todos os campos (Artigo, Redação) populados
             Sem células vazias indevidas ou dados corrompidos
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 4
  Ação:      Pressionar F5 para recarregar a página
  Esperado:  Comportamento de loading se repete normalmente
             Dados recarregados de forma consistente
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente
```

**📸 Evidência Cenário 6:** _(anexar print do spinner de loading se possível)_

---

## 🧪 Script — Cenário 7: Dados Vazios

**Objetivo:** Validar o comportamento da tela quando nenhum resultado é encontrado.

```
PASSO 1
  Ação:      No campo de pesquisa, digitar "XXXXXXXXXXX"
  Esperado:  Listagem fica vazia (sem registros exibidos)
             Nenhum erro de tela (sem mensagens de exceção ou tela branca)
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 2
  Ação:      Verificar a mensagem exibida na área da listagem
  Esperado:  Mensagem amigável exibida, ex:
             "Nenhum registro encontrado"
             "Nenhum dado encontrado"
             ou similar
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 3
  Ação:      Verificar se a tela continua responsiva (clicar em outros elementos)
  Esperado:  Sem travamentos, botões e filtros continuam funcionando
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 4
  Ação:      Abrir o console do navegador (F12 > Console) e verificar erros
  Esperado:  Nenhum erro vermelho no console relacionado ao filtro vazio
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 5
  Ação:      Limpar o campo de pesquisa
  Esperado:  Listagem retorna com todos os registros normalmente
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente
```

**📸 Evidência Cenário 7:** _(anexar print com mensagem de "nenhum dado encontrado")_

---

## 🧪 Script — Cenário 8: Integração com Outros Módulos

**Objetivo:** Validar que a Lei Complementar é corretamente referenciada nos demais módulos.

```
PASSO 1
  Ação:      Acessar o módulo Faturamento > Impostos / Regime Regular
  Esperado:  Módulo abre sem erros
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 2
  Ação:      Localizar um registro que possui Lei Complementar vinculada
  Esperado:  Campo ou referência à Lei Complementar visível no registro
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 3
  Ação:      Clicar no link/referência da Lei Complementar (se disponível)
  Esperado:  Navegação para a tela /LeiComplementar sem erros
             Dados da lei exibidos corretamente
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente

PASSO 4
  Ação:      Clicar no botão Voltar ou navegar de volta ao módulo anterior
  Esperado:  Retorno ao módulo de origem sem perda de contexto
             Dados do registro original ainda visíveis
  Obtido:    _______________
  Status:    [ ] OK  [ ] Erro  [ ] Pendente
```

**📸 Evidência Cenário 8:** _(anexar print da integração entre módulos)_

---

## 📊 Consolidação Final dos Resultados

| # | Cenário | Status | Severidade do Erro |
|---|---------|--------|--------------------|
| 1 | READ (Listagem/Consulta) | `[ ] OK` `[ ] Erro` `[ ] Pendente` | `[ ] Alta` `[ ] Média` `[ ] Baixa` |
| 2 | Pesquisa por Artigo | `[ ] OK` `[ ] Erro` `[ ] Pendente` | `[ ] Alta` `[ ] Média` `[ ] Baixa` |
| 3 | Pesquisa por Redação | `[ ] OK` `[ ] Erro` `[ ] Pendente` | `[ ] Alta` `[ ] Média` `[ ] Baixa` |
| 4 | Paginação | `[ ] OK` `[ ] Erro` `[ ] Pendente` | `[ ] Alta` `[ ] Média` `[ ] Baixa` |
| 5 | Ordenação de Colunas | `[ ] OK` `[ ] Erro` `[ ] Pendente` | `[ ] Alta` `[ ] Média` `[ ] Baixa` |
| 6 | Carregamento de Dados | `[ ] OK` `[ ] Erro` `[ ] Pendente` | `[ ] Alta` `[ ] Média` `[ ] Baixa` |
| 7 | Dados Vazios | `[ ] OK` `[ ] Erro` `[ ] Pendente` | `[ ] Alta` `[ ] Média` `[ ] Baixa` |
| 8 | Integração com Outros Módulos | `[ ] OK` `[ ] Erro` `[ ] Pendente` | `[ ] Alta` `[ ] Média` `[ ] Baixa` |

---

**Total de Passos Executados:** ___ / 37
**Cenários Aprovados:** ___ / 8
**Cenários com Erro:** ___ / 8
**Cenários Pendentes:** ___ / 8

**Versão do ERP testada:** _______________
**Data/Hora de início:** ___/___/______ às ___:___
**Data/Hora de término:** ___/___/______ às ___:___
**Testado por:** _______________

---

## 🐛 Registro de Erros Encontrados

> _(Preencher somente se houver erros. Crie uma issue separada para cada erro crítico.)_

| # | Cenário | Passo | Descrição do Erro | Severidade | Evidência |
|---|---------|-------|-------------------|------------|-----------|
| 1 | | | | | |
| 2 | | | | | |

---

_Script gerado com auxílio do GitHub Copilot — @AgnaldoBarros | Release 2026.05.015_
