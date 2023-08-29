As described [here](https://code.visualstudio.com/blogs/2017/03/07/extension-pack-roundup) you can install the _yo generator code_ to create themes, extensions and packs.

So, we need to install the node package:

```sh
npm install -g yo generator-code
```

then run:

```sh
yo code
```

Complete the procedure answering questions as follows:

E.g.

```
? What type of extension do you want to create? New Extension Pack
? Add the currently installed extensions to the extension pack? No
? What's the name of your extension? Angular Extensions Pack
? What's the identifier of your extension? ddoomm-angular-extensions-pack
? What's the description of your extension? Angular Extensions Pack
? Initialize a git repository? No
```

List all your installed extensions:

```sh
code --list-extensions
```

Now, pick out your preferred extensions and paste them in the created extension pack package.json file, inside _extensionPack_ array.

E.g.

```json
{
  "name": "ddoomm-angular-extensions-pack",
  "displayName": "Angular Extensions Pack",
  "description": "Angular Extensions Pack",
  "publisher": "ddoomm",
  "version": "0.0.1",
  "engines": {
    "vscode": "^1.73.0"
  },
  "categories": ["Extension Packs"],
  "extensionPack": [
    "Angular.ng-template",
    "cyrilletuzi.angular-schematics",
    "infinity1207.angular2-switcher",
    "johnpapa.Angular2",
    "natewallace.angular2-inline",
    "nrwl.angular-console",
    "sanderledegen.angular-follow-selector"
  ]
}
```

_Note: I added manually the publisher identifier._

Copy the created folder _ddoomm-angular-extensions-pack_ inside _your_user_folder/.vscode/extensions_.

Tip: Filter vscode extensions by: **@category:"extension packs" @installed** to quickly enable\disable them for the specific workspace.
