# mtg-barcube-scryfall-query
A Scryfall query to filter cards for my bar cube needs. Based on [this reddit post](https://www.reddit.com/r/mtgcube/comments/10yznk2/the_ultimate_no_extra_resources_scryfall_search/)

## What is filtered?
- choosing anything that needs to be remembered, like specific color taplands, pithing needle etc.
- coin flipping
- token creation
- dice rolling
- counters of any kind
- attractions
- initiative
- monarch
- stickers
- digital-only cards
- dungeons
- shuffle effects
- ring tempting
- double-faced cards
- prepared cards
- rooms
- cards >= 1€

Full Query:
```
-(o:"choose a" o:"the chosen") (-o:flip -o:coin) (-fo:create -fo:token) (-o:dice or (-o:roll -o:die)) (-fo:counter or (o:"counter target" (o:spell or o:ability))) -o:attraction -o:initiative -o:monarch -t:attraction (-o:place -o:sticker) -is:digital -o:"venture into the dungeon” -fo:shuffle -o:"ring tempts " -is:dfc eur<1 game:paper -o:"becomes prepared" -t:room
```
[direct Scryfall link](https://scryfall.com/search?q=-%28o%3A%22choose+a%22+o%3A%22the+chosen%22%29+%28-o%3Aflip+-o%3Acoin%29+%28-fo%3Acreate+-fo%3Atoken%29+%28-o%3Adice+or+%28-o%3Aroll+-o%3Adie%29%29+%28-fo%3Acounter+or+%28o%3A%22counter+target%22+%28o%3Aspell+or+o%3Aability%29%29%29+-o%3Aattraction+-o%3Ainitiative+-o%3Amonarch+-t%3Aattraction+%28-o%3Aplace+-o%3Asticker%29+-is%3Adigital+-o%3A%22venture+into+the+dungeon%E2%80%9D+-fo%3Ashuffle+-o%3A%22ring+tempts+%22+-is%3Adfc+eur%3C1+game%3Apaper+-o%3A%22becomes+prepared%22+-t%3Aroom)
