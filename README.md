# Star Wars Galaxy 2

Star Wars Galaxy 2 is a stellaris mod that brings the star wars galaxy in your vanilla game.

# Contributing

See the [Contributing doc](https://gitlab.com/renegades-modding-group/star-wars-galaxy-2/-/blob/master/CONTRIBUTING.md) for information on how you can help.

# FAQ

- Why do I need Planetary Diversity for this mod?

While in the current version of star wars galaxy 2 (v0.1) Planetary Diversity is not used for custom systems, the upcoming v0.2 update with the addition of the lore-accurate type maps will require it. With the many different planet classes from Planetary Diversity the systems will become even more lore-accurate than with only the vanilla type planets.

- Why are the origins "Syncretic Evolution" and "Necroids" disabled

The simple answer to this is because they doesnt work in combination with a static galaxy. The second species will not be what you selected in the empire creator.
The more complex answer is that because the galaxy is static some of the game_start events that normaly run while the galaxy is generated arent firing. These two origins rely on an effect called "generate_start_pops" in the game_start.12 event. This effect will spawn all the pops for the empire. For an empire with any other origin this effect can be run at any time but for these two origins it needs to run right after the game created/loaded the empire because it uses the last_created_species scope to access the secondary species that comes with these origin. But since the event with this effect isnt called and there being no other way for me to access the secondary species through other means, your secondary species is lost.

- Why is the system not called correctly with the "Shattered Ring" and "Void Dwellers" origin?

These origins use their own system initializers which prevents me from manually renaming them because there is no way to know to which they should be renamed.

# License

You are free to use this mod for everything you want, even your own mod. The only premise is to credit this mod on the steam page.
