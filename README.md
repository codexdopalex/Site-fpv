# E-commerce Full Stack

Projeto full-stack de e-commerce multi-itens com Next.js 14 e PostgreSQL. Esta é a base do projeto.

## Requisitos
- [Node.js 20+](https://nodejs.org)
- [pnpm](https://pnpm.io)
- [Docker](https://www.docker.com/) e docker-compose

## Passo a passo

1. **Clonar o repositório**
   ```bash
   git clone <repo> && cd Site-fpv
   ```
2. **Instalar dependências**
   ```bash
   pnpm install
   ```
3. **Configurar variáveis de ambiente**
   ```bash
   cp .env.example .env
   # edite os valores conforme necessidade
   ```
4. **Subir serviços de banco e cache**
   ```bash
   docker compose up -d
   ```
5. **Aplicar migrações e seed** (serão disponibilizados nas próximas fases)
   ```bash
   pnpm prisma migrate dev
   pnpm prisma db seed
   ```
6. **Rodar o projeto**
   ```bash
   pnpm dev
   ```
7. Acesse `http://localhost:3000` no navegador.

## Flags de Mock
- `USE_MOCK_STRIPE`: habilita modo de pagamento simulado.
- `USE_MOCK_EMAIL`: usa envio de e-mails via Mailpit.
- `USE_MOCK_PIX`: simula pagamento via Pix.

## Estrutura do monorepo
- `apps/web`: aplicação Next.js.

Mais detalhes serão adicionados nas próximas fases.
