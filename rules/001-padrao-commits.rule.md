# Regra Global 001: Padrão de Commits (Git)

Este documento define o padrão inegociável para as mensagens de commit no repositório. Todos os desenvolvedores humanos e agentes de IA devem seguir a especificação abaixo, baseada no **Conventional Commits**.

## 1. Estrutura da Mensagem

A mensagem do commit DEVE seguir estritamente o formato abaixo. Observe que **deve haver um espaço em branco** após os dois-pontos.

> <tipo>: <descrição curta>

## 2. Tipos Permitidos

* **`feat`**: Inclui um **novo recurso** ou funcionalidade.
* **`fix`**: Soluciona um **problema ou bug**.
* **`docs`**: Mudanças exclusivas na **documentação** (ex: README, `.md`).
* **`test`**: Criação, alteração ou exclusão de **testes automatizados**.
* **`build`**: Modificações em arquivos de **build e dependências**.
* **`perf`**: Alterações focadas exclusivamente em melhorar a **performance**.
* **`style`**: Alterações referentes à **formatação do código** (linting, espaçamentos).
* **`refactor`**: Refatorações que **não alteram a funcionalidade final**.
* **`chore`**: Atualizações de **tarefas de manutenção** (ex: atualizar `.gitignore`).
* **`ci`**: Mudanças relacionadas a scripts de **Integração Contínua (CI)**.
* **`raw`**: Mudanças em arquivos de configuração brutos ou parâmetros.
* **`cleanup`**: Remoção de código comentado ou limpeza geral.
* **`remove`**: Exclusão definitiva de arquivos ou funcionalidades obsoletas.

## 3. Exemplos Práticos

* ✅ `feat: implementa rotina de download de imagens`
* ✅ `chore: adiciona configuracoes locais no gitignore`
* ❌ `feature: Implementado busca` *(Erro: usou "feature" em vez de "feat")*
* ❌ `fix:bug no login` *(Erro: faltou o espaço após os dois-pontos)*

## 4. Arquivos para serem commitados

* Sempra faça o commit do arquivo da spec e plano de implementação
* Respeite as regras do .gitignore
* Nunca deixe token, urls ou caminho de pastas no commit

## 5. Condição Prévia Obrigatória (Aprovação)

- Commit somente após aprovação: Nenhum commit deve ser realizado sem que as alterações tenham sido explicitamente revisadas e aprovadas pelo responsável (ou usuário solicitante).

- Validação prévia: Antes de solicitar a aprovação para o commit, certifique-se de que testes, lint e builds necessários foram executados com sucesso.