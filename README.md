# RemoraDelivery

Sistema de delivery e plataforma de pedidos da RemoraLink, pensado para centralizar a gestão de catálogo, pedidos e comunicação entre clientes e estabelecimentos.

## Visão geral

O RemoraDelivery é um projeto em desenvolvimento com foco em um modelo de delivery digital para empresas que precisam oferecer um cardápio acessível, pedidos simples e uma operação eficiente. A proposta principal é permitir que o cliente consulte produtos, formule pedidos e receba confirmação de forma rápida, enquanto a loja gerencia o catálogo e o fluxo operacional.

A estrutura atual do repositório segue um padrão de monorepo, com atenção à separação de responsabilidades e ao uso de arquitetura orientada a domínio (DDD), conforme a documentação de regras de negócio presente em `engineering/docs`.

## Status do projeto

- Estrutura inicial do monorepo criada
- Pacote `core` configurado como base do domínio
- Documentação de regras de negócio em andamento
- Backend e frontend ainda serão implementados conforme a arquitetura definida

## Objetivos

- Facilitar o cadastro e gestão de produtos e empresas
- Permitir pedidos de forma simples e direta para o cliente
- Centralizar regras de negócio no pacote de domínio
- Escalar a solução por módulos em um monorepo
- Preparar a base para integração com APIs e interfaces web/mobile

## Arquitetura

O projeto está organizado em um monorepo para separar claramente responsabilidades entre domínio, infraestrutura e apresentação.

### Estrutura esperada

```text
RemoraDelivery/
├── README.md
├── package.json
├── pnpm-workspace.yaml
├── pnpm-lock.yaml
├── core/
│   └── package.json
├── engineering/
│   ├── demo.drawio
│   ├── demo.excalidraw
│   └── docs/
│       ├── diagrams/
│       └── rules/
│           └── Business/
│               └── rules_business.md
├── .github/
├── .gitignore
└── node_modules/
```

### Modelo de organização

- `core`: domínio e regras de negócio puras
- `backend`: futura API e infraestrutura
- `frontend`: futura interface do cliente e painel da loja
- `engineering`: documentação, regras e artefatos de arquitetura

> A organização final pode evoluir conforme a implementação real, mas a base estrutural já foi pensada para manter a lógica de negócio isolada da interface e da infraestrutura.

## Stack e tecnologia

Atualmente, o projeto já apresenta a base de um monorepo com Node.js e pnpm, e a intenção é evoluir para uma arquitetura modular com foco em DDD. Os módulos seguintes são esperados na evolução natural do sistema:

- Node.js
- pnpm
- JavaScript/TypeScript (em expansão conforme desenvolvimento)
- Arquitetura orientada a domínio
- Monorepo para isolamento de módulos

## Requisitos

Antes de iniciar o projeto, certifique-se de ter instalado:

- Node.js 18 ou superior
- pnpm
- Git
- Editor de código (VS Code recomendado)

## Instalação

Clone o repositório:

```bash
git clone https://github.com/Vidall/RemoraDelivery.git
cd RemoraDelivery
```

Instale as dependências:

```bash
pnpm install
```

## Como desenvolver

1. Trabalhe no pacote principal do domínio em `core/`
2. Mantenha regras de negócio no núcleo e evite espalhá-las na interface
3. Documente mudanças estruturais e de regra em `engineering/docs`
4. Quando novos módulos forem adicionados, mantenha a separação clara entre `core`, `backend` e `frontend`

## Fluxo de trabalho sugerido

```bash
# instalar dependências
pnpm install

# executar scripts do pacote principal
cd core
pnpm install
```

## Status funcional atual

O repositório está em fase inicial de estruturação. O objetivo atual é consolidar a base do domínio e preparar a organização para os módulos de API e frontend.

## Roadmap

### Fase 1 - Base do domínio
- Definir entidades e regras principais
- Estruturar objetos de valor e casos de uso
- Validar fluxo de negócio central

### Fase 2 - API e infraestrutura
- Implementar backend
- Conectar banco de dados e integrações
- Expor endpoints de produtos, pedidos e clientes

### Fase 3 - Interface de usuário
- Desenvolver experiência do cliente
- Construir painel administrativo da loja
- Integrar comunicação de pedidos e status

### Fase 4 - Qualidade e entrega
- Testes automatizados
- CI/CD
- Deploy e monitoramento

## Contribuição

Contribuições são bem-vindas. Para participar:

1. Faça um fork do projeto
2. Crie uma branch para sua feature ou correção
3. Realize commits claros e objetivos
4. Abra um pull request com descrição do problema e da solução

## Convenções recomendadas

- Usar commits em português ou em padrão consistente
- Manter nomes descritivos para branches e funções
- Separar camada de domínio, infraestrutura e apresentação
- Documentar regras importantes no diretório `engineering/docs`

## Licença

Este projeto está sob a licença ISC, conforme informado em `package.json`.

## Contato

- Repositório: https://github.com/Vidall/RemoraDelivery
- Organização/cliente: RemoraLink

## Observação final

Este README tem como objetivo descrever a visão inicial do projeto, a arquitetura do monorepo e o estado atual da implementação. Conforme o desenvolvimento avançar, ele deve ser atualizado para refletir as novas funcionalidades, scripts, integrações e práticas de entrega do projeto.
