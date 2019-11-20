# Useful commands

## Build docker image of service without running tests
```bash
./gradlew clean buildDockerLatest -PdockerDryRun=false -x test -x jacocoTestReport -x sonarqube
```

## Build docker image with specific tag
```bash
./gradlew clean build buildDocker -PdockerDryRun=false -PbuildNumber=ticket-xxx -xtest -xjacocoTestReport -xsonarqube
```

## Get the dependency insight report for a given dependency
```bash
./gradlew -q dependencyInsight --dependency <name>
```

# Useful links
1. https://medium.com/@kevalpatel2106/how-to-decrease-your-gradle-build-time-by-65-310b572b0c43
