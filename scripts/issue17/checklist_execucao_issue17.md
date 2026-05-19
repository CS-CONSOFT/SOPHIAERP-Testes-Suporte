# 📋 Checklist de Execução — Lei Complementar (AA143)
**Tela:** https://dsv17.sophiaerp.cloud/LeiComplementar
**Responsáveis:** @MatheusAutranAndrade | @WaldsonBrelaz
**Data de execução:** ___/___/______
**Versão do ERP:** _______________
**Ambiente:** Desenvolvimento (dsv17)

---

### ⚙️ Pré-execução

- [ ] Usuário logado com permissão no módulo **Faturamento > Regras Fiscais**
- [ ] Ambiente `dsv17` acessível e estável
- [ ] Dados de Lei Complementar (AA143) carregados no sistema
- [ ] Múltiplos artigos cadastrados (mínimo 15 para validar paginação)

---

### 🧪 Cenário 1 — READ (Listagem / Consulta)

| Passo | Ação | Resultado Esperado | ✅/❌ | Observação |
|-------|------|--------------------|-------|------------|
| 1 | Acessar https://dsv17.sophiaerp.cloud/LeiComplementar | Tela carrega sem erros | `[ ]` | |
| 2 | Verificar coluna **Artigo** na listagem | Coluna visível e com dados | `[ ]` | |
| 3 | Verificar coluna **Redação da Lei Complementar** | Coluna visível e com dados | `[ ]` | |
| 4 | Verificar se os dados refletem a Lei Complementar cadastrada | Dados corretos e consistentes | `[ ]` | |

**Status do Cenário 1:** `[ ] OK` `[ ] Erro` `[ ] Pendente`
> **Resultado Obtido:** _(descrever)_
> **Evidência:** _(anexar print)_

---

### 🧪 Cenário 2 — Pesquisa por Artigo

| Passo | Ação | Resultado Esperado | ✅/❌ | Observação |
|-------|------|--------------------|-------|------------|
| 1 | Localizar o campo **"Pesquisar por artigo ou redação"** | Campo de pesquisa visível | `[ ]` | |
| 2 | Digitar um artigo conhecido (ex: `Art. 15`) | Listagem filtra e exibe apenas artigos correspondentes | `[ ]` | |
| 3 | Verificar se apenas registros com o termo aparecem | Filtro funcionando corretamente | `[ ]` | |
| 4 | Limpar o filtro | Todos os artigos retornam na listagem | `[ ]` | |

**Status do Cenário 2:** `[ ] OK` `[ ] Erro` `[ ] Pendente`
> **Resultado Obtido:** _(descrever)_
> **Evidência:** _(anexar print)_

---

### 🧪 Cenário 3 — Pesquisa por Redação

| Passo | Ação | Resultado Esperado | ✅/❌ | Observação |
|-------|------|--------------------|-------|------------|
| 1 | No campo de pesquisa, digitar `imposto` | Filtra artigos cuja redação contém "imposto" | `[ ]` | |
| 2 | Digitar `reforma` | Filtra artigos com "reforma" na redação | `[ ]` | |
| 3 | Digitar `tributária` | Filtra corretamente (case-insensitive) | `[ ]` | |
| 4 | Digitar `TRIBUTÁRIA` (maiúsculas) | Mesmo resultado que minúsculas (case-insensitive) | `[ ]` | |
| 5 | Limpar o campo | Todos os registros retornam | `[ ]` | |

**Status do Cenário 3:** `[ ] OK` `[ ] Erro` `[ ] Pendente`
> **Resultado Obtido:** _(descrever)_
> **Evidência:** _(anexar print)_

---

### 🧪 Cenário 4 — Paginação

| Passo | Ação | Resultado Esperado | ✅/❌ | Observação |
|-------|------|--------------------|-------|------------|
| 1 | Verificar quantos itens são exibidos por padrão | Quantidade padrão visível (ex: 10 ou 15) | `[ ]` | |
| 2 | Alterar para **10 itens por página** | Lista exibe exatamente 10 registros | `[ ]` | |
| 3 | Alterar para **25 itens por página** | Lista exibe até 25 registros | `[ ]` | |
| 4 | Alterar para **50 itens por página** | Lista exibe até 50 registros | `[ ]` | |
| 5 | Clicar no botão **Próxima Página** | Registros mudam corretamente | `[ ]` | |
| 6 | Clicar no botão **Página Anterior** | Retorna aos registros anteriores | `[ ]` | |
| 7 | Voltar para a **primeira página** | Dados consistentes com o início | `[ ]` | |

**Status do Cenário 4:** `[ ] OK` `[ ] Erro` `[ ] Pendente`
> **Resultado Obtido:** _(descrever)_
> **Evidência:** _(anexar print)_

---

### 🧪 Cenário 5 — Ordenação de Colunas

