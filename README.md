# Oscar Party 🎬

A web app for hosting Oscar award prediction parties! Invite friends, make your picks for every category, and see who comes closest when the winners are announced.

Live site: [https://oscar-party-3-forms.matchthetarget.com](https://oscar-party-3-forms.matchthetarget.com)

---

## Features

- **Ballot Creation**: Easily make your predictions for each Oscar category.
- **Friends & Groups**: Invite friends to join your Oscar Party and compete together.
- **Automatic Scoring**: Scores are updated instantly as winners are revealed.
- **Leaderboard**: Track who’s in the lead in real-time.
- **Responsive Design**: Works on desktop or mobile.

---

## Tech Stack

- **Framework:** Ruby on Rails 8
- **Database:** PostgreSQL
- **Web Server:** Puma
- **Front-end:** Hotwire (Turbo/Stimulus), Importmap  
- **Containerization:** Docker, Dev Containers
- **Other:** Redis (for background jobs), Solid Cache/Queue/Cable, Devise (authentication), Pundit (authorization), Simple Form, Kaminari

See [`Gemfile`](https://github.com/fredricngo/oscar-party/blob/main/Gemfile) for more details about installed gems.

---

## Development Setup

**Easy local setup using Dev Containers:**

1. **Install [Docker](https://www.docker.com/products/docker-desktop) & [VS Code](https://code.visualstudio.com/).**
2. Open repo in VS Code, and *"Reopen in Container"* if prompted.

The container automatically provisions:
- Ruby, Rails, Node, Postgres, Redis
- Ruby gems and npm packages

See [`/.devcontainer/devcontainer.json`](https://github.com/fredricngo/oscar-party/blob/main/.devcontainer/devcontainer.json) and [`/.devcontainer/docker-compose.yml`](https://github.com/fredricngo/oscar-party/blob/main/.devcontainer/docker-compose.yml) for details.

**Manual Setup:**

```bash
git clone https://github.com/fredricngo/oscar-party.git
cd oscar-party
bin/setup
bin/dev   # Starts server and JS compiler
```

**Database Credentials (for dev containers):**
- Host: `localhost`
- User: `student`
- Password: `postgres`
- Database: `oscar_party_4_associations` or `postgres`

---

## Testing & CI

GitHub Actions CI runs lint, vulnerability, and dependency scans on every push and pull request:

- Ruby static analysis: `bin/brakeman`
- JS dependency audit: `bin/importmap audit`
- Style enforcement: `bin/rubocop`

See [`ci.yml`](https://github.com/fredricngo/oscar-party/blob/main/.github/workflows/ci.yml).

---

## Error Handling

Custom error pages for common web issues:

| Error | Page                       |
|-------|----------------------------|
| 400   | [public/400.html](public/400.html)          |
| 404   | [public/404.html](public/404.html)          |
| 406   | [public/406-unsupported-browser.html](public/406-unsupported-browser.html) |
| 422   | [public/422.html](public/422.html)          |
| 500   | [public/500.html](public/500.html)          |

---

## Contributing

Pull requests welcome! For major changes, please open an issue first to discuss what you would like to change.

---

## License

Some rights reserved. See [LICENSE.txt](LICENSE.txt).

---

## Author

Maintained by [fredricngo](https://github.com/fredricngo)
