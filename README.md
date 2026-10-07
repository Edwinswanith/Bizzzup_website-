This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

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

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

1. Import this repository into [Vercel](https://vercel.com/new) and use the repository root as the Root Directory.
2. Use the **Next.js** framework preset. `vercel.json` configures `npm ci` for installation and `npm run build` for the build. Leave the Output Directory at the framework default.
3. Add these server-side environment variables in the Vercel project settings for Production and, if needed, Preview:
   - `GOOGLE_API_KEY`: enables the Gemini chat endpoint (`/api/chat`).
   - `GEMINI_MODEL` (optional): overrides the chat model, which defaults to `gemini-3.8-flash`. Use a model available to your Google API project.
   - `RESEND_API_KEY`: enables the contact email endpoint (`/api/contact`). Configure Resend to send from `contact@bizzzup.com`; messages go to `hello@bizzzup.com`.
4. Deploy. After changing environment variables, redeploy to apply them.

For local development, copy `.env.example` to `.env.local` and fill in the values. The site can build without these keys, but the corresponding API integrations require them at runtime.

To deploy from the command line, run `npx vercel` for a preview or `npx vercel --prod` for production from the repository root. `.vercelignore` excludes local environment files, build output, and browser artifacts from CLI uploads. Project linking data in `.vercel/` is already ignored by Git.

The existing standalone Next.js output supports the Docker deployment; Vercel builds the application through its Next.js integration.

Configuration reference: [Vercel project configuration](https://vercel.com/docs/project-configuration/vercel-json).
