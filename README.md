# PasseioApp

Uma aplicação Angular moderna para explorar e descobrir lugares incríveis. A aplicação utiliza autenticação via Google OAuth2 e oferece uma experiência de galeria e categorização de locais.

## 🚀 Como Começar

### Pré-requisitos

- Node.js 18+ instalado
- npm ou yarn

### Instalação e Execução

1. **Instale as dependências:**
```bash
npm install
```

2. **Inicie o servidor de desenvolvimento:**
```bash
npm start
```

3. **Acesse a aplicação:**
- Abra seu navegador em `http://localhost:4200/`
- A aplicação recarregará automaticamente ao salvar mudanças

## 🔐 Como Fazer Login

### Passo a Passo:

1. Acesse a página inicial (Landing Page) em `http://localhost:4200/`
2. Na página de boas-vindas, clique no botão **"Login com Google"**
3. Você será redirecionado para a página de autenticação do Google
4. Faça login com sua conta Google
5. Autorize a aplicação a acessar seu perfil, email e informações públicas
6. Você será redirecionado de volta para a aplicação e terá acesso completo

### O que você pode fazer após login:

- **Galeria**: Explore uma galeria de imagens de lugares incríveis
- **Categorias**: Veja lugares organizados por categorias (praias, montanhas, cidades, etc.)
- **Detalhes do Local**: Clique em qualquer lugar para ver informações completas
- **Perfil**: Acesse seu perfil do Google na aplicação

### Configurações de Autenticação

A aplicação está configurada com OAuth2 do Google:
- **Client ID**: 581641606828-4k2bukrq9j79ptds5dndkasfkm5bv8lu.apps.googleusercontent.com
- **Escopos**: openid, profile, email
- **Redireccionamento**: http://localhost:4200/

## 📦 Servidor de API

A aplicação usa um servidor JSON mock para dados. Para ter a API funcionando também:

### Terminal Separado 1: Servidor de Desenvolvimento

```bash
npm start
# Aplicação em http://localhost:4200/
```

### Terminal Separado 2: API Mock

```bash
# Desenvolvimento (porta 3000)
npm run server

# OU Produção (porta 4000)
npm run server:production
```

Dados disponíveis em `api/db.json`

## 🏗️ Estrutura do Projeto

```
src/app/
├── landingpage/          # Página inicial com login
├── galeria/              # Galeria de imagens
├── categorias/           # Categorias de lugares
├── lugares/              # Detalhes de lugares
├── template/             # Componentes de layout
├── auth.config.ts        # Configuração OAuth2
├── auth.guard.ts         # Proteção de rotas
└── authgoogle.service.ts # Serviço de autenticação
```

## 🔧 Scripts Disponíveis

```bash
npm start                      # Inicia servidor de desenvolvimento (porta 4200)
npm run build                  # Build para produção
npm run watch                  # Modo watch de desenvolvimento
npm test                       # Executa testes unitários
npm run server                 # Inicia servidor mock API (porta 3000)
npm run server:production      # Inicia servidor mock produção (porta 4000)
```

## 🧪 Testes

Para executar os testes unitários com Karma:

```bash
npm test
```

## 🏢 Build para Produção

Para criar uma versão otimizada para produção:

```bash
npm run build
```

Os artefatos serão armazenados no diretório `dist/`.

## 🐳 Docker

A aplicação possui suporte Docker:

```bash
# Build da imagem
docker build -t passeio-app .

# Executar container
docker run -p 80:80 passeio-app
```

## 🛠️ Ferramentas Utilizadas

- **Angular 19**: Framework frontend moderno
- **TypeScript**: Linguagem principal
- **Tailwind CSS**: Utilitários CSS para estilos
- **Angular OAuth2 OIDC**: Autenticação segura com Google
- **JSON Server**: Mock de API para desenvolvimento
- **Karma**: Test runner para testes unitários

## 📚 Recursos Adicionais

- [Angular Docs](https://angular.dev)
- [Angular CLI](https://angular.dev/tools/cli)
- [OAuth2 OIDC Library](https://github.com/manfredsteyer/angular-oauth2-oidc)
- [Tailwind CSS](https://tailwindcss.com)

## 🤝 Dúvidas?

Caso tenha dúvidas sobre como usar a aplicação, consulte:
1. Este README
2. O código nos componentes (bem comentado)
3. A documentação oficial do Angular
