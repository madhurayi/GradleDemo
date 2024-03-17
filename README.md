# Setup of basic gradle using cli:
````
    gradle init --type java-application
````
The above command will setup a basic gradle project

```dtd
 ./gradlew build
```
The above command can build your project

To prepare a jar which is executable, you need to setup manifest property in `build.gradle` to identify what is the main class to execute

```dtd
./gradlew jar
```
The above command creates a new jar file in `build/libs` folder
```groovy
jar{
    manifest {
        attributes(
                'Main-Class': 'org.example.Main'
        )
    }
}
```
The above command can build your project

```dtd
java -jar build/libs/filename.jar
```
The above command will execute your code
