# Java I/O

## NIO 2 usefull code snippets

### Create directory with subdirectories if needed

```java
Path path = Paths.get(dirPath);
boolean dirExists = Files.exists(dirPathObj);
if (dirExists) {
  log.warn("The directory already exists");
} else {
  try {
    Files.createDirectories(dirPathObj);
  } catch (IOException ex) {
    log.error("Can't create a new directory: " + ex.getMessage());
  }
}
```
