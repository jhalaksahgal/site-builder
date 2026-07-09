# Site Builder

Site Builder is an AI-assisted website creation platform.  
Instead of building pages manually from scratch, users describe what they want, and the system helps generate and organize website content and structure.

## What the Project Does

At a product level, the platform helps users go from an idea to a working website flow:

1. **Input stage**  
   The user provides prompts/instructions (for example: business type, style, audience, sections needed).

2. **AI-assisted generation stage**  
   The system interprets input and creates website-ready outputs such as page structure, section content, and suggested layout direction.

3. **Refinement stage**  
   Users can adjust generated results (edit text, regenerate parts, update structure, or refine style choices).

4. **Assembly stage**  
   The generated/refined pieces are organized into a coherent website structure through the builder interface.

5. **Persistence stage**  
   Website/project data is saved through backend APIs and database models so users can continue editing later.

## How It Works (System Flow)

- The **client** provides the interactive builder experience and sends user actions/prompts to backend APIs.
- The **server** handles request processing, generation workflows, and business logic.
- **Prisma/database** stores project state (site data, generated content metadata, and related entities).

## Project Structure

- **`client/`**: Frontend application (builder UI and user interaction layer)
- **`server/`**: Backend application (API, controllers, generation workflow handling, persistence)

## Run Locally

### 1) Clone the repository

```bash
git clone https://github.com/jhalaksahgal/site-builder.git
cd site-builder
```

### 2) Install dependencies

```bash
cd client && npm install
cd ../server && npm install
cd ..
```

### 3) Configure environment variables

- Update `client/.env`
- Add/update `server/.env` (if required)

### 4) Start the backend

```bash
cd server
npm run dev
```

### 5) Start the frontend (new terminal)

```bash
cd client
npm run dev
```

## Common Scripts

### Client (`client/`)

```bash
npm run dev
npm run build
npm run preview
npm run lint
```

### Server (`server/`)

```bash
npm run dev
npm run build
npm start
```

### Prisma (from `server/`)

```bash
npx prisma generate
npx prisma migrate dev
npx prisma studio
```

## Tech Foundation

- TypeScript-first full-stack architecture
- Vite-based frontend
- Node.js backend
- Prisma ORM for data access

## Summary

This project is built around an **AI-assisted website creation loop**:  
**Prompt → Generate → Edit → Organize → Save**,  
with a frontend builder interface and a backend service layer that powers generation and persistence.