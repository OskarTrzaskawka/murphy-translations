# Translating Murphy

Thanks for helping Murphy speak your language! 💛

This folder holds every text the Murphy Discord bot shows: replies, buttons, errors, command descriptions and more. There is one file per language, and anyone can suggest improvements. Every change is reviewed by the Murphy team before it reaches the bot.

## How it works

1. `EnglishUS.json` is the **source**. All other files are translations of it.
2. You edit the file for your language and open a pull request.
3. A maintainer reviews it. Approved changes ship with the next bot update.

You don't need to know how to code. You only change the text on the right side of each line.

## Files

Each file is named after its language in English:

| File | Language |
| --- | --- |
| `EnglishUS.json` | English (US), the source |
| `Polish.json` | Polish |
| `German.json` | German |
| `SpanishES.json` / `SpanishLATAM.json` | Spanish (Spain / Latin America) |
| `PortugueseBR.json` / `PortuguesePT.json` | Portuguese (Brazil / Portugal) |
| `ChineseCN.json` / `ChineseTW.json` | Chinese (Simplified / Traditional) |
| … | 56 languages in total |

## Quick start

1. **Fork** this repository (button in the top right).
2. Open your language's file and click the ✏️ pencil to edit it in the browser.
3. Change the texts you want to improve.
4. Click **Commit changes**, then **Create pull request**.
5. In the description, say which language you worked on and anything we should know.

Small fixes are very welcome. You don't have to translate a whole file at once.

## The golden rules

### 1. Translate only the values, never the keys

```json
"hug": "{a} hugs {b}. 🤗"
```

`"hug"` is the **key**: leave it exactly as it is. Translate only the text after the colon.

### 2. Keep every `{placeholder}` exactly as it is

Words in curly braces are filled in by the bot: a user, a number, a time.

✅ `"{a} umarmt {b}. 🤗"`  
❌ `"{a} umarmt {benutzer}. 🤗"` (renamed)  
❌ `"{a} umarmt jemanden. 🤗"` (removed)

You may move them around to fit your grammar, but don't rename, translate or delete them. Common ones: `{a}` and `{b}` (two users), `{user}`, `{count}`, `{time}`, `{channel}`, `{role}`, `{percent}`.

### 3. Don't translate commands and code in backticks

Anything between backticks stays in English, because these are real commands:

✅ ``"Use `/afk off` when you're back."`` → ``"Użyj `/afk off`, gdy wrócisz."``  
❌ ``"Użyj `/afk wyłącz`"``

The same goes for technical lines like `DELETE /channels` or `scope=bot`.

### 4. Keep the formatting

Discord formatting must stay where it is:

- `**bold**`, `*italic*`, `-# small text`, `> quote`, `## heading`
- emojis such as 🎉 💞 ☢️
- mentions and timestamps such as `<@123>` and `<t:123:R>`
- line breaks written as `\n`

### 5. Some texts have a 100-character limit

Discord allows at most **100 characters** for command descriptions, option descriptions and choices. They usually sit under keys like these:

- `description`
- `options`
- `command_choices`
- `social.cmd`, `social.opt`, `social.group`
- `afk.cmd`, `afk.opt`
- `reactions.groups`, `reactions.actions`

Keep those short. Longer texts are cut off or rejected by Discord.

### 6. Leave names as they are

Don't translate **Murphy**, **Premium**, **Discord**, **Spotify**, **AFK**, **DLC** or other product names.

### 7. Keep the JSON valid

- Every text is wrapped in `"double quotes"`.
- A `"` inside a text must be written as `\"`.
- Lines are separated by commas, but there is no comma after the last line of a block.
- Save the file as **UTF-8** and keep the 2-space indentation.

If GitHub shows red marks in the file, something broke. Check the quotes and commas near that line.

## Style guide

- **Sound natural.** Write the way people in your language talk on Discord: friendly, short, clear. Don't translate word for word.
- **Use "you" informally** where your language has a choice (like *du*, *tu* or *ty*), unless that sounds rude in your culture.
- **Jokes can change.** Pick-up lines, roasts and fortunes in the `social.pool` section are meant to be fun. Adapt them so they're funny in your language, and keep them friendly.
- **Stay consistent.** If you translate "queue" or "server" one way, use the same word everywhere.
- **Gender:** some lines describe what one user does to another. If your language needs gender forms, use a neutral wording or the style common in your community, for example `zrobił(a)`.

## Untranslated or new texts

- **Missing text:** if a line is missing from your file, the bot shows the English text instead. You can add the missing line by copying it from `EnglishUS.json` and translating it.
- **Text still in English:** if a line in your file is still in English, it simply hasn't been translated yet. Go ahead and translate it.

## Adding a new language

Want Murphy in a language that isn't here yet?

1. Copy `EnglishUS.json` to a new file named after the language in English, for example `Welsh.json`.
2. Translate as much as you like. Partial files are fine.
3. Open a pull request and mention the language code (such as `cy`).

A maintainer will register the language in the bot so people can pick it with the language setting.

**Note:** Discord shows slash-command names and descriptions in only about 30 languages. In every other language, the menus Discord draws itself stay in English, but all of Murphy's replies use your translation.

## Questions?

- Ask in the Murphy support server: <https://discord.gg/U5fzuzbgkF>
- Or open an issue in this repository.

Thank you for making Murphy feel at home for more people! 🌍
