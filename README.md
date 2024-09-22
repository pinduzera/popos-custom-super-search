# popos-custom-super-search
Extra custom search queries to be used with Pop!_OS super key.

This is my custom repository because I have noticed that after some updates my `config.ron` gets resetted, so I wan't this repo to save my custom file and add useful ones as time pass by. 

Feel free to use it =)

## How to add a Cutom search

Pretty much edit the `config.ron` file.

`sudo nano /usr/lib/pop-launcher/plugins/web/config.ron`

Add this to the final of the rule list:

```{bash}
(
    matches: ["bg", "bgg", "boardgamegeek"],
    queries: [(
                name: "BoardGameGeek", 
                query: "https://boardgamegeek.com/geeksearch.php?action=search&objecttype=boardgame&q="
              )]
),
```

Remember that the search text will be appended to the end of the "query" parameter, so, remember to reorder the query of whatever website you are using.

If you want to use a cusom Icon , you can add the `icon:` after the query with the icon link. But if the site has one, it will use that by default.

