Timestamp markdown is a rather "internationalized" way of displaying date and time where the information is rendered according to timezone and locale of the user on their end. this tool makes creating these markdowns a little convenient, alternatively - if you are looking to do this in a standalone manner, just use a tool [like this](https://www.epochconverter.com/) to retrieve the unix epoch time and insert it in the markdown.

Either of the following notations are acceptable:

`<t:EPOCH_SECONDS>` → e.g <t:1472750028>

![Styleless timestamp preview](https://cdn.discordapp.com/attachments/652544869314854934/862699749652430868/timestamp_1.png)

`<t:EPOCH_SECONDS:STYLE>` → e.g <t:1472750028:R>

![Relative style timestamp preview](https://cdn.discordapp.com/attachments/652544869314854934/862699751602651156/timestamp_2.png)

Here is a list of available styles from [discord documentation](https://discord.com/developers/docs/reference#message-formatting-timestamp-styles).

| Style | Example Output               | Description     |
| ----- | ---------------------------- | --------------- |
| t     | 16:20                        | Short Time      |
| T     | 16:20:30                     | Long Time       |
| d     | 20/04/2021                   | Short Date      |
| D     | 20 April 2021                | Long Date       |
| f    | 20 April 2021 16:20          | Short Date/Time |
| F     | Tuesday, 20 April 2021 16:20 | Long Date/Time  |
| R     | 2 months ago                 | Relative Time   |

Otherwise, this tool is at your service.

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
