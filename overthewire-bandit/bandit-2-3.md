## 🏴‍☠️ Bandit Level 3 - OverTheWire

**Data**: 28/04/2026  
**Tempo gasto**: ~8 min  
**Dificuldade**: ★☆☆☆☆

Resolução do Level 3 do wargame Bandit da OverTheWire. Projeto focado em praticar comandos Linux básicos e conceitos de segurança.

## 🎯 Objetivo do Nível

O Level 3 ensina como encontrar arquivos ocultos em diretórios. A senha para o Level 4 está armazenada em um arquivo oculto no diretório `inhere`.

**Credenciais Level 3:**
- **Host:** bandit.labs.overthewire.org
- **Port:** 2220  
- **Usuário:** bandit3
- **Senha:** Você descobre no Level 2

## 🛠️ Comandos Utilizados

| Comando | Descrição |
| --- | --- |
| `ssh` | Conectar no servidor remoto via SSH |
| `ls -la` | Listar todos arquivos, incluindo ocultos |
| `cat` | Ler conteúdo de arquivos |
| `cd` | Navegar entre diretórios |
| `file` | Identificar tipo de arquivo |

## 📚 Resolução Passo a Passo

1. **Conectar no servidor:**
   ```bash
   ssh bandit3@bandit.labs.overthewire.org -p 2220

2. **Entrar no diretório indicado:**
   ```bash
   cd inhere

3. **Listar arquivos ocultos:**
   ```bash
   ls -la
   ```
   Arquivos ocultos começam com .

4. **Ler o arquivo oculto encontrado:**
   ```bash
   cat .hidden
5. **Senha do Level 4 encontrada ✅**

## 💡 Principais Aprendizados

- Arquivos ocultos no Linux começam com . e não aparecem no ls normal
- ls -a mostra todos, ls -la mostra em lista com detalhes e permissões
- Wargames são laboratórios seguros pra praticar pentest e linha de comando
- Sempre explorar com ls -la ao entrar em diretórios desconhecidos

## 🚀 Próximo Nível

**Level 4:** Arquivos legíveis apenas por humanos → Dica: use `file./-*` pra identificar o tipo

## 🔗 Links Úteis

- [OverTheWire Bandit Level 3](https://overthewire.org/wargames/bandit/bandit3.html)
- [Manual do ls](https://man7.org/linux/man-pages/man1/ls.1.html)

---
**Status:** ✅ Concluído | **Próximo:** Bandit Level 4
