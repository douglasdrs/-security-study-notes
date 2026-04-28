# 🏴‍☠️OverTheWire Bandit - Level 0 → 1

**Data:** 25/04/2026  
**Tempo gasto:** ~5 min  
**Dificuldade:** ★☆☆☆☆ 

## 🎯 Objetivo
Conectar no servidor do Bandit via SSH usando o usuário `bandit0` na porta `2220` para encontrar a senha do Level 1.

## 🧠 Conceitos Aprendidos
- `ssh` - protocolo para acesso remoto seguro
- Flag `-p` - especifica porta não-padrão no SSH. Porta padrão é 22
- Primeiro contato com ambiente de wargame

## 🔍 Raciocínio / Passo a passo
1. O level 0 dá todos os dados: host, user, porta e senha
2. Comando padrão do SSH é `ssh user@host`, mas precisei adicionar a porta
3. Consultei `man ssh` e vi que a flag é `-p` minúsculo
4. Conectei e dentro do servidor usei `ls` e `cat readme` pra pegar a senha do level 1

## 💻 Comandos Úteis
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
ls
cat readme
exit
