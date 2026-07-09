# Teste Caixa Preta - Configurações de Faturamento (CRUD Completo / DD000)

## Identificação
- **Módulo:** Faturamento > Regras Fiscais
- **Programa/Sistema:** SOPHIAERP (CS110A_GestaoERP)
- **Resource (Tela):** `ConfigFaturamento` → https://dsv17.sophiaerp.cloud/ConfigFaturamento
- **Action (Ação):** create, read, update, delete, patch (certificado digital), webservices
- **Funcionalidade:** Configuração de Faturamento por Estabelecimento (DD000)
- **Versão do ERP:** <!-- Preencher na execução -->
- **Responsável pelo teste:** AgnaldoBarros
- **Data do teste:** 2026-05-18
- **Ambiente:** Desenvolvimento (dsv17)

---

## Campos do Recurso (ICsicp_Dd000)

| Campo | Descrição | Obrigatório |
|-------|-----------|:-----------:|
| Dd000FilialId | Estabelecimento/Filial | **Sim** |
| Dd000CtrlSerieNfId | Série NF-e | Não |
| Dd000PvCcustoId | Centro de Custo - Pré-Venda | Não |
| Dd000PvAgcobradorId | Agente Cobrador - Pré-Venda | Não |
| Dd000PvNatoperacaoId | Natureza de Operação - Pré-Venda | Não |
| Dd000PvContaId | Conta - Pré-Venda | Não |
| Dd000PdCcustoId | Centro de Custo - Pedido Venda | Não |
| Dd000PdAgcobradorId | Agente Cobrador - Pedido Venda | Não |
| Dd000PdNatoperacaoId | Natureza de Operação - Pedido Venda | Não |
| Dd000PdvCcustoId | Centro de Custo - PDV | Não |
| Dd000CtCcustoId | Centro de Custo - Contrato Venda | Não |
| Dd000NdCcustoId | Centro de Custo - Nota Direta | Não |
| Dd000DcCcustoId | Centro de Custo - Devolução Compra | Não |
| Dd000DisCcustoId | Centro de Custo - Devolução Interna Saída | Não |
| Dd000RegraLimiteDesconto | Regra de Limite de Desconto | Não |
| Dd000QualRegraAplicar | Qual Regra Aplicar | Não |
| Dd000FormaCalculo | Forma de Cálculo | Não |
| Dd000OrigemCalculo | Origem do Cálculo | Não |
| Dd000AmbienteNfe | Ambiente NF-e (Homologação/Produção) | Não |
| Dd000VersaoNfe | Versão NF-e | Não |
| Dd000FusoHorario | Fuso Horário | Não |
| Dd000LocalCertificado | Local do Certificado Digital | Não |
| Dd000AlmoxarifadoId | Almoxarifado padrão | Não |

---

## Cenário 1 — READ (Listagem / Consulta)

### Pré-condições
> Usuário logado com permissão no módulo Faturamento. Ao menos uma configuração de faturamento cadastrada.

### Passos para reprodução
1. Acessar o menu **Faturamento > Regras Fiscais > Config. Faturamento**
2. Verificar se a listagem carrega corretamente com as colunas: Estabelecimento, Série NF-e, Conta PV, Vinculações (Pré-Venda, Pedido Venda, Contrato Venda), Ações
3. Utilizar o filtro por **Estabelecimento** e verificar filtragem
4. Utilizar o campo de **Pesquisa** (texto) e verificar filtragem por C. Custo / Agente Cobrador / Natureza de Operação
5. Validar **paginação** (navegação entre páginas, itens por página)

### Resultado Esperado
> Listagem exibida corretamente, filtros e paginação funcionais, colunas de vinculações exibindo os nomes corretamente.

### Resultado Obtido
>  Preencher após execução 

### Status: 
- [ ] Erro
- [ ] [ ] Ok
- [ ] [ ] Pendente

<!-- Preencher após execução -->
---

## Cenário 2 — CREATE (Inclusão de Nova Configuração)

### Pré-condições
> Usuário logado com permissão de escrita. Estabelecimento, Série NF-e, Centros de Custo, Naturezas de Operação e Agentes Cobradores previamente cadastrados.

### Passos para reprodução
1. Na listagem de Config. Faturamento, clicar no botão **Adicionar**
2. Selecionar o **Estabelecimento** (obrigatório)
3. Selecionar a **Série NF-e**
4. Preencher as vinculações da **grade de Vendas**: CC, Agente Cobrador e Natureza de Operação para cada tipo (Pré-Venda, Pedido Venda, Contrato Venda, Nota Direta, Devolução Compra, PDV, Devolução Interna Saída)
5. Preencher as configurações de **Desconto**: Regra de Limite, Qual Regra Aplicar, Forma de Cálculo, Origem de Cálculo
6. Preencher as configurações de **NF-e**: Ambiente, Versão, Fuso Horário, Local do Certificado
7. Selecionar o **Almoxarifado**
8. Clicar em **Salvar**

### Resultado Esperado
> Configuração criada com sucesso, mensagem de confirmação exibida e registro visível na listagem.

### Resultado Obtido
>  Preencher após execução 

