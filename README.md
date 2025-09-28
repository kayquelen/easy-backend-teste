# Backend API - EasyPanel

API REST otimizada para deploy no EasyPanel.

## 🚀 Endpoints

### Health Check
```
GET /api/health
```

### Todos API
```
GET    /api/todos       # Listar todos
GET    /api/todos/:id   # Buscar por ID
POST   /api/todos       # Criar novo
PUT    /api/todos/:id   # Atualizar
DELETE /api/todos/:id   # Deletar
```

## 🛠️ Desenvolvimento Local

```bash
# Instalar dependências
npm install

# Rodar em desenvolvimento
npm run dev

# Rodar em produção
npm start
```

## 🐳 Docker

```bash
# Build
npm run docker:build

# Run
npm run docker:run
```

## 📦 Deploy no EasyPanel

1. **Criar nova app**
2. **Build Method**: Dockerfile
3. **Port**: 3001
4. **Environment Variables**:
   ```
   PORT=3001
   NODE_ENV=production
   FRONTEND_URL=https://seu-frontend.easypanel.host
   ```

## 🔗 Comunicação com Frontend

O backend estará disponível em:
- `https://seu-backend.easypanel.host/api/health`
- `https://seu-backend.easypanel.host/api/todos`

Configure o frontend para consumir essas URLs.
