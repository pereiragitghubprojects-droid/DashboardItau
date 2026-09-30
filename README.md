# 🟠 Itaú Customer Dashboard

> Dashboard web responsiva para gerenciamento e visualização de informações de clientes, inspirada em experiências modernas de internet banking.

⚠️ **Aviso:** este projeto é exclusivamente educacional e demonstrativo. Não possui vínculo oficial com o Itaú Unibanco e não utiliza dados reais de clientes, contas ou transações.

---

## 📌 Sobre o projeto

O **Itaú Customer Dashboard** é uma interface de dashboard bancária desenvolvida para simular um ambiente onde um cliente pode visualizar e gerenciar suas principais informações financeiras.

O projeto foi pensado com foco em:

* 🎨 Interface moderna e responsiva
* 👤 Gerenciamento de perfil do cliente
* 💰 Visualização de saldo
* 💳 Gerenciamento de cartões
* 📊 Resumo financeiro
* 📈 Gráficos e indicadores
* 🔄 Histórico de movimentações
* 🔐 Área de autenticação
* ⚡ Experiência rápida e intuitiva

A aplicação pode servir como **projeto de portfólio**, estudo de frontend/backend ou base para uma futura aplicação financeira.

---

## 🖥️ Preview

### Dashboard

A dashboard apresenta uma visão centralizada das principais informações do cliente:

```text
┌─────────────────────────────────────────────────────────────┐
│ 🟠 ITAÚ                    🔔     👤 Cliente                │
├───────────────┬─────────────────────────────────────────────┤
│               │                                             │
│ Dashboard     │  Olá, Cliente 👋                           │
│               │                                             │
│ Conta         │  Saldo disponível                          │
│               │  R$ 8.540,32                               │
│ Cartões       │                                             │
│               │  ┌──────────┐ ┌──────────┐ ┌──────────┐   │
│ Transferências│  │ Cartão   │ │ Entradas │ │ Saídas   │   │
│               │  │ R$ 2.500  │ │ R$ 5.200 │ │ R$ 2.100 │   │
│ Investimentos │  └──────────┘ └──────────┘ └──────────┘   │
│               │                                             │
│ Configurações │  📊 Movimentações financeiras              │
│               │  ───────────────────────────────────────   │
│ Sair          │                                             │
│               │  Últimas transações                        │
└───────────────┴─────────────────────────────────────────────┘
```

---

# 🚀 Funcionalidades

## 👤 Cliente

* Visualização de dados pessoais
* Foto/avatar do usuário
* Dados da conta
* Status da conta
* Atualização de informações

## 💰 Conta

* Saldo disponível
* Saldo bloqueado
* Limite disponível
* Dados bancários
* Histórico financeiro

## 💳 Cartões

* Visualização de cartões
* Limite disponível
* Limite utilizado
* Data de vencimento
* Últimas compras
* Status do cartão

## 📊 Dashboard financeira

Indicadores para acompanhamento financeiro:

* Saldo atual
* Entradas
* Saídas
* Gastos do mês
* Faturas
* Investimentos

## 📈 Gráficos

A dashboard possui visualizações para facilitar a análise financeira:

* Gastos por categoria
* Entradas x saídas
* Evolução do saldo
* Histórico mensal
* Distribuição de despesas

## 🔄 Transações

Visualização das últimas movimentações:

```text
PIX recebido                 + R$ 850,00
Supermercado                 - R$ 230,40
Pagamento recebido           + R$ 2.500,00
Netflix                      - R$ 39,90
Transferência                - R$ 500,00
```

---

# 🏗️ Arquitetura

O projeto pode evoluir para uma arquitetura completa:

```text
                    ┌──────────────────┐
                    │    Frontend      │
                    │ React / Next.js  │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │   API Gateway    │
                    └────────┬─────────┘
                             │
          ┌──────────────────┼──────────────────┐
          ▼                  ▼                  ▼
   ┌────────────┐     ┌────────────┐     ┌────────────┐
   │ Auth       │     │ Customer   │     │ Account    │
   │ Service    │     │ Service    │     │ Service    │
   └────────────┘     └────────────┘     └────────────┘
                             │
              ┌──────────────┼──────────────┐
              ▼              ▼              ▼
        ┌──────────┐   ┌──────────┐   ┌──────────┐
        │PostgreSQL│   │  Redis   │   │   Kafka  │
        └──────────┘   └──────────┘   └──────────┘
```

---

# 🛠️ Tecnologias

## Frontend

* HTML5
* CSS3
* Tailwind CSS
* JavaScript / TypeScript
* React
* Next.js
* Recharts

## Backend

Para uma evolução do projeto:

* Java 21
* Spring Boot
* Spring Security
* Spring Data JPA
* Spring Validation
* REST API

## Banco de dados

* PostgreSQL
* Redis

## DevOps

* Docker
* Docker Compose
* GitHub Actions
* Kubernetes

## Observabilidade

* Spring Boot Actuator
* Prometheus
* Grafana
* OpenTelemetry

---

# 📂 Estrutura do projeto

Uma possível estrutura:

