# Running Grasscutter

This is the start to finish guide on running Grasscutter from scratch.\
**This is only required if you are locally hosting (localhost'ing) your own server.**

## Prerequisites

- Grasscutter's [latest release](#releases-of-grasscutter) in the form of a JAR file.
  - It is recommended to use the **latest release**.
- [Java (JDK) 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html) - Required for compiling Grasscutter.
    - Greater versions of Java might work, but are unsupported.
- [MongoDB Server](https://www.mongodb.com/try/download/community) - Required for storing Grasscutter's data.
- A copy of [Grasscutter's resources](https://gitlab.com/YuukiPS/GC-Resources) - Required for the server to function.
  - The link above will take you to the latest version of these resources.
  - [Click here](https://autopatchgc.yuanshen.zip/dev_pc/serverdata/3.7/latest) for a direct download of the resources for REL3.7

## Running the Server

The server can be run in 2 ways:
- [Standalone, using the command line](#standalone)
- [Together with Cultivation](#with-cultivation)

### Standalone

1. Copy/Place your Grasscutter JAR into a folder. 
   1. This 'folder' will be referred to as your working directory.
2. Copy/Place your Grasscutter resources into your working directory.
   1. This should be a '.zip' file.
   2. You can extract the contents into a folder called 'resources', but this is not recommended.
3. Open a command prompt in your working directory.
   1. On Windows, you can do this by holding shift and right-clicking in the folder, then selecting 'Open PowerShell window here'.
4. Run the command `java -jar <name of your jar>.jar`.
   1. By default, this should be `java -jar grasscutter.jar`.
   2. If the server asks to place a copy of _something_, [see](/Troubleshooting#fixing-the-config)
5. Leave this command prompt open.
   1. Closing it will close the server.

### With Cultivation

TODO: Write.

# Releases of Grasscutter

Grasscutter comes in a variety of 'flavors' (releases).
- The latest release is the most stable version of Grasscutter.
  - Download it [here](https://github.com/Grasscutters/Grasscutter/releases/).
  - This is the recommended version for production use.
  - It is updated every month, at the end of the month.
- The most up-to-date build of **development**.
  - Download it [here](https://autopatchgc.yuanshen.zip/dev_pc/grasscutter/development/latest).
  - This is the recommended version for playing.
  - This version can contain some bug fixes, be wary.
  - It is updated whenever a new commit is added to the `development` branch.
- The most up-to-date build of **unstable**.
  - Download it [here](https://autopatchgc.yuanshen.zip/dev_pc/grasscutter/unstable/latest).
  - This is **not** a build for production use.
  - This version contains the most features, but the most bugs.
  - It is updated whenever a new commit is added to the `unstable` branch.