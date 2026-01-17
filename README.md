# Scriptify DTS Generator
Generator for TypeScript declarations Scriptify functions and constants

## Example
Generate functions and constant declarations
```java
ScriptTsDeclarationGenerator generator = new ScriptTsDeclarationGenerator(script);
// Generated declaration string
String declaration = generator.generate();
// Save generated declaration
generator.save(Path.of("types.d.ts"));
```
Generate TypeScript (with JavaScript support) project with declarations
```java
ScriptTsProjectGenerator generator = new ScriptTsProjectGenerator(script);
generator.generate(Path.of("code"), ScriptTsProjectGenerator.TYPESCRIPT);
// Your can also use ScriptTsProjectGenerator.JAVASCRIPT
```

## Maven
Adding repository:
```xml
<repositories>
    <repository>
        <id>densy-repository-snapshots</id>
        <url>https://repo.densy.org/snapshots</url>
    </repository>
</repositories>
```

Adding dependency:
```xml
<dependency>
    <groupId>org.densy.scriptify.declaration</groupId>
    <artifactId>generator</artifactId>
    <version>1.0.1-SNAPSHOT</version>
</dependency>
```

## Gradle
Adding repository:
```groovy
maven {
    name "densyRepositorySnapshots"
    url "https://repo.densy.org/snapshots"
}
```

Adding dependency:
```groovy
implementation "org.densy.scriptify.declaration:generator:1.0.1-SNAPSHOT"
```