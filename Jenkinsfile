node {
   stage 'Stage 1'
   echo 'Hello World 1'
   stage 'Stage 2'
   echo 'Hello World 2'
   stage 'Checkout'
    /* Checkout the code we are currently running against */
    checkout scm
   stage 'Build'
    /* Build the Docker image with a Dockerfile, tagging it with the build number */
    def app = docker.build "docker/whalesay:${env.BUILD_NUMBER}"
}
