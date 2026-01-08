# ONURB Pass — Backend (Render)

Backend para ONURB Pass:
- Auth (buyer/organizer) com JWT
- Eventos + lotes
- Pedidos + tickets + check-in
- **Modo DEMO** (sem provedor) para você lançar antes do CNPJ
- Integração InfinitePay pronta (liga depois por ENV)

## Rodar local
```bash
npm i
cp .env.example .env
npm run migrate
npm run seed
npm run dev
```

## Deploy no Render
- Crie um PostgreSQL no Render
- Crie um Web Service (Node)
  - Build: `npm install && npm run migrate`
  - Start: `npm start`
- Configure ENV conforme `.env.example`

## Endpoints principais
- Health: `GET /health`

### Modo DEMO (sem provedor)
- Criar compra demo: `POST /public/purchase`
- Listar compras por email: `GET /public/purchases?email=...`
- Vendas (painel demo): `GET /public/sales`
