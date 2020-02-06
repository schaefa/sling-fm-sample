# Sample Feature Model Project

This project is using a HTL page together with a Sling Model to create
a page. The instance is started with Sling 12 Feature Model Starter.

## Build

**Attention**: The project needs to be fully build before it can be
started (also after each change):
```
mvn clean install
```

**Note**: the reason for this is that the artifact and the FM is not
installed before the *install* build cycle but the Sling instance is
started before.

## Launching

There are two ways to launch the project. Either use the Sling Starter
Feature Maven Plugin in the **launch** profile or launch it directly with
the Sling Feature Starter JAR file.

Launch the Project with the Maven Profile:
```
mvn install -P launch
```

Launch the Project with the Sling Feature Starter JAR file in the
root folder of this project:
```
    java -jar repository/org/apache/sling/org.apache.sling.kickstart/0.0.1-SNAPSHOT/org.apache.sling.kickstart-0.0.1-SNAPSHOT.jar \
  -af target/slingfeature-tmp/feature-test.json
```

To Launch the same thing with a process in the background:
```
java -jar repository/org/apache/sling/org.apache.sling.kickstart/0.0.1-SNAPSHOT/org.apache.sling.kickstart-0.0.1-SNAPSHOT.jar \
  start \
  -af target/slingfeature-tmp/feature-test.json &
```

To stop the instance:
```
java -jar repository/org/apache/sling/org.apache.sling.kickstart/0.0.1-SNAPSHOT/org.apache.sling.kickstart-0.0.1-SNAPSHOT.jar \
  stop
```

## Usage

The Sling instance is bound to port **8080** and can be accessed
[local instance](http://localhost:8080).

The [HTL Page](http://localhost:8080/content/sampleFM/home.html) is
printing out some text and the current user which is obtained using a
Sling Model.