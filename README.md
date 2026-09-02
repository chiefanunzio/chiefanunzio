# ~/nunzio

```
$ cat docker-compose.yml
```

```yaml
version: "3.9"

services:

  frontend:
    image: nunzio/angular:latest
    tech: [Angular, Signals, RxJS, Kendo UI, Nx, Module Federation]
    restart: sempre-quando-serve-uno-stato-pulito

  backend:
    image: nunzio/infra:latest
    tech: [Docker, Kubernetes, self-hosted-stack]
    depends_on: [nessun-vendor]

  principles:
    image: nunzio/manifesto:v1
    environment:
      - VENDOR_LOCK_IN=false
      - CODICE_LEGGIBILE=true
      - CLEVER_MA_FRAGILE=rejected

  offline:
    image: nunzio/falegnameria:local-only
    note: "stesso rigore, ritmo più lento, niente CI/CD"
```

```
$ docker compose up -d
[+] Running 4/4
 ✔ frontend    started
 ✔ backend     started
 ✔ principles  started
 ✔ offline     started
```

---

### logs --tail

```
2026-08  MFE platform  → refactor state management: da servizi custom a Signals mirati
2026-06  MFE platform  → loader condiviso costruito a mano (niente lib esterne se non serve)
2026-06  MFE platform  → grid dati con rendering custom via TemplateRef
```

---

```
$ nunzio --status
uptime: sempre in imparo-qualcosa-di-nuovo
mood:   pragmatico > alla moda
```