```text
itau-customer-dashboard/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── layouts/
│   │   ├── services/
│   │   ├── hooks/
│   │   ├── utils/
│   │   └── types/
│   │
│   ├── public/
│   ├── package.json
│   └── README.md
│
├── backend/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/example/banking/
│   │   │   │       ├── controller/
│   │   │   │       ├── service/
│   │   │   │       ├── repository/
│   │   │   │       ├── entity/
│   │   │   │       ├── dto/
│   │   │   │       ├── config/
│   │   │   │       └── security/
│   │   │   │
│   │   │   └── resources/
│   │   │       └── application.yml
│   │   │
│   │   └── test/
│   │
│   └── pom.xml
│
├── docker/
│   └── docker-compose.yml
│
├── docs/
│   ├── architecture.md
│   └── api.md
│
├── .github/
│   └── workflows/
│       └── ci.yml
│
├── .gitignore
└── README.md
```

---

# 🔐 Segurança

Como o projeto possui temática bancária, segurança deve ser uma das principais preocupações.

A versão backend pode implementar:

* JWT
* OAuth 2.0
* Spring Security
* Hash de senhas
* Controle de sessão
* RBAC
* Rate limiting
* Validação de entrada
* Logs de auditoria
* Criptografia de informações sensíveis

### Exemplo de fluxo de autenticação

```text
Cliente
   │
   ▼
Login
   │
   ▼
Auth Service
   │
   ├── Validação
   │
   └── JWT
        │
        ▼
   API Gateway
        │
        ▼
 Customer Dashboard
```

---

# 🔌 API

Exemplos de endpoints para uma futura API:

### Authentication

```http
POST /api/auth/login
POST /api/auth/register
POST /api/auth/refresh
POST /api/auth/logout
```

### Customer

```http
GET    /api/customers/me
PUT    /api/customers/me
GET    /api/customers/me/profile
```

### Account

```http
GET /api/accounts
GET /api/accounts/{id}
GET /api/accounts/{id}/balance
GET /api/accounts/{id}/transactions
```

### Cards

```http
GET /api/cards
GET /api/cards/{id}
GET /api/cards/{id}/statement
```

### Transactions

```http
GET  /api/transactions
GET  /api/transactions/{id}
POST /api/transactions
```

---

# 🐳 Executando com Docker

Clone o projeto:

```bash
git clone https://github.com/seu-usuario/itau-customer-dashboard.git
```

Entre no projeto:

```bash
cd itau-customer-dashboard
```

Execute os containers:

```bash
docker compose up -d
```

Verifique os containers:

```bash
docker compose ps
```

Para encerrar:

```bash
docker compose down
```

---

# 💻 Executando o Frontend

```bash
cd frontend
npm install
npm run dev
```

A aplicação estará disponível em:

```text
http://localhost:3000
```

---

# ☕ Executando o Backend

Entre na pasta:

```bash
cd backend
```

Execute:

```bash
./mvnw spring-boot:run
```

No Windows:

```bash
mvnw.cmd spring-boot:run
```

API:

```text
http://localhost:8080
```

---

# 🧪 Testes

Frontend:

```bash
npm test
```

Backend:

```bash
./mvnw test
```

Build:

```bash
./mvnw clean package
```

---

# 📊 Roadmap

* [x] Layout inicial da dashboard
* [x] Responsividade
* [x] Área do cliente
* [x] Cards financeiros
* [x] Histórico de transações
* [ ] Autenticação
* [ ] Backend Spring Boot
* [ ] PostgreSQL
* [ ] Redis
* [ ] API REST
* [ ] Controle de permissões
* [ ] Testes automatizados
* [ ] Docker
* [ ] CI/CD
* [ ] Observabilidade
* [ ] Kubernetes

---

# 🎯 Objetivo

O objetivo deste projeto é demonstrar conhecimentos em:

```text
Frontend
   ↓
Arquitetura de Software
   ↓
Backend
   ↓
APIs REST
   ↓
Segurança
   ↓
Banco de Dados
   ↓
Cache
   ↓
Docker
   ↓
CI/CD
   ↓
Observabilidade
```

O projeto também pode ser utilizado como **case de portfólio para desenvolvimento backend**, especialmente para demonstrar conhecimentos em Java, Spring Boot, APIs, bancos de dados e arquitetura de sistemas.

---

# 👨‍💻 Autor

**Pereira GitHub Projects**

Projeto desenvolvido para fins de estudo, portfólio e demonstração técnica.

---

## ⚠️ Disclaimer

Este projeto é uma implementação independente para fins educacionais.

**Itaú** e seus elementos de marca são propriedade de seus respectivos titulares. Este projeto não representa um produto oficial, parceria ou sistema interno do Itaú Unibanco.

Não utilize dados bancários reais neste projeto.

---

## ⭐ Contribuição

Contribuições são bem-vindas.

```bash
git checkout -b feature/nova-feature
git commit -m "feat: adiciona nova funcionalidade"
git push origin feature/nova-feature
```

Depois, abra um Pull Request.

---

## 📄 Licença

Este projeto pode ser disponibilizado sob a licença MIT para fins educacionais, conforme a licença escolhida pelo autor.
