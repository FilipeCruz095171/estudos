# Guia de Comandos Essenciais de Terminal

Este é um guia de referência rápida para os comandos mais comuns utilizados em terminais, com foco em shells **Unix-like (Bash, Zsh)** e **Windows PowerShell**.

## Uma Nota sobre PowerShell

O PowerShell é um shell moderno e poderoso. Uma de suas grandes vantagens é que ele possui "aliases" (apelidos) para a maioria dos comandos Unix. Por exemplo, digitar `ls` no PowerShell funciona, mas na verdade ele está executando o comando `Get-ChildItem`. Neste guia, mostrarei o comando principal do PowerShell e seus aliases mais comuns.

---

## 🧭 Navegação no Sistema de Arquivos

Comandos para se mover entre pastas e ver onde você está.

| Ação | Comando (Unix/Bash) | Comando (PowerShell) | Exemplo de Uso |
| :--- | :--- | :--- | :--- |
| **Listar arquivos/pastas** | `ls` | `Get-ChildItem` (aliases: `ls`, `gci`, `dir`) | `ls -la` (mostra detalhes e arquivos ocultos) |
| **Mudar de diretório** | `cd` | `Set-Location` (alias: `cd`, `sl`) | `cd Documentos` ou `cd ..` (para voltar um nível) |
| **Mostrar diretório atual**| `pwd` | `Get-Location` (alias: `pwd`, `gl`) | `pwd` |

---

## 📂 Manipulação de Arquivos e Diretórios

Comandos para criar, apagar, mover e copiar.

| Ação | Comando (Unix/Bash) | Comando (PowerShell) | Exemplo de Uso |
| :--- | :--- | :--- | :--- |
| **Criar diretório** | `mkdir` | `New-Item -ItemType Directory` (alias: `mkdir`, `md`) | `mkdir meu-projeto` |
| **Criar arquivo vazio** | `touch` | `New-Item -ItemType File` | `touch notas.txt` |
| **Copiar arquivo** | `cp` | `Copy-Item` (alias: `cp`, `cpi`) | `cp arquivo_original.txt arquivo_copia.txt` |
| **Mover ou Renomear** | `mv` | `Move-Item` (alias: `mv`, `mi`) | `mv nome_antigo.txt nome_novo.txt` |
| **Remover arquivo** | `rm` | `Remove-Item` (alias: `rm`, `ri`, `del`) | `rm arquivo_para_deletar.txt` |
| **Remover diretório vazio** | `rmdir` | `Remove-Item` (alias: `rmdir`, `rd`) | `rmdir diretorio_vazio` |
| **Remover diretório com arquivos**| `rm -r` | `Remove-Item -Recurse` | `rm -r projeto_inteiro` **(CUIDADO!)**|

---

## 📜 Visualização e Saída de Texto

Comandos para ver o conteúdo de arquivos e exibir texto na tela.

| Ação | Comando (Unix/Bash) | Comando (PowerShell) | Exemplo de Uso |
| :--- | :--- | :--- | :--- |
| **Exibir texto na tela** | `echo` | `Write-Output` (alias: `echo`) | `echo "Olá, mundo!"` |
| **Exibir conteúdo do arquivo** | `cat` | `Get-Content` (alias: `cat`, `gc`, `type`) | `cat config.json` |
| **Exibir conteúdo paginado** | `less` ou `more` | `less` ou `more` | `less arquivo_muito_longo.log` |
| **Salvar saída em um arquivo**| `>` | `>` ou `Out-File` | `echo "Meu texto" > novo_arquivo.txt` (sobrescreve) |
| **Anexar saída a um arquivo** | `>>` | `>>` ou `Out-File -Append`| `echo "Outra linha" >> novo_arquivo.txt` (adiciona no fim) |

---

## 🔎 Busca e Filtro

| Ação | Comando (Unix/Bash) | Comando (PowerShell) | Exemplo de Uso |
| :--- | :--- | :--- | :--- |
| **Buscar texto em arquivos** | `grep` | `Select-String` (alias: `sls`) | `grep "erro" log_do_servidor.txt` |
| **Encontrar arquivos** | `find` | `Get-ChildItem -Recurse` | `find . -name "*.js"` |

---

## ✨ Dicas e Atalhos Essenciais

| Ação | Atalho | Descrição |
| :--- | :--- | :--- |
| **Autocompletar** | `Tab` | Pressione Tab para autocompletar nomes de arquivos, pastas e comandos. **O atalho mais importante!** |
| **Navegar no histórico** | `Seta para Cima` / `Seta para Baixo` | Percorre os comandos que você já digitou. |
| **Parar um comando** | `Ctrl + C` | Interrompe um comando que está em execução (ou travado). |
| **Limpar a tela** | `clear` (Unix) / `cls` (Windows) | Limpa todo o texto do terminal. |
| **Buscar no histórico** | `Ctrl + R` (Unix/Bash) | Comece a digitar para buscar um comando antigo que você já usou. |

---

Espero que este guia ajude a organizar seus estudos! Com a prática, esses comandos se tornarão automáticos.