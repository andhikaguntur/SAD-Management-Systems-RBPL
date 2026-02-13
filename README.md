# SAD RBPL
A full-stack monorepo project developed for the final project of Rancang Bangun Perangkat Lunak (RBPL). It is built for Sumber Anugerah Diesel to manage diesel machine booking across different user roles (user, manager, admin) with unified type safety and reusable shared utilities.

## Developer Team
- Andhika Guntur Ramadan - 124240077
- Galang Ivandry - 124240042

## Course Instructor
Simon Pulung Nugroho, S.Kom., M.Cs.

## Getting Started

### 1. Clone the repository

```
git clone <repo-url> .

```

### 2. Install dependencies

Make sure you have pnpm installed globally:

```
npm install -g pnpm
```

Then install everything:

```
pnpm -r install
```

### 3. Running the Apps

Start the backend (Express.js) from the root project directory

```
pnpm run dev:api
```

Start the frontend (Next.js) from the root project directory

```
pnpm run dev:admin # or
pnpm run dev:manager # or
pnpm run dev:user
```

Start frontend and backend concurrently from the root project directory
```
pnpm run dev
```

## Tech Stack

- Next.js
- Express.js
- TypeScript
- Turborepo
- pnpm
- Tailwind CSS

## Shared Code

Use the `@shared` import alias to access shared types/utilities:

```
import { TYPES } from "@shared/types";
```

This alias is configured in the root tsconfig.json and respected by both frontend and backend apps.

## Notes

- This project uses workspace-level lockfile; always install dependencies from the root.
- Recommended workflow: build `@shared` first if using `tsc --build` in composite mode.
- Consider using `.env` files for production configuration and API endpoints