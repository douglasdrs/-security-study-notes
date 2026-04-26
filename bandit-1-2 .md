# OverTheWire Bandit - Level 1 → 2

**Data**: 26/04/2026  
**Tempo gasto**: ~2 min  
**Dificuldade**: ★☆☆☆☆  

---

### 🎯 Objetivo

Conectar no servidor do Bandit via SSH usando o usuário `bandit1` na porta `2220` para encontrar a senha do Level 2. O arquivo com a senha se chama `-`.

---

### 🧠 Conceitos Aprendidos

- **`./` caminho relativo** - Força o shell a tratar o argumento como arquivo no diretório atual
- **Arquivo com nome `-`** - O shell interpreta como stdin/flag, não como nome de arquivo
- **Flag `--`** - Sinaliza para comandos o fim das opções. Tudo depois é tratado como argumento
- **`man bash`** - Seção `QUOTING` explica como o shell trata caracteres especiais

---

### 🔍 Raciocínio / Passo a passo

1. O level 1 me dá: user `bandit1`, host `bandit.labs.overthewire.org`, porta `2220`
2. Conectei com `ssh bandit1@bandit.labs.overthewire.org -p 2220`
3. Dentro do servidor rodei `ls` e apareceu um arquivo chamado `-`
4. Tentei `cat -` mas o terminal travou esperando input do stdin
5. Descobri que `./` especifica o caminho atual: `cat ./-` funcionou
6. Alternativa: `cat < -` ou `cat -- -` também resolve

---

### 💻 Comandos Úteis

ssh bandit1@bandit.labs.overthewire.org -p 2220
ls
cat ./-
cat -- -
man bash
exit

---

**Próximo Level**: `ssh bandit2@bandit.labs.overthewire.org -p 2220`  
**Senha do Level 2**: [Resolva o nível - não colocar aqui]

---
### 💬 Dúvidas ou sugestões?
- Pra perguntas gerais: [Discussions](../../discussions) 
- Pra bugs/dúvidas técnicas: [Issues](../../issues)
- Não respondo senha dos levels. Só conceito.
