# Docker using Maven demo
Simple Spring Boot project to get a handle on how the [Spotify dockerfile-maven plugin](https://github.com/spotify/dockerfile-maven) works.

## Usage
Just use the standard Maven lifecycle phases `package` (build the image) or `deploy` (publish the image).

## Gotchas
You need to disable the default `deploy` behaviour else it tries to publish to a Maven repository 
(_not_ the same as the Docker repo!).

Do this by adding the property
```xml
        <maven.deploy.skip>true</maven.deploy.skip>
```
(other approaches are available...)
