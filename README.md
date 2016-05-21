The guestbook App Engine demo, written in Java, built using Gradle.

# App Engine Java Guestbook


## How to Build

Requires [Gradle](http://gradle.org/) 2.10 or greater, and JDK 7+ in order to run.

To build, run

    gradle clean build

Building will run the tests, but to explicitly run tests you can use the test target

    gradle test

## Run from Command Line

To start the app from command line, just run the command:

	gradle appengineRun

For further information, consult the [Java App Engine](https://developers.google.com/appengine/docs/java/overview) documentation.

To see all the available tasks, run

    gradle tasks

## Run in Intellij IDEA

### Open Project

Firstly, open the project in Intellij IDEA via File -> Open, select the project folder and check "Auto Import" checkbox.

### Configure JDK version

And then verify project SDK is set to JDK 1.7 (not JDK 1.8) via File -> Project Structure -> Project tab -> Project SDK. Also set language level to 7.

After that, press Cmd+Shift+A, input "java compiler" and press Enter key. In the dialog, set project bytecode version to 1.7.

### Add App Engine Facet

Go to File -> Project Structure -> Modules, click plus icon, and add Google App Engine facet. Please make sure the path of latest App Engine SDK is configured correctly.

### Add Run Configuration

Open Run/Debug Configuration dialog, click plus icon, and select Google AppEngine Dev Server.

We need to configure Artifact location so that AppEngine Dev server can find the right project files. Go to File -> Project Structure -> Artifacts, select:

	Gradle: org.wisepersist:appengine-guestbook-java-gradle:appengine-guestbook-java-gradle-1.0-SNAPSHOT.war (exploded)

And then specify output directory to:

	[project dir]/build/exploded-app
	
Click OK buttons to confirm the settings. Now please try to run the project in Intellij IDEA.


## Sponsor

If you would like to contribute this project, please feel free to fork and create pull requests, or contact us at: support (at) wisepersist dot com

This project is sponsored by: [TaskTips](https://task.tips).


