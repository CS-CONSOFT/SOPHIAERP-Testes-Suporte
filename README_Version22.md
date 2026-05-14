# Repositório de Testes Funcionais – SOPHIAERP

Este repositório é dedicado ao registro estruturado dos testes realizados pela equipe de Suporte no SOPHIAERP, utilizando issues para cada avaliação, independentemente do resultado.

## Objetivo

- Centralizar registros de testes de telas (Resources) e ações (Actions) do SOPHIAERP.
- Padronizar documentação dos cenários testados, evidenciando o comportamento do sistema e facilitando acompanhamento pelo time técnico.
- Cada avaliação/teste deve ser cadastrada como uma Issue neste repositório, utilizando o template padrão.

---

## Gabarito de Registro (Checklist do Suporte)

Ao realizar um teste, preencha estes campos:

- **Módulo:** Nome do módulo funcional do ERP (Ex: Cadastro de Clientes).
- **Programa/Sistema:** Sempre "SOPHIAERP".
- **Resource (Tela):** Identificador técnico da tela (Ex: cliente_list).
- **Action (Ação):** Ação executada (Ex: create, update, delete, read).
- **Funcionalidade:** O que está sendo testado (Ex: Criação de cliente PJ).
- **Versão do ERP:** Versão informada na tela.
- **Responsável pelo teste:** Nome do testador.
- **Data do teste:** Data de execução.
- **Ambiente:** Homologação, Produção, ou Desenvolvimento.

### Detalhes do Teste
- **Pré-condições:** O que é necessário antes de testar (Ex: usuário deve estar logado, clientes cadastrados etc.).
- **Passos para reprodução:** Lista detalhada de ações para simular o cenário.

### Resultados
- **Resultado Esperado:** O que deveria acontecer conforme os requisitos.
- **Resultado Obtido:** O que realmente aconteceu.
- **Status:** Marque se ocorreu Erro, foi Ok, ou ficou Pendente.
- **Severidade/Prioridade:** Avalie o impacto (Alta, Média, Baixa).
- **Observações:** Detalhes adicionais ou dúvidas.
- **Evidências:** Imagens/logs anexos.

---

## Sobre Resources e Actions

- **Resource:** Cada tela ou endpoint do SOPHIAERP (Exemplo: `cliente_list` = tela de listagem de clientes).
- **Action:** Operação principal realizada (CRUD - create, read, update, delete), além de outras como exportar, importar, etc.

> Sempre identifique na issue a combinação Resource + Action, isso facilita mapeamento e análise.

---

## Exemplo Preenchido

```yaml
Módulo: Cadastro
Programa/Sistema: SOPHIAERP
Resource (Tela): cliente_list
Action (Ação): create
Funcionalidade: Cadastro de novo cliente PJ
Versão do ERP: 1.2.3
Responsável pelo teste: Maria da Silva
Data do teste: 2026-05-14
Ambiente: Homologação

Pré-condições:
- Usuário com permissão de cadastro
- CPF/CNPJ não cadastrado previamente

Passos para reprodução:
1. Acessar o menu "Clientes"
2. Clicar em "Novo"
3. Preencher todos os campos obrigatórios
4. Salvar

Resultado Esperado:
- Cliente criado com sucesso, mensagem de confirmação exibida.

Resultado Obtido:
- Mensagem de sucesso exibida, cliente disponível na listagem.

Status: Ok

Severidade/Prioridade: Baixa

Observações: Teste realizado sem erros.

Evidências: (anexar prints)
```

---

## Como registrar um novo teste

1. Clique em "New Issue" e selecione o template "Teste Caixa Preta SOPHIAERP".
2. Preencha todos os campos obrigatórios com o máximo de detalhes.
3. Anexe evidências (prints, logs) conforme necessário.
4. Marque o status apropriado.

---

## Integração com GitHub Spaces

Após criar o repositório, você pode criar um [GitHub Copilot Space](https://docs.github.com/pt/early-access/copilot/spaces) e configurar prompts sugeridos para geração de drafts de issues. Recomende que o prompt inicial peça:

> Gerar rascunho de teste para o Resource X com Action Y na funcionalidade Z.

Isso permitirá criar drafts precisos, padronizados e reutilizáveis.

---