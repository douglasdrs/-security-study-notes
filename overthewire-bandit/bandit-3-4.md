## 🏴‍☠️ Bandit Level 4 - OverTheWire

**Data**: 29/04/2026
**Tempo gasto**: ~10 min
**Dificuldade**: ★★☆☆☆

Resolução do Level 4 do wargame Bandit da OverTheWire. Projeto focado em identificar tipos de arquivos no Linux.

## 🎯 Objetivo do Nível

O Level 4 ensina a diferenciar arquivos de texto de arquivos binários. A senha para o Level 5 está armazenada no único arquivo legível por humanos no diretório `inhere`.

**Credenciais Level 4:**
- **Host:** bandit.labs.overthewire.org
- **Port:** 2220  
- **Usuário:** bandit4
- **Senha:** Você descobre no Level 3

## 🛠️ Comandos Utilizados

| Comando | Descrição |
| --- | --- |
| `ssh` | Conectar no servidor remoto via SSH |
| `cd` | Navegar entre diretórios |
| `ls` | Listar arquivos |
| `file` | Identificar o tipo de arquivo |
| `cat` | Ler conteúdo de arquivos de texto |
| `./` | Executar ou referenciar arquivo no diretório atual |

## 📚 Resolução Passo a Passo

1. **Conectar no servidor:**
   ```bash
   ssh bandit4@bandit.labs.overthewire.org -p 2220

2. **Entrar no diretório indicado**
   ```bash
   cd inhere 
   ```
3. **Listar os arquivos**
   ```bash
   ls
   ```
4. **Identificar qual é o texto ASCII**
   ```bash
   file ./*
   ```
5. **Ler o arquivo de texto encontrado**
   ```bash
   cat ./(nome_do_arquivo)
   ```
   Obs: utilizar o nome do arquivo encontrado ao final do comando para
   atingir o objetivo. Utilizei (./), pois o arquivo começa com um caráter especial
   usado como flag.

## 💡Principais Aprendizados

- file é o comando padrão do linux para descobrir o tipo real de um arquivo
- Arquivos podem ter qualquer nome. A extensão não define o conteúdo
- Nomes  de arquivos começando com - precisam de ./ na frente para comandos não confundirem com opções
- file ./* aplica o comando file em todos os arquivos do diretório atual
- Em segurança, sempre valide o tipo do arquivo antes de executar ou ler

## 🚀Próximo Nível 

*Level 5:* Arquivos com propriedades específicas → Dica: use `find` com `-size`

🔗 Links Úteis

- https://overthewire.org/wargames/bandit/bandit4.html
- https://man7.org/linux/man-pages/man1/file.1.html
- https://man7.org/linux/man-pages/man1/find.1.html

---
*Status:* ✅ Concluído | *Próximo:* Bandit Level 5
---








   
