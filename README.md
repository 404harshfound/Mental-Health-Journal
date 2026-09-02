# Mental Health Journal

A small journaling app for tracking mood, gratitude, and stress levels day to day, with a 7-day view to spot trends over time. Signup and login are session-based, with bcrypt-hashed passwords.

Built with Node.js and Express on the backend, MySQL for storage, and a plain HTML/CSS frontend with Chart.js for the history view.

## How it works

1. Sign up or log in — a session is created and kept server-side
2. Add a daily entry: mood, a gratitude note, and a stress level
3. Entries are stored in MySQL against your user ID
4. The last 7 days render as a chart so trends are easy to spot at a glance
5. There's also a quick in-app feedback form

## Run Locally

```bash
git clone https://github.com/404harshfound/Mental-Health-Journal.git
cd Mental-Health-Journal
npm install

cp .env.example .env
# fill in your local MySQL credentials and a session secret

npm start
```

Open `http://localhost:3000`.

Create a MySQL database matching `DB_NAME` in your `.env`, with `users`, `journal_entries`, and `feedbacks` tables — see `server.js` for the exact fields each query expects.

## License

MIT — see [LICENSE](LICENSE)
