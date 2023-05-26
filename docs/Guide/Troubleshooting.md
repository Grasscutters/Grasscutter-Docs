# Troubleshooting

## Fixing the Config

If the server asks you to place a copy of something in the working directory, follow these steps:
1. Open `config.json` in a text editor of your choice
2. Find `folderStructure` in your config
   1. See [Figure A](#figure-a)
3. Find the `resources` part of `folderStructure`
   1. See [Figure B](#figure-b)
4. Change to `./resources.zip`
   1. If your resources are in a different folder, change to the full path of the folder.

### Figure A
```json
{
  "folderStructure": {  
    "resources": "./resources/",
    "data": "./data/",
    "packets": "./packets/",
    "scripts": "resources:Scripts/",
    "plugins": "./plugins/"
  }
}
```

### Figure B
```
"resources": "./resources.zip"
```