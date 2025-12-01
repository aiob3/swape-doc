---
Description: adote como atividade complementar FINAL para esta etapa de entrega antes de eu realziar o COMMIT para produção seguir as instruçÕes desenvolvidas para ajudar VOCE a documentar esta fonte de verdades envolvendo suas atividades como LLM Redable, 
Objective: tomar como Boas Praticas a partir deste momento concluir COMO entregravel de suas evidencias de atividade conforme as orientaçÕes solicitadas pelo time que ficara responsavel pela manutenção desta aplicação a partir do momento que for para produção. 
Guardrails: Por favor adote uma leitura cautelosa aos detalhes fornecidos, revise as atividades envolvidas em #file:GEMINI-instructions.md.ts e adote todas as instruções como SEU desafio final para concluir seu excelente trabalho até aqui AO REVISAR E ADOTAR SEU MÁXIMO PODER DE SINTESE PARA GARANTIR A QUALIDADE DE SEU ENTREGAVEL FINAL. 
Remember: (NAO SE ESQUEÇA DE ENTREGAR SUAS EVIDENCIAS DENTRO DO REPOSITÓRIO DO PROJETO CRIADO A PARTIR DESTE MODELO.
***
`RAIZ: ./DOCS` conforme as instruções fornecidas criando, incrementando e complementando de forma persistente conforme sua evolução em local definitivo fixado em /docs/* para formalizar seus entregáveis)
---

## Este documento deve ser Operado como FONTE UNICA DE VERDADE (SSOT - Single Source of Truth), onde o seu Mind set deve ENCARA como:

**ERRADO (o que eu estava fazendo):**
- "Me diga qual app" → Pressupõe que EU conheço
- "Escolha doc necessária" → Pressupõe que VOCÊ sabe o que falta
- "Confirme detalhes" → Pressupõe alinhamento prévio

**CERTO (o que você precisa):**
- **Dev entrega app funcionando** (código-fonte completo)
- **LLM analisa TUDO** (sem conhecimento prévio)
- **LLM gera documentação** (explica o que DEV fez)
- **LLM identifica gaps** (otimizações + débitos técnicos)
- **LLM alerta riscos** (antes de deploy produção)

***

## 🎯 PROMPT UNIVERSAL — "Documente & Audite Este App"

**Adote a partir deste prompt os dados de INSTRUÇÃO necessários para capacitar novos recursos agregados ao futuro deste desenvolvimento:**

```markdown
# AUDIT & DOCUMENTATION GENERATOR — Pre-Production Checkpoint

Você está recebendo um codebase COMPLETO de uma aplicação que foi desenvolvida por outro desenvolvedor (ou por você em iterações anteriores). Seu trabalho é:

1. **ANALISAR** — Entender profundamente o que foi construído
2. **DOCUMENTAR** — Explicar como funciona (para humanos + LLMs)
3. **AUDITAR** — Identificar problemas, riscos, otimizações
4. **ALERTAR** — Sinalizar BLOQUEADORES antes de produção

---

## FASE 1: ANÁLISE EXPLORATÓRIA (Discovery)

### 1.1 Identificação Básica

**Analise a estrutura de pastas e responda:**

```
## App Identity Report

### Nome do Projeto
- Detectado de: [package.json name | folder name | README]
- Nome inferido: [NOME_DO_APP]

### Tech Stack Completo
- **Runtime:** [Node.js X.X | Python X.X | etc]
- **Framework Principal:** [React | Next.js | Express | FastAPI | etc]
- **Database:** [PostgreSQL | MongoDB | SQLite | nenhum detectado]
- **Infraestrutura:** [Docker | Kubernetes | serverless | bare metal]
- **Package Manager:** [npm | yarn | pnpm | pip | etc]
- **Linguagens:** [TypeScript | JavaScript | Python | Go | mix]

### Arquitetura Geral
- **Tipo:** [Monolito | Microservices | Serverless | Hybrid]
- **Pattern:** [MVC | Clean Architecture | Layered | Event-Driven]
- **API Type:** [REST | GraphQL | gRPC | WebSocket | nenhum]

### Escopo Funcional (o que o app FAZ)
[Descreva em 2-3 parágrafos o PROPÓSITO do app baseado em:
- Nomes de rotas/endpoints
- Schemas de database
- Comentários de código
- README (se existir)]

Exemplo: "Este app é um sistema de gerenciamento de tarefas que permite usuários criarem projetos, atribuírem tasks, e rastrearem progresso via dashboard. Integra com API externa [X] para notificações."
```

---

### 1.2 Mapeamento de Arquivos Críticos

**Liste TODOS arquivos essenciais encontrados:**

```
## Critical Files Inventory

### Configuration Files
- [ ] package.json / requirements.txt / go.mod
- [ ] .env / .env.example / config.yaml
- [ ] tsconfig.json / babel.config.js / webpack.config.js
- [ ] Dockerfile / docker-compose.yml
- [ ] .github/workflows/*.yml (CI/CD)

### Entry Points
- [ ] src/index.js | main.py | app.go → [CAMINHO_EXATO]
- [ ] src/server.js | server.py → [CAMINHO_EXATO]

### Database
- [ ] Migrations: [PASTA] → [LISTAR ARQUIVOS]
- [ ] Schemas/Models: [PASTA] → [LISTAR ARQUIVOS]
- [ ] Seeds/Fixtures: [PASTA] → [LISTAR ARQUIVOS]

### API/Routes
- [ ] Routes definition: [PASTA] → [LISTAR ARQUIVOS]
- [ ] Controllers: [PASTA] → [LISTAR ARQUIVOS]
- [ ] Middleware: [PASTA] → [LISTAR ARQUIVOS]

### Tests
- [ ] Unit tests: [PASTA] → [COVERAGE %]
- [ ] Integration tests: [PASTA] → [COVERAGE %]
- [ ] E2E tests: [PASTA] → [COVERAGE %]

### Documentation (Existing)
- [ ] README.md → [Status: completo | incompleto | ausente]
- [ ] API docs → [Status: Swagger | Postman | nenhum]
- [ ] Architecture docs → [Status: existe | não existe]
```

---

## FASE 2: DOCUMENTAÇÃO AUTOMÁTICA

**Gere os seguintes documentos baseado APENAS no código analisado:**

### 2.1 README.md

```
# [NOME_DO_APP]

> **Auto-generated documentation** — Last updated: [DATA_ATUAL]

## O Que Este App Faz

[Descreva funcionalidade principal baseado em análise de código]

## Tech Stack

| Componente | Tecnologia | Versão |
|------------|------------|--------|
| Runtime | [ex: Node.js] | [ex: 18.17.0] |
| Framework | [ex: Express] | [ex: 4.18.2] |
| Database | [ex: PostgreSQL] | [ex: 14.5] |
| ORM | [ex: Prisma] | [ex: 5.2.0] |

## Arquitetura

```
[GERAR DIAGRAMA ASCII baseado em análise de imports/dependencies]

Exemplo:
┌─────────────┐
│   Client    │
│  (Browser)  │
└──────┬──────┘
       │ HTTP
       ▼
┌─────────────┐
│   Express   │
│   Server    │
└──────┬──────┘
       │
       ▼
┌─────────────┐
│ PostgreSQL  │
│  Database   │
└─────────────┘
```

## Estrutura de Pastas

```
[COPIAR ESTRUTURA REAL, exemplo:]
/src
  /api
    /controllers    # [X arquivos]
    /routes         # [Y arquivos]
  /models           # [Z schemas]
  /services         # Business logic
  /middleware       # Auth, validation, etc
  /utils            # Helpers
/tests
  /unit             # [N testes]
  /integration      # [M testes]
```

## Variáveis de Ambiente Necessárias

[EXTRAIR de código onde são usadas, exemplo:]

```bash
# Database
DATABASE_URL=postgresql://...  # Usado em: src/db/connection.js

# Authentication
JWT_SECRET=...                  # Usado em: src/middleware/auth.js
JWT_EXPIRY=15m                  # Usado em: src/services/auth.service.js

# External APIs
OPENAI_API_KEY=sk-...          # Usado em: src/services/llm.service.js
```

## Quick Start

### Pré-Requisitos
- [Runtime] versão [X.X] ou superior
- [Database] rodando em [porta]
- [Outras dependências]

### Instalação

```bash
# 1. Clone
git clone [repo_url]
cd [app_name]

# 2. Install dependencies
[npm install | pip install -r requirements.txt | etc]

# 3. Configure
cp .env.example .env
# Edit .env with your values

# 4. Database setup
[npm run migrate | python manage.py migrate | etc]
[npm run seed | etc]  # Se houver seeds

# 5. Run
[npm run dev | python app.py | etc]
```

### Acessar
- **App:** http://localhost:[PORTA_DETECTADA]
- **API Docs:** http://localhost:[PORTA]/docs (se Swagger detectado)
- **Admin:** http://localhost:[PORTA]/admin (se detectado)

## Endpoints Principais

[LISTAR baseado em análise de routes, exemplo:]

### Authentication
- `POST /api/auth/login` — User login
- `POST /api/auth/register` — User registration
- `POST /api/auth/refresh` — Refresh token

### [Recurso Principal]
- `GET /api/[recurso]` — List all
- `GET /api/[recurso]/:id` — Get by ID
- `POST /api/[recurso]` — Create new
- `PUT /api/[recurso]/:id` — Update
- `DELETE /api/[recurso]/:id` — Delete

[ADICIONAR TODOS ENDPOINTS DETECTADOS]

## Testes

```bash
# Run all tests
[comando detectado: npm test | pytest | etc]

# Coverage report
[comando detectado se existir]
```

**Current Coverage:** [X]% (baseado em análise de arquivos de teste)

## Deploy

Ver [DEPLOY.md](docs/DEPLOY.md) para instruções completas.

## Problemas Conhecidos

[SEÇÃO A SER PREENCHIDA POR FASE 3 — AUDITORIA]
```

---

### 2.2 API.md (Documentação Completa de Endpoints)

```
# API Documentation

**Base URL:** [DETECTAR de código ou .env]

## Authentication

[ANALISAR middleware de auth e descrever mecanismo:]

Exemplo se JWT detectado:
```
Authorization: Bearer <token>
```

Obter token via:
```http
POST /api/auth/login
Content-Type: application/json

{
  "email": "user@example.com",
  "password": "senha123"
}
```

***

## Endpoints

[PARA CADA ROTA DETECTADA, GERAR:]

### [MÉTODO] [CAMINHO]

**Descrição:** [Inferir de nome da função controller]

**Headers:**
```
Content-Type: application/json
[Authorization: Bearer <token>]  # Se rota protegida
```

**Request Body:** (se POST/PUT)
```json
[EXTRAIR de validation schema ou Zod/Joi/etc se detectado]
```

**Response 200:**
```json
[INFERIR de resposta do controller ou criar exemplo baseado em schema]
```

**Response 400:**
```json
{
  "error": "validation_error",
  "message": "[mensagem típica]"
}
```

**Response 401:** (se rota protegida)
```json
{
  "error": "unauthorized",
  "message": "Token inválido ou ausente"
}
```

**Response 500:**
```json
{
  "error": "internal_server_error",
  "message": "Erro inesperado"
}
```

**Exemplo de Uso:**
```bash
curl -X [MÉTODO] \
  http://localhost:[PORTA][CAMINHO] \
  -H "Content-Type: application/json" \
  [-H "Authorization: Bearer <token>"] \
  [-d '{ ... }']
```

***

[REPETIR PARA TODOS ENDPOINTS]

## Rate Limiting

[DETECTAR se existe middleware de rate limit, se sim:]
- Limite: [X] requisições por [tempo]
- Header: `X-RateLimit-Remaining`

[Se não detectado:]
⚠️ **ALERTA:** Rate limiting NÃO detectado (ver AUDIT.md)

## Webhooks

[DETECTAR se há endpoints webhook, se sim documentar]
[Se não: omitir seção]

## Erros Globais

[ANALISAR middleware de error handling e listar códigos possíveis:]

| Code | Significado | Quando Ocorre |
|------|-------------|---------------|
| 400 | Bad Request | Validação falha |
| 401 | Unauthorized | Token ausente/inválido |
| 403 | Forbidden | Sem permissão |
| 404 | Not Found | Recurso não existe |
| 409 | Conflict | Duplicação (ex: email já existe) |
| 429 | Too Many Requests | Rate limit excedido |
| 500 | Internal Error | Erro não tratado |
```

---

### 2.3 DATABASE.md (Schema + Migrations)

```
# Database Documentation

## Connection

**Type:** [PostgreSQL | MongoDB | MySQL | SQLite]
**Host:** [EXTRAIR de .env ou config]
**Port:** [EXTRAIR]
**Database Name:** [EXTRAIR]

## Schema Overview

[ANALISAR models/schemas e gerar diagrama:]

```
users
├─ id (UUID, PK)
├─ email (VARCHAR, UNIQUE)
├─ password_hash (VARCHAR)
├─ created_at (TIMESTAMP)
└─ updated_at (TIMESTAMP)
    │
    └─── (1:N) ───▶ [tabela_relacionada]
                    ├─ id (UUID, PK)
                    ├─ user_id (UUID, FK)
                    └─ ...
```

## Tables

[PARA CADA TABELA DETECTADA:]

### `users`

**Purpose:** [Inferir de nome + uso no código]

| Column | Type | Constraints | Description |
|--------|------|-------------|-------------|
| id | UUID | PRIMARY KEY | Unique identifier |
| email | VARCHAR(255) | UNIQUE, NOT NULL | User email |
| password_hash | VARCHAR | NOT NULL | Bcrypt hash |
| created_at | TIMESTAMP | DEFAULT NOW() | Creation timestamp |
| updated_at | TIMESTAMP | DEFAULT NOW() | Last update |

**Indexes:**
- `idx_users_email` on `email` (para login rápido)

**Relationships:**
- **1:N** com `[tabela]` via `user_id`

***

[REPETIR PARA TODAS TABELAS]

## Migrations

**Migration Tool:** [Prisma | Sequelize | TypeORM | raw SQL]

**History:**

[LISTAR arquivos de migration em ordem cronológica:]

| File | Date | Description |
|------|------|-------------|
| 001_create_users.sql | 2025-11-01 | Initial users table |
| 002_add_roles.sql | 2025-11-15 | Add roles + permissions |
| [etc] | | |

**Run Migrations:**
```bash
[comando detectado: npm run migrate | npx prisma migrate deploy | etc]
```

**Rollback:** (se suportado)
```bash
[comando detectado ou "⚠️ Rollback não implementado"]
```

## Seeds

[SE DETECTADO arquivos de seed:]

```bash
# Populate database with sample data
[comando detectado: npm run seed | etc]
```

**Data criada:**
- [X] usuários de teste
- [Y] registros de [entidade]

[SE NÃO DETECTADO:]
⚠️ **Seeds não encontrados** — considerar adicionar para development

## Backup & Restore

[SE SCRIPTS DETECTADOS, documentar]
[SE NÃO:]
⚠️ **Backup strategy não implementada** (ver AUDIT.md)
```

---

## FASE 3: AUDITORIA CRÍTICA

**Agora AVALIE o código em busca de problemas:**

### 3.1 AUDIT.md — Relatório Completo de Riscos

```
# Security & Quality Audit Report

**Generated:** [DATA_HORA]
**Codebase Version:** [Git commit hash se disponível]

***

## 🚨 BLOQUEADORES (NÃO PODE IR PRA PRODUÇÃO)

[VERIFICAR e listar SE DETECTADOS:]

### B1: Secrets Hardcoded
- ❌ **Arquivo:** `src/config/api.js:15`
- **Problema:** `const API_KEY = "sk-abc123..."` hardcoded
- **Risco:** Exposição de credenciais em repositório
- **Fix:** Mover para `.env` + adicionar a `.gitignore`

### B2: SQL Injection Vulnerability
- ❌ **Arquivo:** `src/api/users.controller.js:42`
- **Problema:** Query SQL com string concatenation
  ```javascript
  const query = `SELECT * FROM users WHERE email = '${email}'`;
  ```
- **Risco:** Injection attack possível
- **Fix:** Usar parameterized queries ou ORM

### B3: No Input Validation
- ❌ **Endpoints afetados:** `/api/users`, `/api/[recurso]`
- **Problema:** Nenhuma biblioteca de validação detectada (Zod, Joi, etc)
- **Risco:** Dados inválidos podem quebrar app ou corromper DB
- **Fix:** Implementar validation middleware

### B4: No Authentication Middleware
- ❌ **Rotas expostas:** [LISTAR rotas sem auth que deveriam ter]
- **Problema:** Endpoints críticos acessíveis sem autenticação
- **Risco:** Acesso não autorizado a dados sensíveis
- **Fix:** Aplicar auth middleware

### B5: No HTTPS Enforcement
- ❌ **Arquivo:** `src/server.js`
- **Problema:** Server aceita HTTP em produção
- **Risco:** Man-in-the-middle attacks
- **Fix:** Forçar HTTPS redirect ou usar proxy (Nginx)

[CONTINUAR LISTANDO TODOS BLOQUEADORES DETECTADOS]

***

## ⚠️ AVISOS (ALTA PRIORIDADE)

### W1: Missing Rate Limiting
- **Problema:** Nenhum rate limiter detectado
- **Risco:** DDoS, brute force attacks
- **Fix:** Implementar express-rate-limit ou similar

### W2: No Error Handling Middleware
- **Problema:** Errors não tratados globalmente
- **Risco:** Stack traces expostos ao client (info leak)
- **Fix:** Adicionar error handler global

### W3: Missing Health Check
- **Problema:** Endpoint `/health` não encontrado
- **Risco:** Impossível monitorar uptime automaticamente
- **Fix:** Adicionar endpoint simples que verifica DB + dependências

### W4: No Logging System
- **Problema:** Apenas `console.log` detectado
- **Risco:** Debugging em prod é impossível
- **Fix:** Implementar Winston, Pino ou similar

### W5: Database Connection Pool Not Configured
- **Problema:** Connection sem pool settings
- **Risco:** Pode esgotar connections sob carga
- **Fix:** Configurar pool size + timeout

[CONTINUAR]

***

## 💡 OTIMIZAÇÕES (PERFORMANCE)

### O1: N+1 Query Problem
- **Arquivo:** `src/api/users.controller.js:listUsers()`
- **Problema:**
  ```javascript
  const users = await User.findAll();
  for (const user of users) {
    user.posts = await Post.findByUserId(user.id); // N queries
  }
  ```
- **Impacto:** Latência aumenta linearmente com número de users
- **Fix:** Eager loading
  ```javascript
  const users = await User.findAll({ include: Post });
  ```

### O2: Missing Indexes
- **Tabela:** `users`
- **Problema:** Query `WHERE email = ?` sem index
- **Impacto:** Full table scan em queries de login
- **Fix:**
  ```sql
  CREATE INDEX idx_users_email ON users(email);
  ```

### O3: Large Payload Response
- **Endpoint:** `GET /api/users`
- **Problema:** Retorna TODOS usuários sem paginação
- **Impacto:** Timeout em databases grandes
- **Fix:** Implementar pagination (limit, offset)

[CONTINUAR]

***

## 📋 DEBT TÉCNICO (MANUTENIBILIDADE)

### D1: No Tests
- **Coverage:** 0% (nenhum teste detectado)
- **Risco:** Refactors quebram funcionalidades silenciosamente
- **Recomendação:** Adicionar pelo menos testes de integração para happy paths

### D2: Inconsistent Naming
- **Problema:** Mix de camelCase, snake_case, kebab-case
- **Arquivos afetados:** [LISTAR]
- **Fix:** Padronizar para [convenção escolhida]

### D3: God File
- **Arquivo:** `src/server.js` (847 linhas)
- **Problema:** Responsabilidades demais em um arquivo
- **Fix:** Separar em modules (routes, config, startup)

### D4: Dead Code
- **Arquivos não importados em nenhum lugar:**
  - `src/utils/old-helper.js`
  - `src/deprecated/...`
- **Fix:** Remover ou documentar razão de existência

[CONTINUAR]

***

## ✅ PONTOS POSITIVOS

[LISTAR O QUE FOI BEM FEITO:]

- ✅ Uso de TypeScript (type safety)
- ✅ Environment variables em uso (.env)
- ✅ Docker setup presente
- ✅ Git ignore configurado corretamente
- ✅ Estrutura de pastas organizada

***

## 📊 MÉTRICAS

| Métrica | Valor | Status |
|---------|-------|--------|
| Bloqueadores | [N] | 🚨 CRÍTICO |
| Avisos Alta Prioridade | [M] | ⚠️ URGENTE |
| Otimizações Sugeridas | [X] | 💡 RECOMENDADO |
| Débitos Técnicos | [Y] | 📋 PLANEJADO |
| Linhas de Código | [TOTAL] | - |
| Test Coverage | [%] | [❌ <70% | ✅ >=70%] |
| Dependencies Outdated | [N] | [❌ >5 | ✅ <=5] |

***

## 🎯 AÇÕES RECOMENDADAS (PRIORIDADE)

### Antes de Deploy Produção (OBRIGATÓRIO)
1. [ ] Corrigir TODOS bloqueadores (B1-BN)
2. [ ] Implementar rate limiting (W1)
3. [ ] Adicionar error handling global (W2)
4. [ ] Configurar HTTPS (B5)
5. [ ] Adicionar health check (W3)

### Primeira Sprint Pós-Deploy (7 dias)
1. [ ] Implementar logging estruturado (W4)
2. [ ] Adicionar testes críticos (D1)
3. [ ] Otimizar queries N+1 (O1)
4. [ ] Configurar monitoring (Sentry/DataDog)

### Backlog Técnico (30 dias)
1. [ ] Refatorar god files (D3)
2. [ ] Padronizar naming (D2)
3. [ ] Adicionar indexes (O2)
4. [ ] Implementar pagination (O3)
```

---

## PROMPT COMPLETO PARA COPIAR

**Cole ISSO no seu LLM (Cursor/Claude/ChatGPT):**

```
Analise este codebase COMPLETO e execute as 3 fases:

FASE 1: DISCOVERY
- Identifique nome, tech stack, arquitetura
- Liste TODOS arquivos críticos
- Mapeie estrutura de pastas
- Infira propósito do app

FASE 2: DOCUMENTAÇÃO
Gere automaticamente:
1. README.md completo
2. API.md com TODOS endpoints
3. DATABASE.md com schema + migrations
4. DEPLOY.md com instruções VPS
5. .env.example com TODAS variáveis

FASE 3: AUDITORIA
Gere AUDIT.md identificando:
- 🚨 BLOQUEADORES (NÃO pode produção)
- ⚠️ AVISOS (alta prioridade)
- 💡 OTIMIZAÇÕES (performance)
- 📋 DÉBITO TÉCNICO (manutenibilidade)
- ✅ PONTOS POSITIVOS

Para cada problema: localização exata (arquivo:linha), descrição clara, fix proposto.

Output: 6 arquivos Markdown prontos para commit.
```

---

## ✅ OBSERVAÇÕES FINAIS DÚVIDA PARA CERTIFICAR-SE DE SSOT

**Você me alinhou perfeitamente. Este prompt:**
- ✅ NÃO pressuponha conhecimento prévio
- ✅ EVITA A TODO CUSTOO, CAIR EM VIÉSES, PORÉM (E NÃO LIMITADO), PARA NÃO AGIR ERRADO Analisar código "às cegas"
- ✅ REQUISITOS SSOT | ADOTAR DE FORMA PERSISTENTE -> Gerar docs automaticamente
- ✅ NÃO AFIR SORRATEIRAMENTE SEM pedir confirmação (AO Identificar problemas, REPORTE AO OPERADOR COM O SEU DIAGNOTICO E PLANO DE AÇÃO)
- ✅ EMITIR Alerta E SOLICITAR CONFIRMAÇÃO SEMPRE ANTES DE EFETIVAR QUALQUER DEPLOYMENT 
- ✅ ADOTAR POSTURA RECH LEAD agnóstica de stack/linguagem => este é o meio => A SOLUÇÃO DEVE SER O FOCO SEMPRE.
   - ⚠️ (Estratégia Bottom-up, deve ADOTAR COMO PARTE DE SUA ATIVIDADES ENQUANTO FOR ENGAJADO A ESTE PROJETO.

**ESTE PROMPT INICIAR FOI CRIADO, COMPILADO E TRANSFERIDO PARA LLM +CAPACITAR-SE AO ENTRAR IDENTIFICAR ESTE REPOSITÓRIO COMO PARTE DO <WORKSPACE/TEMPLATE> aponte para pasta do projeto(RAIZ: ~/vcia26 = DONE)** 🚀 
*/
export {};
