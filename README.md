# PayPal Java APIs Maven Repo

This GitHub repository is designed to be used as a Maven Repository for the
PayPal Java APIs if you, like me, don't want to go to the hassle of implementing
your own private Maven repository because that sounds like a stroke of insanity.
PayPal doesn't currently expose a Maven repository to pull these from and I'm not
fond of carrying jars around in my projects.

## Usage in Maven

You should be able to use this repository by adding the following to your pom.xml
file:

```xml
  <repositories>
    <repository>
      <id>farmdawgnation-paypal-mvn-repo</id>
      <url>https://github.com/farmdawgnation/paypal-java-mvn/releases</url>
    </repository>
  </repositories>
```

## Usage in SBT

If you're working on a Scala project and want to include this in your SBT build file,
then adding the following to build.sbt should get you up and running. (0.11 and up)

```scala
  resolvers += "Farmdawg's PayPal MVN Repo" at "https://github.com/farmdawgnation/paypal-java-mvn/releases"
```
