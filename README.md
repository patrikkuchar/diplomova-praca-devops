# Diplomova Aplikácia – Inštrukcie na Spustenie

Táto aplikácia je navrhnutá tak, aby mohla byť jednoducho spustená pomocou Docker Compose, ktorý automaticky pripraví všetky potrebné kontajnery. Aplikácia obsahuje front-end, back-end, Keycloak, PostgreSQL, a Redis kontajnery.

## Prerequisites

### 1. Inštalácia Docker Desktop

1. Stiahnite a nainštalujte **Docker Desktop** z [Docker oficiálnej stránky](https://www.docker.com/products/docker-desktop/).
2. Po inštalácii otvorte **Docker Desktop** a overte, či Docker beží.

### 2. Docker Compose

Docker Desktop obsahuje Docker Compose, takže po inštalácii Docker Desktop budete mať prístup aj k príkazom Docker Compose.

> **Poznámka:** Ak používate Linux, môžete si Docker Compose doinštalovať zvlášť podľa inštrukcií v [oficiálnej dokumentácii Docker Compose](https://docs.docker.com/compose/install/).

## Inštrukcie na Spustenie

### 1. Klónovanie repository  
Najskôr si skopírujte tento projekt do vášho lokálneho počítača:
```bash
git clone https://github.com/patrikkuchar/diplomova-praca-devops.git
cd diplomova-praca-devops
 ```

### 2. Spustenie Docker Compose

Spustite projekt v oddelených kontajneroch pomocou príkazu:

```bash
cd prod
docker-compose up -d
```

Tento príkaz automaticky:

- Stiahne potrebné Docker obrazy pre `fe`, `be`, `keycloak`, `postgresql` a `redis` kontajnery (ak ich nemáte lokálne).
- Inicializuje a spustí každý kontajner v oddelenom prostredí, kde každý komponent bude komunikovať podľa definovaného nastavenia v `docker-compose.yml`.

Aby ste mohli kontrolovať stav kontajnerov, použite:

```bash
docker-compose ps
```

Ak chcete zastaviť kontajnery, použite:

```bash
docker-compose down
```

### 3. Otvorenie Aplikácie

Po úspešnom spustení kontajnerov môžete otvoriť aplikáciu vo vašom prehliadači na adrese [http://localhost:4200](http://localhost:4200).