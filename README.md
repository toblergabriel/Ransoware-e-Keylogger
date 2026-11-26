# Estudos de Cibersegurança com Python
### Ransomware simulado | DIO

## Sobre o projeto

Projeto desenvolvido durante os estudos na Digital Innovation One (DIO), com o objetivo de compreender conceitos de cibersegurança por meio de um experimento controlado em Python.

Esta versão do material contém a simulação de um **Ransomware**, com scripts para criptografar e descriptografar arquivos de teste usando a biblioteca `cryptography` e o mecanismo Fernet.

> **Escopo:** o ZIP enviado contém os scripts do experimento de Ransomware. Não foi encontrado um script de Keylogger entre os arquivos recebidos, então essa parte não é apresentada como implementada.

## Estrutura

```text
estudos-ciberseguranca-python/
├── README.md
└── ransoware/
    ├── ransoware.py
    ├── descriptografar.py
    └── test_files/
        ├── senhas.txt
        └── dados_confidenciais.txt
```

Os arquivos `.txt` desta versão foram substituídos por conteúdo fictício. A chave `chave.key` e a mensagem `LEIA ISSO.txt` são geradas durante a execução e não são incluídas no repositório.

## Como funciona

### `ransoware.py`

- Gera uma chave Fernet e grava em `chave.key`.
- Lê os arquivos do diretório `test_files`.
- Criptografa o conteúdo desses arquivos.
- Gera `LEIA ISSO.txt` com uma mensagem fictícia de resgate.

### `descriptografar.py`

- Carrega a chave `chave.key`.
- Localiza os arquivos em `test_files`.
- Descriptografa os conteúdos para restaurar os arquivos.

## Requisitos

- Python 3
- Biblioteca `cryptography`

Instalação:

```bash
python -m pip install cryptography
```

## Execução

Abra o terminal dentro da pasta `ransoware`:

```bash
python ransoware.py
```

Para restaurar os arquivos, execute:

```bash
python descriptografar.py
```

**Importante:** execute a descriptografia com a mesma chave gerada na etapa de criptografia. Não apague nem substitua `chave.key` antes de restaurar os arquivos.

Use somente arquivos descartáveis em `test_files`. O script sobrescreve os arquivos durante a criptografia. Não execute novamente a criptografia sobre arquivos que já estejam criptografados: uma nova chave será gerada e poderá impedir a recuperação com a chave anterior.

## Conceitos estudados

- Criptografia e descriptografia de arquivos.
- Criptografia simétrica autenticada com Fernet.
- Geração e armazenamento de chaves.
- Impacto de ransomware na disponibilidade dos dados.
- Importância de backups e de ambientes isolados para testes.

## Defesa e prevenção

- Manter backups atualizados e testar a restauração.
- Utilizar antivírus/EDR e manter o sistema atualizado.
- Aplicar o princípio do menor privilégio.
- Desconfiar de anexos e links inesperados.
- Isolar arquivos e programas suspeitos em sandbox.
- Proteger chaves criptográficas e credenciais.

## Limitações

Este é um exercício didático e simplificado. A chave é armazenada localmente e os scripts atuam apenas sobre o diretório de testes configurado. O experimento não representa uma solução de segurança nem um ransomware real completo.

## Keylogger

O material enviado para esta versão não continha um script de Keylogger. Essa etapa poderá ser adicionada posteriormente, com foco em captura autorizada, privacidade e mecanismos de defesa.

## Créditos

Estudo realizado durante a trilha de cibersegurança com Python da **Digital Innovation One (DIO)**.

**Autor:** Gabriel  
**Área:** Cibersegurança e Python

---
*Entender como as ameaças funcionam também faz parte de aprender a se defender delas.*
