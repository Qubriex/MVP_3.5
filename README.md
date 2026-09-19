# MVP_3.5

This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app), configured for deployment on [Vercel](https://vercel.com).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Backend

The backend uses [Prisma](https://www.prisma.io) with a Postgres database, and API routes live under `src/app/api/`.

1. Copy `.env.example` to `.env` and set `DATABASE_URL` to your Postgres connection string (e.g. from [Vercel Postgres](https://vercel.com/docs/storage/vercel-postgres), [Neon](https://neon.tech), or [Supabase](https://supabase.com)).
2. Apply the schema to your database:
   ```bash
   npx prisma migrate dev --name init
   ```
3. The Prisma Client is generated automatically on `npm install` (via the `postinstall` script). Regenerate manually after schema changes with:
   ```bash
   npx prisma generate
   ```

Available API routes:

- `GET /api/health` — basic health check, no database required.
- `GET /api/items` — list items.
- `POST /api/items` — create an item (`{ "name": string }` in the request body).

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
