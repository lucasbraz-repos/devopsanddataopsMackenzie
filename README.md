# 🚀 Pipeline CI/CD Automatizado - GitHub Actions

[![CI - Integração Contínua](https://github.com/lucasbraz-repos/devopsanddataopsMackenzie/actions/workflows/ci.yml/badge.svg)](https://github.com/lucasbraz-repos/devopsanddataopsMackenzie/actions/workflows/ci.yml)
[![CD - Deploy Contínuo](https://github.com/lucasbraz-repos/devopsanddataopsMackenzie/actions/workflows/cd.yml/badge.svg)](https://github.com/lucasbraz-repos/devopsanddataopsMackenzie/actions/workflows/cd.yml)

## 📋 Sobre o Projeto

Este projeto implementa um **pipeline CI/CD completo** utilizando **GitHub Actions**, simulando um fluxo real de trabalho DevOps. O objetivo é automatizar todo o processo desde a validação do código até o deploy em produção.

**Atividade Prática:** Criando um Pipeline CI/CD Automatizado no GitHub Actions  
**Curso:** DevOps e DataOps  
**Instituição:** Universidade Presbiteriana Mackenzie  
**Ano:** 2025

---

## 🎯 Objetivos da Atividade

- ✅ Criar e configurar um pipeline CI/CD completo
- ✅ Utilizar Git e GitHub para controle de versão
- ✅ Implementar Integração Contínua (CI)
- ✅ Implementar Deploy Contínuo (CD)
- ✅ Publicar automaticamente no GitHub Pages
- ✅ Analisar logs, métricas e artefatos gerados

---

## 📁 Estrutura do Projeto

```
devopsanddataopsMackenzie/
├── site/
│   └── index.html          # Página web a ser publicada
├── .github/
│   └── workflows/
│       ├── ci.yml          # Pipeline de Integração Contínua
│       └── cd.yml          # Pipeline de Deploy Contínuo
└── README.md               # Documentação do projeto
```

---

## ⚙️ Pipelines Implementados

### 🔵 CI - Integração Contínua (`ci.yml`)

O pipeline de CI é executado automaticamente a cada **push** ou **pull request** na branch `main`.

**Jobs implementados:**

1. **Validação de Arquivos**
   - Verifica a existência da estrutura do projeto
   - Valida arquivos essenciais
   - Lista estrutura de diretórios

2. **Testes de Qualidade**
   - Configura ambiente Node.js
   - Instala e executa HTMLHint para validação de sintaxe
   - Gera estatísticas do código

3. **Testes Automatizados**
   - Valida estrutura HTML (DOCTYPE, tags essenciais)
   - Verifica conteúdo esperado
   - Garante integridade do código

4. **Build e Geração de Artefatos**
   - Cria build do projeto
   - Gera artefatos para deploy
   - Upload com retenção de 30 dias

5. **Relatório de CI**
   - Gera relatório consolidado
   - Exibe métricas e informações do build

### 🟢 CD - Deploy Contínuo (`cd.yml`)

O pipeline de CD publica automaticamente o site no **GitHub Pages** após o sucesso do CI.

**Jobs implementados:**

1. **Build para Produção**
   - Prepara ambiente de produção
   - Cria build otimizado
   - Adiciona metadados do deploy
   - Gera artefatos com retenção de 90 dias

2. **Deploy no GitHub Pages**
   - Configura GitHub Pages
   - Publica o site automaticamente
   - Fornece URL de acesso

3. **Verificação Pós-Deploy**
   - Aguarda propagação
   - Verifica disponibilidade do site
   - Confirma sucesso do deploy

4. **Relatório de CD**
   - Gera relatório final do deploy
   - Exibe URL de acesso e métricas

---

## 🚀 Como Utilizar

### 1️⃣ Clonar o Repositório

```bash
git clone https://github.com/lucasbraz-repos/devopsanddataopsMackenzie.git
cd devopsanddataopsMackenzie
```

### 2️⃣ Fazer Alterações

Edite o arquivo `site/index.html` conforme necessário:

```bash
# Abrir no VS Code
code site/index.html
```

### 3️⃣ Commit e Push

```bash
git add .
git commit -m "feat: atualização do site"
git push origin main
```

### 4️⃣ Acompanhar os Pipelines

1. Acesse a aba **Actions** no GitHub
2. Observe a execução dos workflows:
   - ✅ **CI - Integração Contínua**
   - ✅ **CD - Deploy Contínuo**
3. Verifique os logs detalhados de cada job
4. Acesse os artefatos gerados

### 5️⃣ Acessar o Site Publicado

Após o deploy bem-sucedido, acesse:

```
https://lucasbraz-repos.github.io/devopsanddataopsMackenzie/
```

---

## 🔧 Configuração do GitHub Pages

Para habilitar o GitHub Pages no seu repositório:

1. Vá em **Settings** → **Pages**
2. Em **Source**, selecione: **GitHub Actions**
3. O deploy será automático a partir do workflow `cd.yml`

---

## 📊 Monitoramento e Logs

### Ver Logs dos Workflows

1. Acesse a aba **Actions**
2. Clique no workflow desejado (CI ou CD)
3. Selecione uma execução específica
4. Visualize logs detalhados de cada step

### Baixar Artefatos

1. Na página do workflow, role até **Artifacts**
2. Baixe os artefatos gerados:
   - `site-build` (do CI - 30 dias de retenção)
   - `production-build-X` (do CD - 90 dias de retenção)

### Badges de Status

Adicione badges ao README para mostrar o status dos pipelines:

```markdown
[![CI](https://github.com/SEU-USUARIO/SEU-REPO/actions/workflows/ci.yml/badge.svg)](...)
[![CD](https://github.com/SEU-USUARIO/SEU-REPO/actions/workflows/cd.yml/badge.svg)](...)
```

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Descrição |
|-----------|-----------|
| **Git** | Controle de versão distribuído |
| **GitHub** | Plataforma de hospedagem de código |
| **GitHub Actions** | Automação de workflows CI/CD |
| **GitHub Pages** | Hospedagem de sites estáticos |
| **HTML5/CSS3** | Desenvolvimento web |
| **Node.js** | Ambiente para ferramentas de validação |
| **HTMLHint** | Linter para validação de HTML |

---

## 📚 Conceitos DevOps Aplicados

### Integração Contínua (CI)
- ✅ Automação de testes
- ✅ Validação de código
- ✅ Build automatizado
- ✅ Feedback rápido

### Deploy Contínuo (CD)
- ✅ Deploy automatizado
- ✅ Publicação em produção
- ✅ Rollback facilitado
- ✅ Entrega contínua de valor

### Práticas DevOps
- ✅ Infrastructure as Code (workflows em YAML)
- ✅ Versionamento de configuração
- ✅ Automação completa
- ✅ Monitoramento e logs

---

## 🎓 Aprendizados

Este projeto demonstra:

1. **Automação de processos** com GitHub Actions
2. **Pipelines CI/CD** reais utilizados na indústria
3. **Boas práticas** de DevOps e versionamento
4. **Validação automatizada** de código
5. **Deploy contínuo** para ambiente de produção
6. **Monitoramento** através de logs e artefatos

---

## 📝 Próximos Passos (Opcional)

- [ ] Adicionar testes de segurança (SAST)
- [ ] Implementar análise de performance
- [ ] Configurar notificações (Slack, email)
- [ ] Adicionar ambiente de staging
- [ ] Implementar estratégias de rollback
- [ ] Adicionar testes E2E (End-to-End)

---

## 👥 Autor

**Lucas Braz**  
Universidade Presbiteriana Mackenzie  
Curso: DevOps e DataOps

---

## 📄 Licença

© 2025 - Desenvolvido para fins educacionais  
Atividade desenvolvida com base no material da Profa. Debora Batista Paulo

---

## 🌟 Demonstração

**Site publicado:** [Ver site ao vivo](https://lucasbraz-repos.github.io/devopsanddataopsMackenzie/)

---

## 🤝 Contribuições

Este é um projeto educacional. Sugestões e melhorias são bem-vindas!

1. Fork o projeto
2. Crie uma branch (`git checkout -b feature/melhoria`)
3. Commit suas mudanças (`git commit -m 'feat: adiciona melhoria'`)
4. Push para a branch (`git push origin feature/melhoria`)
5. Abra um Pull Request

---

**Desenvolvido com 💜 para a disciplina de DevOps e DataOps - Mackenzie**
