# TODO APP

A simple, session-based Todo application built with Flask and SQLAlchemy. Log in, add tasks, and track their progress through three states — pending, working, and done — all backed by a SQLite database.

## Features

- **User login/logout** — basic session-based authentication
- **Add tasks** — quickly create new to-do items
- **Status cycling** — click a task to cycle its status: `pending → working → done → pending`
- **Clear all tasks** — wipe the task list in one click
- **Flash messages** — instant feedback for login, logout, and task actions
- **SQLite database** — tasks persisted using Flask-SQLAlchemy
- **Modular structure** — built with Flask Blueprints for clean separation of authentication and task logic

## Project Structure

```
TODO APP/
├── run.py                  # App entry point — creates tables and starts the server
├── app/
│   ├── __init__.py         # App factory, configuration, blueprint registration
│   ├── models.py            # Task database model
│   ├── roots/
│   │   ├── auth.py          # Login/logout routes
│   │   └── tasks.py         # Task CRUD and status routes
│   ├── static/               # CSS/JS assets
│   └── templates/            # HTML templates (login, tasks, etc.)
└── instance/
    └── todo.db               # SQLite database (auto-generated)
```

## Requirements

- Python 3.x
- Flask
- Flask-SQLAlchemy

## Setup

1. Clone the repository
2. Install dependencies:
   ```bash
   pip install flask flask-sqlalchemy
   ```
3. Run the app:
   ```bash
   python run.py
   ```
4. Open `http://127.0.0.1:5000` in your browser
5. Log in with the demo credentials:
   - **Username:** `admin`
   - **Password:** `1234`

## How It Works

1. Log in using the demo credentials above
2. Add a new task using the input field — it starts as **pending**
3. Click a task to cycle its status forward (**pending → working → done**)
4. Use **Clear All** to remove every task at once
5. Log out when finished

## Notes

- This project uses hardcoded demo credentials and a fixed secret key for simplicity — **not suitable for production** without proper authentication and configuration.
- The SQLite database file (`todo.db`) is created automatically on first run.

## License

MIT License — feel free to fork, modify, and share.
