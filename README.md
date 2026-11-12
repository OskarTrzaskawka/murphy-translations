# Translating Murphy

[![Crowdin](https://badges.crowdin.net/murphy-bot/localized.svg)](https://crowdin.com/project/murphy-bot)

Thanks for helping Murphy speak your language! 💛

This repository holds every text the Murphy Discord bot shows: replies, buttons, errors, command descriptions and more. Translations are done by the community on **Crowdin**, a free website where you translate in the browser. No coding and no GitHub account needed.

## 👉 Start translating

1. Open **<https://crowdin.com/project/murphy-bot>**.
2. Sign in to Crowdin (free; you can use GitHub, Google and other accounts) and click **Join**.
3. Pick your language and click **Translate**.
4. Translate texts, or vote for good translations other people suggested.

Small contributions are very welcome. You don't have to translate everything at once.

## How it works

1. `EnglishUS.json` is the **source**. All other files are translations of it.
2. Volunteers translate on Crowdin.
3. A proofreader or the Murphy team **approves** each translation.
4. Crowdin sends the approved translations to this repository as a pull request, which a maintainer reviews and merges.
5. They ship with the next bot update.

Only approved translations reach the bot, so don't worry about making mistakes. Someone checks everything first.

Want to become a **proofreader** for your language? Ask in the support server (link below).

## The golden rules

### 1. Keep every `{placeholder}` exactly as it is

Words in curly braces are filled in by the bot: a user, a number, a time.

✅ `{a} umarmt {b}. 🤗`  
❌ `{a} umarmt {benutzer}. 🤗` (renamed)  
❌ `{a} umarmt jemanden. 🤗` (removed)

You may move them around to fit your grammar, but don't rename, translate or delete them. Common ones: `{a}` and `{b}` (two users), `{user}`, `{count}`, `{time}`, `{channel}`, `{role}`, `{percent}`. Crowdin warns you when a placeholder is missing.

### 2. Don't translate commands and code in backticks

Anything between backticks stays in English, because these are real commands:

✅ ``Use `/afk off` when you're back.`` → ``Użyj `/afk off`, gdy wrócisz.``  
❌ ``Użyj `/afk wyłącz` ``

The same goes for technical lines like `DELETE /channels` or `scope=bot`.

### 3. Keep the formatting

Discord formatting must stay where it is:

- `**bold**`, `*italic*`, `-# small text`, `> quote`, `## heading`
- emojis such as 🎉 💞 ☢️
- mentions and timestamps such as `<@123>` and `<t:123:R>`
- line breaks (`\n`)

### 4. Some texts have a 100-character limit

Discord allows at most **100 characters** for command descriptions, option descriptions and choices. On Crowdin you can see a text's key (its ID) in the editor. Keep texts short when the key contains:

- `description`
- `options`
- `command_choices`
- `social.cmd`, `social.opt`, `social.group`
- `afk.cmd`, `afk.opt`
- `reactions.groups`, `reactions.actions`

Longer texts are cut off or rejected by Discord.

### 5. Leave names as they are

Don't translate **Murphy**, **Premium**, **Discord**, **Spotify**, **AFK**, **DLC** or other product names.

## Style guide

- **Sound natural.** Write the way people in your language talk on Discord: friendly, short, clear. Don't translate word for word.
- **Use "you" informally** where your language has a choice (like *du*, *tu* or *ty*), unless that sounds rude in your culture.
- **Jokes can change.** Pick-up lines, roasts and fortunes in the `social.pool` section are meant to be fun. Adapt them so they're funny in your language, and keep them friendly.
- **Stay consistent.** If you translate "queue" or "server" one way, use the same word everywhere. Crowdin's translation memory and glossary help with this.
- **Gender:** some lines describe what one user does to another. If your language needs gender forms, use a neutral wording or the style common in your community, for example `zrobił(a)`.

## Languages

Murphy can be translated into **314 languages**. See [LANGUAGES.md](LANGUAGES.md) for the full list and file names.

- **Untranslated texts** show in English until someone translates them.
- A file that contains only `{}` is waiting for its first translator.
- When a new language reaches a good level, the Murphy team turns it on in the bot so people can pick it with the language setting.

**Note:** Discord shows slash-command names and descriptions in only about 30 languages. In every other language, the menus Discord draws itself stay in English, but all of Murphy's replies use your translation.

## For maintainers

- Please don't edit the translation files here directly or accept translation pull requests. Crowdin is the single source of truth, and changes made here are overwritten at the next sync.
- To add new English texts, update `EnglishUS.json` here. Crowdin picks them up automatically.
- `crowdin.yml` maps each Crowdin language to its file name.
- The bot pulls approved translations with `npm run locales:pull`.

## Questions?

- Ask in the Murphy support server: <https://discord.gg/U5fzuzbgkF>
- Or open an issue in this repository.

Thank you for making Murphy feel at home for more people! 🌍
