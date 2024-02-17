An API written in Rust. Based on the Luca Palmieri's book "[Zero To Production In Rust](https://www.zero2prod.com)".

# Technology Stack
- Rust
- Actix Web
- PostgreSQL
- sqlx-cli

# Prerequisites
- [Install Rust](https://www.rust-lang.org/tools/install)
- [Install Docker](https://docs.docker.com/get-docker/)
- Install psql - the PostgreSQL CLI tool

# Adding a new SQL migration
Assuming you used the default parameters to launch Postgres in Docker!

```bash
export DATABASE_URL=postgres://postgres:password@127.0.0.1:5432/newsletter
sqlx migrate add create_subscriptions_table
```

# How to run
## PostgreSQL in Docker
```bash
chmod +x scripts/init_db.sh
SKIP_DOCKER=true ./scripts/init_db.sh # Use true/false depending on whether you have the Docker container with PostgreSQL up and running
```

## SQL migration
```bash
sqlx migrate run
```
