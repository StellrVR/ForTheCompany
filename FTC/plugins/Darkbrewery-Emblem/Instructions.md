Do not add or modify the Darkbrewery-Emblem/Emblem/Defaults folder

Instead create your own folder that Emblem will use

You may name it anything you wish but it must reside within BepInEx/plugins/Emblem/

Ex: BepInEx/plugins/Emblem/MyTheme

The organization structure beyond /Emblem/ is up to you!

In your config, point to your files relative to your new Emblem folder, ex:
- MyTheme/Header123.png
- MyTheme/Background
- MyTheme/Video/Awesomevideo.mp4

You do not need to include BepInEx/plugins/Author-ModName/plugins/Emblem/

The final structure being uploaded to thunderstore should look similair to this

MyTheme.zip
│
├── manifest.json
├── icon.png
├── README.md
├── CHANGELOG.md (optional)
│
└── BepInEx/
    │
    ├── config/
    │   └── Darkbrewery-Emblem.cfg
    │
    └── plugins/
        └── Emblem/
            ├── HeaderOfMyTheme.png
            ├── BackgroundOfMyTheme.mp4
            │
            └── Loading/
                ├── LoadingMyRandom1.png
                ├── LoadingMyRandom2.png
                └── LoadingMyRandom3.png


Please report bugs in the discord channel
Good luck and enjoy!