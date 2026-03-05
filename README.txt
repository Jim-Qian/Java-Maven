java -jar ./openapi-generator-cli-7.17.0.jar generate -i ./v1.json -g java -o generated-ws-client --library okhttp-gson -p serializationLibrary=jackson --skip-validate-spec

mvn dependency:copy-dependencies -DincludeScope=runtime -DoutputDirectory=lib
- "-DincludeScope=runtime" gets all dependencies for compile + runtime. Thus will not include stuff like JUnit.
mvn dependency:copy-dependencies -DincludeScope=test -DoutputDirectory=lib
- "-DincludeScope=test" gets all dependencies for compile + runtime + test. 



https://marketplace.visualstudio.com/_apis/public/gallery/publishers/vscjava/vsextensions/vscode-java-pack/latest/vspackage
vscode-java-pack.vsix

https://marketplace.visualstudio.com/_apis/public/gallery/publishers/redhat/vsextensions/java/latest/vspackage
redhat.java.vsix

https://marketplace.visualstudio.com/_apis/public/gallery/publishers/vscjava/vsextensions/vscode-java-debug/latest/vspackage
vscode-java-debug.vsix

https://marketplace.visualstudio.com/_apis/public/gallery/publishers/vscjava/vsextensions/vscode-maven/latest/vspackage
vscode-maven.vsix

https://marketplace.visualstudio.com/_apis/public/gallery/publishers/vscjava/vsextensions/vscode-java-test/latest/vspackage
vscode-java-test.vsix


code --install-extension vscode-java-pack.vsix
Extensions → ... → Install from VSIX