### Status: 
- [ ] Erro
- [ ] [ ] Ok
- [ ] [ ] Pendente

---

## Cenário 3 — UPDATE (Edição de Configuração Existente)

### Pré-condições
> Registro de configuração de faturamento existente na listagem.

### Passos para reprodução
1. Na listagem, localizar o registro desejado e clicar no ícone de **Editar** (lápis)
2. Verificar se todos os campos são carregados corretamente no formulário
3. Alterar um ou mais campos (ex: Série NF-e, Ambiente NF-e, Centro de Custo de um tipo de vinculação)
4. Clicar em **Salvar**

### Resultado Esperado
> Registro atualizado com sucesso, mensagem de confirmação exibida e alterações refletidas na listagem.

### Resultado Obtido
>  Preencher após execução 

### Status: 
- [ ] Erro
- [ ] [ ] Ok
- [ ] [ ] Pendente

---

## Cenário 4 — DELETE (Exclusão de Configuração)

### Pré-condições
> Registro de configuração de faturamento existente.

### Passos para reprodução
1. Na listagem, clicar no ícone de **Excluir** (lixeira) do registro desejado
2. Verificar se o diálogo **"Confirmar Exclusão"** é exibido
3. Clicar em **Excluir** para confirmar
4. Verificar que o registro foi removido da listagem

### Resultado Esperado
> Registro excluído com sucesso, mensagem de confirmação exibida, registro não aparece mais na listagem.

### Resultado Obtido
>  Preencher após execução 

### Status: 
- [ ] Erro
- [ ] [ ] Ok
- [ ] [ ] Pendente

---

## Cenário 5 — PATCH Certificado Digital (Upload)

### Pré-condições
> Registro de configuração de faturamento existente. Arquivo de certificado digital `.pfx` disponível.

### Passos para reprodução
1. Na listagem, clicar no ícone de **Certificado Digital** do registro desejado
2. Verificar se o diálogo de upload é exibido
3. Selecionar o arquivo `.pfx` do certificado
4. Preencher o campo **Senha** do certificado
5. Clicar em **Salvar**

### Resultado Esperado
> Certificado digital associado com sucesso, mensagem de confirmação exibida.

### Resultado Obtido
>  Preencher após execução 

### Status: 
- [ ] Erro
- [ ] [ ] Ok
- [ ] [ ] Pendente

---

## Cenário 6 — Web Services de NF (Dd000W)

### Pré-condições
> Registro de configuração de faturamento existente.

### Passos para reprodução
1. Na listagem, clicar no ícone de **Web Services** de um registro
2. Verificar se a tela `/ConfigFaturamento/:configId/WebServices` é carregada
3. Adicionar um novo Web Service preenchendo os campos: NF-CF, Serviço NF-e, UF
4. Salvar e verificar na listagem de Web Services
5. Editar um Web Service existente
6. Excluir um Web Service existente

### Resultado Esperado
> CRUD de Web Services de NF funcionando corretamente, navegação da tela pai para filha sem erros.

### Resultado Obtido
>  Preencher após execução 

### Status: 
- [ ] Erro
- [ ] [ ] Ok
- [ ] [ ] Pendente

---

## Cenário 7 — Visualização (Readonly)

### Passos para reprodução
1. Na listagem, clicar no ícone de **Visualizar** de um registro
2. Verificar se o formulário é aberto em modo **somente leitura** (campos desabilitados)
3. Verificar que os botões de Salvar **não estão disponíveis**

### Resultado Esperado
> Formulário exibido em modo leitura, sem possibilidade de edição.

### Resultado Obtido
>  Preencher após execução 

### Status: 
- [ ] Erro
- [ ] [ ] Ok
- [ ] [ ] Pendente

---

## Cenário 8 — Validações de Campos Obrigatórios

### Passos para reprodução
1. Abrir o formulário de criação e tentar salvar **sem selecionar o Estabelecimento** → verificar mensagem de validação
2. Verificar se campos de combo (Regra de Desconto, Ambiente NF-e, etc.) são preenchidos corretamente ao carregar o formulário
3. Verificar se a **Série NF-e** filtra conforme o Estabelecimento selecionado

### Resultado Esperado
> Para o campo Estabelecimento (obrigatório) sem preenchimento, o sistema exibe mensagem de erro e não grava. Combos carregam corretamente. Série NF filtra por filial.

### Resultado Obtido
>  Preencher após execução 

### Status: 
- [ ] Erro
- [ ] [ ] Ok
- [ ] [ ] Pendente

---

## Resultados Consolidados

- **Severidade/Prioridade:** Alta
- **Observações:**
  > A tabela `DD000` é central para o processo de faturamento — vincula estabelecimento, série NF-e, naturezas de operação, centros de custo e agentes cobradores para cada tipo de documento (Pré-Venda, Pedido Venda, Contrato Venda, Nota Direta, Devolução). Também concentra a configuração de NF-e (ambiente, versão, certificado digital). Validar especialmente a integridade dos dados de vinculação e o upload do certificado digital.
- **Evidências:**
  - <!-- Anexar prints/vídeos após execução -->

---

### Observação
> Preencha um item para cada teste realizado. Caso identifique múltiplos cenários, crie issues separadas para cada um.
