#Build

##Prepare the release
	mvn release:prepare -Dresume=false -DreleaseVersion=1.7.4.bsiR03 -DdevelopmentVersion=1.7.4-SNAPSHOT -Dtag=lesscss-engine-1.7.4.bsiR03 -Darguments="-Dmaven.javadoc.skip=true"

##Perform the release - publish to BSI Artifactory
	mvn release:perform -Darguments="-Dmaven.javadoc.skip=true"

Without GPG sining add `-Dgpg.skip=true` to `-Darguments`.