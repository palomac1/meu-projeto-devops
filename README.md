# 🚀 Meu Projeto DevOps

[![CI](https://github.com)](https://github.com)
![Docker](https://shields.io)
![GitHub Actions](https://shields.io)
![Linux](https://shields.io)

Projeto prático desenvolvido durante o **Bootcamp DevOps Matera 2026**, cobrindo desde a automação de build e testes via Shell Script até conteinerização com Docker e Integração Contínua (CI) com GitHub Actions.

---

## 🛠️ Tecnologias e Ferramentas

* **Linux & Shell Script:** Automação de build, testes e health check.
* **Docker & Docker Compose:** Empacotamento da aplicação e orquestração multi-container (App + Redis).
* **Git & GitHub:** Versionamento, fluxo de Pull Requests e proteção de branch (`main`).
* **GitHub Actions:** Esteira de Integração Contínua (CI) executada automaticamente a cada push ou PR.

---

## 📂 Estrutura do Projeto

```text
meu-projeto-devops/
├── .github/
│   └── workflows/
│       └── ci.yml        # Pipeline de CI no GitHub Actions
├── docs/                 # Documentação e anotações do projeto
├── scripts/              # Scripts de build, testes automatizados e health check
├── Dockerfile            # Receita da imagem da aplicação
├── compose.yaml          # Orquestração dos containers (Aplicação + Redis)
└── README.md             # Documentação principal
```

---

## ⚙️ Como Executar Localmente

### Pré-requisitos
* [Docker](https://docker.com) e [Docker Compose](https://docker.com) instalados.

### Subindo o ambiente
1. Clone o repositório:
   ```bash
   git clone https://github.com
   cd meu-projeto-devops
   ```

2. Inicie os containers em segundo plano:
   ```bash
   docker compose up -d
   ```

3. Verifique se os serviços estão rodando:
   ```bash
   docker compose ps
   ```

---

## 🔄 Fluxo de CI/CD

Sempre que um novo código é enviado ou um **Pull Request** é aberto para a branch `main`:
1. O **GitHub Actions** inicia um ambiente Ubuntu limpo.
2. Executa a etapa de **Build** (`./scripts/build.sh`).
3. Roda a suíte de **Testes** (`./scripts/test.sh`).
4. Caso algum teste falhe, o merge na `main` é bloqueado automaticamente pelas regras de proteção da branch.

---

## 👩‍💻 Autora

Desenvolvido por **Paloma** ([palomac1](https://github.com)) durante o Bootcamp DevOps Matera 2026.

