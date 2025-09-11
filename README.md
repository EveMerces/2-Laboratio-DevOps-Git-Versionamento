# Laboratório DevOps - Git e Versionamento

Este repositório contém os arquivos e exercícios práticos do laboratório de Git e versionamento, demonstrando as principais operações e boas práticas do controle de versão.

## 📋 Objetivos do Laboratório

- Praticar comandos básicos do Git
- Entender o fluxo de trabalho com branches
- Aprender sobre commits, reverts e merges
- Implementar boas práticas de nomenclatura
- Trabalhar com repositórios remotos

## 🚀 Estrutura do Projeto

```
├── README.md          # Este arquivo
├── script1.py         # Script Python 1
├── script2.py         # Script Python 2 (criado e revertido)
└── script3.py         # Script Python 3
```

## 📝 Exercícios Realizados

### 1. Criação e Commit de Arquivos

**Objetivo:** Criar arquivos Python e fazer commits individuais seguindo boas práticas.

**Comandos utilizados:**
```bash
# Criar arquivo
echo 'print("Este é o script 1 do projeto")' > script1.py

# Adicionar ao staging
git add script1.py

# Commit com mensagem padronizada
git commit -m "[ADSDEVOPS-10] envio do script1.py"

# Push para repositório remoto
git push
```

**Padrão de mensagem de commit:**
- `[JIRA-TASK] descrição da ação`
- Exemplo: `[ADSDEVOPS-10] envio do script1.py`

### 2. Visualização do Histórico

**Objetivo:** Navegar pelo histórico de commits e entender os identificadores.

**Comandos utilizados:**
```bash
# Visualizar histórico de commits
git log

# Visualizar commits no GitLab
# Navegar para: Repositório > Commits
```

### 3. Revert de Commits

**Objetivo:** Aprender a reverter commits de forma segura.

**Comandos utilizados:**
```bash
# Reverter um commit específico
git revert 7bc043

# Verificar status após revert
git status

# Push do commit de revert
git push
```

**Resultado:** O arquivo `script2.py` foi removido do repositório através de um commit de revert.

### 4. Trabalho com Branches

**Objetivo:** Criar e trabalhar com branches para desenvolvimento paralelo.

**Comandos utilizados:**
```bash
# Criar nova branch a partir da main
git checkout -b ADSDEVOPS-12

# Criar arquivo na nova branch
echo 'print("Este é o script 2 do projeto")' > script2.py

# Commit na nova branch
git add script2.py
git commit -m "[ADSDEVOPS-12] #done inclusão do novo script2.py"

# Push da nova branch (primeira vez)
git push --set-upstream origin ADSDEVOPS-12
```

**Boas práticas de nomenclatura:**
- Usar o ID da tarefa do Jira (sem colchetes)
- Exemplo: `ADSDEVOPS-12` ao invés de `[ADSDEVOPS-12]`

### 5. Merge de Branches

**Objetivo:** Integrar mudanças de uma branch para a main.

**Comandos utilizados:**
```bash
# Retornar para a branch main
git checkout main

# Fazer merge da branch de feature
git merge ADSDEVOPS-12

# Push das mudanças para o repositório remoto
git push
```

## 🔧 Comandos Git Essenciais

### Configuração Inicial
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu.email@exemplo.com"
```

### Operações Básicas
```bash
# Status do repositório
git status

# Adicionar arquivos
git add arquivo.txt
git add .  # Adicionar todos os arquivos

# Commit
git commit -m "Mensagem descritiva"

# Push
git push
git push --set-upstream origin nome-da-branch  # Primeira vez
```

### Trabalho com Branches
```bash
# Listar branches
git branch

# Criar nova branch
git checkout -b nome-da-branch

# Trocar de branch
git checkout nome-da-branch

# Merge
git merge nome-da-branch
```

### Histórico e Revert
```bash
# Ver histórico
git log
git log --oneline  # Versão resumida

# Reverter commit
git revert hash-do-commit
```

## 📊 Fluxo de Trabalho Demonstrado

1. **Desenvolvimento na main:**
   - Criação de arquivos
   - Commits individuais
   - Push para repositório remoto

2. **Revert de mudanças:**
   - Identificação do commit a ser revertido
   - Execução do revert
   - Push da correção

3. **Desenvolvimento em branch:**
   - Criação de branch a partir da main
   - Desenvolvimento isolado
   - Push da nova branch

4. **Integração:**
   - Merge da branch para main
   - Sincronização com repositório remoto

## 🎯 Lições Aprendidas

- **Commits atômicos:** Cada commit deve representar uma mudança lógica
- **Mensagens descritivas:** Usar padrões consistentes para facilitar rastreamento
- **Branches para features:** Isolar desenvolvimento em branches separadas
- **Revert vs Reset:** Usar revert para mudanças já publicadas
- **Upstream tracking:** Configurar tracking para branches remotas

## 🔗 Recursos Adicionais

- [Documentação oficial do Git](https://git-scm.com/doc)
- [GitLab Documentation](https://docs.gitlab.com/)
- [Conventional Commits](https://www.conventionalcommits.org/)

## 👥 Contribuidores

Este laboratório foi desenvolvido como parte do curso de DevOps, demonstrando as melhores práticas de versionamento com Git.

---

**Data:** Março 2023  
**Repositório:** git-tests  
**Organização:** lab-git
