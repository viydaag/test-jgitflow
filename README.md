# test-jgitflow

##Features

This goal is a way to easily create feature branches and merge to the development branch without affecting pom version.

To start a new feature : mvn jgitflow:feature-start (create and checkout a new branch with a given name)
If the "pushFeatures" configuration parameter is set to true, the branch will be push to remote.

Work on your feature branch, commit and push.
You could create pull request or not on the development branch.

To end your feature : mvn jgitflow:feature-finish

If you had created a pull request on development branch, feature-finish will close it for you, merge the code into development branch and delete the feature branch.
