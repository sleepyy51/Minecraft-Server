# Docker SMP

This is a little side project aiming to make a reproducible vanilla SMP using a Docker image.\
Since it's mostly for mi personal use I have some plugins plus configs you should modify.\
See Below on  **What's inside my compose?**

## Installation and Usage
You need to have Docker installed
```bash
git clone https://github.com/sleepyy51/Minecraft-Server.git
cd Minecraft-Server/
docker compose up -d
```

## Configuration
This project uses the docker image [itzg/minecraft-server](https://hub.docker.com/r/itzg/minecraft-server), you can modify the compose.yml reading the documentation or using the [following page](https://setupmc.com/java-server/) to create a new compose.yml to your taste.

## What's inside my compose?
By default this server is configured to be offline I recommend changing it back to online
``` yml
ONLINE_MODE: "false"
```
It's configured to run on port 27532, with 8GB of ram, paper for Minecraft in 1.21.11. The container it's limited to 3 cores and 10GB of ram.\
Remember to change the Whitelist, by default no one can enter. You can either add them manually by console or by modifing this lines
``` yml
ENABLE_WHITELIST: "true"
WHITELIST: |-        
```
If you want to change the server icon from this:\
![Server Icon](https://raw.githubusercontent.com/sleepyy51/Minecraft-Server/c5da060513f2f522d605bf82e5e5546f6d22398a/server-icon.png)\
Modify the following line in the compose, make sure to provide a link to a 64x64 png.
``` yml
ICON: "https://raw.githubusercontent.com/sleepyy51/Minecraft-Server/c5da060513f2f522d605bf82e5e5546f6d22398a/server-icon.png"
```
The timezone of the server it's set to America/Mexico_City, you can change it back to UTC removing this line:
``` yml
TZ: "America/Mexico_City"
```

I have the following plugins installed, feel free to edit or delete them!
- [Skins restorer](https://modrinth.com/plugin/skinsrestorer)
- [PatPat (I'ts incredibly funny to pet mobs!)](https://modrinth.com/plugin/patpat)
- [Spark](https://spark.lucko.me/)
- [AuthMe (Because it's an offline server)](https://modrinth.com/plugin/authmerereloaded)
- [Orbital Strike (I'm too lazy to build the actual thing)](https://modrinth.com/plugin/orbitalstrike-wemmbu)

## License

[MIT](https://raw.githubusercontent.com/sleepyy51/Minecraft-Server/refs/heads/main/LICENSE)
