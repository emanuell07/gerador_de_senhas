# 🔐 Gerador de Senhas

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)

Gerador de senhas seguras via linha de comando (CLI) feito em Python. Permite configurar tamanho, quantidade e tipos de caracteres, com opção de salvar as senhas em arquivo.

---

## 📋 Funcionalidades

- 🔡 Senhas com letras maiúsculas e minúsculas
- 🔢 Inclusão opcional de números
- ✳️ Inclusão opcional de símbolos especiais
- 📦 Geração de múltiplas senhas de uma vez
- 💾 Salvamento automático em arquivo `.txt` com timestamp

---

## 🚀 Como usar

### Pré-requisitos

- Python 3.10 ou superior
- Nenhuma dependência externa — só biblioteca padrão!

### Instalação

```bash
git clone https://github.com/emanuell07/gerador-senhas.git
cd gerador-senhas
```

### Comandos

```bash
# Gerar 1 senha com 12 caracteres (padrão)
python gerador_de_senhas.py

# Gerar senha com 16 caracteres
python gerador_de_senhas.py -t 16

# Gerar 5 senhas de uma vez
python gerador_de_senhas.py -q 5

# Gerar sem símbolos especiais
python gerador_de_senhas.py --sem-simbolos

# Gerar sem números
python gerador_de_senhas.py --sem-numeros

# Gerar e salvar em arquivo .txt
python gerador_de_senhas.py -t 20 -q 3 --salvar

# Combinando opções
python gerador_de_senhas.py -t 16 -q 5 --sem-simbolos --salvar
```

---

## 📸 Exemplo de saída

```
🔐 5 senha(s) gerada(s):

  1. Q"^0%\_ct]X+}a9`
  2. ^WvF8J[FB(@F.K#7
  3. 5@@~xk&g.*V!6iZ(
  4. R5EKA+*YeQi{J;xS
  5. #JcG[AZd=:`}+T[c

✅ Salvo em: senhas_20260426_213305.txt
```

---

## ⚙️ Opções disponíveis

| Flag | Descrição | Padrão |
|------|-----------|--------|
| `-t`, `--tamanho` | Tamanho da senha | 12 |
| `-q`, `--quantidade` | Quantas senhas gerar | 1 |
| `--sem-simbolos` | Remove símbolos especiais | False |
| `--sem-numeros` | Remove números | False |
| `-s`, `--salvar` | Salva senhas em arquivo .txt | False |

---

## 🗂 Estrutura do projeto

```
gerador-senhas/
├── gerador_de_senhas.py   # Aplicação principal
└── README.md
```

---

## 🧠 Conceitos praticados

| Conceito | Implementação |
|---|---|
| Módulos da biblioteca padrão | `random`, `string`, `argparse`, `datetime` |
| Funções com parâmetros | `gerar_senha(tamanho, usar_simbolos, usar_numeros)` |
| CLI com flags | `argparse` com argumentos opcionais |
| Escrita em arquivo | `open()` com modo `"w"` |
| f-strings | Formatação de saída no terminal |

---

## 🛣 Próximos passos

- [ ] Verificar força da senha gerada (fraca/média/forte)
- [ ] Modo interativo sem argparse
- [ ] Copiar senha automaticamente para o clipboard com `pyperclip`
- [ ] Interface gráfica com `tkinter`

---

## 📄 Licença

Este projeto está sob a licença MIT.
