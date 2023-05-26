# Grasscutter Docs

This repository contains the documentation for Grasscutter. The documentation is written in Markdown.
Used on the [Grasscutter wiki](https://grasscutter.io/wiki/Home).

## Contributing

If you want to contribute to the documentation, you can do so by forking this repository and making a pull request.
Any useful additions are welcome.

### How to Contribute

1. Fork this repository
2. **Add your changes or additions to the `docs` folder**
3. **Edit the `navigation.json` file to include your new page or any changes you made.**
4. Commit your changes
5. Make a pull request

### How to Add a New Page

Create a new Markdown file in the `docs` folder.

You may also use existing sub-folders or create new ones to organize your pages.

### How to Edit the `navigation.json` File

The `navigation.json` file contains the navigation structure of the wiki. It is used to generate the sidebar on the wiki.

The file is structured as a JSON array of objects. Each object represents a page or a subfolder.

 #### If the object represents a page, it has the following structure:

```json
{
    "name": "Server Errors", 
    "_type": "file", 
    "path": "Troubleshooting/Server-Errors.md"
}
```

- `name` is the name of the page as it will appear in the sidebar
- `_type` is always `file` for pages
- `path` is the path to the page relative to the `docs` folder

#### If the object represents a folder, it has the following structure:

```json
{
    "name": "Troubleshooting", 
    "_type": "dir", 
    "_main": true,
  
    "children": [
        {
            "name": "Server Errors", 
            "_type": "file", 
            "path": "Troubleshooting/Server-Errors.md"
        }
    ]
}
```

- `name` is the name of the folder as it will appear in the sidebar
- `_type` is always `dir` for folders
- `_main` is `true` if the folder is the main folder of the wiki, `false` otherwise. Main folders are displayed in the sidebar as top-level items. **This property should be `false` for subfolders inside main folders**
- `children` is an array of objects representing the pages and subfolders inside the folder. The structure of these objects is the same as the structure of the main object.

#### NOTE
`children` can contain both pages and subfolders. However, **creating another subfolder inside a subfolder is NOT recommended if it can be avoided**.

This is how one `main` object in the `navigation.json` containing both files and subfolders should look like:

```json
{
    "name": "Resources", 
    "_type": "dir", 
    "_main": true,
  
    "children": [
        {
            "name": "MongoDB Tutorial", 
            "_type": "file", 
            "path": "Resources/MongoDB-Tutorial.md"
        },
        {
            "name": "Redirecting Text Blocks", 
            "_type": "file", 
            "path": "Resources/Redirecting-Text-Blocks.md"
        },
        {
            "name": "Fun Stuff", 
            "_type": "dir", 
            "_main": false,
          
            "children": [
                {
                    "name": "Colored nickname and signature", 
                    "_type": "file", 
                    "path": "Resources/Fun-Stuff/Colored-nickname-and-signature.md"
                },
                {
                    "name": "Avatar/Character", 
                    "_type": "file", 
                    "path": "Resources/Fun-Stuff/Avatar-Character.md"
                }
            ]
        }
    ]
}
```

If you want to add a new page to the wiki, and the main or subfolder containing it already exists, you only need to add the page object to the `children` array of the folder object.
