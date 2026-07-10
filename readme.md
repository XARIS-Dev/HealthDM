# HealthDM — Run production images (one command)

---

## Prerequisites

- **Docker** (≥ 24) and **Docker Compose V2** (`docker compose`)
- **Git**, **curl**, **gzip**, **OpenSSL** (`openssl` on PATH)
- **Internet** — first run downloads ~1 GB and pulls Postgres / Redis / Nginx images

---

## Run (single command)

**Fetch and run the script**

### Apple Silicon / Linux ARM64:

```bash
curl -fLO https://raw.githubusercontent.com/XARIS-Dev/HealthDM/refs/heads/main/healthdm-prod-setup.sh
chmod +x healthdm-prod-setup.sh
./healthdm-prod-setup.sh --url https://github.com/XARIS-Dev/HealthDM/releases/download/v2.3.1/healthdm-prod-2.3-linux-arm64.tar.gz
```
### Intel/AMD (Linux or Windows WSL2):

```bash
curl -fLO https://raw.githubusercontent.com/XARIS-Dev/HealthDM/refs/heads/main/healthdm-prod-setup.sh
chmod +x healthdm-prod-setup.sh
./healthdm-prod-setup.sh --url https://github.com/XARIS-Dev/HealthDM/releases/download/v2.3/healthdm-prod-2.3-linux-amd64.tar.gz
```

Then open **http://localhost:8800** . Add the API Keys & ID in the app **Settings** UI when you are ready.

---

## Stop

```bash
cd HealthDM
TAG=local docker compose -f docker-compose.prod.yml down
```

---
