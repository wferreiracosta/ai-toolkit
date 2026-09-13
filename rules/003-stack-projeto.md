# Regra Global 003: Stack Tecnológica e Ferramentas Padrão

Este documento estabelece as tecnologias, ferramentas e restrições obrigatórias para o ciclo de desenvolvimento do repositório.

## 1. Tecnologias Homologadas

O projeto opera com escopo estrito de ferramentas para garantir consistência e simplicidade na manutenção:

- Linguagem: Python (versão 3.10+ recomendada). Todo o código-fonte, scripts auxiliares e testes devem ser escritos exclusivamente em Python.

- Controle de Versão: Git. Utilizado para rastreamento de histórico, ramificação e controle de mudanças.

## 2. Restrições e Governança

Para evitar fragmentação técnica e dependências desnecessárias, aplicam-se as seguintes regras:

- Exclusividade da Stack: É estritamente proibido introduzir outras linguagens de programação, runtimes alternativos (como Node.js, Go, Rust, Ruby) ou ferramentas paralelas sem aprovação formal e atualização prévia desta regra.

- Gerenciamento de Ambiente: Ambientes virtuais (venv) devem ser utilizados localmente e mantidos fora do controle de versão (registrados no .gitignore).

- Versionamento Limpo: Nenhum binário compilado, cache (__pycache__/, *.pyc) ou artefato temporário deve ser versionado no Git.

## 3. Adição de Novas Dependências

Caso uma tarefa demande bibliotecas externas ou frameworks em Python:

- A necessidade deve ser descrita e justificada previamente na Spec (*.spec.md).

- A inclusão da biblioteca deve ser formalmente documentada na seção de Decisões do arquivo de plano de implementação (*.plan.md).

- As dependências devem ser consolidadas no arquivo de regras da stack `.agent\rules\003-stack-projeto.md`

## 4. Dependências Externas Homologadas

As seguintes bibliotecas externas foram aprovadas e homologadas para o projeto:

- **`requests`** (>= 2.31.0): Utilizado para requisições HTTP seguras, controle de cabeçalhos de navegação (User-Agent/Referer) e download com streaming de conteúdo binário.
- **`beautifulsoup4`** (>= 4.12.0): Utilizado para raspagem e análise resiliente do DOM HTML e extração de metadados e scripts JSON-LD.