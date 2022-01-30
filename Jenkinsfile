node {
    checkout scm
    // inside withRegistry we are passing the dockerhub url and dockerHub credential which we are storing inside the Jenkins by the name dockerHub 
    docker.withRegistry('https://registry.hub.docker.com', 'dockerHub') {
        //inside the build function we are passing the repository of the dockerHUB
        def customImage = docker.build("piyush1008/dockerwebapp")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}