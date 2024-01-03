# Welcome to the exercise on publishing packages!

This exercise checks your ability to publish to a GitHub Packages registry. It is automatically graded via a workflow once you have completed the instructions.

## Instructions

<!-- Specific instructions for your exercise -->

Please complete the instructions below:

1. Create your own repository
2. Publish a package of your choice. Ensure the package is associated with this repository. Starter packages can be found in [`sample-packages`](sample-packages/) but may need to be configured further to complete publishing.

<!-- Add your steps below starting with step 2 -->

## Follow steps below to publish using docker registry

1. Should have a docker file with the steps to perform when the package is deployed (sample-packages/docker)
2. Build docker - > Navigate to the docker file folder and build docker image

SYNTAX: docker build . -t IMAGENAME:VERSION
EXAMPLE: docker build . -t publish-pkg-registry:v1

3. Run the docker image

SYNTAX: docker run IMAGENAME:VERSION
EXAMPLE: docker run publish-pkg-registry:v1

4. Login Docker

SYNTAX: docker login docker.pkg.github.com --username USERNAME
EXAMPLE: docker login docker.pkg.github.com --username xyzjdf

5. Tag docker image

SYNTAX: docker tag IMAGENAME:VERSION docker.pkg.github.com/USERNAME/REPONAME/IMAGENAME:VERSION
EXAMPLE: docker tag publish-pkg-registry:v1 docker.pkg.github.com/xyzjdf/exercise-publish-package/publish-pkg-registry:v1

6. Push package 

SYNTAX: docker push IMAGENAME:VERSION docker.pkg.github.com/USERNAME/REPONAME/IMAGENAME:VERSION
EXAMPLE: docker push publish-pkg-registry:v1 docker.pkg.github.com/xyzjdf/exercise-publish-package/publish-pkg-registry:v1

## Troubleshooting

See [Viewing workflow run history](https://docs.github.com/en/actions/monitoring-and-troubleshooting-workflows/viewing-workflow-run-history) if you need assistance.
See [Running a workflow on GitHub](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow) if you need assistance.
See [GitHub Package Registry - Docker Image Registry] (https://www.youtube.com/watch?v=Nm7m92sZZJA) if you need assitance.

## Useful resources

Use these to help you!

Resources specific to this exercise:

<!-- - Add further resources for the learner -->

- [Working with a GitHub Packages registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry)
- [Connecting a repository to a package](https://docs.github.com/en/packages/learn-github-packages/connecting-a-repository-to-a-package)
- [Publishing a package](https://docs.github.com/en/packages/learn-github-packages/publishing-a-package)

