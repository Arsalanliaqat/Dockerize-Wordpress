Dockerize  WordPress
====================

The [`docker-compose.yml`](docker-compose.yml) specifies the following services:

* `db` -- [MariaDB](https://mariadb.org) accessible on the host on `localhost:3306`
* `phpmyadmin` -- [PhpMyAdmin](https://www.phpmyadmin.net) on `localhost:8080`
* `wordpress` -- [WordPress](https://wordpress.com/about/) on `localhost:8000`

Copy `wp-content` to `./wordpress/wp-content` and the SQL dump to `./db/docker-entrypoint-initdb.d` and start with:

```
$ docker compose up
```

MariaDB will [import](https://github.com/docker-library/docs/tree/master/mariadb#initializing-a-fresh-instance) the dump.
