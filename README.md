# Translations for Aaptaha

This is a required Aaptaha submodule.

This repo contains the strings for the bot's interface for ***all*** languages.

The files are arranged in the same directory structure as in the main repo,
with the exception that the files in repo's root folder are in a separate
folder named `Root` here, and a cog's class is in the respective `Cog` folder.

This must be in sync with the main root, since changes can be critically
breaking w.r.t. UX.

English translation serves as the reference translation.

---

## Contributing

Join Aaptaha's meta server by using the `about` command.

Note that all translations will be a part of Aaptaha, and will not be owned by
any specific third-party contributor.

## Setup

Use [Poedit](https://poedit.net). It is available directly in most package
repos, so you can install it directly. For example: `sudo apt install poedit`.

**All commits must be GPG signed.** Please see https://docs.github.com/articles/about-gpg/
for knowing more about it and how to set it up.

So the entire setup can be as follows:

```bash
sudo apt install poedit
git config --global commit.gpgsign=true
git clone git@github.com:aaptaha/aaptaha-translations.git
```

## Repo

This repo is not the typical git repo. Each branch has different history. Think
of it as a combination of different projects combined into one.

- `main` branch will only have the base `.pot` files.

- Each language must have its own branch for its development, and will only
  contain the translated strings (i.e., the `.po` files) and the `.pot` files.

- No branch except `production` will have `.mo` files.

- `production` branch will have all the language branches merged and compiled.

- *`.pot` files, `main` branch, and `production` branch must not be touched by
  anyone except Aaptaha's maintainer.*

## Translation files

- Project name: Aaptaha Translations.

- `PO-Revision-Date` must be there.

- `Language-Team` should be name of language, for eg., `Hindi`.

- `Last Translator` field should have your name and email. If you are not
  comfortable sharing IRL details ~~like me~~, use your GitHub name and email.
  Please use the commit email.

- Filename should be `name_<lang>.po`, where `name` is the one in `.pot` file.

- File should be stored in the same folder as the `.pot` file in
  `./<lang>/LC_MESSAGES/name_<lang>.po`.

## Translating

### Creating new translation files

- Switch to the respective branch (for eg. `git switch hi_IN`).

- Open `.pot` file in Poedit, then choose the appropriate language.

- In Translation -> Properties, fill the fields appropriately as mentioned
  above.

- Translate the strings and save in the correct location.

- Commit the `.po` files.

- Open PR for the respective branch.

### Editing existing translation files

- Switch to the language's branch (For example: `git switch hi_IN`).

- Directly open the `.po` file in Poedit.

- Do necessary modifications.

- Commit the `.po` files.

- Open PR for the respective branch.

---

## License

Copyright (C) 2021 Gouenji Shuuya (https://github.com/gouenji-shuuya).

Licensed under GNU Affero General Public License v3.0.
