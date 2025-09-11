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
├── script2.py         # Script Python 2
└── script3.py         # Script Python 3
```

## 📝 Exercícios Realizados

### 1. Criação e Commit de Arquivos

**Objetivo:** Criar arquivos Python e fazer commits individuais seguindo boas práticas.

**Comandos utilizados:**
```bash
# Criar script1.py
echo 'print("Este é o script 1 do projeto")' > script1.py
git add script1.py
git commit -m "[SIDEVOPS] envio do script1.py"
git push

# Criar script2.py
echo 'print("Este é o script 2 do projeto")' > script2.py
git add script2.py
git commit -m "[SI2A-10] envio do script2.py"
git push

# Criar script3.py
echo 'print("Este é o script 3 do projeto")' > script3.py
git add script3.py
git commit -m "[SI3A] #done envio do script3.py"
git push
```

**Padrão de mensagem de commit utilizado:**
- `[SIDEVOPS] envio do script1.py`
- `[SI2A-10] envio do script2.py`
- `[SI3A] #done envio do script3.py`

### 2. Visualização do Histórico

**Objetivo:** Navegar pelo histórico de commits e entender os identificadores.

**Comandos utilizados:**
```bash
# Visualizar histórico de commits
git log

# Visualizar commits no GitLab
# Navegar para: Repositório > Commits
```

### 3. Criação de Branch

**Objetivo:** Criar uma nova branch para desenvolvimento paralelo.

**Comandos utilizados:**
```bash
# Criar nova branch
git checkout -b SIDEVOPS-12
```

**Resultado:** Foi criada a branch `SIDEVOPS-12` para desenvolvimento isolado.

### 4. Status Atual do Laboratório

**Exercícios Completados:**
- ✅ Criação dos 3 scripts Python
- ✅ Commits individuais de cada arquivo
- ✅ Criação da branch `SIDEVOPS-12`

**Próximos Passos (Opcionais):**
- Revert de commits
- Merge de branches
- Push de mudanças para repositório remoto

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

## 📊 Fluxo de Trabalho Realizado

1. **Desenvolvimento na main:**
   - ✅ Criação de 3 arquivos Python
   - ✅ Commits individuais com mensagens padronizadas
   - ✅ Push para repositório remoto

2. **Criação de branch:**
   - ✅ Criação da branch `SIDEVOPS-12`
   - ✅ Branch configurada para desenvolvimento isolado

3. **Histórico de Commits:**
   - `[SIDEVOPS] envio do script1.py`
   - `[SI2A-10] envio do script2.py`
   - `[SI3A] #done envio do script3.py`

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

**Data:** Dezembro 2024  
**Repositório:** 2-Laboratio-DevOps-Git-Versionamento  
**Aluno:** Evelyn Silva
