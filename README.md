# Docker Containers running Locally

This is an opinionated list of Docker containers I find useful during daily work.

---

Secrets are stored in a `.env` file.

I use [lazydocker](https://github.com/jesseduffield/lazydocker) to minotor containers.

## Build & Run

```bash
docker-compose up --build --detach
```

### Clean Up

```bash
docker-compose down --remove-orphans --volume
```

> Appending the `--volumes` will also remove volumes where data are persisted ourside the
> docker conainer.
>
> It's not used now since we want logs to persist between containers restarts.

## Contaienrs

### SonarQ

It'll be available at [port 9000 on localhost](http://[::1]:9000).

The [default administration credential](https://docs.sonarsource.com/sonarqube/9.8/instance-administration/security/#default-admin-credentials) are:

- username: `admin`
- password: `admin`

> Change it! I put my in the [KeePassXC](https://github.com/keepassxreboot/keepassxc).

## IT Tools

It's available on [port 8181 on localhost](http://[::1]:8181).

## Grafana Labs' LGTM

It's available on [port 3000 on localhost](http://[::1]:3000).

[Default `admin` credentials](https://signoz.io/guides/what-is-the-default-username-and-password-for-grafana-login-page/#grafanas-default-username-and-password)
are:

- username: `admin`
- password: `admin`

> Change it! I put my in the [KeePassXC](https://github.com/keepassxreboot/keepassxc).
