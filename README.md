# GKSS Website

Welcome to the official GKSS Website repository. This is a modern, full-stack SvelteKit web application styled with Tailwind CSS and DaisyUI. Supabase handles backend services including authentication, database, and storage.

This project is maintained under the [MIT License](#license) and will be made public to encourage collaboration. Contributions are welcome — all code changes are reviewed before being merged.

---

## 🚀 Tech Stack

- [SvelteKit](https://kit.svelte.dev) — Frontend Framework
- [Tailwind CSS](https://tailwindcss.com) — Utility-first Styling
- [DaisyUI](https://v4.daisyui.com) — Prebuilt UI Components
- [Supabase](https://supabase.com) — Backend-as-a-Service (PostgreSQL, Auth, Realtime, Storage)
- [Docker](https://www.docker.com) — Local containerized development

---

## ⚙️ Project Setup

### Prerequisites

- [Node.js](https://nodejs.org/) (v16+)
- [Docker + Docker Compose](https://docs.docker.com/get-docker/)
- [Supabase CLI](https://supabase.com/docs/guides/cli)
- A code editor (e.g., [VS Code](https://code.visualstudio.com/))

### 1. Clone the Repository

```bash
git clone https://github.com/NWU-VAAL-GKSS/nwu_vaal_gkss.git
cd nwu_vaal_gkss
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Start SvelteKit (Frontend)

```bash
npm run dev
```

App will be available at: [http://localhost:5173](http://localhost:5173)

---

## 🗃️ Backend: Supabase (Local)

We use Supabase in Docker to provide a self-contained local development backend.

### 1. Install Supabase CLI

```bash
npm install -g supabase
```

### 2. Start Local Supabase

```bash
npx supabase start
```

This starts:

- Supabase Auth
- PostgreSQL
- Storage
- Studio (web dashboard)

Default ports:

- Supabase API: `http://localhost:54321`
- Studio: `http://localhost:54323`

### 3. Setup `.env.local`

Create a `.env.local` in the project root:

```env
PUBLIC_SUPABASE_URL='http://localhost:54321'
PUBLIC_SUPABASE_ANON_KEY='<<your-local-anon-key>>'
```

> 🔐 Anon keys are printed in the terminal when you run `npx supabase start`.

### 4. Supabase Client

The Supabase client is already configured inside the project. No need to create a new client — simply import it where needed.

---

## 📁 Project Structure

```
src/
├── routes/                 # Page routes
│   ├── +page.svelte        # Home page
│   ├── +layout.svelte      # Layout template
│   ├── about/+page.svelte  # About page
│   └── contact/+page.svelte# Contact page
├── components/             # Reusable UI components
│   ├── Header.svelte
│   ├── Footer.svelte
│   └── Card.svelte
├── lib/                    # Supabase clients and utilities
├── app.html                # Entry HTML template
├── app.css                 # Global CSS (Tailwind config)
```

---

## ✍️ How to Contribute

### Content Changes

Edit the appropriate `.svelte` file inside `src/routes/`.

- Home: `src/routes/+page.svelte`
- About: `src/routes/about/+page.svelte`

### Add a New Page

1. Create a folder in `src/routes/` (e.g. `events`)
2. Add a `+page.svelte` file with your content.
3. Add a link to the navigation inside `src/components/Header.svelte`.

### Navigation

Update `Header.svelte`:

```svelte
<nav class="flex space-x-4">
	<a href="/">Home</a>
	<a href="/about">About</a>
	<a href="/events">Events</a>
	<a href="/contact">Contact</a>
</nav>
```

---

## 📦 Common Commands

| Command              | Description                      |
| -------------------- | -------------------------------- |
| `npm run dev`        | Start frontend dev server        |
| `npm run build`      | Build frontend for production    |
| `npm run preview`    | Preview production build         |
| `npx supabase start` | Start Supabase in Docker locally |

---

## 🧠 Contributor Notes

- All changes must go through Pull Requests and be reviewed before merging.
- Feature branches should be prefixed with your initials or team (e.g., `ts-feature-header`)
- Use semantic commits if possible.
- Never commit `.env.local` or secret keys.

---

## 📜 License

This project is open-sourced under the MIT License.  
See [LICENSE](https://github.com/NWU-VAAL-GKSS/nwu_vaal_gkss/tree/main#MIT-1-ov-file) for full terms.

---

## 📚 Docs & Resources

- [SvelteKit Docs](https://kit.svelte.dev/docs)
- [Tailwind CSS Docs](https://tailwindcss.com/docs)
- [DaisyUI Docs](https://daisyui.com/docs)
- [Supabase Docs](https://supabase.com/docs)

---

## 🤝 Maintainers

This repository is actively maintained. Code reviews are strict to ensure project health, scalability, and security. If you'd like to become a project lead, speak with a current maintainer.

---
