# Crowi Develop

## What is this

Develop environment for Crowi developers.


## Requirement

- Docker (Docker Compose)
- Node

I am using "Docker for Mac" and "Node Version Manager (nvm)".


## Usage

### Clone this repository (only first time)

```
$ git clone https://github.com/suzuki/crowi-develop
```

### Clone Crowi and initialize (only first time)

- Notice: Replace URL to your forked Crowi repository.

```
$ git clone git@github.com:crowi/crowi.git
$ cd crowi
$ npm install
```

### Start some docker containers

```
$ docker-compose up -d
```

### Start Crowi

- Notice: Replace "somesecretstring" to your PASSWORD_SEED value.

```
$ cd crowi
$ PASSWORD_SEED=somesecretstring \
  MONGO_URI=mongodb://localhost/crowi \
  ELASTICSEARCH_URI=localhost:9200 \
  REDIS_URL=localhost \
  node app.js
```

### Open Crowi by browser

Open http://localhost:3000/

### Develop, develop, develop

Hack the Crowi as you wish.

#### If you feel tired to development...

```
$ docker-compose stop
```

And go to bed to sleep.


## License

MIT License


## References

I learned the docker configuration from these repositories. Thank you.

- https://github.com/nooby-noob/docker-node-crowi
- https://github.com/Bakudankun/docker-crowi
