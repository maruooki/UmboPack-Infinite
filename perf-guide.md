## Java and JVM Arguments
UmboPack Infinite was developed, tested, and designed for Java 25. Yes, 1.21.1 does use Java 21, but has the capability to use Java 25+, although 26 has not been tested for this modpack. If you have low memory and can't afford to allocate more, consider moving as Java 25 generally has lower memory overhead and better performance than Java 21 during our testing.

It's recommended to use the latest Adoptium Java 25, for those non-techy, that is the version with the most numbers and most recent date. Mojang's bundled Java generally lags behind the latest Adoptium releases and may have older performance optimizations and bug fixes. For the best results, use the latest Adoptium Java 25.

In modern times, we have gone away with the days of `-XX:+UnlockExperimentalVMOptions`, and you really only need two arguments, but change depending on the Java version used. While it is recommended to use Java 25, both JVM arguments for 21 & 25+ will be put below:

Java 21 JVM Arguments: `-XX:+UseZGC -XX:+ZGenerational`

Java 25+ JVM Arguments: `-XX:+UseZGC -XX:+UseCompactObjectHeaders`

If your launcher adds more JVM arguments of things like `-Xms` or `-Xmx`, those are normal.


## Disabling Client-Sided Mods
There are a few mods in UmboPack Infinite that specifically are used exclusively on the client, meaning it is safe to disable/uninstall them if you do not want them. For the sake of simplicity, it is recommended to only disable the mods, as it makes updating easier.

The following mods are safe to disable for extra performance:
- Controlify
- Punchy
- Better Combat Punchy Fix
- Immersive Messages API
- Immersive Damage Indicators
- EMF Compat: Core
- EMF Compat: Create
- Pretty Rain
- Particle Effects
- Sodium Shadowy Path Blocks
- Sounds
- More Sounds


__It is not recommended to just disable every client-side mod, only the ones from the list.__

Distant Horizons is on the server, so it cannot be removed due to AutoModpack, so, it can just be disabled from in-game in Video Settings. Its button is the new one next to the FOV slider on the left.


## Minimum Requirements?
The actual minimum requirements are unknown, but the lowest-ended rig we tested was able to achieve at least 15 FPS, 20-24 FPS once stabilized with minimal effort (on a server, pre-generated world).

CPU: Intel Core I3-8100
GPU: UHD Graphics 630
RAM: 8GB

I have developed the entire modpack while only having 8GB allocated, and it is more than enough for consistent 60+ FPS for hours of gameplay before needing a restart. I'd recommend having at least 6GB minimum.


## Am I lagging, or is it the server?
Client-sided lag is your frame rate, something on your side is lagging, the server is fine.
Server-sided lag is rubberbanding, delayed block breaking/placement, or delayed mob movement. 


## Important for Laptop Users
If playing on a laptop and experiencing heavy lag, make sure Minecraft is using the correct GPU. You can check this in-game using F3 and looking at the top-right. If you see something like Intel UHD or AMD Radeon Graphics, it may be using the incorrect card.


## Why am I crashing on Linux?
Sound Physics Remastered has a crash on Linux with Pipewire. To fix this, you need to set the environment variable like this: `ALSOFT_DRIVERS=pulse` to make it use PulseAudio instead. Depending on your launcher, you can bypass needing to change an entire env for the sake of playing Minecraft by having the command run for your instance.
