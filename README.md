# JhaTasks

A polished, responsive personal and office task-management application built with Next.js, TypeScript, PostgreSQL, Drizzle ORM, Zustand, Framer Motion, and dnd-kit.

## Highlights

- Separate Office, Personal, and unified workspaces
- My Day focus dashboard
- Drag-and-drop Kanban board with advisory WIP limits
- Grouped and sortable List view
- Complete Month, Week, and Day calendar with 30-minute time blocking
- Eisenhower priority matrix
- Productivity insights, streaks, velocity, and work/life balance
- Natural-language task capture
- Global focus timer that logs actual task time
- Recurring tasks, subtasks, markdown notes, tags, and attachments
- Google Calendar, Gmail, Drive, and Google Tasks integration simulations
- Dark and light themes
- Touch-friendly responsive UI for phones, tablets, laptops, and desktops
- Undoable task deletion and JSON data backup

## Responsive support

The interface is tested at:

- 320 × 568 (small phone)
- 390 × 844 (modern phone)
- 768 × 1024 (tablet)
- 1366 × 768 (laptop)
- 1920 × 1080 (desktop)

Mobile includes a safe-area-aware bottom navigation bar, floating task creation, touch drag-and-drop, bottom-sheet dialogs, responsive calendar agendas, and iOS form-focus handling.

## Technology

- Next.js App Router
- React and TypeScript
- Tailwind CSS
- PostgreSQL and Drizzle ORM
- Zustand
- Framer Motion
- dnd-kit
- Lucide icons

## Local setup

1. Install dependencies:

   ```bash
   npm install
   ```

2. Create `.env` with a PostgreSQL connection string:

   ```env
   DATABASE_URL=postgresql://postgres:postgres@127.0.0.1:5432/app_db
   ```

3. Apply the database schema:

   ```bash
   npx drizzle-kit push --config=drizzle.config.json
   ```

4. Start development:

   ```bash
   npm run dev
   ```

Open `http://localhost:3000`.

## Validation

```bash
npx next typegen
npm exec tsc -- --noEmit --pretty false
npm run build
```

The application exposes `/api/health` for runtime and database health checks.

## Data and privacy

- `.env` files are ignored by Git.
- Task data is stored in PostgreSQL.
- The app starts without pre-filled tasks.
- Google integration screens use simulated data and synchronization flows.
