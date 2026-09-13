# Regra Global 002: Estrutura de Diretórios e Relatório de Execução de Specs

Este documento define o padrão arquitetural para o armazenamento das especificações (Specs) no repositório, bem como a obrigatoriedade de documentação pós-execução.

## 1. Localização e Estrutura de Pastas

Todas as especificações técnicas residem obrigatoriamente dentro do diretório `.agent/specs/`. Para manter a organização, a estrutura deve seguir estritamente o padrão de **pastas numeradas**.

* **Padrão da Pasta:** Cada spec deve ser isolada em sua própria pasta, iniciando com um número sequencial de 3 dígitos (ex: `001-nome-da-tarefa/`).
* **Arquivo da Spec:** Dentro desta pasta, o arquivo principal de especificação deve ter **exatamente o mesmo nome da pasta pai**, acrescido da extensão `.spec.md`.
* **Arquivo do Implementation Plan:** Dentro desta pasta, o arquivo principal de plano de implementação deve ter **exatamente o mesmo nome da spec**, acrescido da extensão `.plan.md`.

## 2. Regra de Implementação (Registro Obrigatório)

Para garantir a rastreabilidade, é estritamente proibido finalizar uma tarefa sem registrar suas alterações.

Sempre que a implementação de uma spec for concluída, o executor (Humano ou IA) **DEVE** criar um arquivo com o nome da spec tirando o "spec" e substituindo por "plan" **dentro da pasta correspondente à spec executada**.

### O que o arquivo `*.plan.md` deve conter:
1. **Arquivos Afetados:** Lista dos arquivos criados, modificados ou excluídos.
2. **Ações Realizadas:** Resumo do que foi implementado.
3. **Decisões:** Qualquer dependência nova instalada ou decisão técnica tomada.