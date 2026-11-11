# Afraz Cloud

Production: Flask + PostgreSQL, cookie sessions, CSRF protection and optimistic concurrency. Render Blueprint: `render.yaml`. See `راهنمای استقرار.md` before deployment.

Development (never expose publicly):

```sh
pip install -r requirements.txt
APP_ENV=development BOOTSTRAP_USER=demo BOOTSTRAP_PASSWORD='your-long-dev-password' python app.py
```

Production requires `DATABASE_URL` for PostgreSQL, and bootstrap credentials for first startup. Keep the repository private and never commit secrets. Configure independent backups; JSON exports exclude user accounts. All application users have equal administrative access. This is not an audited accounting or security product.
