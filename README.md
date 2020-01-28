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

The project is launched by its profile:
```
mvn install -P launch
```

## Usage

The Sling instance is bound to port **8080** and can be accessed
[local instance](http://localhost:8080).

The [HTL Page](http://localhost:8080/content/sampleFM/home.html) is
printing out some text and the current user which is obtained using a
Sling Model.