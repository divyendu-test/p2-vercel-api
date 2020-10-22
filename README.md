# Vercel API

Prisma and Vercel's integration using the API folder configuration. This works without any configuration.

## How to run this locally and deploy

### Vercel authentication

A vercel token needs to be set with the environment variable `VERCEL_TOKEN`.

Alternatively, you can login using `vercel login`.

### Secrets

`vercel secret add DATABASE_URL_P2_VERCEL_TEST <Postgres database URL>`

OR put environment variable `DATABASE_URL_P2_VERCEL_TEST` from the Vercel UI after the first deploy and re-deploy to enable it

### Environment variables

The environment variable `DATABASE_URL_P2_VERCEL_TEST` should point to a postgres database.

Please check our internal 1Password E2E vault for a ready-to-use environment variable or  
set up your own database and set the environment variable accordingly.

### Local Run

Create `.env`, `.env.build`, `prisma.env` with

`DATABASE_URL_P2_VERCEL_TEST=<value>`

Run `vercel dev`

### Deploy

`vercel --prod`
