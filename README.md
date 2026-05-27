# Projeto de Consolidação e Liberação de Acesso de Avaliadores

#### Descrição

Este projeto tem como objetivo automatizar o processo de consolidação, padronização, validação e geração de arquivos de liberação de acesso para avaliadores vinculados ao projeto de manutenção predial da FDE.

#### O fluxo realiza:

- Leitura automática de múltiplos arquivos Excel distribuídos por lotes
- Consolidação das bases de avaliadores
- Padronização de colunas
- Tratamento de duplicidades
- Criação de carga histórica
- Identificação de novos registros
- Geração de carga incremental
- Geração automática do arquivo final de liberação de acesso
- Controle de primeira execução (Carga Full) e execuções subsequentes (Carga Incremental)

O projeto foi desenvolvido em Python utilizando pandas para manipulação de dados.

#### Estrutura do Projeto

Projeto/
│
├── Lote 1/
│   └── Cadastro_Avaliador_Lote1.xlsx
│
├── Lote 2/
│   ├── Cadastro_Avaliador_Lote2.xlsx
│   └── Cadastro Pré Teste_TUV Rheinland - Lote 2.xlsx
│
├── Lote 3/
│   └── Cadastro_Avaliador_Lote3.xlsx
│
├── Lote 4/
│   └── Cadastro_Avaliador_Lote4.xlsx
│
├── Base_Historica_Avaliadores.xlsx
├── Base_Unificada_Lotes_Atualizada.xlsx
├── Novos_Avaliadores.xlsx
│
├── Liberacao_Acesso_App/
│   └── liberacao_acesso.xlsx
│
├── controle_carga_full_liberacao.txt
│
└── script.py

#### 2. Padronização de Colunas

#### O processo realiza:

- Remoção de caracteres especiais
- Padronização de acentos
- Conversão para maiúsculo
- Substituição de espaços por _

#### 3. Tratamento de Duplicidades

O processo cria uma chave única baseada nos campos:

- Nome completo do avaliador
- RG
- CPF
- E-mail pessoal
- Telefone
- Cargo

Essa chave é utilizada para remover registros duplicados.





