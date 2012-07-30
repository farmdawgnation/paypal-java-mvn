# PayPal Java APIs Maven Repo

This GitHub repository is designed to be used as a Maven Repository for the
PayPal Java APIs if you, like me, don't want to go to the hassle of implementing
your own private Maven repository because that sounds like a stroke of insanity.
PayPal doesn't currently expose a Maven repository to pull these from and I'm not
fond of carrying jars around in my projects.

A few notes:

* The group id is com.paypal.sdk
* The AdaptivePayments and AdaptiveAccounts APIs are provided.
* You need to depend on both the stubs and the base for the API you want.

## Usage in Maven

You should be able to use this repository by adding the following to your pom.xml
file:

```xml
  <repositories>
    <repository>
      <id>farmdawgnation-paypal-mvn-repo</id>
      <url>https://raw.github.com/farmdawgnation/paypal-java-mvn/master/releases</url>
    </repository>
  </repositories>
```

Then to include a particular artifact, for example adaptive-payments-base, you would
add the following to your pom file.

```xml
  <dependencies>
    ... your own dependencies ...
    <dependency>
      <groupId>com.paypal.sdk</groupId>
      <artifactId>adaptive-payments-base</artifactId>
      <version>1.3.3</version>
    </dependency>
  </dependencies>
```

## Usage in SBT

If you're working on a Scala project and want to include this in your SBT build file,
then adding the following to build.sbt should get you up and running. (0.11 and up)

```scala
  resolvers += "Farmdawg's PayPal MVN Repo" at "https://raw.github.com/farmdawgnation/paypal-java-mvn/master/releases"
```

Then, you'll need to add the actual library you want to the libraryDependencies variable.

```scala
  libraryDependencies += "com.paypal.sdk" % "adaptive-payments-base" % "1.3.3"
```

## Artifacts Included
The following artifacts have been provided in this repository.

* adaptive-payments-base at version 1.3.3
* adaptive-payments-stubs at version 1.3.3
* adaptive-accounts-base at version 1.3.3
* adaptive-accounts-stubs at version 1.3.3
