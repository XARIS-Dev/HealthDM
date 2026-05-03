# HealthDM — Run production images (one command)

---

## Prerequisites

- **Docker** (≥ 24) and **Docker Compose V2** (`docker compose`)
- **Git**, **curl**, **gzip**, **OpenSSL** (`openssl` on PATH)
- **Internet** — first run downloads ~1 GB and pulls Postgres / Redis / Nginx images

---

## Run (single command)

**Fetch and run the script**

```bash
curl -fLO https://raw.githubusercontent.com/sam-platforms/HealthDM/main/Production/healthdm-prod-setup.sh
chmod +x healthdm-prod-setup.sh
./healthdm-prod-setup.sh --url <release-tarball-url>
```

Then open **http://localhost** . Add **Cortex XSIAM** credentials in the app **Settings** UI when you are ready.

---

## Stop

```bash
cd HealthDM
TAG=local docker compose -f docker-compose.prod.yml down
```

---
