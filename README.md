# LavaLust API and React frontend

The application is split into two independently deployable projects:

- [`backend/`](./backend/) contains the LavaLust API, CRUD/authentication
  controllers, database configuration, migrations, and Apache/Docker setup.
- [`frontend/`](./frontend/) contains the React/Vite client.

The API routes and local framework-relative layout are unchanged. The frontend
reads `VITE_API_URL`; use `/api` locally with the Vite proxy, and configure the
production build with the API URL ending in `/api`. Set `API_ALLOWED_ORIGIN` on
the API deployment to the frontend's origin.

See each folder's README for setup and deployment details.

## Push each folder to its own GitHub repository

Create the two target GitHub repositories as empty repositories first, then
replace `<YOUR_GITHUB_USERNAME>` below with their owner. Run these commands from
the project root; Git's subtree command exports each folder as the repository
root:

```sh
git subtree push --prefix=backend https://github.com/<YOUR_GITHUB_USERNAME>/francisco_kate_lab6_api.git main
git subtree push --prefix=frontend https://github.com/<YOUR_GITHUB_USERNAME>/francisco_kate_lab6_frontend.git main
```
