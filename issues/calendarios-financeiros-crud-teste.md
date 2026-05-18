# Teste Caixa Preta - Calendários Financeiros (CRUD)

## Identificação
- **Módulo:** Financeiro (csff120)
- **Programa/Sistema:** SOPHIAERP
- **Resource (Tela):** CalendarioView (tabelasFinanceiras/calendario)
- **Action (Ação):** create, read, update, delete
- **Funcionalidade:** Calendários Financeiros
- **Versão do ERP:** 
- **Responsável pelo teste:** 
- **Data do teste:** 2026-05-18
- **Ambiente:** Homologação

## Detalhes do Teste

### 1. CREATE - Inclusão de Calendário Financeiro
- **Pré-condições:** 
  > Usuário logado com permissão no módulo Financeiro. Estabelecimento previamente cadastrado.

- **Passos para reprodução:**
  1. Acessar o menu Tabelas Financeiras > Calendários Financeiros
  2. Clicar no botão "Adicionar"
  3. Preencher o campo "Estabelecimento"
  4. Preencher o campo "Descrição" (ex: Feriado Nacional)
  5. Preencher o campo "Nome do Dia" (ex: Natal)
  6. Preencher a data correspondente
  7. Confirmar/Salvar o registro

- **Resultado Esperado:** 
  > Registro salvo com sucesso e exibido na listagem.

- **Resultado Obtido:** 
  > <!-- Preencher após execução -->

- **Status:** <!-- [ ] Erro [ ] Ok [ ] Pendente -->

---

### 2. READ - Consulta de Calendários Financeiros
- **Pré-condições:** 
  > Ao menos um calendário financeiro cadastrado.

- **Passos para reprodução:**
  1. Acessar o menu Tabelas Financeiras > Calendários Financeiros
  2. Utilizar os filtros: Estabelecimento, Descrição ou Nome do Dia
  3. Clicar em "Pesquisar"
  4. Verificar se os dados são exibidos corretamente na tabela

- **Resultado Esperado:** 
  > Registros filtrados exibidos corretamente na listagem com paginação funcional.

- **Resultado Obtido:** 
  > <!-- Preencher após execução -->

- **Status:** <!-- [ ] Erro [ ] Ok [ ] Pendente -->

---

### 3. UPDATE - Edição de Calendário Financeiro
- **Pré-condições:** 
  > Registro de calendário financeiro já existente.

- **Passos para reprodução:**
  1. Acessar o menu Tabelas Financeiras > Calendários Financeiros
  2. Localizar o registro desejado na listagem
  3. Clicar no ícone de edição (lápis)
  4. Alterar um ou mais campos (ex: Descrição, Nome do Dia)
  5. Confirmar/Salvar as alterações

- **Resultado Esperado:** 
  > Registro atualizado com sucesso e alterações refletidas na listagem.

- **Resultado Obtido:** 
  > <!-- Preencher após execução -->

- **Status:** <!-- [ ] Erro [ ] Ok [ ] Pendente -->

---

### 4. DELETE - Exclusão de Calendário Financeiro
- **Pré-condições:** 
  > Registro de calendário financeiro existente e sem dependências que impeçam exclusão.

- **Passos para reprodução:**
  1. Acessar o menu Tabelas Financeiras > Calendários Financeiros
  2. Localizar o registro desejado na listagem
  3. Clicar no ícone de exclusão (lixeira)
  4. Confirmar a exclusão na caixa de diálogo
  5. Verificar que o registro foi removido da listagem

- **Resultado Esperado:** 
  > Registro excluído com sucesso e não mais exibido na listagem.

- **Resultado Obtido:** 
  > <!-- Preencher após execução -->

- **Status:** <!-- [ ] Erro [ ] Ok [ ] Pendente -->

---

- **Severidade/Prioridade:** Média

- **Observações:** 
  > Testar também o botão "Limpar" filtros e a alternância de visualização (lista/grid).

- **Evidências:**
  - <!-- Anexar prints/vídeos após execução -->

---

### Observação
> Preencha um item para cada teste realizado. Caso identifique múltiplos cenários, crie issues separadas para cada um.