# [Install Redis Ubuntu](https://redis.io/docs/latest/operate/oss_and_stack/install/install-redis/install-redis-on-linux/)

Redis, which stands for Remote Dictionary Server, is a powerful in-memory data structure store primarily used as a database, cache, and message broker.

This command to adding redis repository GPG key to your system:
```
curl -fsSL https://packages.redis.io/gpg | sudo gpg --dearmor -o /usr/share/keyrings/redis-archive-keyring.gpg
```

This command used to add a new software repository configuration for redis to the apt package manager on a Debian-based Linux system:
```
echo "deb [signed-by=/usr/share/keyrings/redis-archive-keyring.gpg] https://packages.redis.io/deb $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/redis.list
```

Update the package list:
```
sudo apt-get update
```

Install redis:
```
sudo apt-get install redis
```
