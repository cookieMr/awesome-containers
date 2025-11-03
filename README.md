# Docker Containers running Locally

This is an opinionated list of Docker containers I find useful during daily work.

---

Secrets are stored in a `.env` file. See the `.env_sample` file. It has all required
secrets with a dummy values. Change them!

I use [lazydocker](https://github.com/jesseduffield/lazydocker) to monitor containers.

## Build & Run

Pull fresh images:
```bash
docker-compose pull
```
Actual build & run after pull:
```bash
docker-compose up --build --detach
```

### Clean Up

```bash
docker-compose down --remove-orphans
```
Use additional flag `--volumes` to discard volumes (this will remove
saved data used by containers).

> Appending the `--volumes` will also remove volumes where data are persisted outside the
> docker container.
>
> It's not used now since we want logs to persist between containers restarts.

## Containers

* [SonarQ](http://localhost:9000)
  - username: `admin`
  - password: `admin`
    - Change it! I put my in the [KeePassXC](https://github.com/keepassxreboot/keepassxc).
* [Grafana Labs' LGTM](http://localhost:3000)
  - username: `admin`
  - password: `admin`
    - Change it! I put my in the [KeePassXC](https://github.com/keepassxreboot/keepassxc).
* [IT Tools](http://localhost:80)
* [Omni Tools](http://localhost:81)
* [Swagger Editor](http://localhost:8083)
* [Wiremock](http://localhost:8081/__admin/mappings)
  - check the [.env](.env_sample) file to set the mapping path
* [Mermain Live Editor](http://localhost:8082)
* Docker tools:
  - [Composerize](http://localhost:82)
  - [Decomposerize](http://localhost:82/decomposerize/)
  - [Composeverter](http://localhost:82/composeverter/)
* [Meme Editor](http://localhost:3001)
