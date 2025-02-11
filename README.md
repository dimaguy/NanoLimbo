## NanoLimbo

This is lightweight minecraft limbo server, written on Java with Netty.
The main goal of the project is maximum simplicity with a minimum number of sent and processed packets.
This limbo is empty, there are no ability to set schematic building since 
this is not necessary. You can send useful information in chat or BossBar.

No plugins, no logs. The server is fully clear. It only able keep a lot of players while the main server is down.

The general features:
* High performance. The server not saves and not cached any useless (for limbo) data.
* Doesn't spawn threads per player. Uses fixed threads pool.
* Support for **BungeeCord** and **Velocity** info forwarding.
* Support for [BungeeGuard](https://www.spigotmc.org/resources/79601/) handshake format.
* Multiple versions support.
* Fully configurable.
* Lightweight. App size around **2MB.**

![](https://i.imgur.com/sT8p1Gz.png)

### Versions support

Symbol `X` means all minor versions.

- [x] 1.8.X
- [x] 1.9.X
- [x] 1.10.X
- [x] 1.11.X
- [x] 1.12.X
- [x] 1.13.X
- [x] 1.14.X
- [x] 1.15.X
- [x] 1.16.X
- [x] 1.17.X
- [x] 1.18

The server **doesn't** support snapshots.

### Commands

There are no commands. To close server just run `Ctrl+C` in the terminal. It will be closed correctly.

### Installation

The installation process is simple.

1. Download the latest version of program **[here](https://github.com/Nan1t/NanoLimbo/releases)**
2. Put jar file in the folder you want.
3. Create a start script as you did it for Bukkit or BungeeCord with command like this:
`java -jar NanoLimbo-<version>.jar`
4. The server will create `settings.yml` file. It's a server configuration.
5. Configure it as you want and restart server.

### About player info forwarding

The server supports player info forwarding from the proxy. There are several types of info forwarding:

* `LEGACY` - The **BungeeCord** IP forwarding.
* `MODERN` - **Velocity** native info forwarding type.
* `BUNGEE_GUARD` - **BungeeGuard** forwarding type.

If you use BungeeCord, or Velocity with `LEGACY` forwarding, just set this type in the config.  
If you use Velocity with `MODERN` info forwarding, set this type and paste secret key from Velocity 
config into `secret` field.
If you installed BungeeGuard on your proxy, then use `BUNGEE_GUARD` forwarding type. 
Then add your tokens to `tokens` list.

### Contributing

You can create pull request, if you found some bug, optimization ability, or you want to add some functional, 
which is suitable for limbo server and won't significantly load the server.

### Building

Required software:

* JDK 1.8+
* Gradle 7+

To build minimized .jar, go to project root and write in terminal:

```
gradlew shadowJar
```

### Contacts

If you have any question or suggestion, join to [Discord server](https://discord.gg/4VGP3Gv)
