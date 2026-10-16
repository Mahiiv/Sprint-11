## Sprint 11 - Full Stack Integration

In this sprint I connected my Cine-Stream React app to my own Node.js + MongoDB backend from Sprint 10. There is a new Posts page where posts are saved in the database.

### What I did
- Phase 1: React gets posts from my backend with useEffect + fetch. Fixed the CORS error by adding the cors package in Express.
- Phase 2: Add Post form (POST), Delete button (DELETE), Loading message and an error message if the server is down.
- Phase 3: skipped (it was optional).

### Live links
- Frontend (Vercel):https://sprint8cinestream.vercel.app/
- Backend (Render): https://sprint-10-mongoatlas.onrender.com/posts
- Backend repo: https://github.com/Mahiiv/sprint_10_mongoAtlas

### How to run it locally
1. Run `npm install`
2. Make a `.env` file with:
   - `VITE_TMDB_KEY=your tmdb token`
   - `VITE_API_URL=http://localhost:5000`
3. Start the backend from the Sprint 10 repo (`node server.js`)
4. Run `npm run dev`

### Problems I faced
- CORS error: fixed by adding `app.use(cors())` in the backend.
- Double slash in the URL (`//posts`) gave a 404 on Vercel. The `VITE_API_URL` had a `/` at the end, so I removed it.
- The Render link has to go in Vercel's environment variables, not localhost.
