# Docker Containers running Locally

This is an opinionated list of Docker containers I find useful during daily work.

---

Secrets are stored in a `.env` file. See the `.env_sample` file. It has all required
secrets with a dummy values. Change them!

I use [lazydocker](https://github.com/jesseduffield/lazydocker) to monitor containers.

## Build & Run

```bash
docker-compose up --build --detach
```

### Clean Up

```bash
docker-compose down --remove-orphans
```
Use additional flag `--volume` to discard volumes (this will remove
saved data used by containers).

> Appending the `--volume` will also remove volumes where data are persisted ourside the
> docker conainer.
>
> It's not used now since we want logs to persist between containers restarts.

## Contaienrs

### SonarQ

It'll be available at [port 9000 on localhost](http://[::1]:9000).

The [default `admin` credential](https://docs.sonarsource.com/sonarqube/9.8/instance-administration/security/#default-admin-credentials) are:

- username: `admin`
- password: `admin`

> Change it! I put my in the [KeePassXC](https://github.com/keepassxreboot/keepassxc).

### IT Tools

It's available on [port 80 on localhost](http://[::1]:80).

### Grafana Labs' LGTM

It's available on [port 3000 on localhost](http://[::1]:3000).

[Default `admin` credentials](https://signoz.io/guides/what-is-the-default-username-and-password-for-grafana-login-page/#grafanas-default-username-and-password)
are:

- username: `admin`
- password: `admin`

> Change it! I put my in the [KeePassXC](https://github.com/keepassxreboot/keepassxc).

### Wiremock

It's available on port 8081 on localhost and under the
[__admin/mappings](http://[::1]:8081/__admin/mappings)
page you can examin loaded Wiremock mappings.

### Mermain Live Editor

 * while Mermaid Live Editor is available on [port 8082 on localhost](http://[::1]:8082).
