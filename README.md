# Table of contents
- [Information](#information)
- [Why it stores on Github but not in hosting server?](#why-it-stores-on-github-but-not-in-hosting-server)
- [Requesting nameplate, decoration](#requesting-nameplate-decoration)
    - [Request nameplate](#request-nameplate)
    - [Request decoration](#request-decoration)
- [Copyrights](#copyrights)

# Information
### About
This repository is made for storage images and JSON database files here. As bot is hosting on free, not sure if it allowed to modify JSON database inside bot's file, because bot's file is importing from repository and it updates only on bot's repository. So I decided to make this repository for storage non-sensive datas.

### Using fakeProfile plugin
- You need use dev build of modified client, it's not an official plugin of modified client such as Vencord or Equicord, more information about installation check [installation guide](https://github.com/odmDevs/fakeProfile/wiki/Installing).

# Why it stores on Github but not in hosting server?
Hosting and storage issue. Database maybe will weight around from 10-100 KB to 1 MB but the problem that you need store images which is very important for fakeProfile and it dependencies for avatar, banner, badges, decors, effects, nameplates. Like, there's situation that users uploading only animated avatars which can reach to 10 MB and after many times it reaches storage limit to 1 GB or 8 GB on host side, and problem is out here: storage is full and there's no new uploads and updates on database and new users can't apply fakeProfile things. So, what the solution for this? Github repostory. :D

# Requesting nameplate, decoration
But this repository have plus that you can requesting nameplate, decoration into repository via pull requests.

### Request nameplate
> [!IMPORTANT]
> To request new nameplate to fakeProfile you need follow these steps, all these steps required fork of repository and pull request, otherwise it'll be a mess and I can't do anything with this and I don't accepting request in Discord and issues.
1. Make a fork of this repository to make changes only on those locations: `images/nameplates/`, `database/assets/nameplates.json` and `database/store/nameplates.json`
2. In `images/nameplates/` add your nameplate image which must be in resolution `248x42` and in next extension:
    - `.png` if you planning non-animated nameplate.
    - `.webp` if you plannin animated nameplate.
3. In `database/assets/nameplates.json` you need modify JSON file and add a new nameplate in list as a new module:
```json
{
    "imgAlt": "COLLECTIBLES_NAMEPLATES_CHERRY_BLOSSOMS_A11Y",
    "palette": {
        "darkBackground": "#893A99",
        "lightBackground": "#B11FCF",
        "name": "berry"
    },
    "src": "https://odmdevs.github.io/fakeprofile-cdn/images/nameplates/(image_name_here).png"
}
```
- What it means? It means you making new module in `list` like this, and remember that new module adding with `,` after `}`. Where `(image_name_here).png` give your image name, for example: `evernight.png` and it should looks like this: `"src": "https://odmdevs.github.io/fakeprofile-cdn/images/nameplates/evernight.png"`.
4. In `database/store/nameplates.json` you need modify JSON file and add this data in list as a new module:
```json
{
    "name": "(name_here)",
    "src": "https://odmdevs.github.io/fakeprofile-cdn/images/nameplates/(nameplate_image_name_here).png",
    "author": "(your_discord_id)"
}
```
- It's important file because it makes choose it by bot to apply.
5. In pull request make title something like this: `[nameplate] Request of new nameplates` or that makes understand that you requesting this but decoration.

- That's all. If you still don't understand what it means and how to add custom nameplate, check this commit to understand that: https://github.com/odmDevs/fakeprofile-cdn/commit/ccb4cab5b861636f3c50654aa8c62564ee1087ae

### Request decoration
- Soon.

# Copyrights
This repository can contain content/images which are copyrighted material(for example, there's stores some images from Discord's source) or banned material or user-generated content from users which may be copyrighted or stolen with copyright thing, there's no guarantee that it'll filtered at 100%. If you find copyright work or banned material please consider to create an issue about that to notify developer and it'll be removed from repository.