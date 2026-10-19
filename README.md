# echo-ink

minimal blogging platform: write, publish and read posts.

## features

- sign up and sign in
- rich text editor for writing posts
- create, edit and delete your own posts
- home feed, search, single post view and author pages
- profile editing
- email via nodemailer

## stack

- backend: hono on cloudflare workers, prisma (accelerate), postgres, zod
- frontend: react 18, vite, typescript, recoil, tailwind css, framer motion

## run locally

```bash
cd echoink-backend && npm install && npm run dev       # wrangler dev
cd echoink-frontend && npm install && npm run dev      # vite
```

deploy the backend with `npm run deploy` (wrangler).

## env

the backend reads `DATABASE_URL` and `JWT_SECRET` from wrangler. copy `echoink-backend/.dev.vars.example` to `.dev.vars` for local dev, and use `npx wrangler secret put` for production.
