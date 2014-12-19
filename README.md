jemma-maven-repository
======================

A public Maven repository for all dependencies which cannot be found on Maven Central

Adding a JAR into the repo
--------------------------

checkout gh-pages branch

	git checkout gh-pages

Execute the following magen command

	mvn deploy:deploy-file -Durl=file:///path-to-local-clone/maven/ -Dfile=/path/to/jar/file -DgroupId=org.myorg -DartifactId=myartifact -Dpackaging=jar -Dversion=1.0.0  
