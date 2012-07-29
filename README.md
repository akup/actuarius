##About Actuarius##
Actuarius is a Markdown Processor written in Scala using parser combinators. 

The project homepage can be found on github: https://github.com/chenkelmann/actuarius

For detailled information, please consult the Actuarius Wiki: https://github.com/chenkelmann/actuarius/wiki 

To browse the scaladoc online, go to: http://doc.henkelmann.eu/actuarius/index.html

To try Actuarius out, you can use the web dingus on my home page: http://henkelmann.eu/projects/actuarius/dingus 
(The web preview is currently broken but will be fixed (hopefully) soon.)

To get Actuarius, you can either check out the source from github, use maven/sbt to add it as a dependency (see below) or download the binary jar, javadoc jar or source jar directly from my maven repo at http://maven.henkelmann.eu/eu/henkelmann/

##License##
Actuarius is licensed under the 3-clause BSD license. For details see the `LICENSE` file that comes with the source.

##Compatibility##
Actuarius tries to stay as close to the original Markdown syntax definition as possible. There were however some quirks in the original Markdown I did not like. I wrote Actuarius as a Markdown processor for my homebrew blog engine, so I took the liberty to diverge slightly from the way the original Markdown works. The details are explained [in the respective article in the Actuarius Wiki](https://github.com/chenkelmann/actuarius/wiki/Differences-Between-Actuarius-And-Standard-Markdown)

##Maven##
The group id is `eu.henkelmann.actuarius`, the artifact id is `actuarius_[scala-version]`, e.g.`actuarius_2.9.2`. The current stable version is 0.2.3. The current development version is 0.2.4-SNAPSHOT and is currently not available from public repositories.
The repository url is http://maven.henkelmann.eu

Starting with version 0.2.4 there are builds for Scala 2.9.2, 2.9.1-1, 2.9.1, 2.9.0-1, 2.9.0, 2.8.1, 2.8.2 
(How I hate Scala's binary incompatibilities…)

##sbt##
For sbt, define the repo like so:

    resolvers += "Christophs Maven Repo" at "http://maven.henkelmann.eu/"
        
To add the lib to your project, add the following to your `.sbt` file:

    libraryDependencies += "eu.henkelmann.actuarius" % "actuarius" % "0.2.3"
    
Currently, Actuarius itself is built using sbt 0.11.x

##Version History##

###0.2.4###
* added support for scala 2.9.2
* switched to sbt 11.x as build system (thanks to David Pollack for the build file)
* added initial support for fenced code blocks (hint for programming language to format in is parsed but ignored)

###0.2.3###

* moved project to github
* added support for scala 2.9.1
* fixed bug that caused crashes when parsing windows line endings (CR LF)

