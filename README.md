# Magic Research 2 Public Translation Project

**Note: This has moved to Localizor: [https://www.localizor.com/magic-research-2/](https://www.localizor.com/magic-research-2/) - please contribute there instead! The information here might be out of date.**

--------------

# Legacy Documentation

This repository is meant to be used as a way to organize crowd-translations of the game Magic Research 2. Please read on to find out how to contribute!

## Translation Status And Credits

* English (United States): Done (N/A, original language)
* Chinese (Simplified): Done ([@JingruiChen](https://github.com/chen-assert))
* Portuguese (Brazil): In progress (ch1coon)

## Magic Research 2 Translation Guide

This guide is intended as a way to provide a custom translation for Magic Research 2. It is meant for those who would like to translate the game.

**Caution: As this is a text-only game, there is inevitably big, big spoilers for the _entire_ game inside the translations file. If you'd like to experience the game at its fullest and you're able to understand English, I suggest you complete the _full_ game first before starting to translate. Translate it at your own risk!**

The process essentially is as follows:

1. Start with the `base-translations.json` file in English as a base. This file is a key -> value object where the first string is the key (always the string in English) and the second string is the value (by default, exactly the same as the key).
2. Edit the values for the target language.
3. Once you are done editing, load the file into the app via the Options menu.
4. Restart the app.
5. The app will now use the translations.

If a key is not found in a translation file, the game will use the English as a default.

The strings are pretty special in the sense there are many special characters:

- `\n` is a new line (not always supported, but if you see it in one, it probably is).
- Many of the strings are in Markdown format. Refer to the Markdown syntax for more details.
- Double braces inside a string (for example: `"**New spells learned:** {{newSpellsLearnedText}}"`) indicate parameters and they will be replaced when playing the game with some other string.
- Some things wrapped between colons (for example: `"+10:attack:"`) will be replaced with a picture of an icon. Because those are identifiers, if you want the icon to appear, you will want to keep that piece intact.
- Finally, in some cases, you will see some complex pieces which are wrapped first with `^^`, followed by `<>` (for example: `"Can be used ^{{times}}^<{{explanation}}> times per combat"`). These are the underscored tooltips that you see throughout the app. When displayed, the text shown will be what is between `^`; it will be underlined, and if a mouse is hovered over the text, or the text is pressed in mobile, it will show a tooltip with what is in between `<>`.

As of the time of writing, there are about 4000 strings. Some of those may require little or no changes between most languages as they are almost entirely tokens, while some other individual strings are full paragraphs of story. There is no structure or context for the strings - it isn't planned as it was already a monumental undertaking.

## How to Contribute

You are free to create your own translations and distribute them on your own if you'd like. However, because translating the game is a very big task due to the sheer amount of strings, this repository also serves as a way to organize and share the load with others. Ideally we would have a proper tool to keep track what is already translated and what isn't, that would allow discussion, metadata on the keys, etc. but those can be quite expensive, so we're trying a GitHub repository first. If you'd like to contribute via this repository:

1. First, contact `magic.research.game@gmail.com` with your GitHub username or email so we can add you as a collaborator in the repository. Please mention what language(s) you are interested in translating the game to, as well as any alias you would like to be known as, so you can be properly credited.
2. If there is no translation file for your locale, please create one by copying `base-translations.json` and committing.
3. Once that is done (or if there already was a translation file), feel free to edit the file at leisure with any tools. Editing the file directly in this repository might be the best way to start.
4. Once the translations are finished or in a state where they can be beta-tested, feel free to mark it as completed in the list above at the top of this file, together with the version of the translations file used.

We estimate development will be fairly quick during the first few months after release, and several strings may change or be revised. `base-translations.json` will be promptly updated likely at least one day before the release of a new game version, but at this time we don't have plans to wait for the translations to catch up. This is likely to change in the future, once development slows down.

There is a channel in the official [Magic Research Discord server](https://discord.gg/bPhGsaqR9d) called `#mr2-translations`. It can be used as a venue for discussion and collaboration if needed.

## Questions, Suggestions, Etc.

Note from developer: It is my first time trying to build a translatable game from scratch, so chances are there are many, many things we could improve about this, especially in terms of process. There are also likely other elements in the app that will need attention for some locales: things like RTL, number formatting, etc. I am open to suggestions on how best to work. The best way to reach me is likely through Discord as mentioned above, in "How to Contribute".
