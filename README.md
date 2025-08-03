# Projeto Frontend Testes - Deploy via GitHub Actions no Azure App Service

Este projeto é um exemplo de como fazer deploy de um site estático (HTML + CSS) em um **Azure App Service** utilizando um **servidor Node.js com Express** e pipeline de CI/CD do **GitHub Actions**.

---

## 📂 Estrutura do projeto

```
.
├── .github/
│   └── workflows/
│       └── main_front-testes001.yml   # Pipeline GitHub Actions
├── frontend/
│   ├── index.html                     # Página principal
│   └── styles.css                     # Estilos CSS
├── server.js                          # Servidor Node.js usando Express
├── package.json                       # Configuração do projeto Node.js
└── README.md
```

---

## 🚀 Tecnologias utilizadas
- **Node.js 22 LTS**
- **Express.js**
- **Azure App Service**
- **GitHub Actions** para CI/CD

---

## 🔧 Como executar localmente

1. Clone o repositório:
   ```bash
   git clone <URL_DO_REPOSITORIO>
   cd CI_CD
   ```

2. Instale as dependências:
   ```bash
   npm install
   ```

3. Rode a aplicação:
   ```bash
   npm start
   ```

4. Acesse no navegador:
   ```
   http://localhost:3000
   ```

---

## ⚙️ Pipeline de Deploy (GitHub Actions)

O workflow **`main_front-testes001.yml`** faz:
1. Checkout do repositório.
2. Login no Azure usando Service Principal.
3. Instala dependências (`npm install`).
4. Faz o deploy no Azure App Service usando a action **`azure/webapps-deploy@v3`**.

> Toda vez que houver um **push na branch `main`**, a pipeline será disparada automaticamente.

---

## 🌐 URL da aplicação

> [https://front-testes001.azurewebsites.net](https://front-testes001.azurewebsites.net)

---

## 📝 Observações
- O App Service está configurado com runtime **Node 22 LTS**.
- O `server.js` serve os arquivos estáticos contidos na pasta **`frontend/`**.
- Você pode adaptar para projetos React/Angular/Vue facilmente.
