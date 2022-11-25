# Redis-Docker-Compose-template
A template that helps you quick start a Redis server easily.

<br />

### Fast run
1. Clone and get into this repo
```bash
git clone https://github.com/geeksloth/redis-docker-compose-template.git && cd redis-docker-compose-template
```
2. Run Docker Compose with detached flag
```bash
docker compose up -d
```
3. Connect to Redis with password: ```mysimplepassword```

<br />

### More Practical Way (recommended)

1. Clone and get into the repo by the 1st previous step.
```bash
git clone https://github.com/geeksloth/redis-docker-compose-template.git && cd redis-docker-compose-template
```

2. Change ```--requirepass 03fbc...669``` in *docker-compose.yml* file to your password. Which you can generate with **SHA-256** algorithm, or simply using online tools eg. [SHA256 Online](https://emn178.github.io/online-tools/sha256.html)

3. Modify the ```--save 20 1``` to save a snapshot of your database every 60 seconds if at least 1 write operation was performed.

4. Save your *docker-compose.yml* and run it by 
```bash
docker compose up -d
```

5. Connect to your Redis with *your password* hashed in the step 2.
