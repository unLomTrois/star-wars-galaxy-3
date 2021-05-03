# Star Wars Galaxy 2

Star Wars Galaxy 2 is a mod for the game Stellaris created by Paradox Interactive, which aims to bring an accurate representation of the
Star Wars galaxy into your game.
With the help of Planetary Diversity, a giant galaxy full of different planets can be created inside your game.

# Contributing

See the [Contributing doc](https://gitlab.com/renegades-modding-group/star-wars-galaxy-2/-/blob/master/CONTRIBUTING.md) for information on how you can help.

# Discord

The [Renegades Modding Group Community Discord](https://discord.gg/4xfQ78sPpm) is the best place for you to interact with the community and contributors. Select the Star Wars Galaxy 2 role in the role channel and join us.

# FAQ

- Why do I need Planetary Diversity for this mod?

While in the current version of star wars galaxy 2 (v0.1) Planetary Diversity is not used for custom systems, the upcoming v0.2 update with the addition of the lore-accurate type maps will require it. With the many different planet classes from Planetary Diversity the systems will become even more lore-accurate than with only the vanilla type planets.

- Why are the origins "Syncretic Evolution" and "Necroids" disabled

The simple answer to this is because they don't work in combination with a static galaxy. The second species will not be what you selected in the empire creator.
The more complex answer is that because the galaxy is static some of the game_start events that normally run while the galaxy is generated arent firing. These two origins rely on an effect called "generate_start_pops" in the game_start.12 event. This effect will spawn all the pops for the empire. For an empire with any other origin, this effect can be run at any time but for these two origins, it needs to run right after the game created/loaded the empire because it uses the last_created_species scope to access the secondary species that comes with these origins. But since the event with this effect isn't called and there being no other way for me to access the secondary species through other means, your secondary species is lost.

- Why is my starting system not called correctly with the "Shattered Ring" and "Void Dwellers" origin?

These origins use their own system initializers which means the system gets a random name. For a single-player game, there may be a way to figure out to what this system should be renamed since only one empire can have the origin, but for multiplayer this would be impossible.

- Why do Fallen Empires and Marauders only have one system?

The way these empires spawn on a normal map doesn't work on a static map. To make them work like in vanilla a lot of work needs to be done which could add conflicts with other mods.

# License
This is entirely a community-driven, non-profit project.
Please contact me (chriskar) if you want to use this for your own mod.
