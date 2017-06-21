![Reservoir - Drupal distribution](https://raw.githubusercontent.com/acquia/reservoir/8.x-1.x/reservoir-logo.png)

# Reservoir - Docker

This Docker container gives you an easy way to evaluate [Reservoir](https://github.com/acquia/reservoir).

## Quickstart

Pull the Reservoir image and start it on port `8888`.
```
docker pull drpal/acquia-reservoir:1.0.0

docker run -d -p 8888:80 drpal/acquia-reservoir:1.0.0
```

Start a MySQL container.
```
docker run -d --name mysql -e MYSQL_ROOT_PASSWORD=root mysql:latest
```

Fetch the IP address of the MySQL container.
```
docker network inspect bridge
```

Install Reservoir and specify the IP address of the MySQL container.
