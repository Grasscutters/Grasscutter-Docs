# Contributing to Grasscutter

See [this](https://github.com/Grasscutters/Grasscutter/blob/development/CONTRIBUTING.md) for the contributor code of conduct.\
You must agree to these terms before contributing to this project.

## Prerequisites

Anything in **bold** is required to have.\
Everything else is a recommendation.

- **[Java (JDK) 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)** - Required for compiling Grasscutter.
  - Greater versions of Java might work, but are unsupported.
- **[MongoDB Server](https://www.mongodb.com/try/download/community)** - Required for storing Grasscutter's data.
  - [MongoDB Compass](https://www.mongodb.com/try/download/compass) is recommended for managing the database.
  - You can use a MongoDB cloud database.
- **[Gradle 7.0+](https://gradle.org/releases/)** - Required for compiling Grasscutter.
  - You can also use the Gradle wrapper found when cloning the project.
- A text editor/IDE for viewing/editing source code
  - [IntelliJ IDEA](https://www.jetbrains.com/idea/) is recommended.
  - [Visual Studio Code](https://code.visualstudio.com/) is recommended alongside IntelliJ IDEA.
  - Either or is recommended.
- _A semi-decent knowledge of general software development._

## Understanding Branches

Grasscutter currently has 2 primary branches:
- `development` - This is the more _stable_ branch of Grasscutter.
  - This receives mainly version updates and major bug fixes.
- `unstable` - This is the wild west of Grasscutter.
  - This receives all updates, including experimental features and bug fixes.
  - This branch is not recommended for production use.

When you make a contribution, if you have a **minor fix**, please make a pull request to `development`.\
If you have a major fix, such as a **rewrite of a system** or a new **feature**, please make a pull request to `unstable`.

## Building

### With IntelliJ IDEA

It is recommended to change your settings to the following:
- **Build and run using:** `IntelliJ IDEA`
- **Run tests using:** `IntelliJ IDEA`

Afterwards, you can use IntelliJ's artifact build system to create a JAR file.

If you are actively working on a feature, consider creating a new profile for an `Application`.\
If ran in `Debug` with [`HotswapAgent`](http://hotswapagent.org/mydoc_quickstart-jdk17.html), you can make changes to the code *mostly* without restarting the server.

### With Gradle

You can use the Gradle wrapper to build Grasscutter.\
To do this, run the following command in the root directory of the project:

```shell
gradlew jar
```