| Passo | Ação | Resultado Esperado | ✅/❌ | Observação |
|-------|------|--------------------|-------|------------|
| 1 | Clicar no cabeçalho da coluna **Artigo** (1º clique) | Ordenação crescente aplicada (A→Z / 1→N) | `[ ]` | |
| 2 | Clicar novamente no cabeçalho **Artigo** (2º clique) | Ordenação decrescente (Z→A / N→1) | `[ ]` | |
| 3 | Clicar no cabeçalho **Redação da Lei Complementar** (1º clique) | Ordenação crescente aplicada | `[ ]` | |
| 4 | Clicar novamente em **Redação** (2º clique) | Ordenação decrescente | `[ ]` | |

**Status do Cenário 5:** `[ ] OK` `[ ] Erro` `[ ] Pendente`
> **Resultado Obtido:** _(descrever)_
> **Evidência:** _(anexar print)_

---

### 🧪 Cenário 6 — Carregamento de Dados

| Passo | Ação | Resultado Esperado | ✅/❌ | Observação |
|-------|------|--------------------|-------|------------|
| 1 | Acessar a tela e observar imediatamente | Indicador de loading/spinner visível | `[ ]` | |
| 2 | Aguardar o carregamento completo | Spinner desaparece após carga | `[ ]` | |
| 3 | Verificar se os dados foram carregados | Todos os registros visíveis e corretos | `[ ]` | |
| 4 | Recarregar a página (F5) e repetir observação | Comportamento consistente no reload | `[ ]` | |

**Status do Cenário 6:** `[ ] OK` `[ ] Erro` `[ ] Pendente`
> **Resultado Obtido:** _(descrever)_
> **Evidência:** _(anexar print)_

---

### 🧪 Cenário 7 — Dados Vazios

| Passo | Ação | Resultado Esperado | ✅/❌ | Observação |
|-------|------|--------------------|-------|------------|
| 1 | No campo de pesquisa, digitar `XXXXXXXXXXX` | Listagem fica vazia sem erros na tela | `[ ]` | |
| 2 | Verificar se uma mensagem é exibida | Mensagem "Nenhum dado encontrado" ou similar | `[ ]` | |
| 3 | Verificar se a tela permanece responsiva | Sem travamentos ou erros de console | `[ ]` | |
| 4 | Limpar o filtro | Dados retornam normalmente | `[ ]` | |

**Status do Cenário 7:** `[ ] OK` `[ ] Erro` `[ ] Pendente`
> **Resultado Obtido:** _(descrever)_
> **Evidência:** _(anexar print)_

---

### 🧪 Cenário 8 — Integração com Outros Módulos

| Passo | Ação | Resultado Esperado | ✅/❌ | Observação |
|-------|------|--------------------|-------|------------|
| 1 | Acessar **Impostos / Regime Regular** e localizar um registro com Lei Complementar vinculada | Referência à Lei Complementar visível | `[ ]` | |
| 2 | Clicar no link/referência da Lei Complementar | Navegação para tela de Lei Complementar sem erros | `[ ]` | |
| 3 | Retornar ao módulo anterior | Retorno sem perda de contexto/dados | `[ ]` | |

**Status do Cenário 8:** `[ ] OK` `[ ] Erro` `[ ] Pendente`
> **Resultado Obtido:** _(descrever)_
> **Evidência:** _(anexar print)_

---

## 📊 Resultado Consolidado

| Cenário | Descrição | Status |
|---------|-----------|--------|
| 1 | READ (Listagem/Consulta) | `[ ] OK` `[ ] Erro` `[ ] Pendente` |
| 2 | Pesquisa por Artigo | `[ ] OK` `[ ] Erro` `[ ] Pendente` |
| 3 | Pesquisa por Redação | `[ ] OK` `[ ] Erro` `[ ] Pendente` |
| 4 | Paginação | `[ ] OK` `[ ] Erro` `[ ] Pendente` |
| 5 | Ordenação de Colunas | `[ ] OK` `[ ] Erro` `[ ] Pendente` |
| 6 | Carregamento de Dados | `[ ] OK` `[ ] Erro` `[ ] Pendente` |
| 7 | Dados Vazios | `[ ] OK` `[ ] Erro` `[ ] Pendente` |
| 8 | Integração com Outros Módulos | `[ ] OK` `[ ] Erro` `[ ] Pendente` |

**Total de cenários:** 8
**Aprovados:** ___
**Com erro:** ___
**Pendentes:** ___

**Severidade geral:** `[ ] Alta` `[ ] Média` `[ ] Baixa`

**Observações finais:**
> _(descrever aqui qualquer observação relevante sobre o comportamento da tela)_

**Evidências:**
> _(listar e anexar todos os prints/vídeos coletados)_

---
_Checklist gerado com auxílio do GitHub Copilot — @AgnaldoBarros | Release 2026.05.015_
