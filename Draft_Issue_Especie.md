# Teste Caixa Preta - Espécie (CRUD Completo)

## Identificação
- **Módulo:** [Especificar módulo onde Espécie está localizado]
- **Programa/Sistema:** SOPHIAERP
- **Resource (Tela):** `Especie` → https://dsv17ff105.sophiaerp.cloud/Especie
- **Action (Ação):** create, read, update, delete
- **Funcionalidade:** Gestão de Espécies (Classificação de Documentos/Títulos)
- **Versão do ERP:** <!-- Preencher na execução -->
- **Responsável pelo teste:** <!-- Seu nome -->
- **Data do teste:** <!-- Data de hoje -->
- **Ambiente:** Desenvolvimento (dsv17ff105)

---

## Campos do Recurso (Espécie)

| Campo | Descrição | Obrigatório |
|-------|-----------|:-----------:|
| EspcId | ID da Espécie | **Sim** |
| EspcDescricao | Descrição da Espécie | **Sim** |
| EspcStatus | Status (Ativo/Inativo) | Não |
| EspcTipo | Tipo de Espécie | Não |

---

## Cenário 1 — READ (Listagem / Consulta)

### Pré-condições
> Usuário logado com permissão no módulo. Ao menos uma espécie cadastrada.

### Passos para reprodução
1. Acessar **Espécie**
2. Verificar se a listagem carrega corretamente com as colunas esperadas
3. Utilizar filtros disponíveis
4. Utilizar o campo de **Pesquisa** (texto) para buscar espécies
5. Validar **paginação** (navegação entre páginas, itens por página)

### Resultado Esperado
> Listagem exibida corretamente, filtros e paginação funcionais, colunas exibindo os dados corretamente.

### Resultado Obtido
> <!-- Preencher após execução -->

### Status: <!-- [ ] Erro  [ ] Ok  [ ] Pendente -->

---

## Cenário 2 — CREATE (Inclusão de Nova Espécie)

### Pré-condições
> Usuário logado com permissão de escrita.

### Passos para reprodução
1. Na listagem de Espécie, clicar no botão **Adicionar**
2. Preencher os campos obrigatórios (Descrição, etc.)
3. Preencher campos opcionais conforme necessário
4. Clicar em **Salvar**

### Resultado Esperado
> Espécie criada com sucesso, mensagem de confirmação exibida e registro visível na listagem.

### Resultado Obtido
> <!-- Preencher após execução -->

### Status: <!-- [ ] Erro  [ ] Ok  [ ] Pendente -->

---

## Cenário 3 — UPDATE (Edição de Espécie Existente)

### Pré-condições
> Registro de espécie existente na listagem.

### Passos para reprodução
1. Na listagem, localizar o registro desejado e clicar no ícone de **Editar** (lápis)
2. Verificar se todos os campos são carregados corretamente no formulário
3. Alterar um ou mais campos (ex: Descrição, Status, Tipo)
4. Clicar em **Salvar**

### Resultado Esperado
> Registro atualizado com sucesso, mensagem de confirmação exibida e alterações refletidas na listagem.

### Resultado Obtido
> <!-- Preencher após execução -->

### Status: <!-- [ ] Erro  [ ] Ok  [ ] Pendente -->

---

## Cenário 4 — DELETE (Exclusão de Espécie)

### Pré-condições
> Registro de espécie existente.

### Passos para reprodução
1. Na listagem, clicar no ícone de **Excluir** (lixeira) do registro desejado
2. Verificar se o diálogo **"Confirmar Exclusão"** é exibido
3. Clicar em **Excluir** para confirmar
4. Verificar que o registro foi removido da listagem

### Resultado Esperado
> Registro excluído com sucesso, mensagem de confirmação exibida, registro não aparece mais na listagem.

### Resultado Obtido
> <!-- Preencher após execução -->

### Status: <!-- [ ] Erro  [ ] Ok  [ ] Pendente -->

---

## Cenário 5 — Visualização (Readonly)

### Passos para reprodução
1. Na listagem, clicar no ícone de **Visualizar** de um registro
2. Verificar se o formulário é aberto em modo **somente leitura** (campos desabilitados)
3. Verificar que os botões de Salvar **não estão disponíveis**

### Resultado Esperado
> Formulário exibido em modo leitura, sem possibilidade de edição.

### Resultado Obtido
> <!-- Preencher após execução -->

### Status: <!-- [ ] Erro  [ ] Ok  [ ] Pendente -->

---

## Cenário 6 — Validações de Campos Obrigatórios

### Passos para reprodução
1. Abrir o formulário de criação e tentar salvar **sem preencher a Descrição** → verificar mensagem de validação
2. Verificar se campos de combo (Status, Tipo, etc.) são preenchidos corretamente ao carregar o formulário
3. Validar comportamento de campos obrigatórios

### Resultado Esperado
> Para campos obrigatórios sem preenchimento, o sistema exibe mensagem de erro e não grava. Combos carregam corretamente.

### Resultado Obtido
> <!-- Preencher após execução -->

### Status: <!-- [ ] Erro  [ ] Ok  [ ] Pendente -->

---

## Resultados Consolidados

- **Severidade/Prioridade:** <!-- Média/Alta -->
- **Observações:**
  > <!-- A tabela de Espécies é utilizada para classificar documentos/títulos no ERP. Adicionar observações relevantes -->
- **Evidências:**
  - <!-- Anexar prints/vídeos após execução -->

---

### Observação
> Preencha um item para cada teste realizado. Caso identifique múltiplos cenários, crie issues separadas para cada um.
