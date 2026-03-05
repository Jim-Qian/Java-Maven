OpenAPI Generator:
java -jar ./openapi-generator-cli-7.17.0.jar generate -i ./v1.json -g java -o generated-ws-client --library okhttp-gson -p serializationLibrary=jackson --skip-validate-spec


Maven:
mvn dependency:copy-dependencies -DincludeScope=runtime -DoutputDirectory=lib
- "-DincludeScope=runtime" gets all dependencies for compile + runtime. Thus will not include stuff like JUnit.
mvn dependency:copy-dependencies -DincludeScope=test -DoutputDirectory=lib
- "-DincludeScope=test" gets all dependencies for compile + runtime + test. 


Visual Studio Code Extensions for Java:
1. https://marketplace.visualstudio.com/_apis/public/gallery/publishers/vscjava/vsextensions/vscode-java-pack/latest/vspackage
vscode-java-pack.vsix
2. https://marketplace.visualstudio.com/_apis/public/gallery/publishers/redhat/vsextensions/java/latest/vspackage
redhat.java.vsix
3. https://marketplace.visualstudio.com/_apis/public/gallery/publishers/vscjava/vsextensions/vscode-java-debug/latest/vspackage
vscode-java-debug.vsix
4. https://marketplace.visualstudio.com/_apis/public/gallery/publishers/vscjava/vsextensions/vscode-maven/latest/vspackage
vscode-maven.vsix
5. https://marketplace.visualstudio.com/_apis/public/gallery/publishers/vscjava/vsextensions/vscode-java-test/latest/vspackage
vscode-java-test.vsix


Install Visual Studio Extension from .vsix File:
code --install-extension vscode-java-pack.vsix
Extensions → ... → Install from VSIX

---------------------------------------------------------------------------------------------------------------
Jars and lib folder:
JUnit 4:
junit-4.13.2.jar
hamcrest-core-1.3.jar


JUnit 5:
junit-jupiter-api-5.10.3.jar
junit-jupiter-engine-5.10.3.jar
junit-platform-commons-1.10.3.jar
junit-platform-engine-1.10.3.jar
apiguardian-api-1.1.2.jar
opentest4j-1.3.0.jar


Guava:
checker-qual-3.42.0.jar
error_prone_annotations-2.26.1.jar
failureaccess-1.0.2.jar
guava-33.2.1-jre.jar
j2objc-annotations-3.0.0.jar
jsr305-3.0.2.jar
listenablefuture-9999.0-empty-to-avoid-conflict-with-guava.jar


Mockito:
byte-buddy-1.14.12.jar
byte-buddy-agent-1.14.12.jar
mockito-core-5.11.0.jar
objenesis-3.3.jar