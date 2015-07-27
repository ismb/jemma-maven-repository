jemma-maven-repository
======================

A public Maven repository for all dependencies which cannot be found on Maven Central

Adding a JAR into the repo
--------------------------

checkout gh-pages branch

	git checkout gh-pages

Execute the following maven command:

	mvn deploy:deploy-file -Durl=file:///path-to-local-clone/maven/ -Dfile=/path/to/jar/file -DgroupId=org.myorg -DartifactId=myartifact -Dpackaging=jar -Dversion=1.0.0  
	
Example from the jemma-maven-repository folder (gh-pages branch):

	mvn deploy:deploy-file -Durl=file:///`pwd`/maven -Dfile=/home/tomasi/tmp/jemma.osgi.ah.webui.base-2.0.12.jar -DgroupId=org.energy-home -DartifactId=jemma.osgi.ah.webui.base -Dpackaging=jar -Dversion=2.0.12

Note: in case you want to install some jar only in your local repository for testing, you can use something like: 

	mvn install:install-file -Dfile=/home/tomasi/tmp/wstx-asl-3.2.3.jar -DgroupId=woodstox -DartifactId=wstx-asl -Dversion=3.2.3 -Dpackaging=jar	
