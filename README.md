# planetbusters
Small game for the LibGDX jam

Sadly I'm just to swamped with Space Grunts and Heroes of Loot 2 work so
I simply don't have time to put a lot more into this.

I do think it can be fleshed into a pretty fun game with shops, weapon upgrades
different planet environments and more, so let me know if you do something with it!
It's actually possible I might pick this up later in the year to do something with it
myself.. we'll see!

As it is now, it's just a quick shooter, you can't die or lose, no menu or interface, etc.


# how to play 

The default keyboard settings are the only ones available so:
arrow keys to run,  X to shoot

You can change those in ArcadeCanvas or if I have time I'll add the keyboard setup stuff
I used in my other games.

# libgdx usage
So you might notice some weird things going on that could be done different (better?)
when I would use more of LibGDX's stuff, but I mainly use LibGDX as the layer between my
own framework and the OS.

The upside of this is that it makes things portable to other systems where libgdx
doesn't run, or even to other middleware.

Also I'm not the cleanest of coders, this is actually one of my neater sources (but it's
also very small compared to other stuff). My idea is: if the code works, it works, move on!


## build

This project has been modernized to build the Desktop target with Java 21 and Gradle 8, while Android/iOS migration is pending.

Prerequisites (Linux):
- Java 17, 21, or any newer LTS version (21+); the build will target Java 8 bytecode for compatibility with LibGDX 1.7.x.

Desktop (run + package):

```bash
# Run the game (opens a window)
./gradlew desktop:run

# Build a runnable fat jar (includes assets and dependencies)
./gradlew desktop:dist

# Output: desktop/build/libs/desktop-1.0.jar
```

Android/iOS
- Android and iOS modules are temporarily excluded from the build while the project is upgraded to current Android Gradle Plugin / iOS toolchain. If you need these targets, open an issue or PR and we can migrate them next.

Troubleshooting:
- If you see Java compile warnings about source/target 8 being obsolete, they are safe; we intentionally build Java 8 bytecode for library compatibility.
