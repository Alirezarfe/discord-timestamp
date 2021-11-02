Learn more about Discord timestamp markdown [here](https://github.com/Alirezarfe/random-docs/blob/main/src/Discord/Markdown.md#timestamp).

### Query Parameters
*All of the following parameters are optional*

- `?from=DATETIME` defaults to current time, example of acceptable syntax:
    - `YYYY-MM-DD_HH:MM:SS`
    - `YYYY-MM-DD`
    - `MM-DD_HH:MM` 
    - Plain numbers will be treated as Discord snowflake ID \
    You may omit the year in date, and seconds in time or the time overall.
- `?style=STYLE` from [Discord Dev Docs](https://discord.com/developers/docs/reference#message-formatting-timestamp-styles), it defaults to Discord's default, which at the moment is `f`
- `?add=DURATION` a duration to add to or subtract from the current time, example of acceptable arguments are: 2h30m, 1w2d, 1h20m40s, 60 etc. to subtract a duration simply prefix the argument with minus `-` sign

Bad arguments will be omitted.

### Examples

- <https://alirezarfe.github.io/discord-timestamp/?add=-2h&style=R>
- <https://alirezarfe.github.io/discord-timestamp/?add=1h45m>
- <https://alirezarfe.github.io/discord-timestamp/?style=F>
- <https://alirezarfe.github.io/discord-timestamp/?from=2012-05-08>
- <https://alirezarfe.github.io/discord-timestamp/?from=2022-01-01_5:30>
- <https://alirezarfe.github.io/discord-timestamp/?from=04-01>
- <https://alirezarfe.github.io/discord-timestamp/?from=04-01_18:45>
- <https://alirezarfe.github.io/discord-timestamp/?from=905037423627604029>

### TODO

- [x] Allow defining specific dates, times
- [ ] More user friendly (?)
