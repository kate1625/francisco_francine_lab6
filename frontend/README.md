# LavaLust React frontend

This React/Vite application is the client for the LavaLust product API.

## Configure the API

For local development, copy `.env.example` to `.env`. `VITE_API_URL=/api` uses
the Vite proxy, which forwards requests to `http://localhost:3000`. The backend
must be running on port 3000.

For a production build, set `VITE_API_URL` in the frontend hosting provider's
build environment to the separately deployed API base URL ending in `/api`,
for example `https://your-backend-url.onrender.com/api`. Do not use `/api` as
the production value when the API is deployed on a different host. Rebuild or
redeploy the frontend after changing this build-time variable.

The API deployment must set `API_ALLOWED_ORIGIN` to the frontend's exact origin
(scheme and hostname, without a path or trailing slash), for example
`https://your-frontend-url.onrender.com`. For local development, set it to
`http://localhost:5173`.

## Run locally

```sh
npm ci
npm run dev
```

## Build

```sh
npm run build
```
