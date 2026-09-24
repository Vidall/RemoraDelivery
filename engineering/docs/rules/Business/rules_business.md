# Sistema PVD e Delivery da RemoraLink - Especificação completa

## Contexto do projeto

Sistema servirá como cardápio digital para cadastrar a empresa e seus produtos e regras, e seus clientes realizarem o pedido de forma simples e rapida, contará com uma comunicação direta entre cliente e loja via maquina de impressão.

## Arquitetura geral - DDD com monorepo

O projeto é dividido em **três pacotes independentes** dentro de um monorepo:

```
financas-web/
├── core/          ← domínio puro: entidades, VOs, regras de negócio, interfaces
├── backend/       ← Nest.js: infraestrutura, API, banco de dados (depende do core)
├── frontend/      ← Next.js: interface, componentes, páginas (depende do core)
└── package.json   ← root do monorepo (npm workspaces ou pnpm workspaces)
```

### Regras de negócio que vivem no core (exemplos)