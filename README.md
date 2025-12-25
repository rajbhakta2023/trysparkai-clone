# TrySparkAI Website Clone

This repository will house a close reproduction of the public face of [trysparkai.com](https://trysparkai.com/), along with any customizations we need for our own presentation.

## Goals

1. Capture the structure, styling, and content of the live site so we can quickly iterate on features.
2. Document the cloning and customization steps as part of the project board below.

## Getting started

1. Install dependencies (stack TBD; feel free to use `bun` if we're building the frontend).
2. Run the local dev server (`bun dev` / equivalent once scaffolding exists).
3. Coordinate further updates via the GitHub project board.

## Vercel deployment

- The captured homepage lives in `public/index.html` and is served by `@vercel/static`, so the first deploy is just the static snapshot we recorded.  
- `vercel.json` routes all traffic to `public/index.html`, so you can add client-side logic and rewrites later without changing this config.
- To deploy: install the [Vercel CLI](https://vercel.com/download) (already available in ACFS), run `vercel login` or export a `VERCEL_TOKEN`, then `vercel --prod` from this directory. Vercel will read `vercel.json` and publish the static snapshot on the platform.

## Previewing locally

- Fetch the site with `curl -L https://trysparkai.com/ -o public/index.html` whenever you want a fresh snapshot before deploying.
- Launch a quick preview server with `python3 -m http.server 8000` inside this directory, then browse to `http://localhost:8000/` through your tunnel/SSH port forward.
