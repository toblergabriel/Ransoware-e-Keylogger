# 🔐 Estudos de Cibersegurança com Python
### Simulação de Ransomware e Keylogger

## 📌 Sobre o projeto

Este projeto foi desenvolvido para estudos pessoais, com o objetivo de compreender, na prática, o funcionamento de algumas ameaças digitais utilizando a linguagem Python.

O projeto apresenta dois experimentos educacionais:

- **Ransomware Simulado:** estudo de criptografia e descriptografia de arquivos, com geração de uma mensagem fictícia de resgate.
- **Keylogger Simulado:** estudo da captura de eventos do teclado utilizando Python e registro das teclas em um arquivo de texto.

A proposta é entender como essas ameaças funcionam, identificar os riscos envolvidos e conhecer medidas de prevenção e defesa.

## 🎯 Objetivos

- Compreender o funcionamento básico de Ransomware e Keylogger.
- Explorar bibliotecas Python utilizadas em estudos de segurança.
- Entender os conceitos de criptografia e descriptografia.
- Estudar a captura de eventos do teclado.
- Identificar riscos relacionados à exposição de informações.
- Conhecer mecanismos de proteção contra ameaças digitais.

---

## 🦠 1. Ransomware Simulado

O primeiro experimento aborda o funcionamento de um Ransomware, um tipo de malware que utiliza criptografia para impedir o acesso aos arquivos de uma vítima.

### Arquivos utilizados

- `ransoware.py`: responsável pela geração da chave e criptografia dos arquivos.
- `descriptografar.py`: responsável por recuperar os arquivos utilizando a chave gerada.
- `chave.key`: arquivo que armazena a chave criptográfica.
- `LEIA ISSO.txt`: mensagem fictícia de resgate.
- `test_files/`: diretório com arquivos utilizados nos experimentos.

### Funcionamento

**Criptografia:**
1. Geração de uma chave utilizando Fernet.
2. Armazenamento da chave em um arquivo.
3. Leitura dos arquivos presentes no diretório de testes.
4. Criptografia dos arquivos.
5. Criação de uma mensagem fictícia de resgate.

**Descriptografia:**
1. Leitura da chave criptográfica.
2. Localização dos arquivos de teste.
3. Descriptografia dos conteúdos.
4. Recuperação dos arquivos originais.

### Biblioteca utilizada

`cryptography` — biblioteca Python utilizada para implementar a criptografia Fernet.

Instalação:

```bash
python -m pip install cryptography
```

---

## ⌨️ 2. Keylogger Simulado

O segundo experimento aborda o funcionamento de um Keylogger, ferramenta capaz de registrar eventos do teclado durante sua execução.

O script foi desenvolvido utilizando Python e a biblioteca `pynput`.

### Funcionamento

O programa utiliza um listener para identificar as teclas pressionadas e registrar as informações em um arquivo chamado `log.txt`.

Entre as funcionalidades estudadas estão:

- Captura de caracteres digitados.
- Registro de espaços e quebras de linha.
- Identificação de teclas especiais.
- Ignorar determinadas teclas modificadoras, como Shift, Ctrl e Alt.
- Registro dos eventos em um arquivo `.txt`.

### Tratamento das teclas

O código utiliza condições para diferenciar algumas teclas especiais:

| Tecla | Comportamento |
|---|---|
| Espaço | Registra um espaço |
| Enter | Adiciona uma quebra de linha |
| Tab | Registra uma tabulação |
| Backspace | Registra um espaço no arquivo |
| Esc | Registra `[ESC]` |
| Shift / Ctrl / Alt | Ignora os eventos |
| Outras teclas especiais | Registra sua representação |

### Biblioteca utilizada

`pynput` — biblioteca Python que permite monitorar e controlar dispositivos de entrada, como teclado e mouse.

Instalação:

```bash
python -m pip install pynput
```

Execução:

```bash
python keylogger.py
```

O arquivo `log.txt` é criado no diretório de execução e recebe os registros durante o funcionamento do programa.

**Observação:** este experimento não possui implementação de envio automático por e-mail. O código apresentado realiza somente a captura e o registro local dos eventos.

---

## 🛡️ 3. Segurança e Prevenção

Além dos experimentos, o projeto aborda algumas medidas importantes para proteção contra ameaças digitais:

- **Antivírus:** identificação e bloqueio de arquivos e comportamentos maliciosos.
- **Firewall:** monitoramento e controle das conexões de rede.
- **Backups:** manutenção de cópias de segurança para recuperação de arquivos.
- **Sandboxing:** execução de programas suspeitos em ambientes isolados.
- **Conscientização:** cuidado com links, anexos e arquivos desconhecidos.
- **Monitoramento:** identificação de atividades suspeitas no sistema.
- **Privacidade:** proteção de informações pessoais e credenciais.

## 🛠️ Tecnologias e ferramentas

- Python 3
- Cryptography (Fernet)
- Pynput
- Visual Studio Code
- Kali Linux

## 📚 Aprendizados

O desenvolvimento desses experimentos proporcionou uma visão mais prática sobre conceitos de cibersegurança e programação com Python.

Foi possível compreender como determinadas ameaças digitais operam, como arquivos podem ter seu acesso comprometido e como informações digitadas podem ser expostas por programas maliciosos.

Além da implementação dos scripts, o projeto reforçou a importância de medidas preventivas, como backups, monitoramento de atividades suspeitas, proteção de credenciais e conscientização dos usuários.

## ⚠️ Aviso de segurança

Este projeto possui finalidade exclusivamente educacional e foi desenvolvido como parte dos estudos em cibersegurança.

Os experimentos devem ser executados somente em ambientes controlados, com arquivos fictícios e autorização adequada.

O Keylogger deve ser utilizado exclusivamente em sessões próprias e autorizadas. Não utilize os scripts para monitorar terceiros ou coletar informações sem consentimento.

Não publique chaves criptográficas, senhas reais ou registros que contenham informações pessoais.

## 🎓 Créditos

Projeto desenvolvido durante os estudos na plataforma **Digital Innovation One (DIO)**.

**Autor:** Gabriel

**Área de estudo:** Cibersegurança e Python

---

*Conhecer o funcionamento das ameaças digitais é um passo importante para aprender a identificá-las e se defender delas.*
