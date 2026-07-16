# Desafio DevSecOps — Gerenciador de Tarefas

## Sobre o Projeto
Este repositório faz parte do desafio prático do módulo de DevSecOps da ADA Tech.
Você receberá este projeto com vulnerabilidades propositais e uma pipeline incompleta.
Seu objetivo é **implementar a pipeline de segurança** e **corrigir as vulnerabilidades**.

## Estado atual
A pipeline está **incompleta**. Os steps de segurança precisam ser implementados por você.

## Sua missão
1. Implementar os steps de segurança no `pipeline.yml`
2. Fazer a pipeline **quebrar** ao detectar os problemas
3. Corrigir as vulnerabilidades encontradas
4. Fazer a pipeline **passar** com tudo verde ✅
5. Documentar o funcionamento da pipeline neste README

## O que implementar
- [X] Secrets Scanning com **Gitleaks**
- [X] SAST com **Semgrep**
- [X] SCA com **Grype**
- [X] Deploy com **GitHub Pages**

## Como a pipeline funciona
> **Substitua este bloco pela sua explicação após implementar a pipeline.**
> A pipeline roda automaticamente a cada push para a main para validar a segurança da aplicação antes do deploy.
> O primeiro passo é baixar o conteúdo do repositório para o ambiente do GitHub Actions.
> O segundo passo é a build, uma validação simples da estrutura do projeto, pra ter certeza que todos os arquivos necessários estão disponíveis para o processo de build.
> Gitleaks, responsável por apontar segredos e chaves expostos no código-fonte ou no histórico do repositório.
> Coloquei as chaves no **GitHub Secrets**, apesar delas não serem usadas para nada.
> Semgrep, o SAST faz a análise estática do código procurando por padrões inseguros de programação.
> Grype, verifica as dependências do projeto apontando bibliotecas com vulnerabilidades conhecidas registradas em bancos públicos de consultoria de segurança.
> Por fim, é feito o deploy no GitHub Pages.

### Fluxo resumido
Push na main
        ↓
Checkout do código
        ↓
Build
        ↓
Gitleaks (busca por chaves e senhas)
        ↓
Semgrep (busca por padrões vulneráveis)
        ↓
Grype (análise de dependências)
        ↓
Deploy

## URL de Produção
> [Página](https://igorpachpcx.github.io/projeto-devsecop-desafio/)
