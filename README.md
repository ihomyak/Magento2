![Magento 2](https://cdn.rawgit.com/rafaelstz/magento2-snippets-visualstudio/master/images/icon.png)

#  Magento 2 Docker to Development

It is fork by [Rafael Corrêa Gomes & Co](https://github.com/clean-docker/Magento2)

### Apache 2.4 + PHP 7.0 + OPCache + MariaDB + N98 Magerun 2 + XDebug + Redis

### Requirements

**Linux:**

Install [Docker](https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/) and [Docker-compose](https://docs.docker.com/compose/install/#install-compose).

### How to use

Execute in your terminal, change the *M2DOCKER* to use the name of your project:

```
curl -s https://raw.githubusercontent.com/ihomyak/Magento2/master/init | bash -s M2DOCKER clone
```

If you want to install the Magento 2, use like that:

```
cd M2DOCKER
./shell
rm index.php
install-magento2
```

You can specify the version that want install (e.g. `install-magento2 2.2`).

fix error "Cron script readiness check failed"
php bin/magento setup:cron:run

**This project will be downgrade of PHP version to 7.0, for work with Magento 2.0 and Magento 2.2.6**

Add tags for configurations to any versions of Magento2  

### Xdebug
Thanks for https://blog.denisbondar.com/post/phpstorm_docker_xdebug

> Решение проблемы оказалось достаточно простым. Я просто создал общую сеть для бандла в docker-compose (192.168.220.0/28) и таким образом добился одинакового IP-адреса хоста (192.168.220.1) на всех машинах членов команды разработки.

> Если Вы используете MacOS или Windows, то вместо адреса 192.168.220.1 Вам нужно будет указать host.docker.internal в приведенном ниже docker-compose.yml.


### Panels

Enjoy your new panels!

**Web server:** http://localhost:9080/

**PHPMyAdmin:** http://localhost:9090

**Local emails:** http://localhost:9025

### Features commands

| Commands  | Description  | Options & Examples |
|---|---|---|
| `./init`  | If you didn't use the CURL setup command above, please use this command changing the name of the project.  | `./init MYMAGENTO2` |
| `./start`  | If you continuing not using the CURL you can start your container manually  | |
| `./stop`  | Stop your project containers  | |
| `./kill`  | Stops containers and removes containers, networks, volumes, and images created to the specific project  | |
| `./shell`  | Access your container  | `./shell root` | |
| `./magento`  | Use the power of the Magento CLI  | |
| `./xdebug`  |  Enable / Disable the XDebug | |
| `./composer`  |  Use Composer commands | `./composer update` |

### License

MIT © 2018 [Viktor](https://github.com/ihomyak/).
