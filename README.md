# test-jgitflow

##Features

This goal is a way to easily create feature branches and merge to the development branch without affecting pom version.

To start a new feature : mvn jgitflow:feature-start (create and checkout a new branch with a given name)
If the "pushFeatures" configuration parameter is set to true, the branch will be push to remote.

Work on your feature branch, commit and push.
You could create pull request or not on the development branch.

To end your feature : mvn jgitflow:feature-finish

If you had created a pull request on development branch, feature-finish will close it for you, merge the code into development branch and delete the feature branch.

##Release

This goal merges all code from development branch to master. It also updates the pom version of master and development to next number.

The start a release : mvn jgitflow:release-start (create and checkout a release branch)
If the "pushReleases" configuration parameter is set to true, the branch will be push to remote.

If you have last minute commit to do, you could do it on release branch.

To finalize the release : mvn jgitflow:release-finish

release-finish merges code from release branch to master, updates the poms versions, createa a tag and delete release branch.
