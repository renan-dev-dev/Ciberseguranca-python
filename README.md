# Simulação de Ataques e Defesa em Python: Ransomware e Keylogger

Este repositório contém dois projetos práticos desenvolvidos em Python para fins puramente **educacionais e de conscientização sobre cibersegurança**:

1. **Simulador de Ransomware** (Criptografia e Descriptografia de Arquivos)
2. **Simulador de Keylogger** (Captura de Teclas em Segundo Plano)

---

# AVISO LEGAL / DISCLAIMER

> **ISENÇÃO DE RESPONSABILIDADE:** Os scripts contidos neste repositório foram desenvolvidos exclusivamente para demonstrações acadêmicas e testes em ambientes controlados (Sandbox). O uso não autorizado dessas ferramentas em sistemas de terceiros é ilegal e pode violar as leis de cibersegurança vigentes. O autor não se responsabiliza por qualquer uso indevido do código.

---

# Estrutura do Repositório

```text
ciberseguranca-python/
├── Keylogger/
│   ├── keylogger_email.py   # Script do keylogger com envio de logs
│   ├── keylogger.pyw        # Script do keylogger silencioso
│   └── log.txt              # Registro das teclas capturadas
├── Malware/
│   ├── test_files/          # Pasta com arquivos de teste para simulação
│   ├── chave.key            # Chave simétrica gerada para descriptografia
│   ├── ransomware.py        # Script que criptografa os arquivos-alvo
│   ├── descriptografar.py   # Script que restaura os arquivos criptografados
│   └── LEIA ISSO.txt        # Nota de resgate simulada
└── README.md                # Documentação oficial do repositório
```

---

# 1. Simulador de Ransomware

## Sobre o Projeto

Este módulo simula o comportamento de um ransomware moderno utilizando criptografia simétrica por meio da biblioteca `cryptography.fernet`.

## Como Funciona

**Geração de Chave:** O script `ransomware.py` gera uma chave única (`chave.key`).

**Criptografia:** O código percorre a pasta `test_files/` e criptografa o conteúdo de todos os arquivos suportados.

**Nota de Resgate:** É criado um arquivo `LEIA ISSO.txt` com instruções simuladas.

**Descriptografia:** Ao executar `descriptografar.py` com a chave correta (`chave.key`), todos os arquivos são restaurados ao seu estado original.

---

# 2. Simulador de Keylogger

## Sobre o Projeto

Este módulo captura as teclas pressionadas pelo usuário no sistema operacional para demonstrar como um malware pode obter credenciais e informações confidenciais de forma imperceptível.

## Como Funciona

**Captura de Eventos:** Utiliza bibliotecas como `pynput` para escutar as entradas do teclado em segundo plano.

**Execução Silenciosa (.pyw):** Ao utilizar a extensão `.pyw` no script, a janela do console do Windows fica oculta durante a execução.

**Armazenamento de Dados:** As teclas e frases digitadas são armazenadas continuamente no arquivo `log.txt`.
